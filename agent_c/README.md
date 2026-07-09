# Agent C Worker Package

Folder này là package runtime tự-contained cho Agent C. Khi chạy Agent C, chỉ
nạp các file trong chính folder này và telemetry thuộc domain Agent C. Không
nạp file từ `agent_a/`, `agent_b/`, hoặc root `agent-l1/`.

## Nhiệm Vụ

Agent C xử lý ATM endpoint, ATM management, IAM, MFA, PAM, SSO, VPN, directory
service, AD/Kerberos, privileged identity, HSM-adjacent telemetry, ATM
tampering, credential abuse, và adversarial mimicry.

Agent C có vai trò adversarial defensive: nghĩ như attacker để nhận diện
bypass, obfuscation, false-normal behavior, và likely attack-pattern
transition. Agent C không cung cấp exploit steps, không score, không priority,
không chọn playbook, không containment, không action.

## File Trong Package

- `agent_c_atm_iam_adversarial_system_prompt.md`: prompt chính để chạy worker.
- `agent_c_atm_iam_capec_attack_matrix.md`: matrix domain riêng cho Agent C,
  dùng để map observed ATM/IAM behavior sang ATT&CK/CAPEC/CWE.
- `layer1_standard_agent_output_schema.json`: schema local để validate output
  JSON của Agent C.
- `attack_vector_prediction_reference.md`: ATT&CK reference local cho mapping
  và prediction context.
- `capec_attack_pattern_prediction_reference.md`: CAPEC reference local cho
  CAPEC mapping và prediction context.
- `edge_case_matrix.md`: context cho MFA bypass, trusted access, Kerberos/ticket
  abuse, zero-day-like chain, ATM/HSM edge cases, và telemetry gap.
- `surface_context_matrix.md`: surface context để điền `surfaces_and_context`
  và xác định bề mặt cần L2 verify tiếp.

## Cách Dùng Runtime

1. Route telemetry vào Agent C chỉ khi telemetry thuộc ATM, IAM, MFA, PAM, SSO,
   VPN, AD/Kerberos, privileged identity, hoặc HSM-adjacent domain.
2. Nạp `agent_c_atm_iam_adversarial_system_prompt.md` làm system prompt.
3. Cung cấp matrix và các reference local trong folder này. Nếu bị giới hạn
   token, retrieval/RAG chỉ nên lấy các dòng liên quan theo user, SPN, ticket,
   privileged role, ATM/HSM surface, `mitre_attack_id`, `capec_id`, hoặc
   edge-case flag trong telemetry.
4. Worker phải output đúng một JSON object theo
   `layer1_standard_agent_output_schema.json`.
5. Validate JSON bằng schema local trong folder này.
6. Gửi output sang Layer 2. Layer 2 mới verify, score, route, và quyết định
   response.

## Output Prediction

Khi có finding positive và có cơ sở, Agent C có thể emit:

```json
{
  "attack_pattern_prediction": {
    "prediction_horizon": "short_term",
    "predicted_attack_patterns": [
      {
        "mitre_attack_id": "T1550.003",
        "capec_id": "",
        "pattern_name": "Pass-the-ticket or Kerberos ticket expansion after Kerberoasting",
        "prediction_basis": "Observed Kerberoasting pattern plus local identity and ATT&CK edge-case references.",
        "watch_signal": "Verify unusual service-ticket reuse, privileged logons, or lateral Kerberos authentication attempts for the same user, host, or SPN set."
      }
    ],
    "source_references": [
      "attack_vector_prediction_reference.md",
      "edge_case_matrix.md"
    ]
  }
}
```

Prediction này là signal cho L2 verify, không phải quyết định incident.
