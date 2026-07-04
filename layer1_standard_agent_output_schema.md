# Layer 1 Standard Agent JSON Output Schema

This is the standard output object for all Layer 1 agents. It replaces the old flat object with a finding-only JSON body that contains only what the agent observed, mapped, and predicted.

Do not include preprocessing metadata, orchestrator instructions, consensus fields, policy fields, Kafka routing fields, severity, confidence, final score, priority, or containment actions in the model output.

## Legacy Field Mapping

| Old Field | New Location | Owner |
| --- | --- | --- |
| `agent` | `agent.agent_id`, `agent.agent_name`, `agent.agent_type` | Layer 1 |
| `timestamp` | `timestamp`, `evidence.event_time` | Layer 1 |
| `severity` | Not emitted by Layer 1 | Excluded |
| `source_ip` | `entities.source_ip` | Layer 1 |
| `destination_ip` | `entities.destination_ip` | Layer 1 |
| `mitre_tactic` | `attack_mapping.mitre_attack[]` | Layer 1 |
| `confidence` | Not emitted by Layer 1 | Excluded |
| `raw_log_ref` | `source_scope.raw_log_refs[]`, `evidence.raw_log_refs[]` | Layer 1 |

## Standard JSON Object

```json
{
  "schema_version": "littleboy.soc.layer1.agent_finding.v3",
  "timestamp": "ISO8601",
  "agent": {
    "agent_id": "agent_id",
    "agent_name": "Agent Display Name",
    "agent_type": "agent-specific-type",
    "watch_domain": "agent-specific-watch-domain"
  },
  "threat_detected": true,
  "source_scope": {
    "source_log_domain": "agent-specific-source-log-domain-enum|null",
    "banking_domain_observed": "agent-specific-banking-domain-enum|null",
    "telemetry_window": {
      "start": null,
      "end": null
    },
    "log_source": null,
    "source_system": null,
    "raw_log_refs": []
  },
  "finding": {
    "finding_type": "signature_match|baseline_anomaly|behavioral_anomaly|mapping_match|policy_deviation|unknown_or_novel_abnormality|null",
    "finding_category": "network_edr|web_api_ueba|atm_iam|identity|transaction|data_movement|zero_day_like|prompt_injection_attempt|unknown|null",
    "known_or_unknown": "known_pattern|approximate_pattern|unknown_pattern|zero_day_like|novel_chain|null",
    "zero_day_suspected": false,
    "summary": "Short factual description of what was observed.",
    "why_abnormal": [],
    "observed_behavior": [],
    "matched_rules_or_models": []
  },
  "entities": {
    "user": null,
    "account_id_masked": null,
    "customer_id_masked": null,
    "account_type": "employee|privileged|service|vendor|customer|shared|break_glass|unknown|null",
    "source_ip": null,
    "destination_ip": null,
    "source_host": null,
    "destination_host": null,
    "host": null,
    "device_id": null,
    "atm_terminal_id": null,
    "session_id": null,
    "request_id": null,
    "transaction_id": null,
    "object_id_masked": null,
    "api_endpoint": null,
    "http_method": null,
    "domain": null,
    "destination_port": null,
    "protocol": null,
    "url_or_path_masked": null,
    "process_name": null,
    "process_hash": null,
    "file_hash": null
  },
  "evidence": {
    "event_time": null,
    "log_source": null,
    "event_ids": [],
    "raw_log_refs": [],
    "raw_snippets_masked": [],
    "observed_sequence": [],
    "baseline_deviation": null,
    "observed_counts": {},
    "payload_indicators": [],
    "network_indicators": {
      "ports": [],
      "protocols": [],
      "dns_queries": [],
      "asn": null,
      "geo": null
    },
    "identity_indicators": {
      "authentication_method": null,
      "mfa_method": null,
      "role_or_group": null,
      "privilege_change": null,
      "pam_or_ticket_ref": null
    },
    "host_indicators": {
      "process_tree": [],
      "command_lines_masked": [],
      "file_paths_masked": [],
      "registry_keys_masked": [],
      "service_names": []
    },
    "api_transaction_indicators": {
      "status_code": null,
      "user_agent_masked": null,
      "api_client_id": null,
      "business_operation": null,
      "before_state_masked": null,
      "after_state_masked": null
    },
    "atm_indicators": {
      "terminal_id": null,
      "atm_location_masked": null,
      "device_health_signal": null,
      "cash_or_card_operation": null,
      "firmware_or_peripheral_signal": null
    }
  },
  "attack_mapping": {
    "mitre_attack": [
      {
        "tactic_id": null,
        "tactic_name": null,
        "technique_id": null,
        "technique_name": null,
        "subtechnique_id": null,
        "subtechnique_name": null
      }
    ],
    "capec": [
      {
        "capec_id": null,
        "name": null
      }
    ],
    "cwe": [],
    "mapping_status": "known_mapping|approximate_mapping|unknown_mapping",
    "mapping_rationale": null
  },
  "surface_and_edge_context": {
    "asset_surface": "Identity / IAM|Public Internet / Edge|Network / Perimeter|Endpoint / User|Server / Workload|Data / Storage|Cloud Control Plane|SaaS / Office / Email|Mobile|ICS / OT|ESXi / Hypervisor|Containers / Kubernetes|unknown|null",
    "target_asset_or_service": null,
    "edge_case_flags": [
      "zero_day_unknown_exploit",
      "telemetry_gap_evasion",
      "identity_mfa_bypass",
      "living_off_the_land"
    ],
    "critical_bank_path_flags": {
      "core_banking": false,
      "ebanking": false,
      "swift_or_payment": false,
      "atm_or_hsm": false,
      "iam_or_privileged_access": false,
      "customer_data": false,
      "backup_or_recovery": false,
      "fraud_control": false
    }
  },
  "next_likely_threat_steps": [
    {
      "technique_id": null,
      "technique_name": null,
      "why_likely": null,
      "watch_for_next": []
    }
  ],
  "safety": {
    "prompt_injection_observed": false,
    "prompt_injection_evidence_masked": [],
    "log_contains_instruction_like_text": false,
    "log_instruction_ignored": true,
    "sensitive_values_masked": true
  },
  "quality": {
    "missing_fields": [],
    "assumptions": [],
    "limitations": []
  }
}
```
