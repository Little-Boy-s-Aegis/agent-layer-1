# Threat Grading Report Based on MITRE ATT&CK, CAPEC, and CWE

Generated: 2026-07-03T22:33:50

## Scope

This report grades attack vectors for defensive prioritization. It uses the provided local dataset, which integrates ATT&CK techniques, CAPEC attack patterns, CWE weakness mappings, data sources, mitigations, and observed threat-group/software usage. The scoring is not an exploit guide and should be tuned with local asset criticality, exposure, and control maturity before operational use.

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

Final severity is calculated on a 0-10 scale using the deterministic mechanic from the supplied scoring note:

`raw_product = ImpactScore * AssetCriticality * ExploitLikelihood * DetectionConfidence`

The raw product follows the proposed 1-12 action model, then normalizes to 0-10:

`FinalRiskScore_0_10 = min(10, (raw_product / 12) * 10)`

Grades: Critical 7.5-10, Medium High 4.1-7.49, Medium Low 2.5-4.09, Low 0-2.49.

Auto-containment is allowed when `FinalRiskScore_0_10 >= 6.0` and `DetectionConfidence >= 0.60`. In this offline report, asset criticality, exploit likelihood, and BFT confidence are deterministic proxies derived from MITRE metadata, data-source coverage, observed public usage, CAPEC likelihood, and edge-case flags. Replace these proxy inputs with live asset inventory, EPSS/CVE data, and real watcher votes in production.

## ConfidentScore Matrix

| Condition | ConfidentScore | DetectionConfidence Used | Meaning |
|---|---:|---:|---|
| 0/3 agents detect | 0 | 0.0 | No Layer 1 agent detected the threat. |
| 1/3 agents detect | 3 | 0.6 | Single-agent signal only; weak confidence but eligible for the current containment gate if final score is high enough. |
| 2/3 agents detect but evidence differs | 6 | 0.6 | Majority detection exists, but evidence does not correlate to the same event/session/IP/user. |
| 2/3 agents detect and evidence correlates to same event/session/IP/user | 8 | 1.0 | Majority detection with correlated evidence. |
| 3/3 agents detect same threat pattern | 10 | 1.2 | Full Layer 1 agreement on the same threat pattern. |

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

- Technique grade distribution: Critical: 427, Low: 343, Medium High: 152, Medium Low: 21
- CAPEC grade distribution: Critical: 272, Medium High: 110, Medium Low: 101, Low: 75
- Most frequent max surfaces: Identity / IAM: 182, Server / Workload: 129, ICS / OT: 112, Public Internet / Edge: 99, Network / Perimeter: 96, ESXi / Hypervisor: 92, Data / Storage: 85, Cloud Control Plane: 82
- Most frequent max edge cases: Telemetry Gap / Evasion: 293, Zero-Day / Unknown Exploit: 164, Identity / MFA Bypass: 152, Air-Gapped / ICS Safety: 109, Cloud / SaaS Tenant Blast Radius: 67, Living-off-the-Land: 61, Destructive / Ransomware: 48, Exploit Chain / Multi-Step: 20
- Most frequent tactics: Stealth: 148, Persistence: 135, Privilege Escalation: 104, Execution: 81, Collection: 80, Credential Access: 79, Discovery: 74, Command and Control: 66

## Highest-Risk ATT&CK Attack Vectors

|rank|attack_id|attack_vector|tactics|final_score|threat_grade|impact_score|asset_criticality|exploit_likelihood|detection_confidence|confident_score|max_surface|max_edge_case|recommended_action|related_capec_count|related_cwe_count|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|1|T1105|Ingress Tool Transfer|Command and Control|10|Critical|4|3|1.5|1.2|10|ESXi / Hypervisor|Living-off-the-Land|Auto-intercept / quarantine via pre-approved playbook|0|0|
|2|T1573.001|Symmetric Cryptography|Command and Control|10|Critical|4|3|1.5|1.2|10|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|0|0|
|3|T1056.001|Keylogging|Collection; Credential Access|10|Critical|4|3|1.5|1.2|10|Data / Storage|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|1|0|
|4|T1132.001|Standard Encoding|Command and Control|10|Critical|4|3|1.5|1.2|10|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|0|0|
|5|T1074.001|Local Data Staging|Collection|10|Critical|4|3|1.5|1.2|10|ESXi / Hypervisor|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|0|0|
|6|T1573.002|Asymmetric Cryptography|Command and Control|10|Critical|4|3|1.5|1.2|10|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|0|0|
|7|T1486|Data Encrypted for Impact|Impact|10|Critical|4|3|1.5|1.2|10|Cloud Control Plane|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|0|0|
|8|T1560.001|Archive via Utility|Collection|10|Critical|4|3|1.5|1.2|10|Data / Storage|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|0|0|
|9|T1119|Automated Collection|Collection|10|Critical|4|3|1.5|1.2|10|Identity / IAM|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|1|7|
|10|T1090|Proxy|Command and Control|10|Critical|4|3|1.5|1.2|10|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|0|0|
|11|T1560|Archive Collected Data|Collection|10|Critical|4|3|1.5|1.2|10|Data / Storage|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|0|0|
|12|T1490|Inhibit System Recovery|Impact|10|Critical|4|3|1.5|1.2|10|Cloud Control Plane|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|0|0|
|13|T1489|Service Stop|Impact|10|Critical|4|3|1.5|1.2|10|Cloud Control Plane|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|0|0|
|14|T1485|Data Destruction|Impact|10|Critical|4|3|1.5|1.2|10|Cloud Control Plane|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|0|0|
|15|T1048.003|Exfiltration Over Unencrypted Non-C2 Protocol|Exfiltration|10|Critical|4|3|1.5|1.2|10|ESXi / Hypervisor|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|0|0|
|16|T1657|Financial Theft|Impact|10|Critical|4|3|1.5|1.2|10|Identity / IAM|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|0|0|
|17|T1071.001|Web Protocols|Command and Control|10|Critical|4|3|1.5|1.0|8|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|0|0|
|18|T1005|Data from Local System|Collection|10|Critical|4|3|1.5|1.0|8|ESXi / Hypervisor|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|4|10|
|19|T1041|Exfiltration Over C2 Channel|Exfiltration|10|Critical|4|3|1.5|1.0|8|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|0|0|
|20|T1113|Screen Capture|Collection|10|Critical|4|3|1.5|1.0|8|Data / Storage|Living-off-the-Land|Auto-intercept / quarantine via pre-approved playbook|1|1|
|21|T1571|Non-Standard Port|Command and Control|10|Critical|4|3|1.5|1.0|8|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|0|0|
|22|T1102.002|Bidirectional Communication|Command and Control|10|Critical|4|3|1.5|1.0|8|ESXi / Hypervisor|Telemetry Gap / Evasion|Auto-intercept / quarantine via pre-approved playbook|0|0|
|23|T1071.004|DNS|Command and Control|10|Critical|4|3|1.5|1.0|8|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|0|0|
|24|T1567.002|Exfiltration to Cloud Storage|Exfiltration|10|Critical|4|3|1.25|1.2|10|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|0|0|
|25|T1560.003|Archive via Custom Method|Collection|10|Critical|4|3|1.5|1.0|8|Data / Storage|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|0|0|
|26|T1572|Protocol Tunneling|Command and Control|10|Critical|4|3|1.5|1.0|8|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|0|0|
|27|T1125|Video Capture|Collection|10|Critical|4|3|1.25|1.2|10|Data / Storage|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|1|1|
|28|T1090.003|Multi-hop Proxy|Command and Control|10|Critical|4|3|1.5|1.0|8|ESXi / Hypervisor|Telemetry Gap / Evasion|Auto-intercept / quarantine via pre-approved playbook|0|0|
|29|T1090.001|Internal Proxy|Command and Control|10|Critical|4|3|1.25|1.2|10|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|1|1|
|30|T1529|System Shutdown/Reboot|Impact|10|Critical|4|3|1.5|1.0|8|ESXi / Hypervisor|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|0|0|
|31|T1001.003|Protocol or Service Impersonation|Command and Control|10|Critical|4|3|1.5|1.0|8|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|0|0|
|32|T1561.002|Disk Structure Wipe|Impact|10|Critical|4|3|1.25|1.2|10|Identity / IAM|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|0|0|
|33|T1132.002|Non-Standard Encoding|Command and Control|10|Critical|4|3|1.25|1.2|10|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|0|0|
|34|T1114.002|Remote Email Collection|Collection|10|Critical|4|3|1.25|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|1|7|
|35|T1561.001|Disk Content Wipe|Impact|10|Critical|4|3|1.25|1.2|10|Identity / IAM|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|0|0|
|36|T1573|Encrypted Channel|Command and Control|10|Critical|4|3|1.25|1.2|10|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|0|0|
|37|T1560.002|Archive via Library|Collection|10|Critical|4|3|1.25|1.2|10|Data / Storage|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|0|0|
|38|T1185|Browser Session Hijacking|Collection|10|Critical|4|3|1.25|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|2|3|
|39|T1491.001|Internal Defacement|Impact|10|Critical|4|3|1.25|1.2|10|ESXi / Hypervisor|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|0|0|
|40|T1496.001|Compute Hijacking|Impact|10|Critical|4|3|1.25|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|0|0|
|41|T1074.002|Remote Data Staging|Collection|10|Critical|4|3|1.25|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|0|0|
|42|T1567|Exfiltration Over Web Service|Exfiltration|10|Critical|4|3|1.25|1.2|10|ESXi / Hypervisor|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|0|0|
|43|T1056|Input Capture|Collection; Credential Access|10|Critical|4|3|1.25|1.2|10|Data / Storage|Exploit Chain / Multi-Step|Auto-intercept / quarantine via pre-approved playbook|2|1|
|44|T1074|Data Staged|Collection|10|Critical|4|3|1.25|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|0|0|
|45|T1048|Exfiltration Over Alternative Protocol|Exfiltration|10|Critical|4|3|1.25|1.2|10|Cloud Control Plane|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|0|0|
|46|T1132|Data Encoding|Command and Control|10|Critical|4|3|1.25|1.2|10|ESXi / Hypervisor|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|0|0|
|47|T1213.006|Databases|Collection|10|Critical|4|3|1.25|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|0|0|
|48|T1048.002|Exfiltration Over Asymmetric Encrypted Non-C2 Protocol|Exfiltration|10|Critical|4|3|1.25|1.2|10|ESXi / Hypervisor|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|0|0|
|49|T1665|Hide Infrastructure|Command and Control|10|Critical|4|3|1.25|1.2|10|ESXi / Hypervisor|Telemetry Gap / Evasion|Auto-intercept / quarantine via pre-approved playbook|0|0|
|50|T1537|Transfer Data to Cloud Account|Exfiltration|10|Critical|4|3|1.25|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|0|0|

## Highest-Risk CAPEC Attack Patterns

|rank|capec_id|attack_pattern|severity_label|likelihood_label|final_score|threat_grade|impact_score|asset_criticality|exploit_likelihood|detection_confidence|confident_score|max_surface|max_edge_case|recommended_action|related_technique_count|related_cwe_count|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|1|CAPEC-150|Collect Data from Common Resource Locations|Medium|Unknown|10|Critical|4|3|1.5|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|6|7|
|2|CAPEC-639|Probe System Files|Medium|Unknown|10|Critical|4|3|1.5|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|5|1|
|3|CAPEC-636|Hiding Malicious Data or Code within Files|High|Unknown|10|Critical|4|3|1.5|1.2|10|Identity / IAM|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|5|1|
|4|CAPEC-555|Remote Services with Stolen Credentials|Very High|Unknown|10|Critical|4|3|1.5|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|3|7|
|5|CAPEC-37|Retrieve Embedded Sensitive Data|Very High|High|10|Critical|4|3|1.5|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|2|14|
|6|CAPEC-568|Capture Credentials via Keylogger|High|Unknown|10|Critical|4|3|1.5|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|1|0|
|7|CAPEC-647|Collect Data from Registries|Medium|Medium|10|Critical|4|3|1.5|1.0|8|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|3|1|
|8|CAPEC-593|Session Hijacking|Very High|High|10|Critical|4|3|1.25|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|3|1|
|9|CAPEC-482|TCP Flood|Unknown|Unknown|10|Critical|4|3|1.25|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|3|1|
|10|CAPEC-654|Credential Prompt Impersonation|High|Medium|10|Critical|4|3|1.25|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|2|1|
|11|CAPEC-648|Collect Data from Screen Capture|Medium|Medium|10|Critical|4|3|1.5|1.0|8|Identity / IAM|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|2|1|
|12|CAPEC-634|Probe Audio and Video Peripherals|High|Low|10|Critical|4|3|1.25|1.2|10|Data / Storage|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|2|1|
|13|CAPEC-545|Pull Data from System Resources|Unknown|Unknown|10|Critical|4|3|1.5|1.0|8|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|2|8|
|14|CAPEC-532|Altered Installed BIOS|High|Low|10|Critical|4|3|1.25|1.2|10|Identity / IAM|Supply Chain / Trusted Dependency|Auto-intercept / quarantine via pre-approved playbook|2|0|
|15|CAPEC-528|XML Flood|Medium|Low|10|Critical|4|3|1.25|1.2|10|Public Internet / Edge|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|2|1|
|16|CAPEC-125|Flooding|Medium|High|10|Critical|4|3|1.25|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|2|2|
|17|CAPEC-94|Adversary in the Middle (AiTM)|Very High|High|10|Critical|4|3|1.25|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|1|5|
|18|CAPEC-675|Retrieve Data from Decommissioned Devices|Medium|Medium|10|Critical|4|3|1.25|1.2|10|Data / Storage|Destructive / Ransomware|Auto-intercept / quarantine via pre-approved playbook|1|1|
|19|CAPEC-662|Adversary in the Browser (AiTB)|Very High|High|10|Critical|4|3|1.25|1.2|10|Public Internet / Edge|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|1|2|
|20|CAPEC-569|Collect Data as Provided by Users|Unknown|Unknown|10|Critical|4|3|1.25|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|1|0|
|21|CAPEC-490|Amplification|Unknown|Unknown|10|Critical|4|3|1.25|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|1|1|
|22|CAPEC-489|SSL Flood|Unknown|Unknown|10|Critical|4|3|1.25|1.2|10|Public Internet / Edge|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|1|1|
|23|CAPEC-488|HTTP Flood|Unknown|Unknown|10|Critical|4|3|1.25|1.2|10|Public Internet / Edge|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|1|1|
|24|CAPEC-469|HTTP DoS|Low|Unknown|10|Critical|4|3|1.25|1.2|10|Public Internet / Edge|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|1|2|
|25|CAPEC-465|Transparent Proxy Abuse|Medium|Unknown|10|Critical|4|3|1.25|1.2|10|ESXi / Hypervisor|Telemetry Gap / Evasion|Auto-intercept / quarantine via pre-approved playbook|1|1|
|26|CAPEC-25|Forced Deadlock|High|Low|10|Critical|4|3|1.25|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|1|6|
|27|CAPEC-227|Sustained Client Engagement|Unknown|Unknown|10|Critical|4|3|1.25|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|1|1|
|28|CAPEC-204|Lifting Sensitive Data Embedded in Cache|Medium|Unknown|10|Critical|4|3|1.5|1.0|8|ESXi / Hypervisor|Telemetry Gap / Evasion|Auto-intercept / quarantine via pre-approved playbook|1|4|
|29|CAPEC-148|Content Spoofing|Medium|Medium|10|Critical|4|3|1.25|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|1|1|
|30|CAPEC-131|Resource Leak Exposure|Medium|Medium|10|Critical|4|3|1.25|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|1|1|
|31|CAPEC-130|Excessive Allocation|Medium|Medium|10|Critical|4|3|1.25|1.2|10|Cloud Control Plane|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|1|3|
|32|CAPEC-89|Pharming|Very High|High|10|Critical|4|3|1.5|1.0|8|Data / Storage|Rare but High Impact|Auto-intercept / quarantine via pre-approved playbook|0|2|
|33|CAPEC-77|Manipulating User-Controlled Variables|Very High|High|10|Critical|4|3|1.5|1.0|8|Data / Storage|Rare but High Impact|Auto-intercept / quarantine via pre-approved playbook|0|7|
|34|CAPEC-75|Manipulating Writeable Configuration Files|Very High|High|10|Critical|4|3|1.5|1.0|8|Data / Storage|Rare but High Impact|Auto-intercept / quarantine via pre-approved playbook|0|6|
|35|CAPEC-44|Overflow Binary Resource File|Very High|High|10|Critical|4|3|1.5|1.0|8|Data / Storage|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|0|3|
|36|CAPEC-123|Buffer Manipulation|Very High|High|10|Critical|4|3|1.5|1.0|8|Data / Storage|Rare but High Impact|Auto-intercept / quarantine via pre-approved playbook|0|1|
|37|CAPEC-163|Spear Phishing|High|High|10|Critical|3|3|1.5|1.2|10|Identity / IAM|Cloud / SaaS Tenant Blast Radius|Auto-intercept / quarantine via pre-approved playbook|7|1|
|38|CAPEC-640|Inclusion of Code in Existing Process|High|Low|10|Critical|3|3|1.5|1.2|10|ICS / OT|Air-Gapped / ICS Safety|Auto-intercept / quarantine via pre-approved playbook|4|2|
|39|CAPEC-642|Replace Binaries|High|Unknown|10|Critical|3|3|1.5|1.2|10|ICS / OT|Air-Gapped / ICS Safety|Auto-intercept / quarantine via pre-approved playbook|3|1|
|40|CAPEC-471|Search Order Hijacking|Medium|Unknown|10|Critical|3|3|1.5|1.2|10|Data / Storage|Telemetry Gap / Evasion|Auto-intercept / quarantine via pre-approved playbook|3|1|
|41|CAPEC-21|Exploitation of Trusted Identifiers|High|High|10|Critical|3|3|1.5|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|3|9|
|42|CAPEC-542|Targeted Malware|Unknown|Unknown|10|Critical|3|3|1.5|1.2|10|Network / Perimeter|Telemetry Gap / Evasion|Auto-intercept / quarantine via pre-approved playbook|2|0|
|43|CAPEC-478|Modification of Windows Service Configuration|High|Low|10|Critical|3|3|1.5|1.2|10|Identity / IAM|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|2|1|
|44|CAPEC-158|Sniffing Network Traffic|Medium|Unknown|10|Critical|3|3|1.5|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|2|1|
|45|CAPEC-650|Upload a Web Shell to a Web Server|High|Unknown|10|Critical|3|3|1.5|1.2|10|Identity / IAM|Zero-Day / Unknown Exploit|Auto-intercept / quarantine via pre-approved playbook|1|2|
|46|CAPEC-65|Sniff Application Code|High|Low|10|Critical|3|3|1.5|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|1|4|
|47|CAPEC-616|Establish Rogue Location|Medium|Medium|10|Critical|3|3|1.5|1.2|10|ESXi / Hypervisor|Telemetry Gap / Evasion|Auto-intercept / quarantine via pre-approved playbook|1|1|
|48|CAPEC-57|Utilizing REST's Trust in the System Resource to Obtain Sensitive Data|Very High|Medium|10|Critical|3|3|1.5|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|1|3|
|49|CAPEC-543|Counterfeit Websites|High|Unknown|10|Critical|3|3|1.5|1.2|10|ESXi / Hypervisor|Telemetry Gap / Evasion|Auto-intercept / quarantine via pre-approved playbook|1|0|
|50|CAPEC-31|Accessing/Intercepting/Modifying HTTP Cookies|High|High|10|Critical|3|3|1.5|1.2|10|Identity / IAM|Identity / MFA Bypass|Auto-intercept / quarantine via pre-approved playbook|1|11|

## Highest-Risk Tactic and Surface Intersections

|tactic|surface|technique_count|avg_final_score|max_final_score|critical_count|medium_high_count|
|---|---|---|---|---|---|---|
|Impact|Public Internet / Edge|14|10|10|14|0|
|Impact|ESXi / Hypervisor|8|10|10|8|0|
|Impact|SaaS / Office / Email|6|10|10|6|0|
|Impact|Containers / Kubernetes|5|10|10|5|0|
|Collection|ESXi / Hypervisor|4|10|10|4|0|
|Credential Access|Containers / Kubernetes|4|10|10|4|0|
|Lateral Movement|ESXi / Hypervisor|4|10|10|4|0|
|Exfiltration|SaaS / Office / Email|3|10|10|3|0|
|Command and Control|SaaS / Office / Email|1|10|10|1|0|
|Exfiltration|Identity / IAM|1|10|10|1|0|
|Defense Impairment|Containers / Kubernetes|1|10|10|1|0|
|Initial Access|Containers / Kubernetes|1|10|10|1|0|
|Command and Control|ESXi / Hypervisor|34|9.88|10|34|0|
|Impact|Endpoint / User|14|9.88|10|14|0|
|Defense Impairment|ESXi / Hypervisor|4|9.85|10|4|0|
|Collection|Endpoint / User|16|9.84|10|16|0|
|Persistence|ESXi / Hypervisor|15|9.79|10|15|0|
|Defense Impairment|SaaS / Office / Email|9|9.79|10|9|0|
|Exfiltration|ESXi / Hypervisor|11|9.77|10|11|0|
|Privilege Escalation|ESXi / Hypervisor|11|9.77|10|11|0|
|Exfiltration|Server / Workload|13|9.74|10|13|0|
|Lateral Movement|Cloud Control Plane|10|9.69|10|10|0|
|Lateral Movement|Containers / Kubernetes|2|9.69|10|2|0|
|Command and Control|Endpoint / User|31|9.68|10|31|0|
|Credential Access|Endpoint / User|31|9.66|10|31|0|
|Lateral Movement|Endpoint / User|13|9.66|10|12|1|
|Exfiltration|Endpoint / User|9|9.63|10|9|0|
|Lateral Movement|SaaS / Office / Email|6|9.59|10|6|0|
|Initial Access|ESXi / Hypervisor|5|9.55|10|5|0|
|Privilege Escalation|Public Internet / Edge|9|9.52|10|9|0|
|Credential Access|Server / Workload|53|9.51|10|51|2|
|Credential Access|Public Internet / Edge|21|9.49|10|20|1|
|Impact|Cloud Control Plane|23|9.46|10|22|0|
|Persistence|Cloud Control Plane|25|9.38|10|23|2|
|Privilege Escalation|Containers / Kubernetes|8|9.38|10|7|1|
|Persistence|Containers / Kubernetes|8|9.3|10|7|1|
|Privilege Escalation|SaaS / Office / Email|15|9.29|10|14|1|
|Collection|Cloud Control Plane|14|9.29|10|13|0|
|Command and Control|Identity / IAM|7|9.28|10|7|0|
|Command and Control|Public Internet / Edge|29|9.26|10|28|0|
|Collection|Server / Workload|32|9.24|10|30|0|
|Command and Control|Server / Workload|47|9.17|10|44|1|
|Impact|Network / Perimeter|23|9.06|10|21|0|
|Stealth|ESXi / Hypervisor|25|9.03|10|22|3|
|Collection|Public Internet / Edge|20|9.0|10|18|1|
|Stealth|Containers / Kubernetes|5|9.0|10|4|1|
|Impact|Server / Workload|34|8.99|10|31|0|
|Privilege Escalation|Cloud Control Plane|24|8.99|10|20|3|
|Lateral Movement|Data / Storage|5|8.88|10|4|1|
|Persistence|SaaS / Office / Email|29|8.79|10|27|1|

## Highest-Risk Edge-Case Stressors

|edge_case|technique_count|avg_final_score|max_final_score|critical_count|medium_high_count|
|---|---|---|---|---|---|
|Cloud / SaaS Tenant Blast Radius|245|7.8|10|176|36|
|Living-off-the-Land|434|7.74|10|288|112|
|Insider / Trusted Access|310|7.73|10|227|42|
|Zero-Day / Unknown Exploit|650|7.11|10|408|126|
|Identity / MFA Bypass|446|6.55|10|262|70|
|Exploit Chain / Multi-Step|468|6.37|10|266|75|
|Destructive / Ransomware|208|6.11|10|120|16|
|Telemetry Gap / Evasion|700|4.29|10|248|96|
|Supply Chain / Trusted Dependency|191|3.86|10|54|32|
|Rare but High Impact|116|3.8|10|35|16|
|Air-Gapped / ICS Safety|144|1.6|10|21|6|
|AI-Scaled Social Engineering|73|1.35|10|5|2|

## Defensive Control Priorities

These are weighted by the final scores of the ATT&CK techniques they mitigate or observe.

### Mitigations

|rank|mitigation|weighted_priority|
|---|---|---|
|1|User Account Management|988.6|
|2|Privileged Account Management|955.5|
|3|Audit|929.3|
|4|Disable or Remove Feature or Program|595.4|
|5|Execution Prevention|583.4|
|6|Network Intrusion Prevention|522.4|
|7|Restrict File and Directory Permissions|505.4|
|8|User Training|492.1|
|9|Filter Network Traffic|440.1|
|10|Multi-factor Authentication|414.1|
|11|Password Policies|410.6|
|12|Update Software|363.0|
|13|Behavior Prevention on Endpoint|360.8|
|14|Operating System Configuration|349.6|
|15|Network Segmentation|338.6|
|16|Encrypt Sensitive Information|297.5|
|17|Software Configuration|272.2|
|18|Restrict Web-Based Content|258.1|
|19|Restrict Registry Permissions|174.4|
|20|Code Signing|170.3|

### Data Sources

|rank|data_source|weighted_priority|
|---|---|---|
|1|Process|3962.6|
|2|File|2521.4|
|3|Network Traffic|1857.0|
|4|Command|1767.6|
|5|Module|863.9|
|6|Application Log|844.0|
|7|Windows Registry|769.1|
|8|User Account|739.0|
|9|Logon Session|705.0|
|10|Service|331.9|
|11|Cloud Service|287.1|
|12|Active Directory|281.9|
|13|Script|235.0|
|14|Cloud Storage|172.5|
|15|Scheduled Job|158.2|
|16|Instance|136.5|
|17|Drive|131.5|
|18|Driver|130.9|
|19|Sensor Health|129.6|
|20|Firewall|104.8|

## Coverage Notes

- Techniques with CAPEC mappings: 180 of 943.
- Techniques with CWE mappings: 168 of 943.
- Techniques without CAPEC/CWE mappings are not treated as low risk. Their CAPEC/CWE component defaults to neutral because missing mappings are a data-coverage issue, not proof of low threat.
- Observed usage is based on MITRE group/software relationships in the local dataset. It is a public-reporting signal, not a probability of compromise in your environment.
- Surface multipliers represent default exposure/impact assumptions. Replace them with local asset exposure, business impact, and compensating-control data for production risk governance.

## Complete Appendices

Complete per-vector scores are in `attack_vector_scores.csv` and the workbook sheet `Technique Scores`.
Complete per-surface multipliers are in `surface_multiplier_matrix.csv` and the workbook sheet `Surface Matrix`.
Complete edge-case stressor multipliers are in `edge_case_matrix.csv` and the workbook sheet `Edge Case Matrix`.
Edge-case aggregate priorities are in `edge_case_summary.csv` and the workbook sheet `Edge Case Summary`.
Complete CAPEC scores are in `capec_attack_pattern_scores.csv` and the workbook sheet `CAPEC Scores`.
