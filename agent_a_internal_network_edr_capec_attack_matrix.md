# Agent A CAPEC + MITRE ATT&CK Watch Matrix

Generated: 2026-07-04T20:59:48

Agent: Rule-Based + ML Hybrid Internal Network & EDR Agent

Internal network, EDR, endpoint, server, lateral movement, C2, data movement, ransomware, and baseline anomaly monitoring.

This file is a Layer 1 watchlist source. It is not an exploit guide and does not authorize containment. Layer 1 uses it to map observations to ATT&CK/CAPEC/CWE labels, predict likely next steps, and emit structured JSON to the deterministic Layer 2 orchestrator.

## Scope

- Input: sanitized, normalized telemetry from Layer 0 preprocessing.
- Output: read-only JSON finding for Layer 2 correlation.
- Layer 1 does not compute FinalRiskScore, DetectionConfidence, priority tier, or auto-containment.
- Layer 2 performs BFT consensus, deterministic scoring, OPA policy checks, and playbook execution.

## Primary Surfaces

Network / Perimeter, Endpoint / User, Server / Workload, Data / Storage, ESXi / Hypervisor

## Primary Evidence Fields

- process tree and command line
- hash, signer, file path, and module load
- source/destination IP, port, protocol, and DNS domain
- endpoint hostname, EDR alert ID, and user
- baseline deviation and first-seen timestamp

## Included Matrix Size

- Relevant ATT&CK candidates found: 771
- ATT&CK rows included here: 90
- Relevant CAPEC candidates found: 215
- CAPEC rows included here: 70
- CAPEC IDs directly linked from included ATT&CK rows: 21

## Included ATT&CK ID Set

- T1570, T1041, T1027, T1490, T1567, T1005, T1053, T1560, T1572, T1573, T1105, T1048, T1090, T1021
- T1489, T1071.004, T1036, T1486, T1205.002, T1048.003, T1197, T1071.001, T1480.001, T1074, T1218.014, T1048.001, T1480, T1485
- T1037, T1048.002, T1011, T1021.002, T1567.001, T1567.003, T1037.004, T1505, T1205, T1567.004, T1127.001, T1125, T1090.001, T1219
- T1059, T1218.009, T1564.006, T1127, T1027.013, T1020, T1021.001, T1210, T1021.004, T1218.003, T1027.018, T1543.003, T1074.001, T1574.001
- T1567.002, T1090.003, T1686, T1001.003, T1074.002, T1011.001, T1574.011, T1176, T1029, T1573.002, T1560.002, T1070.003, T1014, T1547.006
- T1218.013, T1542, T1219.001, T1053.005, T1102.002, T1102.003, T1127.003, T1046, T1505.004, T1070.007, T1216, T1205.001, T1027.003, T1546
- T1556.008, T1546.004, T1124, T1573.001, T1560.001, T1001

## Included CAPEC ID Set

- CAPEC-542, CAPEC-481, CAPEC-646, CAPEC-465, CAPEC-574, CAPEC-471, CAPEC-573, CAPEC-634, CAPEC-102, CAPEC-552, CAPEC-158, CAPEC-203, CAPEC-177, CAPEC-700
- CAPEC-555, CAPEC-35, CAPEC-675, CAPEC-543, CAPEC-643, CAPEC-180, CAPEC-165, CAPEC-292, CAPEC-673, CAPEC-637, CAPEC-589, CAPEC-457, CAPEC-640, CAPEC-204
- CAPEC-616, CAPEC-267, CAPEC-448, CAPEC-649, CAPEC-217, CAPEC-578, CAPEC-572, CAPEC-15, CAPEC-698, CAPEC-504, CAPEC-678, CAPEC-669, CAPEC-186, CAPEC-159
- CAPEC-665, CAPEC-478, CAPEC-697, CAPEC-551, CAPEC-17, CAPEC-482, CAPEC-21, CAPEC-655, CAPEC-652, CAPEC-560, CAPEC-550, CAPEC-268, CAPEC-620, CAPEC-509
- CAPEC-523, CAPEC-564, CAPEC-662, CAPEC-489, CAPEC-148, CAPEC-130, CAPEC-529, CAPEC-150, CAPEC-593, CAPEC-19, CAPEC-270, CAPEC-609, CAPEC-561, CAPEC-9

## MITRE ATT&CK Matrix Vectors

| rank | attack_id | attack_vector | tactics | global_score_ref | grade_ref | surface | edge_case | related_capec | watch_focus |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | T1570 | Lateral Tool Transfer | Lateral Movement | 10 | Critical | ESXi / Hypervisor | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Process; File; Network Share |
| 2 | T1041 | Exfiltration Over C2 Channel | Exfiltration | 10 | Critical | ESXi / Hypervisor | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; File |
| 3 | T1027 | Obfuscated Files or Information | Stealth | 10 | Critical | ESXi / Hypervisor | Telemetry Gap / Evasion | CAPEC-267; CAPEC-542 | Telemetry Gap / Evasion; Watch: Command; Network Traffic; Process; File |
| 4 | T1490 | Inhibit System Recovery | Impact | 10 | Critical | Cloud Control Plane | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Process; Windows Registry; Service; File; Snapshot; Cloud Storage |
| 5 | T1567 | Exfiltration Over Web Service | Exfiltration | 10 | Critical | ESXi / Hypervisor | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Network Traffic; Process; File; Application Log |
| 6 | T1005 | Data from Local System | Collection | 10 | Critical | ESXi / Hypervisor | Destructive / Ransomware | CAPEC-204; CAPEC-37; CAPEC-545; CAPEC-647 | Destructive / Ransomware; Watch: Command; Process; File |
| 7 | T1053 | Scheduled Task/Job | Execution; Persistence; Privilege Escalation | 10 | Critical | ESXi / Hypervisor | Exploit Chain / Multi-Step |  | Exploit Chain / Multi-Step; Watch: Command; Process; File; Scheduled Job |
| 8 | T1560 | Archive Collected Data | Collection | 10 | Critical | Data / Storage | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Process; File; Module |
| 9 | T1572 | Protocol Tunneling | Command and Control | 10 | Critical | ESXi / Hypervisor | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; Application Log |
| 10 | T1573 | Encrypted Channel | Command and Control | 10 | Critical | ESXi / Hypervisor | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; Module; Application Log |
| 11 | T1105 | Ingress Tool Transfer | Command and Control | 10 | Critical | ESXi / Hypervisor | Living-off-the-Land |  | Living-off-the-Land; Watch: Command; Process; Network Traffic; File |
| 12 | T1048 | Exfiltration Over Alternative Protocol | Exfiltration | 10 | Critical | Cloud Control Plane | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Network Traffic; Process; File; Cloud Storage |
| 13 | T1090 | Proxy | Command and Control | 10 | Critical | ESXi / Hypervisor | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Process; Network Traffic; Firewall |
| 14 | T1021 | Remote Services | Lateral Movement | 10 | Critical | ESXi / Hypervisor | Identity / MFA Bypass | CAPEC-555 | Identity / MFA Bypass; Watch: Command; Process; Logon Session; Network Traffic |
| 15 | T1489 | Service Stop | Impact | 10 | Critical | Cloud Control Plane | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Process; Service; File; Logon Session |
| 16 | T1071.004 | DNS | Command and Control | 10 | Critical | ESXi / Hypervisor | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process |
| 17 | T1036 | Masquerading | Stealth | 10 | Critical | ESXi / Hypervisor | Cloud / SaaS Tenant Blast Radius | CAPEC-177 | Cloud / SaaS Tenant Blast Radius; Watch: Command; Process; File; Service; Image |
| 18 | T1486 | Data Encrypted for Impact | Impact | 10 | Critical | Cloud Control Plane | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Process; File; Cloud Storage |
| 19 | T1205.002 | Socket Filters | Stealth; Persistence; Command and Control | 10 | Critical | Network / Perimeter | Living-off-the-Land |  | Living-off-the-Land; Watch: Network Traffic; Process; Module; Driver; Service |
| 20 | T1048.003 | Exfiltration Over Unencrypted Non-C2 Protocol | Exfiltration | 10 | Critical | ESXi / Hypervisor | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Network Traffic; Process; File |
| 21 | T1197 | BITS Jobs | Stealth; Persistence; Execution | 7.5 | Critical | Network / Perimeter | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Process; Network Traffic; Service |
| 22 | T1071.001 | Web Protocols | Command and Control | 10 | Critical | ESXi / Hypervisor | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Network Traffic; Process |
| 23 | T1480.001 | Environmental Keying | Stealth | 10 | Critical | Data / Storage | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Process; Command; Network Traffic; WMI; Module; File; Logon Session |
| 24 | T1074 | Data Staged | Collection | 10 | Critical | Cloud Control Plane | Cloud / SaaS Tenant Blast Radius |  | Cloud / SaaS Tenant Blast Radius; Watch: Command; Process; File; Cloud Storage |
| 25 | T1218.014 | MMC | Stealth | 10 | Critical | Data / Storage | Living-off-the-Land |  | Living-off-the-Land; Watch: Command; Process; Network Traffic; Windows Registry; Module; File |
| 26 | T1048.001 | Exfiltration Over Symmetric Encrypted Non-C2 Protocol | Exfiltration | 10 | Critical | ESXi / Hypervisor | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Network Traffic; Process |
| 27 | T1480 | Execution Guardrails | Stealth | 10 | Critical | ESXi / Hypervisor | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Process; Network Traffic; Windows Registry; WMI; Module; File; Logon Session; User Account |
| 28 | T1485 | Data Destruction | Impact | 10 | Critical | Cloud Control Plane | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Process; File; Volume; Cloud Storage |
| 29 | T1037 | Boot or Logon Initialization Scripts | Persistence; Privilege Escalation | 10 | Critical | ESXi / Hypervisor | Identity / MFA Bypass | CAPEC-564 | Identity / MFA Bypass; Watch: Process; File; Windows Registry; Scheduled Job; Script; Service |
| 30 | T1048.002 | Exfiltration Over Asymmetric Encrypted Non-C2 Protocol | Exfiltration | 10 | Critical | ESXi / Hypervisor | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Network Traffic; Process; File |
| 31 | T1011 | Exfiltration Over Other Network Medium | Exfiltration | 10 | Critical | Data / Storage | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Network Traffic; Process; File; Sensor Health |
| 32 | T1021.002 | SMB/Windows Admin Shares | Lateral Movement | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-561 | Identity / MFA Bypass; Watch: Process; Logon Session; Network Traffic |
| 33 | T1567.001 | Exfiltration to Code Repository | Exfiltration | 10 | Critical | ESXi / Hypervisor | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Network Traffic; Process; File |
| 34 | T1567.003 | Exfiltration to Text Storage Sites | Exfiltration | 10 | Critical | ESXi / Hypervisor | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Network Traffic; Process; File |
| 35 | T1037.004 | RC Scripts | Persistence; Privilege Escalation | 10 | Critical | ESXi / Hypervisor | Living-off-the-Land |  | Living-off-the-Land; Watch: Command; Process; File; Script |
| 36 | T1505 | Server Software Component | Persistence | 10 | Critical | ESXi / Hypervisor | Living-off-the-Land |  | Living-off-the-Land; Watch: Command; Network Traffic; Process; Scheduled Job; Application Log |
| 37 | T1205 | Traffic Signaling | Stealth; Persistence; Command and Control | 8.33 | Critical | Network / Perimeter | Exploit Chain / Multi-Step |  | Exploit Chain / Multi-Step; Watch: Command; Network Traffic; Process |
| 38 | T1567.004 | Exfiltration Over Webhook | Exfiltration | 10 | Critical | ESXi / Hypervisor | Cloud / SaaS Tenant Blast Radius |  | Cloud / SaaS Tenant Blast Radius; Watch: Command; Network Traffic; Process; File; Application Log |
| 39 | T1127.001 | MSBuild | Stealth; Execution | 7.5 | Critical | Network / Perimeter | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; Network Traffic; Script; Module; File |
| 40 | T1125 | Video Capture | Collection | 10 | Critical | Data / Storage | Zero-Day / Unknown Exploit | CAPEC-634 | Zero-Day / Unknown Exploit; Watch: Command; Network Traffic; Process; Module; File |
| 41 | T1090.001 | Internal Proxy | Command and Control | 10 | Critical | ESXi / Hypervisor | Zero-Day / Unknown Exploit | CAPEC-465 | Zero-Day / Unknown Exploit; Watch: Command; Network Traffic; Process; Firewall; Service |
| 42 | T1219 | Remote Access Tools | Command and Control | 10 | Critical | Network / Perimeter | Living-off-the-Land |  | Living-off-the-Land; Watch: Process; Network Traffic; Windows Registry; File; Service |
| 43 | T1059 | Command and Scripting Interpreter | Execution | 6.25 | Medium High | Cloud Control Plane | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Process; User Account |
| 44 | T1218.009 | Regsvcs/Regasm | Stealth | 7.5 | Critical | Network / Perimeter | Living-off-the-Land |  | Living-off-the-Land; Watch: Command; Process; Network Traffic; Windows Registry; Module; File |
| 45 | T1564.006 | Run Virtual Instance | Stealth | 10 | Critical | ESXi / Hypervisor | Living-off-the-Land |  | Living-off-the-Land; Watch: Command; Process; Windows Registry; File; Service; Image |
| 46 | T1127 | Trusted Developer Utilities Proxy Execution | Stealth; Execution | 7.5 | Critical | Network / Perimeter | Zero-Day / Unknown Exploit | CAPEC-670 | Zero-Day / Unknown Exploit; Watch: Process; Network Traffic; Module; File |
| 47 | T1027.013 | Encrypted/Encoded File | Stealth | 9.0 | Critical | Network / Perimeter | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Process; Command; Network Traffic; Module |
| 48 | T1020 | Automated Exfiltration | Exfiltration | 8.33 | Critical | Network / Perimeter | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; Network Traffic; Scheduled Job |
| 49 | T1021.001 | Remote Desktop Protocol | Lateral Movement | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Logon Session; Process; Network Traffic |
| 50 | T1210 | Exploitation of Remote Services | Lateral Movement | 10 | Critical | ESXi / Hypervisor | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; Network Traffic; Module; File; Application Log |
| 51 | T1021.004 | SSH | Lateral Movement | 10 | Critical | ESXi / Hypervisor | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Command; Network Traffic; Process; Logon Session |
| 52 | T1218.003 | CMSTP | Stealth | 7.5 | Critical | Server / Workload | Living-off-the-Land |  | Living-off-the-Land; Watch: Command; Process; Network Traffic; Windows Registry; File |
| 53 | T1027.018 | Invisible Unicode | Stealth | 7.5 | Critical | Network / Perimeter | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Process; Network Traffic; Script; Module; File |
| 54 | T1543.003 | Windows Service | Persistence; Privilege Escalation | 9.0 | Critical | Server / Workload | Zero-Day / Unknown Exploit | CAPEC-478 | Zero-Day / Unknown Exploit; Watch: Windows Registry; Process; Service; Driver |
| 55 | T1074.001 | Local Data Staging | Collection | 10 | Critical | ESXi / Hypervisor | Cloud / SaaS Tenant Blast Radius |  | Cloud / SaaS Tenant Blast Radius; Watch: Command; Process; Snapshot; File |
| 56 | T1574.001 | DLL | Stealth; Execution | 10 | Critical | Data / Storage | Telemetry Gap / Evasion | CAPEC-471 | Telemetry Gap / Evasion; Watch: Process; Windows Registry; Module; File |
| 57 | T1567.002 | Exfiltration to Cloud Storage | Exfiltration | 10 | Critical | ESXi / Hypervisor | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Network Traffic; Process; File |
| 58 | T1090.003 | Multi-hop Proxy | Command and Control | 10 | Critical | ESXi / Hypervisor | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Firmware; Network Traffic; Process |
| 59 | T1686 | Disable or Modify System Firewall | Defense Impairment | 10 | Critical | ESXi / Hypervisor | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Command; Process; Firewall; Windows Registry |
| 60 | T1001.003 | Protocol or Service Impersonation | Command and Control | 10 | Critical | ESXi / Hypervisor | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process |
| 61 | T1074.002 | Remote Data Staging | Collection | 10 | Critical | Cloud Control Plane | Cloud / SaaS Tenant Blast Radius |  | Cloud / SaaS Tenant Blast Radius; Watch: Command; Network Traffic; Process; File; Cloud Storage; Network Share |
| 62 | T1011.001 | Exfiltration Over Bluetooth | Exfiltration | 10 | Critical | Data / Storage | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Process; Network Traffic; File |
| 63 | T1574.011 | Services Registry Permissions Weakness | Stealth; Execution | 6.25 | Medium High | Server / Workload | Zero-Day / Unknown Exploit | CAPEC-478 | Zero-Day / Unknown Exploit; Watch: Process; Windows Registry; Service |
| 64 | T1176 | Software Extensions | Persistence | 7.5 | Critical | Network / Perimeter | Zero-Day / Unknown Exploit | CAPEC-698 | Zero-Day / Unknown Exploit; Watch: Command; Process; Network Traffic; Windows Registry; File |
| 65 | T1029 | Scheduled Transfer | Exfiltration | 8.33 | Critical | Network / Perimeter | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; Network Traffic; Scheduled Job |
| 66 | T1573.002 | Asymmetric Cryptography | Command and Control | 10 | Critical | ESXi / Hypervisor | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; Module; Application Log |
| 67 | T1560.002 | Archive via Library | Collection | 10 | Critical | Data / Storage | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Process; File; Module |
| 68 | T1070.003 | Clear Command History | Stealth | 9.38 | Critical | ESXi / Hypervisor | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Command; Process; File |
| 69 | T1014 | Rootkit | Stealth | 7.5 | Critical | Server / Workload | Telemetry Gap / Evasion | CAPEC-552 | Telemetry Gap / Evasion; Watch: Process; File; Module; Driver; Service |
| 70 | T1547.006 | Kernel Modules and Extensions | Persistence; Privilege Escalation | 7.5 | Critical | Server / Workload | Exploit Chain / Multi-Step | CAPEC-552 | Exploit Chain / Multi-Step; Watch: Command; Kernel; Process; File |
| 71 | T1218.013 | Mavinject | Stealth | 7.5 | Critical | Network / Perimeter | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; Command; Network Traffic; Module; File |
| 72 | T1542 | Pre-OS Boot | Stealth; Persistence | 7.5 | Critical | Server / Workload | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Firmware; Drive; Process; File |
| 73 | T1219.001 | IDE Tunneling | Command and Control | 8.33 | Critical | Network / Perimeter | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; File; Network Traffic |
| 74 | T1053.005 | Scheduled Task | Execution; Persistence; Privilege Escalation | 10 | Critical | Identity / IAM | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; Windows Registry; Scheduled Job; File |
| 75 | T1102.002 | Bidirectional Communication | Command and Control | 10 | Critical | ESXi / Hypervisor | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Process; Network Traffic |
| 76 | T1102.003 | One-Way Communication | Command and Control | 10 | Critical | ESXi / Hypervisor | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Network Traffic; Process |
| 77 | T1127.003 | JamPlus | Stealth; Execution | 6.25 | Medium High | Network / Perimeter | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; File; Network Traffic |
| 78 | T1046 | Network Service Discovery | Discovery | 7.5 | Critical | Cloud Control Plane | Zero-Day / Unknown Exploit | CAPEC-300 | Zero-Day / Unknown Exploit; Watch: Process; Network Traffic |
| 79 | T1505.004 | IIS Components | Persistence | 7.5 | Critical | Server / Workload | Exploit Chain / Multi-Step | CAPEC-698 | Exploit Chain / Multi-Step; Watch: Process; File; Module; Service; Application Log |
| 80 | T1070.007 | Clear Network Connection History and Configurations | Stealth | 7.5 | Critical | Public Internet / Edge | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Command; Network Traffic; Process; Windows Registry; File; Firewall |
| 81 | T1216 | System Script Proxy Execution | Stealth | 7.5 | Critical | Server / Workload | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Command; Process; Module; File |
| 82 | T1205.001 | Port Knocking | Stealth; Persistence; Command and Control | 8.33 | Critical | Network / Perimeter | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Process; Network Traffic |
| 83 | T1027.003 | Steganography | Stealth | 10 | Critical | Data / Storage | Telemetry Gap / Evasion | CAPEC-636 | Telemetry Gap / Evasion; Watch: Process; Network Traffic; File |
| 84 | T1546 | Event Triggered Execution | Privilege Escalation; Persistence | 10 | Critical | Identity / IAM | Cloud / SaaS Tenant Blast Radius |  | Cloud / SaaS Tenant Blast Radius; Watch: Command; Network Traffic; Process; Windows Registry; WMI; Scheduled Job; File; Script; Cloud Service |
| 85 | T1556.008 | Network Provider DLL | Defense Impairment; Persistence; Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; File; Windows Registry; Module |
| 86 | T1546.004 | Unix Shell Configuration Modification | Privilege Escalation; Persistence | 6.25 | Medium High | Server / Workload | Identity / MFA Bypass | CAPEC-19 | Identity / MFA Bypass; Watch: Process; File; Network Traffic |
| 87 | T1124 | System Time Discovery | Discovery | 9.0 | Critical | ESXi / Hypervisor | Living-off-the-Land | CAPEC-295 | Living-off-the-Land; Watch: Process; Command; Scheduled Job; File; Module; User Account |
| 88 | T1573.001 | Symmetric Cryptography | Command and Control | 10 | Critical | ESXi / Hypervisor | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; Module; Application Log |
| 89 | T1560.001 | Archive via Utility | Collection | 10 | Critical | Data / Storage | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Process; File; Module |
| 90 | T1001 | Data Obfuscation | Command and Control | 10 | Critical | ESXi / Hypervisor | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Network Traffic; Process |

## CAPEC Attack Pattern Matrix

| rank | capec_id | attack_pattern | severity_ref | likelihood_ref | global_score_ref | surface | edge_case | related_attack | watch_focus |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | CAPEC-542 | Targeted Malware | Unknown | Unknown | 10 | Network / Perimeter | Telemetry Gap / Evasion | T1027; T1587.001 | Telemetry Gap / Evasion |
| 2 | CAPEC-481 | Contradictory Destinations in Traffic Routing Schemes | High | Medium | 10 | ESXi / Hypervisor | Telemetry Gap / Evasion | T1090.004 | Telemetry Gap / Evasion; CWE: CWE-923 |
| 3 | CAPEC-646 | Peripheral Footprinting | Medium | Low | 7.5 | Network / Perimeter | Destructive / Ransomware | T1120 | Destructive / Ransomware; CWE: CWE-200 |
| 4 | CAPEC-465 | Transparent Proxy Abuse | Medium | Unknown | 10 | ESXi / Hypervisor | Telemetry Gap / Evasion | T1090.001 | Telemetry Gap / Evasion; CWE: CWE-441 |
| 5 | CAPEC-574 | Services Footprinting | Low | Low | 5.0 | Server / Workload | Zero-Day / Unknown Exploit | T1007 | Zero-Day / Unknown Exploit; CWE: CWE-200 |
| 6 | CAPEC-471 | Search Order Hijacking | Medium | Unknown | 10 | Data / Storage | Telemetry Gap / Evasion | T1574.001; T1574.004; T1574.008 | Telemetry Gap / Evasion; CWE: CWE-427 |
| 7 | CAPEC-573 | Process Footprinting | Low | Low | 7.5 | ESXi / Hypervisor | Zero-Day / Unknown Exploit | T1057 | Zero-Day / Unknown Exploit; CWE: CWE-200 |
| 8 | CAPEC-634 | Probe Audio and Video Peripherals | High | Low | 10 | Data / Storage | Zero-Day / Unknown Exploit | T1123; T1125 | Zero-Day / Unknown Exploit; CWE: CWE-267 |
| 9 | CAPEC-102 | Session Sidejacking | High | High | 7.5 | Network / Perimeter | Destructive / Ransomware |  | Destructive / Ransomware; CWE: CWE-294; CWE-319; CWE-522; CWE-523; CWE-614 |
| 10 | CAPEC-552 | Install Rootkit | High | Medium | 10 | Identity / IAM | Telemetry Gap / Evasion | T1014; T1542.003; T1547.006 | Telemetry Gap / Evasion; CWE: CWE-284 |
| 11 | CAPEC-158 | Sniffing Network Traffic | Medium | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1040; T1111 | Identity / MFA Bypass; CWE: CWE-311 |
| 12 | CAPEC-203 | Manipulate Registry Information | Medium | Unknown | 10 | Identity / IAM | Telemetry Gap / Evasion | T1112; T1647 | Telemetry Gap / Evasion; CWE: CWE-15 |
| 13 | CAPEC-177 | Create files with the same name as files protected with a higher classification | Very High | Unknown | 10 | ESXi / Hypervisor | Telemetry Gap / Evasion | T1036 | Telemetry Gap / Evasion; CWE: CWE-706 |
| 14 | CAPEC-700 | Network Boundary Bridging | High | Medium | 3.75 | Network / Perimeter | Telemetry Gap / Evasion | T1599 | Telemetry Gap / Evasion |
| 15 | CAPEC-555 | Remote Services with Stolen Credentials | Very High | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1021; T1114.002; T1133 | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-294; CWE-308; CWE-309; CWE-521; CWE-522 |
| 16 | CAPEC-35 | Leverage Executable Code in Non-Executable Files | Very High | High | 10 | Data / Storage | Rare but High Impact | T1027.006; T1027.009; T1564.009 | Rare but High Impact; CWE: CWE-270; CWE-272; CWE-282; CWE-59; CWE-94; CWE-95; CWE-96; CWE-97 |
| 17 | CAPEC-675 | Retrieve Data from Decommissioned Devices | Medium | Medium | 10 | Data / Storage | Destructive / Ransomware | T1052 | Destructive / Ransomware; CWE: CWE-1266 |
| 18 | CAPEC-543 | Counterfeit Websites | High | Unknown | 10 | ESXi / Hypervisor | Telemetry Gap / Evasion | T1036.005 | Telemetry Gap / Evasion |
| 19 | CAPEC-643 | Identify Shared Files/Directories on System | Medium | Medium | 6.0 | Network / Perimeter | Zero-Day / Unknown Exploit | T1135 | Zero-Day / Unknown Exploit; CWE: CWE-200; CWE-267 |
| 20 | CAPEC-180 | Exploiting Incorrectly Configured Access Control Security Levels | Medium | High | 9.38 | Data / Storage | Rare but High Impact | T1574.010 | Rare but High Impact; CWE: CWE-1190; CWE-1191; CWE-1193; CWE-1220; CWE-1268; CWE-1280; CWE-1297; CWE-1311; CWE-1315; CWE-1318; CWE-1320; CWE-1321; CWE-732 |
| 21 | CAPEC-165 | File Manipulation | Medium | Unknown | 9.38 | Data / Storage | Telemetry Gap / Evasion | T1036.003 | Telemetry Gap / Evasion |
| 22 | CAPEC-292 | Host Discovery | Low | Unknown | 9.0 | ESXi / Hypervisor | Telemetry Gap / Evasion | T1018 | Telemetry Gap / Evasion; CWE: CWE-200 |
| 23 | CAPEC-673 | Developer Signing Maliciously Altered Software | High | Medium | 5.0 | Network / Perimeter | Supply Chain / Trusted Dependency | T1195.002 | Supply Chain / Trusted Dependency |
| 24 | CAPEC-637 | Collect Data from Clipboard | Low | Low | 7.5 | Data / Storage | Zero-Day / Unknown Exploit | T1115 | Zero-Day / Unknown Exploit; CWE: CWE-267 |
| 25 | CAPEC-589 | DNS Blocking | Unknown | Unknown | 3.33 | Network / Perimeter | Destructive / Ransomware |  | Destructive / Ransomware; CWE: CWE-300 |
| 26 | CAPEC-457 | USB Memory Attacks | High | Low | 8.33 | Network / Perimeter | Air-Gapped / ICS Safety | T1091; T1092 | Air-Gapped / ICS Safety; CWE: CWE-1299 |
| 27 | CAPEC-640 | Inclusion of Code in Existing Process | High | Low | 10 | ICS / OT | Air-Gapped / ICS Safety | T1505.005; T1574.006; T1574.013; T1620 | Air-Gapped / ICS Safety; CWE: CWE-114; CWE-829 |
| 28 | CAPEC-204 | Lifting Sensitive Data Embedded in Cache | Medium | Unknown | 10 | ESXi / Hypervisor | Telemetry Gap / Evasion | T1005 | Telemetry Gap / Evasion; CWE: CWE-1239; CWE-1258; CWE-311; CWE-524 |
| 29 | CAPEC-616 | Establish Rogue Location | Medium | Medium | 10 | ESXi / Hypervisor | Telemetry Gap / Evasion | T1036.005 | Telemetry Gap / Evasion; CWE: CWE-200 |
| 30 | CAPEC-267 | Leverage Alternate Encoding | High | High | 10 | ESXi / Hypervisor | Telemetry Gap / Evasion | T1027 | Telemetry Gap / Evasion; CWE: CWE-172; CWE-173; CWE-180; CWE-181; CWE-20; CWE-692; CWE-697; CWE-73; CWE-74 |
| 31 | CAPEC-448 | Embed Virus into DLL | High | Medium | 10 | Data / Storage | Telemetry Gap / Evasion | T1027.009 | Telemetry Gap / Evasion; CWE: CWE-506 |
| 32 | CAPEC-649 | Adding a Space to a File Extension | Medium | Low | 9.38 | Data / Storage | Telemetry Gap / Evasion | T1036.006 | Telemetry Gap / Evasion; CWE: CWE-46 |
| 33 | CAPEC-217 | Exploiting Incorrectly Configured SSL/TLS | Unknown | Low | 5.0 | Data / Storage | Destructive / Ransomware |  | Destructive / Ransomware; CWE: CWE-201 |
| 34 | CAPEC-578 | Disable Security Software | Medium | Medium | 10 | Identity / IAM | Identity / MFA Bypass | T1556.006 | Identity / MFA Bypass; CWE: CWE-284 |
| 35 | CAPEC-572 | Artificially Inflate File Sizes | Medium | High | 10 | Data / Storage | Rare but High Impact | T1027.001 | Rare but High Impact |
| 36 | CAPEC-15 | Command Delimiters | High | High | 10 | Data / Storage | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-138; CWE-140; CWE-146; CWE-154; CWE-157; CWE-184; CWE-185; CWE-697; CWE-77; CWE-78; CWE-93 |
| 37 | CAPEC-698 | Install Malicious Extension | High | Medium | 7.5 | Server / Workload | Telemetry Gap / Evasion | T1176; T1505.004 | Telemetry Gap / Evasion; CWE: CWE-507; CWE-829 |
| 38 | CAPEC-504 | Task Impersonation | High | Medium | 7.5 | Server / Workload | Telemetry Gap / Evasion | T1036.004 | Telemetry Gap / Evasion; CWE: CWE-1021 |
| 39 | CAPEC-678 | System Build Data Maliciously Altered | High | Low | 5.0 | Network / Perimeter | Supply Chain / Trusted Dependency | T1195.002 | Supply Chain / Trusted Dependency |
| 40 | CAPEC-669 | Alteration of a Software Update | High | Medium | 5.0 | Network / Perimeter | Supply Chain / Trusted Dependency | T1195.002 | Supply Chain / Trusted Dependency |
| 41 | CAPEC-186 | Malicious Software Update | High | Unknown | 5.0 | Network / Perimeter | Supply Chain / Trusted Dependency | T1195.002 | Supply Chain / Trusted Dependency; CWE: CWE-494 |
| 42 | CAPEC-159 | Redirect Access to Libraries | Very High | High | 6.25 | Server / Workload | Rare but High Impact | T1574.008 | Rare but High Impact; CWE: CWE-706 |
| 43 | CAPEC-665 | Exploitation of Thunderbolt Protection Flaws | Very High | Low | 10 | Identity / IAM | Identity / MFA Bypass | T1211; T1542.002; T1556 | Identity / MFA Bypass; CWE: CWE-1188; CWE-288; CWE-345; CWE-353; CWE-862 |
| 44 | CAPEC-478 | Modification of Windows Service Configuration | High | Low | 10 | Identity / IAM | Zero-Day / Unknown Exploit | T1543.003; T1574.011 | Zero-Day / Unknown Exploit; CWE: CWE-284 |
| 45 | CAPEC-697 | DHCP Spoofing | High | Low | 10 | Identity / IAM | Identity / MFA Bypass | T1557.003 | Identity / MFA Bypass; CWE: CWE-923 |
| 46 | CAPEC-551 | Modify Existing Service | Unknown | Unknown | 10 | Identity / IAM | Telemetry Gap / Evasion | T1543 | Telemetry Gap / Evasion; CWE: CWE-284; CWE-522 |
| 47 | CAPEC-17 | Using Malicious Files | Very High | High | 9.38 | Public Internet / Edge | Living-off-the-Land | T1574.005; T1574.010 | Living-off-the-Land; CWE: CWE-270; CWE-272; CWE-282; CWE-285; CWE-59; CWE-693; CWE-732 |
| 48 | CAPEC-482 | TCP Flood | Unknown | Unknown | 10 | Cloud Control Plane | Cloud / SaaS Tenant Blast Radius | T1498.001; T1499.001; T1499.002 | Cloud / SaaS Tenant Blast Radius; CWE: CWE-770 |
| 49 | CAPEC-21 | Exploitation of Trusted Identifiers | High | High | 10 | Identity / IAM | Identity / MFA Bypass | T1134; T1528; T1539 | Identity / MFA Bypass; CWE: CWE-290; CWE-302; CWE-346; CWE-384; CWE-539; CWE-6; CWE-602; CWE-642; CWE-664 |
| 50 | CAPEC-655 | Avoid Security Tool Identification by Adding Data | High | High | 10 | Data / Storage | Rare but High Impact | T1027.001 | Rare but High Impact |
| 51 | CAPEC-652 | Use of Known Kerberos Credentials | High | Medium | 10 | Identity / IAM | Identity / MFA Bypass | T1558 | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-294; CWE-307; CWE-308; CWE-309; CWE-522; CWE-654; CWE-836 |
| 52 | CAPEC-560 | Use of Known Domain Credentials | High | High | 10 | Identity / IAM | Identity / MFA Bypass | T1078 | Identity / MFA Bypass; CWE: CWE-1273; CWE-262; CWE-263; CWE-307; CWE-308; CWE-309; CWE-522; CWE-654 |
| 53 | CAPEC-550 | Install New Service | Unknown | Unknown | 10 | Identity / IAM | Cloud / SaaS Tenant Blast Radius | T1543 | Cloud / SaaS Tenant Blast Radius; CWE: CWE-284 |
| 54 | CAPEC-268 | Audit Log Manipulation | Unknown | Unknown | 10 | ESXi / Hypervisor | Cloud / SaaS Tenant Blast Radius | T1070 | Cloud / SaaS Tenant Blast Radius; CWE: CWE-117 |
| 55 | CAPEC-620 | Drop Encryption Level | High | Unknown | 9.38 | Identity / IAM | Telemetry Gap / Evasion | T1600 | Telemetry Gap / Evasion; CWE: CWE-757 |
| 56 | CAPEC-509 | Kerberoasting | High | Unknown | 9.38 | Identity / IAM | Identity / MFA Bypass | T1558.003 | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-294; CWE-308; CWE-309; CWE-521; CWE-522 |
| 57 | CAPEC-523 | Malicious Software Implanted | High | Low | 5.0 | Network / Perimeter | Supply Chain / Trusted Dependency | T1195.002 | Supply Chain / Trusted Dependency |
| 58 | CAPEC-564 | Run Software at Logon | Unknown | Unknown | 10 | Identity / IAM | Exploit Chain / Multi-Step | T1037; T1543.001; T1543.004; T1547 | Exploit Chain / Multi-Step; CWE: CWE-284 |
| 59 | CAPEC-662 | Adversary in the Browser (AiTB) | Very High | High | 10 | Public Internet / Edge | Identity / MFA Bypass | T1185 | Identity / MFA Bypass; CWE: CWE-300; CWE-494 |
| 60 | CAPEC-489 | SSL Flood | Unknown | Unknown | 10 | Public Internet / Edge | Cloud / SaaS Tenant Blast Radius | T1499.002 | Cloud / SaaS Tenant Blast Radius; CWE: CWE-770 |
| 61 | CAPEC-148 | Content Spoofing | Medium | Medium | 10 | Cloud Control Plane | Cloud / SaaS Tenant Blast Radius | T1491 | Cloud / SaaS Tenant Blast Radius; CWE: CWE-345 |
| 62 | CAPEC-130 | Excessive Allocation | Medium | Medium | 10 | Cloud Control Plane | Cloud / SaaS Tenant Blast Radius | T1499.003 | Cloud / SaaS Tenant Blast Radius; CWE: CWE-1325; CWE-404; CWE-770 |
| 63 | CAPEC-529 | Malware-Directed Internal Reconnaissance | Medium | Medium | 4.17 | Network / Perimeter | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 64 | CAPEC-150 | Collect Data from Common Resource Locations | Medium | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1003; T1119; T1213; T1530; T1555; T1602 | Identity / MFA Bypass; CWE: CWE-1239; CWE-1258; CWE-1266; CWE-1272; CWE-1323; CWE-1330; CWE-552 |
| 65 | CAPEC-593 | Session Hijacking | Very High | High | 10 | Identity / IAM | Identity / MFA Bypass | T1185; T1550.001; T1563 | Identity / MFA Bypass; CWE: CWE-287 |
| 66 | CAPEC-19 | Embedding Scripts within Scripts | High | High | 10 | Identity / IAM | Rare but High Impact | T1027.009; T1546.004; T1546.016 | Rare but High Impact; CWE: CWE-284 |
| 67 | CAPEC-270 | Modification of Registry Run Keys | Medium | Medium | 10 | Identity / IAM | Insider / Trusted Access | T1547.001; T1547.014 | Insider / Trusted Access; CWE: CWE-15 |
| 68 | CAPEC-609 | Cellular Traffic Intercept | Low | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1111 | Identity / MFA Bypass; CWE: CWE-311 |
| 69 | CAPEC-561 | Windows Admin Shares with Stolen Credentials | Unknown | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1021.002 | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-294; CWE-308; CWE-309; CWE-521; CWE-522 |
| 70 | CAPEC-9 | Buffer Overflow in Local Command-Line Utilities | High | High | 7.5 | Server / Workload | Exploit Chain / Multi-Step |  | Exploit Chain / Multi-Step; CWE: CWE-118; CWE-119; CWE-120; CWE-20; CWE-680; CWE-697; CWE-733; CWE-74 |

## Layer 2 Correlation Hints

- Treat same user, source IP, destination IP, host, session ID, request ID, transaction ID, object ID, or time window as correlation keys.
- Treat overlapping ATT&CK technique, CAPEC pattern, CWE, edge case, or affected banking surface as pattern correlation keys.
- A single-agent hit is still forwarded. Layer 2 decides whether it is 1-of-3, 2-of-3, or 3-of-3 consensus.
- Unknown or zero-day-like behavior should be emitted with `unknown_or_novel_abnormality` and the best available evidence.

## Agent Prompt Reference

Use the matching system prompt in `layer1_agent_system_prompts.md` for Agent A.
