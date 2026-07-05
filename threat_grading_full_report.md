# Threat Grading Report Deprecated For Layer 1 Runtime

This repository no longer owns runtime threat grading.

Layer 1 workers are read-only sensors. They emit only:

- `threat_detected`
- `capec_id`
- `mitre_attack_id`
- `raw_evidence`

Layer 1 must not calculate or emit risk score, confidence score, priority, response mode, playbook selection, containment eligibility, or automated action.

The previous generated threat grading export has been deprecated for Layer 1 runtime because it included operational scoring and action-decision columns. Clean runtime scoring inputs were moved to Layer 2 under:

- `../agent-l2/risk_scoring/attack_vector_risk_scores.md`
- `../agent-l2/risk_scoring/capec_risk_scores.md`
- `../agent-l2/risk_scoring/surface_multiplier_matrix.md`
- `../agent-l2/risk_scoring/edge_case_matrix.md`

Layer 2 independently verifies Layer 1 findings from logs and context, computes final risk, applies OPA/SOC Autopilot guardrails, and decides allowed defensive actions.
