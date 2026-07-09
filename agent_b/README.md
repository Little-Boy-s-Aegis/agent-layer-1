# Agent B Worker Package

Folder này là package runtime tự-contained cho Agent B. Khi chạy Agent B, chỉ
nạp các file trong chính folder này và telemetry thuộc domain Agent B. Không
nạp file từ `agent_a/`, `agent_c/`, hoặc root `agent-l1/`.

## Nhiệm Vụ

Agent B xử lý eBanking API, web, WAF, reverse proxy, API gateway, session,
token, device-binding, UEBA, workflow, transaction audit, fraud flow, và
customer-data behavior.

Agent B chỉ detect, map ATT&CK/CAPEC/API-web context, và predict
attack-pattern transition dạng hypothesis. Agent B không score, không priority,
không chọn playbook, không containment, không action.

## File Trong Package

- `agent_b_ebanking_api_web_ueba_system_prompt.md`: prompt chính để chạy
  worker.
- `agent_b_ebanking_api_web_capec_attack_matrix.md`: matrix domain riêng cho
  Agent B, dùng để map observed web/API/UEBA behavior sang ATT&CK/CAPEC/CWE.
- `layer1_standard_agent_output_schema.json`: schema local để validate output
  JSON của Agent B.
- `attack_vector_prediction_reference.md`: ATT&CK reference local cho mapping
  và prediction context.
- `capec_attack_pattern_prediction_reference.md`: CAPEC reference local cho
  CAPEC mapping và prediction context.
- `edge_case_matrix.md`: context cho workflow bypass, zero-day-like payload,
  insider/trusted access, cloud blast radius, telemetry gap, và các edge cases
  khác.
- `surface_context_matrix.md`: surface context để điền `surfaces_and_context`
  và xác định bề mặt cần L2 verify tiếp.

## Cách Dùng Runtime

1. Route telemetry vào Agent B chỉ khi telemetry thuộc eBanking, API, web, WAF,
   gateway, session/token, UEBA, fraud, hoặc transaction workflow domain.
2. Nạp `agent_b_ebanking_api_web_ueba_system_prompt.md` làm system prompt.
3. Cung cấp matrix và các reference local trong folder này. Nếu bị giới hạn
   token, retrieval/RAG chỉ nên lấy các dòng liên quan theo endpoint, object
   type, `mitre_attack_id`, `capec_id`, surface, edge-case flag, hoặc keyword
   trong telemetry.
4. Worker phải output đúng một JSON object theo
   `layer1_standard_agent_output_schema.json`.
5. Validate JSON bằng schema local trong folder này.
6. Gửi output sang Layer 2. Layer 2 mới verify, score, route, và quyết định
   response.

## Output Prediction

Khi có finding positive và có cơ sở, Agent B có thể emit:

```json
{
  "attack_pattern_prediction": {
    "prediction_horizon": "immediate",
    "predicted_attack_patterns": [
      {
        "mitre_attack_id": "T1213",
        "capec_id": "",
        "pattern_name": "Customer-data collection after object access abuse",
        "prediction_basis": "Observed unauthorized object access plus local CAPEC and ATT&CK references.",
        "watch_signal": "Verify bulk statement reads, export calls, pagination bursts, or related database audit reads for the same user/session/source."
      }
    ],
    "source_references": [
      "capec_attack_pattern_prediction_reference.md",
      "attack_vector_prediction_reference.md",
      "edge_case_matrix.md"
    ]
  }
}
```

Prediction này là signal cho L2 verify, không phải quyết định incident.
