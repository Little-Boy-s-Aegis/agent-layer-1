# Agent L1 - Layer 1 Sensor Workers

> **Part of the [Little Boy's Aegis](https://github.com/Little-Boy-s-Aegis) project** -- an AI-powered Security Operations Center for banking infrastructure.

This folder contains three self-contained Layer 1 worker packages for the
Project Little Boy Aegis banking SOC architecture.

Layer 1 is a read-only sensor layer. It inspects clean routed telemetry,
identifies whether a security-relevant abnormality is present, maps the finding
to the best CAPEC and MITRE ATT&CK identifiers, predicts likely attack-pattern
transitions for defensive verification, and emits a strict extended JSON object
for the orchestrator stored in `../agent-l2`.

## Architecture at a Glance

```text
clean telemetry
      |
      +--> Agent A: internal network / EDR --------+
      +--> Agent B: eBanking / API / web / UEBA ---+--> one v4 JSON finding each
      +--> Agent C: ATM / IAM / privileged access -+           |
                                                                v
                                                    Layer 2 verification and response
```

Workers do not call response tools or mutate infrastructure. Their only product
is a masked, schema-valid observation that Layer 2 can independently verify.

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
  "finding_type": "observed_threat_pattern | observed_suspicious_pattern | anomaly_no_mapping | no_threat | prompt_injection_attempt",
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
`surfaces_and_context`, `attack_pattern_prediction`, `quality`. Include when data
is available from telemetry.

Each worker folder contains its own copy of
`layer1_standard_agent_output_schema.json`. There is no shared runtime schema
or shared runtime reference file at the Layer 1 root.

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
- numeric probability, likelihood, confidence, or score for predictions
- operational attacker instructions, exploit steps, or response actions

## Worker Packages

Each `agent_*` folder is self-contained and includes:

- one system prompt;
- one domain CAPEC/ATT&CK watch matrix;
- one local `layer1_standard_agent_output_schema.json`;
- `attack_vector_prediction_reference.md`;
- `capec_attack_pattern_prediction_reference.md`;
- `edge_case_matrix.md`;
- `surface_context_matrix.md`.

`agent_a/` covers internal network, endpoint, EDR, lateral movement,
credential access, and defense impairment.

`agent_b/` covers eBanking, API, WAF, web, UEBA, fraud workflow, and
customer-facing application behavior.

`agent_c/` covers ATM, IAM, HSM, privileged identity, Active Directory, PAM,
VPN, and adversarial misuse.

### Per-worker artifact map

| Artifact | Purpose |
|---|---|
| `*_system_prompt.md` | Worker role, decision rules, safety constraints, and output instructions |
| `*_capec_attack_matrix.md` | Domain-specific CAPEC and ATT&CK mappings |
| `layer1_standard_agent_output_schema.json` | Local Draft 2020-12-compatible output contract |
| `attack_vector_prediction_reference.md` | Non-scoring attack-vector transition guidance |
| `capec_attack_pattern_prediction_reference.md` | CAPEC transition reference |
| `surface_context_matrix.md` | Banking surface and context vocabulary |
| `edge_case_matrix.md` | Ambiguity, injection, missing-data, and no-threat handling |

## Reference Files

Layer 1 keeps runtime artifacts inside the individual worker folders only.
Generated CSV/JSON exports and threat-grading artifacts do not belong in Layer
1. The root folder is an index and repo boundary, not a shared runtime context.

Runtime risk scoring, playbook routing, containment, and final predictive
defense belong to the orchestrator in `../agent-l2`. Layer 1 may emit
non-scoring attack-pattern prediction hints; Layer 2 must independently verify
them before using them. The authoritative scoring inputs live under
`../agent-l2/risk_scoring`.

## How To Use

1. Route each clean telemetry batch to the matching worker folder by domain.
2. Provide the worker only the files in its own folder plus the telemetry
   needed for its domain.
3. The worker returns one JSON object using the extended schema above,
   including `attack_pattern_prediction` when a positive finding supports a
   likely next attack pattern.
4. Send every Layer 1 output to the orchestrator in `../agent-l2`.
5. Let the orchestrator independently verify logs, compute final risk, apply
   policy guardrails, select playbooks, and decide allowed actions.

If multiple Layer 1 workers report at the same time, do not merge or score them
inside Layer 1. Send each extended-schema output as a separate finding. The
orchestrator decides whether they describe the same attack.

### Minimal validation workflow

For each worker change, evaluate at least four fixtures: a clear threat, benign
activity, insufficient evidence, and a prompt-injection attempt. Validate the
returned object against that worker's local schema before publishing it to the
Layer 2 topic. Preserve the original event timestamp and mask credentials,
tokens, account identifiers, and unnecessary personal data in `raw_evidence`.

## Versioning and Safety

- All three schema copies must remain behaviorally compatible at the same
  `schema_version`.
- Breaking contract changes require a coordinated Layer 2 schema and prompt
  update.
- Reference updates must not introduce risk scores, action recommendations, or
  containment language into Layer 1.
- This repository contains prompt and reference artifacts only; it does not
  provide a network service or package installation step.

## Validation

Use these checks after editing:

```bash
for f in agent_*/layer1_standard_agent_output_schema.json; do
  python3 -m json.tool "$f" >/dev/null
done
find . -name '*.csv' -print
find . -maxdepth 1 -type f \
  \( -name '*grading*' -o -name 'threat_grading*' -o -name '*.json' \) \
  -print
rg -n "risk_score|confidence_score|priority|response_mode|playbook_id|recommended_action|containment_eligible|auto_execute|Score=|predicted_techniques|watch_for_next" .
```

Expected result:

- JSON parses successfully.
- No CSV files are present.
- No shared runtime JSON/schema/reference artifacts are present at the Layer 1
  root.
- Each worker package contains its own Markdown prediction references and local
  JSON schema.
- No Layer 1 prompt, matrix, schema, or example emits score, priority, playbook,
  action, containment, or predictive-defense fields.
- Layer 1 prediction is limited to `attack_pattern_prediction`; final
  predictive defense is performed by Layer 2 after independent verification.

## Related Repositories

| Repository | Description |
|---|---|
| [aegis-bank-deployment](https://github.com/Little-Boy-s-Aegis/aegis-bank-deployment) | Docker Compose orchestration |
| [aegis-bank-backend](https://github.com/Little-Boy-s-Aegis/aegis-bank-backend) | Spring Boot banking API |
| [aegis-bank-web-client](https://github.com/Little-Boy-s-Aegis/aegis-bank-web-client) | Next.js banking portal |
| [aegis-bank-mobile-app](https://github.com/Little-Boy-s-Aegis/aegis-bank-mobile-app) | Flutter mobile app |
| [dashboard](https://github.com/Little-Boy-s-Aegis/dashboard) | SOC Dashboard (Go + React) |
| [agent-layer-2](https://github.com/Little-Boy-s-Aegis/agent-layer-2) | Meta Analyzer / SOAR orchestrator prompts |
| [aegis-soar-engine](https://github.com/Little-Boy-s-Aegis/aegis-soar-engine) | SOAR Decision Engine |
| [aegis-staging-sandbox](https://github.com/Little-Boy-s-Aegis/aegis-staging-sandbox) | Staging simulation APIs |
| [aegis-bank-terraform](https://github.com/Little-Boy-s-Aegis/aegis-bank-terraform) | AWS Terraform infrastructure |
