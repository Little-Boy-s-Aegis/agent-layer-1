# Threat Grading Report Based on MITRE ATT&CK, CAPEC, and CWE

Generated: 2026-07-05T06:23:15+08:00

## Scope

This report grades attack vectors for defensive prioritization. It uses the provided local dataset, which integrates ATT&CK techniques, CAPEC attack patterns, CWE weakness mappings, data sources, mitigations, and observed threat-group/software usage. The scoring is not an exploit guide and should be tuned with local asset criticality, exposure, control maturity, calibrated agent confidence, and real watcher votes before operational use.

## Source Baseline

- Local dataset source: MITRE ATT&CK v19.1 (May 2026)
- Dataset generated/enriched: 2026-07-03T17:38:53.955090
- ATT&CK techniques scored: 943
- CAPEC attack patterns scored: 558
- CWE weaknesses available for consequence weighting: 944
- Coverage note: MITRE's public CAPEC page lists 559 total patterns; this report scores the 558 CAPEC entries present in the supplied local JSON.
- Official MITRE ATT&CK version history: https://attack.mitre.org/resources/versions/
- Official CAPEC list: https://capec.mitre.org/data/index.html
- Official CWE list: https://cwe.mitre.org/data/index.html

## Scoring Model

Final severity is calculated on a 0-10 scale using the corrected deterministic mechanic:

`raw_product = ImpactScore * AssetCriticality * ExploitLikelihood * DetectionConfidence`

The true maximum raw product is `4 * 3 * 1.5 * 1.2 = 21.6`, so the normalized score is:

`FinalRiskScore_0_10 = min(10, (raw_product / 21.6) * 10)`

Layer 2 derives `DetectionConfidence` from structural agreement and Layer 1 evidentiary confidence:

`AgentConfidenceFactor = min(calibrated agent_confidence values among agreeing agents)`

`DetectionConfidence = StructuralAgreement * AgentConfidenceFactor`

`ConfidentScore = base_bucket_score * AgentConfidenceFactor`

Layer 1 `finding.agent_confidence` is confidence in the agent's own observation and evidence quality. It is not final risk, priority, Layer 2 `DetectionConfidence`, or containment eligibility.

Grades: Critical 7.5-10, Medium High 4.1-7.49, Medium Low 2.5-4.09, Low 0-2.49.

Auto-containment is allowed only when all of these are true: `StructuralAgreement >= 1.0`, `DetectionConfidence >= 0.60`, and `FinalRiskScore_0_10 >= 6.0`. The structural floor means a single agent can raise analyst-visible severity but can never trigger automated containment by itself.

Current offline score rows do not include historical Layer 1 finding JSONs, so `agent_confidence_factor` is set to `1.0` and `structural_agreement` preserves the previous BFT proxy. In production, replace that default with the minimum calibrated confidence from the agreeing agents.

## Agent Confidence Rubric

| Evidentiary basis | agent_confidence range |
|---|---:|
| Confirmed signature/IOC match, or exact reproduction of a known attack pattern | 0.85-1.0 |
| Strong, quantified baseline deviation with no plausible benign explanation | 0.65-0.84 |
| Anomaly detected, but a plausible benign explanation exists | 0.35-0.64 |
| Sparse telemetry, single weak indicator, or heavy reliance on assumption | 0.10-0.34 |
| No real evidentiary basis / pure pattern-completion | do not emit `threat_detected=true` |

`confidence_rationale` must name the concrete evidence behind the selected value.

## ConfidentScore Matrix

| Condition | Base ConfidentScore | StructuralAgreement | AgentConfidenceFactor | DetectionConfidence Used | Meaning |
|---|---:|---:|---|---|---|
| 0/3 agents detect | 0 | 0.0 | n/a | 0.0 | No Layer 1 agent detected the threat. |
| 1/3 agents detect | 3 | 0.6 | confidence of the detecting agent | `0.6 * factor` | Single-agent signal only; visible for analyst ranking, never eligible for auto-containment by itself. |
| 2/3 agents detect but evidence differs | 6 | 0.6 | minimum confidence among detecting agents | `0.6 * factor` | Majority detection exists, but evidence does not correlate to the same event/session/IP/user. |
| 2/3 agents detect and evidence correlates | 8 | 1.0 | minimum confidence among agreeing agents | `1.0 * factor` | Majority detection with correlated evidence. |
| 3/3 agents detect same threat pattern | 10 | 1.2 | minimum confidence among agreeing agents | `1.2 * factor` | Full Layer 1 agreement on the same threat pattern. |

The aggregation uses `min()` instead of average so the least confident agreeing agent sets the evidentiary ceiling. This prevents one overconfident or miscalibrated agent from lifting a weak consensus.

## Surface Context for Asset Criticality

| Surface | Context Weight | Meaning |
|---|---:|---|
| Public Internet / Edge | 1.35 | Externally reachable services, public infrastructure, edge devices, phishing ingress, and internet discovery. |
| Identity / IAM | 1.35 | Accounts, credentials, authentication, directory services, tokens, MFA, and identity-provider control. |
| Cloud Control Plane | 1.32 | IaaS/SaaS administration, cloud APIs, instances, snapshots, volumes, tenant controls, and storage services. |
| SaaS / Office / Email | 1.28 | Office suites, SaaS applications, email-borne attacks, OAuth consent, web credentials, and collaboration platforms. |
| Network / Perimeter | 1.25 | Network devices, firewalls, VPN/proxy/router paths, DNS, network telemetry, lateral movement, and C2 traffic. |
| Server / Workload | 1.22 | Windows/Linux/ESXi/IaaS workloads, services, command execution, persistence, privilege escalation, and impact. |
| Data / Storage | 1.25 | Files, cloud storage, network shares, volumes, snapshots, backups, collection, exfiltration, encryption, and destruction. |
| Endpoint / User | 1.15 | User workstations, OS process/file/module/script telemetry, malware execution, local persistence, and endpoint privilege. |
| Containers / Kubernetes | 1.22 | Containers, pods, container CLI/API, orchestration actions, and containerized workload control. |
| ESXi / Hypervisor | 1.32 | ESXi, hypervisor CLI, virtualization management, and high-blast-radius host control. |
| Mobile | 1.12 | Android/iOS platforms, mobile application, device, SIM, SMS, and mobile operating-system behaviors. |
| ICS / OT | 1.45 | Industrial systems, PLC/RTU/IED, control servers, HMI, safety systems, process control impairment, and response inhibition. |

## Edge-Case Stressors

| Edge Case | Peak Multiplier | Meaning |
|---|---:|---|
| Zero-Day / Unknown Exploit | 1.22 | Externally reachable or client-side exploit paths where signature-based detection and patch availability may lag exploitation. |
| Exploit Chain / Multi-Step | 1.18 | Techniques likely to compound with credential theft, privilege escalation, persistence, lateral movement, or chained weaknesses. |
| Telemetry Gap / Evasion | 1.18 | Low-observability, stealth, log tampering, tool impairment, encrypted channels, or insufficient data-source coverage. |
| Identity / MFA Bypass | 1.2 | Credential, token, session, MFA, OAuth, SSO, and account-abuse cases that can bypass network-centric controls. |
| Supply Chain / Trusted Dependency | 1.18 | Dependency, update, code-signing, trusted relationship, vendor, package, repository, or build/deployment compromise. |
| Destructive / Ransomware | 1.22 | Encryption, data destruction, recovery inhibition, service disruption, backup targeting, and high-impact extortion paths. |
| Cloud / SaaS Tenant Blast Radius | 1.18 | Cloud control-plane, SaaS, tenant, instance, bucket, snapshot, identity-provider, OAuth, and cross-account blast-radius risk. |
| Living-off-the-Land | 1.15 | Abuse of native interpreters, admin tools, scripts, services, registries, scheduled jobs, and legitimate management channels. |
| AI-Scaled Social Engineering | 1.12 | Phishing, voice, content generation, impersonation, and information-gathering paths that can scale with AI-assisted tradecraft. |
| Insider / Trusted Access | 1.14 | Valid account, trusted relationship, pre-authorized access, internal abuse, and session misuse scenarios. |
| Air-Gapped / ICS Safety | 1.28 | ICS/OT, removable media, firmware, safety, response inhibition, process-control impairment, and isolated-environment compromise. |
| Rare but High Impact | 1.16 | Low public reporting frequency but high consequence, high severity, weak mappings, or poor visibility. |

## Portfolio Summary

- Technique grade distribution: Critical: 66, Medium High: 361, Medium Low: 141, Low: 375
- CAPEC grade distribution: Critical: 36, Medium High: 236, Medium Low: 103, Low: 183
- Most frequent max surfaces: Identity / IAM: 182, Server / Workload: 129, ICS / OT: 112, Public Internet / Edge: 99, Network / Perimeter: 96, ESXi / Hypervisor: 92, Data / Storage: 85, Cloud Control Plane: 82
- Most frequent max edge cases: Telemetry Gap / Evasion: 293, Zero-Day / Unknown Exploit: 164, Identity / MFA Bypass: 152, Air-Gapped / ICS Safety: 109, Cloud / SaaS Tenant Blast Radius: 67, Living-off-the-Land: 61, Destructive / Ransomware: 48, Exploit Chain / Multi-Step: 20
- Most frequent tactics: Stealth: 148, Persistence: 135, Privilege Escalation: 104, Execution: 81, Collection: 80, Credential Access: 79, Discovery: 74, Command and Control: 66

## Highest-Risk ATT&CK Attack Vectors

|rank|attack_id|attack_vector|tactics|final_score|threat_grade|impact_score|asset_criticality|exploit_likelihood|structural_agreement|agent_confidence_factor|detection_confidence|confident_score|max_surface|max_edge_case|recommended_action|auto_containment_allowed|related_capec_count|related_cwe_count|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|1|T1105|Ingress Tool Transfer|Command and Control|10|Critical|4|3|1.5|1.2|1|1.2|10|ESXi / Hypervisor|Living-off-the-Land|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|2|T1573.001|Symmetric Cryptography|Command and Control|10|Critical|4|3|1.5|1.2|1|1.2|10|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|3|T1056.001|Keylogging|Collection; Credential Access|10|Critical|4|3|1.5|1.2|1|1.2|10|Data / Storage|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|True|1|0|
|4|T1132.001|Standard Encoding|Command and Control|10|Critical|4|3|1.5|1.2|1|1.2|10|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|5|T1074.001|Local Data Staging|Collection|10|Critical|4|3|1.5|1.2|1|1.2|10|ESXi / Hypervisor|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|6|T1573.002|Asymmetric Cryptography|Command and Control|10|Critical|4|3|1.5|1.2|1|1.2|10|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|7|T1486|Data Encrypted for Impact|Impact|10|Critical|4|3|1.5|1.2|1|1.2|10|Cloud Control Plane|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|8|T1560.001|Archive via Utility|Collection|10|Critical|4|3|1.5|1.2|1|1.2|10|Data / Storage|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|9|T1119|Automated Collection|Collection|10|Critical|4|3|1.5|1.2|1|1.2|10|Identity / IAM|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|True|1|7|
|10|T1090|Proxy|Command and Control|10|Critical|4|3|1.5|1.2|1|1.2|10|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|11|T1560|Archive Collected Data|Collection|10|Critical|4|3|1.5|1.2|1|1.2|10|Data / Storage|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|12|T1490|Inhibit System Recovery|Impact|10|Critical|4|3|1.5|1.2|1|1.2|10|Cloud Control Plane|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|13|T1489|Service Stop|Impact|10|Critical|4|3|1.5|1.2|1|1.2|10|Cloud Control Plane|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|14|T1485|Data Destruction|Impact|10|Critical|4|3|1.5|1.2|1|1.2|10|Cloud Control Plane|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|15|T1048.003|Exfiltration Over Unencrypted Non-C2 Protocol|Exfiltration|10|Critical|4|3|1.5|1.2|1|1.2|10|ESXi / Hypervisor|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|16|T1657|Financial Theft|Impact|10|Critical|4|3|1.5|1.2|1|1.2|10|Identity / IAM|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|17|T1071.001|Web Protocols|Command and Control|8.33|Critical|4|3|1.5|1|1|1|8|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|18|T1005|Data from Local System|Collection|8.33|Critical|4|3|1.5|1|1|1|8|ESXi / Hypervisor|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|True|4|10|
|19|T1041|Exfiltration Over C2 Channel|Exfiltration|8.33|Critical|4|3|1.5|1|1|1|8|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|20|T1113|Screen Capture|Collection|8.33|Critical|4|3|1.5|1|1|1|8|Data / Storage|Living-off-the-Land|Auto-intercept / quarantine via pre-approved playbook|True|1|1|
|21|T1571|Non-Standard Port|Command and Control|8.33|Critical|4|3|1.5|1|1|1|8|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|22|T1102.002|Bidirectional Communication|Command and Control|8.33|Critical|4|3|1.5|1|1|1|8|ESXi / Hypervisor|Telemetry Gap / Evasion|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|23|T1071.004|DNS|Command and Control|8.33|Critical|4|3|1.5|1|1|1|8|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|24|T1567.002|Exfiltration to Cloud Storage|Exfiltration|8.33|Critical|4|3|1.25|1.2|1|1.2|10|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|25|T1560.003|Archive via Custom Method|Collection|8.33|Critical|4|3|1.5|1|1|1|8|Data / Storage|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|26|T1572|Protocol Tunneling|Command and Control|8.33|Critical|4|3|1.5|1|1|1|8|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|27|T1125|Video Capture|Collection|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Data / Storage|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|True|1|1|
|28|T1090.003|Multi-hop Proxy|Command and Control|8.33|Critical|4|3|1.5|1|1|1|8|ESXi / Hypervisor|Telemetry Gap / Evasion|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|29|T1090.001|Internal Proxy|Command and Control|8.33|Critical|4|3|1.25|1.2|1|1.2|10|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|True|1|1|
|30|T1529|System Shutdown/Reboot|Impact|8.33|Critical|4|3|1.5|1|1|1|8|ESXi / Hypervisor|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|31|T1001.003|Protocol or Service Impersonation|Command and Control|8.33|Critical|4|3|1.5|1|1|1|8|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|32|T1561.002|Disk Structure Wipe|Impact|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Identity / IAM|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|33|T1132.002|Non-Standard Encoding|Command and Control|8.33|Critical|4|3|1.25|1.2|1|1.2|10|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|34|T1114.002|Remote Email Collection|Collection|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|True|1|7|
|35|T1561.001|Disk Content Wipe|Impact|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Identity / IAM|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|36|T1573|Encrypted Channel|Command and Control|8.33|Critical|4|3|1.25|1.2|1|1.2|10|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|37|T1560.002|Archive via Library|Collection|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Data / Storage|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|38|T1185|Browser Session Hijacking|Collection|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|True|2|3|
|39|T1491.001|Internal Defacement|Impact|8.33|Critical|4|3|1.25|1.2|1|1.2|10|ESXi / Hypervisor|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|40|T1496.001|Compute Hijacking|Impact|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|41|T1074.002|Remote Data Staging|Collection|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|42|T1567|Exfiltration Over Web Service|Exfiltration|8.33|Critical|4|3|1.25|1.2|1|1.2|10|ESXi / Hypervisor|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|43|T1056|Input Capture|Collection; Credential Access|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Data / Storage|Exploit Chain / Multi-Step|Auto-intercept / quarantine via pre-approved playbook|True|2|1|
|44|T1074|Data Staged|Collection|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|45|T1048|Exfiltration Over Alternative Protocol|Exfiltration|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Cloud Control Plane|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|46|T1132|Data Encoding|Command and Control|8.33|Critical|4|3|1.25|1.2|1|1.2|10|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|47|T1213.006|Databases|Collection|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|48|T1048.002|Exfiltration Over Asymmetric Encrypted Non-C2 Protocol|Exfiltration|8.33|Critical|4|3|1.25|1.2|1|1.2|10|ESXi / Hypervisor|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|49|T1665|Hide Infrastructure|Command and Control|8.33|Critical|4|3|1.25|1.2|1|1.2|10|ESXi / Hypervisor|Telemetry Gap / Evasion|Auto-intercept / quarantine via pre-approved playbook|True|0|0|
|50|T1537|Transfer Data to Cloud Account|Exfiltration|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|True|0|0|

## Highest-Risk CAPEC Attack Patterns

|rank|capec_id|attack_pattern|severity_label|likelihood_label|final_score|threat_grade|impact_score|asset_criticality|exploit_likelihood|structural_agreement|agent_confidence_factor|detection_confidence|confident_score|max_surface|max_edge_case|recommended_action|auto_containment_allowed|related_technique_count|related_cwe_count|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|1|CAPEC-150|Collect Data from Common Resource Locations|Medium|Unknown|10|Critical|4|3|1.5|1.2|1|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|True|6|7|
|2|CAPEC-639|Probe System Files|Medium|Unknown|10|Critical|4|3|1.5|1.2|1|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|True|5|1|
|3|CAPEC-636|Hiding Malicious Data or Code within Files|High|Unknown|10|Critical|4|3|1.5|1.2|1|1.2|10|Identity / IAM|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|True|5|1|
|4|CAPEC-555|Remote Services with Stolen Credentials|Very High|Unknown|10|Critical|4|3|1.5|1.2|1|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|True|3|7|
|5|CAPEC-37|Retrieve Embedded Sensitive Data|Very High|High|10|Critical|4|3|1.5|1.2|1|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|True|2|14|
|6|CAPEC-568|Capture Credentials via Keylogger|High|Unknown|10|Critical|4|3|1.5|1.2|1|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|True|1|0|
|7|CAPEC-647|Collect Data from Registries|Medium|Medium|8.33|Critical|4|3|1.5|1|1|1|8|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|True|3|1|
|8|CAPEC-593|Session Hijacking|Very High|High|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|True|3|1|
|9|CAPEC-482|TCP Flood|Unknown|Unknown|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|True|3|1|
|10|CAPEC-654|Credential Prompt Impersonation|High|Medium|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|True|2|1|
|11|CAPEC-648|Collect Data from Screen Capture|Medium|Medium|8.33|Critical|4|3|1.5|1|1|1|8|Identity / IAM|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|True|2|1|
|12|CAPEC-634|Probe Audio and Video Peripherals|High|Low|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Data / Storage|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|True|2|1|
|13|CAPEC-545|Pull Data from System Resources|Unknown|Unknown|8.33|Critical|4|3|1.5|1|1|1|8|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|True|2|8|
|14|CAPEC-532|Altered Installed BIOS|High|Low|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Identity / IAM|Supply Chain / Trusted Dependency|Auto-intercept / quarantine via pre-approved playbook|True|2|0|
|15|CAPEC-528|XML Flood|Medium|Low|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Public Internet / Edge|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|True|2|1|
|16|CAPEC-125|Flooding|Medium|High|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|True|2|2|
|17|CAPEC-94|Adversary in the Middle (AiTM)|Very High|High|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|True|1|5|
|18|CAPEC-675|Retrieve Data from Decommissioned Devices|Medium|Medium|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Data / Storage|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|True|1|1|
|19|CAPEC-662|Adversary in the Browser (AiTB)|Very High|High|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Public Internet / Edge|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|True|1|2|
|20|CAPEC-569|Collect Data as Provided by Users|Unknown|Unknown|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|True|1|0|
|21|CAPEC-490|Amplification|Unknown|Unknown|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|True|1|1|
|22|CAPEC-489|SSL Flood|Unknown|Unknown|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Public Internet / Edge|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|True|1|1|
|23|CAPEC-488|HTTP Flood|Unknown|Unknown|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Public Internet / Edge|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|True|1|1|
|24|CAPEC-469|HTTP DoS|Low|Unknown|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Public Internet / Edge|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|True|1|2|
|25|CAPEC-465|Transparent Proxy Abuse|Medium|Unknown|8.33|Critical|4|3|1.25|1.2|1|1.2|10|ESXi / Hypervisor|Telemetry Gap / Evasion|Auto-intercept / quarantine via pre-approved playbook|True|1|1|
|26|CAPEC-25|Forced Deadlock|High|Low|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|True|1|6|
|27|CAPEC-227|Sustained Client Engagement|Unknown|Unknown|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|True|1|1|
|28|CAPEC-204|Lifting Sensitive Data Embedded in Cache|Medium|Unknown|8.33|Critical|4|3|1.5|1|1|1|8|ESXi / Hypervisor|Telemetry Gap / Evasion|Auto-intercept / quarantine via pre-approved playbook|True|1|4|
|29|CAPEC-148|Content Spoofing|Medium|Medium|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|True|1|1|
|30|CAPEC-131|Resource Leak Exposure|Medium|Medium|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|True|1|1|
|31|CAPEC-130|Excessive Allocation|Medium|Medium|8.33|Critical|4|3|1.25|1.2|1|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|True|1|3|
|32|CAPEC-89|Pharming|Very High|High|8.33|Critical|4|3|1.5|1|1|1|8|Data / Storage|Rare but High Impact|Auto-intercept / quarantine via pre-approved playbook|True|0|2|
|33|CAPEC-77|Manipulating User-Controlled Variables|Very High|High|8.33|Critical|4|3|1.5|1|1|1|8|Data / Storage|Rare but High Impact|Auto-intercept / quarantine via pre-approved playbook|True|0|7|
|34|CAPEC-75|Manipulating Writeable Configuration Files|Very High|High|8.33|Critical|4|3|1.5|1|1|1|8|Data / Storage|Rare but High Impact|Auto-intercept / quarantine via pre-approved playbook|True|0|6|
|35|CAPEC-44|Overflow Binary Resource File|Very High|High|8.33|Critical|4|3|1.5|1|1|1|8|Data / Storage|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|True|0|3|
|36|CAPEC-123|Buffer Manipulation|Very High|High|8.33|Critical|4|3|1.5|1|1|1|8|Data / Storage|Rare but High Impact|Auto-intercept / quarantine via pre-approved playbook|True|0|1|
|37|CAPEC-163|Spear Phishing|High|High|7.5|Medium High|3|3|1.5|1.2|1|1.2|10|Identity / IAM|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|True|7|1|
|38|CAPEC-640|Inclusion of Code in Existing Process|High|Low|7.5|Medium High|3|3|1.5|1.2|1|1.2|10|ICS / OT|Air-Gapped / ICS Safety|Auto-intercept / quarantine via pre-approved playbook|True|4|2|
|39|CAPEC-642|Replace Binaries|High|Unknown|7.5|Medium High|3|3|1.5|1.2|1|1.2|10|ICS / OT|Air-Gapped / ICS Safety|Auto-intercept / quarantine via pre-approved playbook|True|3|1|
|40|CAPEC-471|Search Order Hijacking|Medium|Unknown|7.5|Medium High|3|3|1.5|1.2|1|1.2|10|Data / Storage|Telemetry Gap / Evasion|Auto-intercept / quarantine via pre-approved playbook|True|3|1|
|41|CAPEC-21|Exploitation of Trusted Identifiers|High|High|7.5|Medium High|3|3|1.5|1.2|1|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|True|3|9|
|42|CAPEC-542|Targeted Malware|Unknown|Unknown|7.5|Medium High|3|3|1.5|1.2|1|1.2|10|Network / Perimeter|Telemetry Gap / Evasion|Auto-intercept / quarantine via pre-approved playbook|True|2|0|
|43|CAPEC-478|Modification of Windows Service Configuration|High|Low|7.5|Medium High|3|3|1.5|1.2|1|1.2|10|Identity / IAM|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|True|2|1|
|44|CAPEC-158|Sniffing Network Traffic|Medium|Unknown|7.5|Medium High|3|3|1.5|1.2|1|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|True|2|1|
|45|CAPEC-650|Upload a Web Shell to a Web Server|High|Unknown|7.5|Medium High|3|3|1.5|1.2|1|1.2|10|Identity / IAM|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|True|1|2|
|46|CAPEC-65|Sniff Application Code|High|Low|7.5|Medium High|3|3|1.5|1.2|1|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|True|1|4|
|47|CAPEC-616|Establish Rogue Location|Medium|Medium|7.5|Medium High|3|3|1.5|1.2|1|1.2|10|ESXi / Hypervisor|Telemetry Gap / Evasion|Auto-intercept / quarantine via pre-approved playbook|True|1|1|
|48|CAPEC-57|Utilizing REST's Trust in the System Resource to Obtain Sensitive Data|Very High|Medium|7.5|Medium High|3|3|1.5|1.2|1|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|True|1|3|
|49|CAPEC-543|Counterfeit Websites|High|Unknown|7.5|Medium High|3|3|1.5|1.2|1|1.2|10|ESXi / Hypervisor|Telemetry Gap / Evasion|Auto-intercept / quarantine via pre-approved playbook|True|1|0|
|50|CAPEC-31|Accessing/Intercepting/Modifying HTTP Cookies|High|High|7.5|Medium High|3|3|1.5|1.2|1|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|True|1|11|

## Highest-Risk Tactic and Surface Intersections

|tactic|surface|technique_count|avg_final_score|max_final_score|critical_count|medium_high_count|
|---|---|---|---|---|---|---|
|Collection|ESXi / Hypervisor|2|9.16|10|2|0|
|Impact|Cloud Control Plane|16|8.23|10|12|4|
|Credential Access|Data / Storage|4|8.05|10|2|2|
|Exfiltration|ESXi / Hypervisor|10|7.94|10|8|2|
|Impact|ESXi / Hypervisor|3|7.87|8.33|2|1|
|Command and Control|ESXi / Hypervisor|34|7.65|10|17|17|
|Impact|Public Internet / Edge|2|7.63|8.33|1|1|
|Impact|Identity / IAM|7|6.98|10|4|2|
|Exfiltration|Cloud Control Plane|3|6.94|8.33|2|1|
|Lateral Movement|ESXi / Hypervisor|4|6.88|7.5|0|4|
|Collection|Cloud Control Plane|7|6.74|8.33|4|2|
|Stealth|ESXi / Hypervisor|13|6.47|7.5|0|13|
|Persistence|Public Internet / Edge|2|6.36|7.5|0|2|
|Collection|SaaS / Office / Email|2|6.25|6.94|0|2|
|Privilege Escalation|Cloud Control Plane|6|6.11|7.5|0|6|
|Privilege Escalation|ESXi / Hypervisor|4|5.99|6.25|0|4|
|Execution|Data / Storage|3|5.97|7.5|0|3|
|Persistence|ESXi / Hypervisor|7|5.95|6.25|0|7|
|Lateral Movement|Identity / IAM|16|5.92|6.25|0|16|
|Defense Impairment|ESXi / Hypervisor|3|5.9|6.25|0|3|
|Execution|Identity / IAM|4|5.87|7.5|0|3|
|Defense Impairment|Identity / IAM|16|5.86|6.25|0|16|
|Privilege Escalation|Data / Storage|2|5.73|6.25|0|2|
|Stealth|Data / Storage|26|5.66|7.5|0|26|
|Persistence|Cloud Control Plane|5|5.63|6.25|0|5|
|Persistence|Identity / IAM|57|5.59|7.5|0|53|
|Collection|Public Internet / Edge|2|5.56|5.56|0|2|
|Command and Control|Public Internet / Edge|1|5.56|5.56|0|1|
|Credential Access|Public Internet / Edge|1|5.56|5.56|0|1|
|Stealth|Identity / IAM|16|5.42|7.5|0|14|
|Privilege Escalation|Identity / IAM|49|5.26|7.5|0|42|
|Lateral Movement|Cloud Control Plane|2|5.21|5.21|0|2|
|Persistence|Data / Storage|1|5.21|5.21|0|1|
|Privilege Escalation|Public Internet / Edge|1|5.21|5.21|0|1|
|Discovery|Identity / IAM|4|5|7.5|0|4|
|Credential Access|Cloud Control Plane|3|4.86|6.25|0|2|
|Stealth|Cloud Control Plane|3|4.86|6.25|0|2|
|Credential Access|Identity / IAM|66|4.62|7.5|0|50|
|Exfiltration|Data / Storage|7|4.56|8.33|3|1|
|Defense Impairment|Data / Storage|3|4.51|5.21|0|2|
|Execution|ESXi / Hypervisor|6|4.5|6.25|0|4|
|Defense Impairment|Cloud Control Plane|12|4.35|7.5|0|5|
|Discovery|ESXi / Hypervisor|11|4.29|5.21|0|9|
|Persistence|Network / Perimeter|8|4.2|5.56|0|5|
|Persistence|SaaS / Office / Email|4|4.17|4.17|0|4|
|Stealth|Network / Perimeter|24|4.1|5.56|0|16|
|Collection|Data / Storage|29|4.05|10|8|7|
|Collection|Identity / IAM|17|4.02|10|3|6|
|Execution|Cloud Control Plane|11|3.95|5.21|0|6|
|Credential Access|Network / Perimeter|5|3.94|4.63|0|3|

## Highest-Risk Edge-Case Stressors

|edge_case|technique_count|avg_final_score|max_final_score|critical_count|medium_high_count|
|---|---|---|---|---|---|
|Cloud / SaaS Tenant Blast Radius|245|5.09|10|35|141|
|Insider / Trusted Access|310|4.89|10|26|201|
|Living-off-the-Land|434|4.74|10|28|260|
|Zero-Day / Unknown Exploit|650|4.5|10|66|342|
|Destructive / Ransomware|208|4.35|10|48|72|
|Identity / MFA Bypass|446|4.03|10|23|239|
|Exploit Chain / Multi-Step|468|3.92|10|22|244|
|Telemetry Gap / Evasion|700|2.64|10|26|222|
|Rare but High Impact|116|2.32|8.33|1|34|
|Supply Chain / Trusted Dependency|191|2.26|8.33|1|53|
|Air-Gapped / ICS Safety|144|1.05|10|6|15|
|AI-Scaled Social Engineering|73|0.77|6.94|0|5|

## Defensive Control Priorities

These are weighted by the recalculated final scores of the ATT&CK techniques they mitigate or observe.

### Mitigations

|rank|mitigation|weighted_priority|
|---|---|---|
|1|User Account Management|621.56|
|2|Audit|576.1|
|3|Privileged Account Management|570.25|
|4|Network Intrusion Prevention|371.68|
|5|Disable or Remove Feature or Program|361.32|
|6|Execution Prevention|342.49|
|7|User Training|315.87|
|8|Restrict File and Directory Permissions|311.73|
|9|Filter Network Traffic|304.3|
|10|Multi-factor Authentication|262.07|
|11|Password Policies|244.31|
|12|Network Segmentation|225.05|
|13|Update Software|221.12|
|14|Operating System Configuration|218.53|
|15|Behavior Prevention on Endpoint|214.88|
|16|Encrypt Sensitive Information|192.49|
|17|Software Configuration|172.49|
|18|Restrict Web-Based Content|167.41|
|19|Restrict Registry Permissions|108.84|
|20|Code Signing|100.56|

### Data Sources

|rank|data_source|weighted_priority|
|---|---|---|
|1|Process|2532.31|
|2|File|1603.05|
|3|Network Traffic|1239.14|
|4|Command|1150.97|
|5|Application Log|560.53|
|6|Module|535.1|
|7|Windows Registry|471.44|
|8|User Account|467.41|
|9|Logon Session|449.95|
|10|Service|218.01|
|11|Cloud Service|184.9|
|12|Active Directory|166.35|
|13|Script|150.56|
|14|Cloud Storage|134.14|
|15|Scheduled Job|99.4|
|16|Sensor Health|98.21|
|17|Instance|90.39|
|18|Drive|88.3|
|19|Driver|85.08|
|20|Firewall|73.76|

## Calibration Monitoring

- Log every `finding.agent_confidence` and `finding.confidence_rationale` alongside the eventual analyst disposition: true positive, false positive, or benign-confirmed.
- Periodically compute each agent's calibration curve by comparing reported confidence bands with actual true-positive rate.
- Apply a per-agent calibration correction before Layer 2 computes `AgentConfidenceFactor`; Agent A, Agent B, and Agent C should be calibrated independently because their detection styles differ.
- Alert on confidence drift, such as an agent repeatedly reporting high-confidence findings that analysts later close as benign.

## Coverage Notes

- Techniques with CAPEC mappings: 180 of 943.
- Techniques with CWE mappings: 168 of 943.
- Techniques without CAPEC/CWE mappings are not treated as low risk. Their CAPEC/CWE component defaults to neutral because missing mappings are a data-coverage issue, not proof of low threat.
- Observed usage is based on MITRE group/software relationships in the local dataset. It is a public-reporting signal, not a probability of compromise in your environment.
- Surface multipliers represent default exposure/impact assumptions. Replace them with local asset exposure, business impact, and compensating-control data for production risk governance.
- This offline artifact uses `agent_confidence_factor=1.0` because no real Layer 1 finding-confidence history is present in the workspace.

## Complete Appendices

Complete per-vector scores are in `attack_vector_scores.csv` and the workbook sheet `Technique Scores`.
Complete per-surface multipliers are in `surface_multiplier_matrix.csv` and the workbook sheet `Surface Matrix`.
Complete edge-case stressor multipliers are in `edge_case_matrix.csv` and the workbook sheet `Edge Case Matrix`.
Edge-case aggregate priorities are in `edge_case_summary.csv` and the workbook sheet `Edge Case Summary`.
Complete CAPEC scores are in `capec_attack_pattern_scores.csv` and the workbook sheet `CAPEC Scores`.
