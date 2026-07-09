# Agent A Worker Package

Folder này là package runtime tự-contained cho Agent A. Khi chạy Agent A, chỉ
nạp các file trong chính folder này và telemetry thuộc domain Agent A. Không
nạp file từ `agent_b/`, `agent_c/`, hoặc root `agent-l1/`.

## Nhiệm Vụ

Agent A xử lý internal network, EDR, endpoint, server/workload, process, file,
registry, DNS, proxy, firewall, sensor-health, malware, C2, lateral movement,
ransomware, exfiltration, và defense evasion.

Agent A chỉ detect, map ATT&CK/CAPEC, và predict attack-pattern transition dạng
hypothesis. Agent A không score, không priority, không chọn playbook, không
containment, không action.

## File Trong Package

- `agent_a_internal_network_edr_system_prompt.md`: prompt chính để chạy worker.
- `agent_a_internal_network_edr_capec_attack_matrix.md`: matrix domain riêng
  cho Agent A, dùng để map observed behavior sang ATT&CK/CAPEC/CWE.
- `layer1_standard_agent_output_schema.json`: schema local để validate output
  JSON của Agent A.
- `attack_vector_prediction_reference.md`: ATT&CK reference local cho mapping
  và prediction context.
- `capec_attack_pattern_prediction_reference.md`: CAPEC reference local cho
  CAPEC mapping và prediction context.
- `edge_case_matrix.md`: context cho zero-day-like, living-off-the-land,
  insider/trusted access, ransomware, telemetry gap, và các edge cases khác.
- `surface_context_matrix.md`: surface context để điền `surfaces_and_context`
  và xác định bề mặt cần L2 verify tiếp.

## Cách Dùng Runtime

1. Route telemetry vào Agent A chỉ khi telemetry thuộc internal network, EDR,
   endpoint, server/workload, hoặc sensor-health domain.
2. Nạp `agent_a_internal_network_edr_system_prompt.md` làm system prompt.
3. Cung cấp matrix và các reference local trong folder này. Nếu bị giới hạn
   token, retrieval/RAG chỉ nên lấy các dòng liên quan theo `mitre_attack_id`,
   `capec_id`, surface, edge-case flag, hoặc keyword trong telemetry.
4. Worker phải output đúng một JSON object theo
   `layer1_standard_agent_output_schema.json`.
5. Validate JSON bằng schema local trong folder này.
6. Gửi output sang Layer 2. Layer 2 mới verify, score, route, và quyết định
   response.

## Output Prediction

Khi có finding positive và có cơ sở, Agent A có thể emit:

```json
{
  "attack_pattern_prediction": {
    "prediction_horizon": "short_term",
    "predicted_attack_patterns": [
      {
        "mitre_attack_id": "T1003",
        "capec_id": "",
        "pattern_name": "Credential access after lateral movement",
        "prediction_basis": "Observed internal movement plus local ATT&CK and edge-case references.",
        "watch_signal": "Verify LSASS, SAM, credential-store, or suspicious local memory-access behavior near the same host and time window."
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
