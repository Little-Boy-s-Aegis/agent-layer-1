# Agent L1 - Layer 1 Sensor Workers

This folder contains the Layer 1 runtime contract, specialist sensor prompts,
and watch matrices for the Project Little Boy Aegis banking SOC architecture.

Layer 1 is a read-only sensor layer. It inspects clean routed telemetry,
identifies whether a security-relevant abnormality is present, maps the finding
to the best CAPEC and MITRE ATT&CK identifiers, and emits a strict extended
JSON object for the orchestrator stored in `../agent-l2`.

## Runtime Contract

Every Layer 1 worker must output exactly one JSON object matching the extended
schema `littleboy.soc.layer1.agent_finding.v4`. Required fields:

```json
{
  "schema_version": "littleboy.soc.layer1.agent_finding.v4",
  "timestamp": "<ISO8601 UTC>",
  "agent_id": "<agent identifier>",
  "agent_name": "<human-readable name>",
  "agent_type": "rule_ml_hybrid | contextual_ai | adversarial_ai",
  "threat_detected": true,
  "finding_type": "confirmed_threat | suspected_threat | anomaly_no_mapping | no_threat | prompt_injection_attempt",
  "capec_id": "CAPEC-### or empty string",
  "mitre_attack_id": "T#### or empty string",
  "raw_evidence": "Masked factual evidence string",
  "safety": {
    "prompt_injection_observed": false,
    "evidence_masked": false
  }
}
```

Optional enrichment fields: `banking_domain_observed`, `entities`, `attack_mapping`,
`surfaces_and_context`, `quality`. Include when data is available from telemetry.

The authoritative schema is `layer1_standard_agent_output_schema.json`.

Layer 1 must not calculate, emit, or imply:

- risk score
- confidence score
- priority
- response mode
- incident routing
- OPA or policy decision
- playbook selection
- containment eligibility
- automated action

## Worker Files

- `agent_a/agent_a_internal_network_edr_system_prompt.md`: internal network,
  endpoint, EDR, lateral movement, credential access, and defense impairment.
- `agent_b/agent_b_ebanking_api_web_ueba_system_prompt.md`: eBanking, API,
  WAF, web, UEBA, fraud workflow, and customer-facing application behavior.
- `agent_c/agent_c_atm_iam_adversarial_system_prompt.md`: ATM, IAM, HSM,
  privileged identity, Active Directory, PAM, VPN, and adversarial misuse.
- `agent_*/agent_*_capec_attack_matrix.md`: domain watch matrices used only
  for mapping and analyst context.

## Reference Files

The root Markdown files are reference material for mapping and context:

- `attack_vector_scores.md`
- `capec_attack_pattern_scores.md`
- `surface_multiplier_matrix.md`
- `edge_case_matrix.md`
- `edge_case_summary.md`

Despite some legacy filenames, these files are not runtime scoring authority for
Layer 1. Runtime risk scoring belongs to the orchestrator in
`../agent-l2/risk_scoring`.

`threat_grading_full_report.md` and `threat_grading_summary.json` are retained
only as migration notes. They must not be used to make Layer 1 score or action
decisions.

## How To Use

1. Route each clean telemetry batch to the matching worker prompt by domain.
2. Provide the worker only the telemetry needed for its domain.
3. The worker returns one JSON object using the extended schema above.
4. Send every Layer 1 output to the orchestrator in `../agent-l2`.
5. Let the orchestrator independently verify logs, compute final risk, apply
   policy guardrails, select playbooks, and decide allowed actions.

If multiple Layer 1 workers report at the same time, do not merge or score them
inside Layer 1. Send each extended-schema output as a separate finding. The
orchestrator decides whether they describe the same attack.

## Validation

Use these checks after editing:

```bash
python3 -m json.tool layer1_standard_agent_output_schema.json >/dev/null
find . -name '*.csv' -print
rg -n "structural_agreement|base_confident|verification_modifier" .
rg -n "block_ip|quarantine_host|force_logout|disable_account|auto_execute" agent_a agent_b agent_c
```

Expected result:

- JSON parses successfully.
- No CSV files are required.
- No Layer 1 prompt outputs confidence, consensus, risk score, or action fields.
- Any action words found in reference material are descriptive context only, not
  authorization for Layer 1 execution.
