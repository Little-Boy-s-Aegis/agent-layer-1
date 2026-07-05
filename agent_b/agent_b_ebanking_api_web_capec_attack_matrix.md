# Agent B CAPEC + MITRE ATT&CK Watch Matrix

Generated: 2026-07-04T20:59:48

Agent: Contextual AI eBanking API & Web UEBA Agent

eBanking API, web, WAF, session, token, business workflow, transaction, customer object access, and UEBA monitoring.

This file is a Layer 1 watchlist source. It is not an exploit guide and does not authorize containment. Layer 1 uses it to map observations to ATT&CK/CAPEC/CWE labels, predict likely next steps, and emit structured JSON to the deterministic Layer 2 orchestrator.

## Scope

- Input: sanitized, normalized telemetry from Layer 0 preprocessing.
- Output: read-only JSON finding for Layer 2 correlation.
- Layer 1 does not compute risk score, priority tier, routing, or auto-containment.
- Layer 2 performs BFT consensus, deterministic scoring, OPA policy checks, and playbook execution.

## Primary Surfaces

Public Internet / Edge, SaaS / Office / Email, Cloud Control Plane, Identity / IAM, Data / Storage

## Primary Evidence Fields

- request ID, session ID, device ID, and source IP
- endpoint, method, status code, and API client ID
- masked customer/account/object/transaction identifiers
- business workflow step and before/after state
- WAF payload snippet or application error snippet

## Included Matrix Size

- Relevant ATT&CK candidates found: 721
- ATT&CK rows included here: 90
- Relevant CAPEC candidates found: 323
- CAPEC rows included here: 70
- CAPEC IDs directly linked from included ATT&CK rows: 39

## Included ATT&CK ID Set

- T1539, T1606, T1550.004, T1078, T1185, T1133, T1657, T1190, T1056.003, T1528, T1505.003, T1119, T1567, T1189
- T1499.004, T1048, T1606.001, T1606.002, T1566, T1550.001, T1534, T1078.004, T1078.001, T1213.004, T1566.002, T1213.005, T1556.007, T1550
- T1621, T1056, T1552, T1684, T1213.003, T1556.006, T1213.001, T1078.003, T1538, T1078.002, T1552.005, T1552.008, T1212, T1213.002
- T1213.006, T1213, T1566.001, T1556, T1059.009, T1555.003, T1552.001, T1114.002, T1199, T1530, T1496.004, T1684.001, T1556.009, T1056.004
- T1557, T1537, T1499.002, T1566.004, T1566.003, T1567.002, T1040, T1114.003, T1659, T1667, T1648, T1105, T1071.001, T1555
- T1072, T1114, T1552.007, T1499.003, T1671, T1598.003, T1204, T1635, T1056.002, T1548, T1526, T1649, T1137, T1496.003
- T1535, T1098.005, T1070.008, T1557.003, T1491.002, T1602.002

## Included CAPEC ID Set

- CAPEC-31, CAPEC-488, CAPEC-593, CAPEC-469, CAPEC-63, CAPEC-60, CAPEC-662, CAPEC-21, CAPEC-196, CAPEC-560, CAPEC-600, CAPEC-2, CAPEC-141, CAPEC-652
- CAPEC-565, CAPEC-98, CAPEC-32, CAPEC-509, CAPEC-555, CAPEC-665, CAPEC-528, CAPEC-489, CAPEC-650, CAPEC-65, CAPEC-383, CAPEC-578, CAPEC-59, CAPEC-588
- CAPEC-244, CAPEC-163, CAPEC-150, CAPEC-125, CAPEC-568, CAPEC-57, CAPEC-480, CAPEC-464, CAPEC-86, CAPEC-37, CAPEC-18, CAPEC-110, CAPEC-66, CAPEC-17
- CAPEC-482, CAPEC-657, CAPEC-633, CAPEC-561, CAPEC-180, CAPEC-654, CAPEC-94, CAPEC-122, CAPEC-592, CAPEC-591, CAPEC-575, CAPEC-439, CAPEC-438, CAPEC-70
- CAPEC-137, CAPEC-35, CAPEC-158, CAPEC-681, CAPEC-479, CAPEC-676, CAPEC-245, CAPEC-160, CAPEC-107, CAPEC-19, CAPEC-545, CAPEC-25, CAPEC-655, CAPEC-187

## MITRE ATT&CK Matrix Vectors

| rank | attack_id | attack_vector | tactics | global_score_ref | grade_ref | surface | edge_case | related_capec | watch_focus |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | T1539 | Steal Web Session Cookie | Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-21; CAPEC-31 | Identity / MFA Bypass; Watch: Process; File; Logon Session; User Account; Application Log |
| 2 | T1606 | Forge Web Credentials | Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-196 | Identity / MFA Bypass; Watch: Process; Network Traffic; Web Credential; File; Logon Session |
| 3 | T1550.004 | Web Session Cookie | Lateral Movement | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-60 | Identity / MFA Bypass; Watch: Web Credential; Logon Session; User Account |
| 4 | T1078 | Valid Accounts | Stealth; Persistence; Privilege Escalation; Initial Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-560 | Identity / MFA Bypass; Watch: Process; Logon Session; User Account |
| 5 | T1185 | Browser Session Hijacking | Collection | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-593; CAPEC-662 | Identity / MFA Bypass; Watch: Process; User Account; Network Traffic; Module; Logon Session |
| 6 | T1133 | External Remote Services | Persistence; Initial Access | 10 | Critical | Public Internet / Edge | Identity / MFA Bypass | CAPEC-555 | Identity / MFA Bypass; Watch: Network Traffic; Logon Session; User Account; Application Log |
| 7 | T1657 | Financial Theft | Impact | 10 | Critical | Identity / IAM | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Process; File; Logon Session; Application Log |
| 8 | T1190 | Exploit Public-Facing Application | Initial Access | 9.0 | Critical | Public Internet / Edge | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; Module; Application Log |
| 9 | T1056.003 | Web Portal Capture | Collection; Credential Access | 10 | Critical | Data / Storage | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Network Traffic; File |
| 10 | T1528 | Steal Application Access Token | Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-21 | Identity / MFA Bypass; Watch: Cloud Service; Cloud Storage; File; User Account; Application Log |
| 11 | T1505.003 | Web Shell | Persistence | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-650 | Identity / MFA Bypass; Watch: Network Traffic; Process; File; Logon Session |
| 12 | T1119 | Automated Collection | Collection | 10 | Critical | Identity / IAM | Cloud / SaaS Tenant Blast Radius | CAPEC-150 | Cloud / SaaS Tenant Blast Radius; Watch: Process; Script; File; User Account |
| 13 | T1567 | Exfiltration Over Web Service | Exfiltration | 10 | Critical | ESXi / Hypervisor | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Network Traffic; Process; File; Application Log |
| 14 | T1189 | Drive-by Compromise | Initial Access | 9.0 | Critical | Public Internet / Edge | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; User Account; File; Logon Session; Application Log |
| 15 | T1499.004 | Application or System Exploitation | Impact | 10 | Critical | Cloud Control Plane | Destructive / Ransomware | CAPEC-25 | Destructive / Ransomware; Watch: Network Traffic; Instance; Process; Service; Application Log |
| 16 | T1048 | Exfiltration Over Alternative Protocol | Exfiltration | 10 | Critical | Cloud Control Plane | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Network Traffic; Process; File; Cloud Storage |
| 17 | T1606.001 | Web Cookies | Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-464 | Identity / MFA Bypass; Watch: Web Credential; Network Traffic; File; Logon Session |
| 18 | T1606.002 | SAML Tokens | Credential Access | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Web Credential; Logon Session; User Account |
| 19 | T1566 | Phishing | Initial Access | 7.5 | Critical | Public Internet / Edge | Identity / MFA Bypass | CAPEC-98 | Identity / MFA Bypass; Watch: Process; File; Logon Session; Application Log |
| 20 | T1550.001 | Application Access Token | Lateral Movement | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-593 | Identity / MFA Bypass; Watch: Web Credential; User Account |
| 21 | T1534 | Internal Spearphishing | Lateral Movement | 10 | Critical | Identity / IAM | Cloud / SaaS Tenant Blast Radius | CAPEC-163 | Cloud / SaaS Tenant Blast Radius; Watch: Command; Network Traffic; Process; Logon Session; User Account; Application Log |
| 22 | T1078.004 | Cloud Accounts | Stealth; Persistence; Privilege Escalation; Initial Access | 9.38 | Critical | Public Internet / Edge | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Logon Session; User Account |
| 23 | T1078.001 | Default Accounts | Stealth; Persistence; Privilege Escalation; Initial Access | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-70 | Identity / MFA Bypass; Watch: Logon Session; User Account |
| 24 | T1213.004 | Customer Relationship Management Software | Collection | 10 | Critical | SaaS / Office / Email | Cloud / SaaS Tenant Blast Radius |  | Cloud / SaaS Tenant Blast Radius; Watch: Logon Session; Application Log |
| 25 | T1566.002 | Spearphishing Link | Initial Access | 7.5 | Critical | Public Internet / Edge | Zero-Day / Unknown Exploit | CAPEC-163 | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; Application Log |
| 26 | T1213.005 | Messaging Applications | Collection | 10 | Critical | Identity / IAM | Cloud / SaaS Tenant Blast Radius |  | Cloud / SaaS Tenant Blast Radius; Watch: Logon Session; Application Log |
| 27 | T1556.007 | Hybrid Identity | Defense Impairment; Persistence; Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: User Account; Active Directory; Module; Logon Session; Application Log; Cloud Service |
| 28 | T1550 | Use Alternate Authentication Material | Lateral Movement | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; Web Credential; User Account; Logon Session; Application Log |
| 29 | T1621 | Multi-Factor Authentication Request Generation | Credential Access | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Logon Session; User Account; Application Log |
| 30 | T1056 | Input Capture | Collection; Credential Access | 10 | Critical | Data / Storage | Exploit Chain / Multi-Step | CAPEC-569; CAPEC-654 | Exploit Chain / Multi-Step; Watch: Process; Network Traffic; File |
| 31 | T1552 | Unsecured Credentials | Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Command; Network Traffic; Process; Windows Registry; File; Cloud Service; User Account; Application Log |
| 32 | T1684 | Social Engineering | Stealth | 10 | Critical | Identity / IAM | Cloud / SaaS Tenant Blast Radius |  | Cloud / SaaS Tenant Blast Radius; Watch: Command; Process; Network Traffic; File; Logon Session; User Account; Application Log |
| 33 | T1213.003 | Code Repositories | Collection | 10 | Critical | Cloud Control Plane | Cloud / SaaS Tenant Blast Radius |  | Cloud / SaaS Tenant Blast Radius; Watch: Logon Session; Cloud Service; Application Log |
| 34 | T1556.006 | Multi-Factor Authentication | Defense Impairment; Persistence; Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-578 | Identity / MFA Bypass; Watch: User Account; Active Directory; File; Script; Application Log; Cloud Service |
| 35 | T1213.001 | Confluence | Collection | 10 | Critical | Identity / IAM | Cloud / SaaS Tenant Blast Radius |  | Cloud / SaaS Tenant Blast Radius; Watch: Network Traffic; Logon Session; Application Log |
| 36 | T1078.003 | Local Accounts | Stealth; Persistence; Privilege Escalation; Initial Access | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Logon Session; User Account |
| 37 | T1538 | Cloud Service Dashboard | Discovery | 7.5 | Critical | Cloud Control Plane | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Cloud Storage; Logon Session; User Account; Application Log |
| 38 | T1078.002 | Domain Accounts | Stealth; Persistence; Privilege Escalation; Initial Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Logon Session; Process; Network Traffic; User Account |
| 39 | T1552.005 | Cloud Instance Metadata API | Credential Access | 9.38 | Critical | Cloud Control Plane | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Network Traffic; Cloud Service |
| 40 | T1552.008 | Chat Messages | Credential Access | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: User Account; Application Log |
| 41 | T1212 | Exploitation for Credential Access | Credential Access | 9.38 | Critical | Identity / IAM | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; User Account; Application Log |
| 42 | T1213.002 | Sharepoint | Collection | 10 | Critical | Identity / IAM | Cloud / SaaS Tenant Blast Radius |  | Cloud / SaaS Tenant Blast Radius; Watch: Logon Session; Cloud Service; Application Log |
| 43 | T1213.006 | Databases | Collection | 10 | Critical | Cloud Control Plane | Cloud / SaaS Tenant Blast Radius |  | Cloud / SaaS Tenant Blast Radius; Watch: Network Traffic; Process; File; Cloud Storage; Cloud Service; Application Log |
| 44 | T1213 | Data from Information Repositories | Collection | 10 | Critical | Cloud Control Plane | Cloud / SaaS Tenant Blast Radius | CAPEC-150 | Cloud / SaaS Tenant Blast Radius; Watch: Command; Process; Network Traffic; Cloud Service; Cloud Storage; File; Application Log; Network Share |
| 45 | T1566.001 | Spearphishing Attachment | Initial Access | 6.0 | Medium High | Public Internet / Edge | Zero-Day / Unknown Exploit | CAPEC-163 | Zero-Day / Unknown Exploit; Watch: Process; Network Traffic; File; Application Log |
| 46 | T1556 | Modify Authentication Process | Defense Impairment; Persistence; Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-665 | Identity / MFA Bypass; Watch: Process; User Account; Windows Registry; File; Module; Cloud Service |
| 47 | T1059.009 | Cloud API | Execution | 6.25 | Medium High | Cloud Control Plane | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Command; User Account; Cloud Service |
| 48 | T1555.003 | Credentials from Web Browsers | Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; File |
| 49 | T1552.001 | Credentials In Files | Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-191; CAPEC-639 | Identity / MFA Bypass; Watch: Command; Process; Network Traffic; File; Logon Session |
| 50 | T1114.002 | Remote Email Collection | Collection | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-555 | Identity / MFA Bypass; Watch: Command; Logon Session; Network Traffic; Application Log |
| 51 | T1199 | Trusted Relationship | Initial Access | 6.25 | Medium High | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Network Traffic; Logon Session; Application Log |
| 52 | T1530 | Data from Cloud Storage | Collection | 10 | Critical | Cloud Control Plane | Identity / MFA Bypass | CAPEC-150 | Identity / MFA Bypass; Watch: Network Traffic; User Account; Cloud Storage |
| 53 | T1496.004 | Cloud Service Hijacking | Impact | 10 | Critical | Cloud Control Plane | Cloud / SaaS Tenant Blast Radius |  | Cloud / SaaS Tenant Blast Radius; Watch: User Account; Application Log; Cloud Service |
| 54 | T1684.001 | Impersonation | Stealth | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Command; Logon Session; Application Log |
| 55 | T1556.009 | Conditional Access Policies | Defense Impairment; Persistence; Credential Access | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Active Directory; Application Log; Cloud Service |
| 56 | T1056.004 | Credential API Hooking | Collection; Credential Access | 10 | Critical | Data / Storage | Identity / MFA Bypass | CAPEC-383 | Identity / MFA Bypass; Watch: Process; Module; File |
| 57 | T1557 | Adversary-in-the-Middle | Credential Access; Collection | 10 | Critical | Public Internet / Edge | Identity / MFA Bypass | CAPEC-94 | Identity / MFA Bypass; Watch: Network Traffic; File; Windows Registry; Application Log |
| 58 | T1537 | Transfer Data to Cloud Account | Exfiltration | 10 | Critical | Cloud Control Plane | Cloud / SaaS Tenant Blast Radius |  | Cloud / SaaS Tenant Blast Radius; Watch: Network Traffic; Cloud Storage; Snapshot; Application Log |
| 59 | T1499.002 | Service Exhaustion Flood | Impact | 10 | Critical | Public Internet / Edge | Destructive / Ransomware | CAPEC-469; CAPEC-482; CAPEC-488; CAPEC-489; CAPEC-528 | Destructive / Ransomware; Watch: Process; Network Traffic; Firewall; Sensor Health; Application Log |
| 60 | T1566.004 | Spearphishing Voice | Initial Access | 3.75 | Medium Low | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Application Log |
| 61 | T1566.003 | Spearphishing via Service | Initial Access | 5.0 | Medium High | Public Internet / Edge | Zero-Day / Unknown Exploit | CAPEC-163 | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; File; Application Log |
| 62 | T1567.002 | Exfiltration to Cloud Storage | Exfiltration | 10 | Critical | ESXi / Hypervisor | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Network Traffic; Process; File |
| 63 | T1040 | Network Sniffing | Credential Access; Discovery | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-158; CAPEC-57; CAPEC-65 | Identity / MFA Bypass; Watch: Command; Network Traffic; Process; Service; User Account; Cloud Service |
| 64 | T1114.003 | Email Forwarding Rule | Collection | 10 | Critical | Public Internet / Edge | Cloud / SaaS Tenant Blast Radius |  | Cloud / SaaS Tenant Blast Radius; Watch: Command; Process; File; Cloud Service; Application Log |
| 65 | T1659 | Content Injection | Initial Access; Command and Control | 10 | Critical | Public Internet / Edge | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Process; File; Network Traffic |
| 66 | T1667 | Email Bombing | Impact | 10 | Critical | Identity / IAM | Destructive / Ransomware |  | Destructive / Ransomware; Watch: File; Application Log |
| 67 | T1648 | Serverless Execution | Execution | 6.25 | Medium High | Cloud Control Plane | Cloud / SaaS Tenant Blast Radius |  | Cloud / SaaS Tenant Blast Radius; Watch: Application Log; Cloud Service |
| 68 | T1105 | Ingress Tool Transfer | Command and Control | 10 | Critical | ESXi / Hypervisor | Living-off-the-Land |  | Living-off-the-Land; Watch: Command; Process; Network Traffic; File |
| 69 | T1071.001 | Web Protocols | Command and Control | 10 | Critical | ESXi / Hypervisor | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Network Traffic; Process |
| 70 | T1555 | Credentials from Password Stores | Credential Access | 10 | Critical | Cloud Control Plane | Cloud / SaaS Tenant Blast Radius | CAPEC-150 | Cloud / SaaS Tenant Blast Radius; Watch: Process; Cloud Service; File |
| 71 | T1072 | Software Deployment Tools | Execution; Lateral Movement | 10 | Critical | Identity / IAM | Zero-Day / Unknown Exploit | CAPEC-187; CAPEC-657 | Zero-Day / Unknown Exploit; Watch: Command; Process; Application Log; Network Traffic |
| 72 | T1114 | Email Collection | Collection | 10 | Critical | SaaS / Office / Email | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Command; Process; Network Traffic; File; Logon Session; Application Log; Network Share |
| 73 | T1552.007 | Container API | Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Command; Process; User Account; Application Log |
| 74 | T1499.003 | Application Exhaustion Flood | Impact | 10 | Critical | Cloud Control Plane | Cloud / SaaS Tenant Blast Radius | CAPEC-130 | Cloud / SaaS Tenant Blast Radius; Watch: Network Traffic; Process; Sensor Health; Cloud Service; Application Log |
| 75 | T1671 | Cloud Application Integration | Persistence | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Active Directory; Application Log; Cloud Service |
| 76 | T1598.003 | Spearphishing Link | Reconnaissance | 2.08 | Low | Public Internet / Edge | Telemetry Gap / Evasion | CAPEC-163 | Telemetry Gap / Evasion; Watch: Network Traffic; Application Log |
| 77 | T1204 | User Execution | Execution | 7.5 | Critical | Cloud Control Plane | Cloud / SaaS Tenant Blast Radius |  | Cloud / SaaS Tenant Blast Radius; Watch: Network Traffic; Process; Container; File; Instance; Application Log |
| 78 | T1635 | Steal Application Access Token | Credential Access | 0 | Low | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass |
| 79 | T1056.002 | GUI Input Capture | Collection; Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Command; Process; Script |
| 80 | T1548 | Abuse Elevation Control Mechanism | Privilege Escalation | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-114; CAPEC-115; CAPEC-122; CAPEC-233 | Identity / MFA Bypass; Watch: User Account; Process; Windows Registry; File; Logon Session |
| 81 | T1526 | Cloud Service Discovery | Discovery | 6.25 | Medium High | Cloud Control Plane | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: User Account; Logon Session; Cloud Service |
| 82 | T1649 | Steal or Forge Authentication Certificates | Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Command; Active Directory; File; Windows Registry; Application Log |
| 83 | T1137 | Office Application Startup | Persistence | 10 | Critical | Identity / IAM | Cloud / SaaS Tenant Blast Radius |  | Cloud / SaaS Tenant Blast Radius; Watch: User Account; Process; Windows Registry; File; Application Log |
| 84 | T1496.003 | SMS Pumping | Impact | 10 | Critical | Identity / IAM | Cloud / SaaS Tenant Blast Radius |  | Cloud / SaaS Tenant Blast Radius; Watch: User Account; Application Log |
| 85 | T1535 | Unused/Unsupported Cloud Regions | Stealth | 10 | Critical | Cloud Control Plane | Cloud / SaaS Tenant Blast Radius |  | Cloud / SaaS Tenant Blast Radius; Watch: Cloud Storage; Instance; Network Traffic; User Account |
| 86 | T1098.005 | Device Registration | Persistence; Privilege Escalation | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: User Account; Active Directory; Application Log |
| 87 | T1070.008 | Clear Mailbox Data | Stealth | 7.5 | Critical | SaaS / Office / Email | Living-off-the-Land |  | Living-off-the-Land; Watch: Command; Process; File; Application Log |
| 88 | T1557.003 | DHCP Spoofing | Credential Access; Collection | 8.33 | Critical | Network / Perimeter | Destructive / Ransomware | CAPEC-697 | Destructive / Ransomware; Watch: Network Traffic; Application Log |
| 89 | T1491.002 | External Defacement | Impact | 10 | Critical | Cloud Control Plane | Cloud / SaaS Tenant Blast Radius |  | Cloud / SaaS Tenant Blast Radius; Watch: Network Traffic; Process; File; Cloud Storage; Logon Session |
| 90 | T1602.002 | Network Device Configuration Dump | Collection | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Command; Network Traffic; User Account |

## CAPEC Attack Pattern Matrix

| rank | capec_id | attack_pattern | severity_ref | likelihood_ref | global_score_ref | surface | edge_case | related_attack | watch_focus |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | CAPEC-31 | Accessing/Intercepting/Modifying HTTP Cookies | High | High | 10 | Identity / IAM | Identity / MFA Bypass | T1539 | Identity / MFA Bypass; CWE: CWE-113; CWE-20; CWE-302; CWE-311; CWE-315; CWE-384; CWE-472; CWE-539; CWE-565; CWE-602; CWE-642 |
| 2 | CAPEC-488 | HTTP Flood | Unknown | Unknown | 10 | Public Internet / Edge | Cloud / SaaS Tenant Blast Radius | T1499.002 | Cloud / SaaS Tenant Blast Radius; CWE: CWE-770 |
| 3 | CAPEC-593 | Session Hijacking | Very High | High | 10 | Identity / IAM | Identity / MFA Bypass | T1185; T1550.001; T1563 | Identity / MFA Bypass; CWE: CWE-287 |
| 4 | CAPEC-469 | HTTP DoS | Low | Unknown | 10 | Public Internet / Edge | Cloud / SaaS Tenant Blast Radius | T1499.002 | Cloud / SaaS Tenant Blast Radius; CWE: CWE-770; CWE-772 |
| 5 | CAPEC-63 | Cross-Site Scripting (XSS) | Very High | High | 10 | Public Internet / Edge | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-20; CWE-79 |
| 6 | CAPEC-60 | Reusing Session IDs (aka Session Replay) | High | High | 9.38 | Identity / IAM | Identity / MFA Bypass | T1134.001; T1550.004 | Identity / MFA Bypass; CWE: CWE-200; CWE-285; CWE-290; CWE-294; CWE-346; CWE-384; CWE-488; CWE-539; CWE-664; CWE-732 |
| 7 | CAPEC-662 | Adversary in the Browser (AiTB) | Very High | High | 10 | Public Internet / Edge | Identity / MFA Bypass | T1185 | Identity / MFA Bypass; CWE: CWE-300; CWE-494 |
| 8 | CAPEC-21 | Exploitation of Trusted Identifiers | High | High | 10 | Identity / IAM | Identity / MFA Bypass | T1134; T1528; T1539 | Identity / MFA Bypass; CWE: CWE-290; CWE-302; CWE-346; CWE-384; CWE-539; CWE-6; CWE-602; CWE-642; CWE-664 |
| 9 | CAPEC-196 | Session Credential Falsification through Forging | Medium | Medium | 10 | Identity / IAM | Identity / MFA Bypass | T1134.002; T1134.003; T1606 | Identity / MFA Bypass; CWE: CWE-384; CWE-664 |
| 10 | CAPEC-560 | Use of Known Domain Credentials | High | High | 10 | Identity / IAM | Identity / MFA Bypass | T1078 | Identity / MFA Bypass; CWE: CWE-1273; CWE-262; CWE-263; CWE-307; CWE-308; CWE-309; CWE-522; CWE-654 |
| 11 | CAPEC-600 | Credential Stuffing | High | High | 5.62 | Identity / IAM | Identity / MFA Bypass | T1110.004 | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-307; CWE-308; CWE-309; CWE-522; CWE-654 |
| 12 | CAPEC-2 | Inducing Account Lockout | Medium | High | 10 | Identity / IAM | Identity / MFA Bypass | T1531 | Identity / MFA Bypass; CWE: CWE-645 |
| 13 | CAPEC-141 | Cache Poisoning | High | High | 5.0 | Public Internet / Edge | Identity / MFA Bypass | T1557.002 | Identity / MFA Bypass; CWE: CWE-345; CWE-346; CWE-348; CWE-349 |
| 14 | CAPEC-652 | Use of Known Kerberos Credentials | High | Medium | 10 | Identity / IAM | Identity / MFA Bypass | T1558 | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-294; CWE-307; CWE-308; CWE-309; CWE-522; CWE-654; CWE-836 |
| 15 | CAPEC-565 | Password Spraying | High | High | 5.62 | Identity / IAM | Identity / MFA Bypass | T1110.003 | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-307; CWE-308; CWE-309; CWE-521; CWE-654 |
| 16 | CAPEC-98 | Phishing | Very High | High | 7.5 | Identity / IAM | Identity / MFA Bypass | T1566; T1598 | Identity / MFA Bypass; CWE: CWE-451 |
| 17 | CAPEC-32 | XSS Through HTTP Query Strings | High | High | 7.5 | Public Internet / Edge | Rare but High Impact |  | Rare but High Impact; CWE: CWE-80 |
| 18 | CAPEC-509 | Kerberoasting | High | Unknown | 9.38 | Identity / IAM | Identity / MFA Bypass | T1558.003 | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-294; CWE-308; CWE-309; CWE-521; CWE-522 |
| 19 | CAPEC-555 | Remote Services with Stolen Credentials | Very High | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1021; T1114.002; T1133 | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-294; CWE-308; CWE-309; CWE-521; CWE-522 |
| 20 | CAPEC-665 | Exploitation of Thunderbolt Protection Flaws | Very High | Low | 10 | Identity / IAM | Identity / MFA Bypass | T1211; T1542.002; T1556 | Identity / MFA Bypass; CWE: CWE-1188; CWE-288; CWE-345; CWE-353; CWE-862 |
| 21 | CAPEC-528 | XML Flood | Medium | Low | 10 | Public Internet / Edge | Cloud / SaaS Tenant Blast Radius | T1498.001; T1499.002 | Cloud / SaaS Tenant Blast Radius; CWE: CWE-770 |
| 22 | CAPEC-489 | SSL Flood | Unknown | Unknown | 10 | Public Internet / Edge | Cloud / SaaS Tenant Blast Radius | T1499.002 | Cloud / SaaS Tenant Blast Radius; CWE: CWE-770 |
| 23 | CAPEC-650 | Upload a Web Shell to a Web Server | High | Unknown | 10 | Identity / IAM | Zero-Day / Unknown Exploit | T1505.003 | Zero-Day / Unknown Exploit; CWE: CWE-287; CWE-553 |
| 24 | CAPEC-65 | Sniff Application Code | High | Low | 10 | Identity / IAM | Identity / MFA Bypass | T1040 | Identity / MFA Bypass; CWE: CWE-311; CWE-318; CWE-319; CWE-693 |
| 25 | CAPEC-383 | Harvesting Information via API Event Monitoring | Low | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1056.004 | Identity / MFA Bypass; CWE: CWE-311; CWE-319; CWE-419; CWE-602 |
| 26 | CAPEC-578 | Disable Security Software | Medium | Medium | 10 | Identity / IAM | Identity / MFA Bypass | T1556.006 | Identity / MFA Bypass; CWE: CWE-284 |
| 27 | CAPEC-59 | Session Credential Falsification through Prediction | High | High | 10 | Identity / IAM | Rare but High Impact |  | Rare but High Impact; CWE: CWE-200; CWE-285; CWE-290; CWE-330; CWE-331; CWE-346; CWE-384; CWE-488; CWE-539; CWE-6; CWE-693 |
| 28 | CAPEC-588 | DOM-Based XSS | Very High | High | 10 | Public Internet / Edge | Rare but High Impact |  | Rare but High Impact; CWE: CWE-20; CWE-79; CWE-83 |
| 29 | CAPEC-244 | XSS Targeting URI Placeholders | High | High | 7.5 | Public Internet / Edge | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-83 |
| 30 | CAPEC-163 | Spear Phishing | High | High | 10 | Identity / IAM | Cloud / SaaS Tenant Blast Radius | T1534; T1566.001; T1566.002; T1566.003; T1598.001; T1598.002; T1598.003 | Cloud / SaaS Tenant Blast Radius; CWE: CWE-451 |
| 31 | CAPEC-150 | Collect Data from Common Resource Locations | Medium | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1003; T1119; T1213; T1530; T1555; T1602 | Identity / MFA Bypass; CWE: CWE-1239; CWE-1258; CWE-1266; CWE-1272; CWE-1323; CWE-1330; CWE-552 |
| 32 | CAPEC-125 | Flooding | Medium | High | 10 | Cloud Control Plane | Cloud / SaaS Tenant Blast Radius | T1498.001; T1499 | Cloud / SaaS Tenant Blast Radius; CWE: CWE-404; CWE-770 |
| 33 | CAPEC-568 | Capture Credentials via Keylogger | High | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1056.001 | Identity / MFA Bypass |
| 34 | CAPEC-57 | Utilizing REST's Trust in the System Resource to Obtain Sensitive Data | Very High | Medium | 10 | Identity / IAM | Identity / MFA Bypass | T1040 | Identity / MFA Bypass; CWE: CWE-287; CWE-300; CWE-693 |
| 35 | CAPEC-480 | Escaping Virtualization | Very High | Low | 10 | Cloud Control Plane | Rare but High Impact | T1611 | Rare but High Impact; CWE: CWE-693 |
| 36 | CAPEC-464 | Evercookie | Medium | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1606.001 | Identity / MFA Bypass; CWE: CWE-359 |
| 37 | CAPEC-86 | XSS Through HTTP Headers | Very High | High | 10 | Public Internet / Edge | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-80 |
| 38 | CAPEC-37 | Retrieve Embedded Sensitive Data | Very High | High | 10 | Identity / IAM | Identity / MFA Bypass | T1005; T1552.004 | Identity / MFA Bypass; CWE: CWE-1239; CWE-1258; CWE-1266; CWE-1272; CWE-1278; CWE-1301; CWE-1330; CWE-226; CWE-311; CWE-312; CWE-314; CWE-315; CWE-318; CWE-525 |
| 39 | CAPEC-18 | XSS Targeting Non-Script Elements | Very High | High | 10 | Public Internet / Edge | Rare but High Impact |  | Rare but High Impact; CWE: CWE-80 |
| 40 | CAPEC-110 | SQL Injection through SOAP Parameter Tampering | Very High | High | 10 | Public Internet / Edge | Rare but High Impact |  | Rare but High Impact; CWE: CWE-20; CWE-89 |
| 41 | CAPEC-66 | SQL Injection | High | High | 7.5 | Public Internet / Edge | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-1286; CWE-89 |
| 42 | CAPEC-17 | Using Malicious Files | Very High | High | 9.38 | Public Internet / Edge | Living-off-the-Land | T1574.005; T1574.010 | Living-off-the-Land; CWE: CWE-270; CWE-272; CWE-282; CWE-285; CWE-59; CWE-693; CWE-732 |
| 43 | CAPEC-482 | TCP Flood | Unknown | Unknown | 10 | Cloud Control Plane | Cloud / SaaS Tenant Blast Radius | T1498.001; T1499.001; T1499.002 | Cloud / SaaS Tenant Blast Radius; CWE: CWE-770 |
| 44 | CAPEC-657 | Malicious Automated Software Update via Spoofing | High | High | 10 | Public Internet / Edge | Supply Chain / Trusted Dependency | T1072 | Supply Chain / Trusted Dependency; CWE: CWE-494 |
| 45 | CAPEC-633 | Token Impersonation | Medium | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1134 | Identity / MFA Bypass; CWE: CWE-1270; CWE-287 |
| 46 | CAPEC-561 | Windows Admin Shares with Stolen Credentials | Unknown | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1021.002 | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-294; CWE-308; CWE-309; CWE-521; CWE-522 |
| 47 | CAPEC-180 | Exploiting Incorrectly Configured Access Control Security Levels | Medium | High | 9.38 | Data / Storage | Rare but High Impact | T1574.010 | Rare but High Impact; CWE: CWE-1190; CWE-1191; CWE-1193; CWE-1220; CWE-1268; CWE-1280; CWE-1297; CWE-1311; CWE-1315; CWE-1318; CWE-1320; CWE-1321; CWE-732 |
| 48 | CAPEC-654 | Credential Prompt Impersonation | High | Medium | 10 | Identity / IAM | Identity / MFA Bypass | T1056; T1548.004 | Identity / MFA Bypass; CWE: CWE-1021 |
| 49 | CAPEC-94 | Adversary in the Middle (AiTM) | Very High | High | 10 | Identity / IAM | Identity / MFA Bypass | T1557 | Identity / MFA Bypass; CWE: CWE-287; CWE-290; CWE-294; CWE-300; CWE-593 |
| 50 | CAPEC-122 | Privilege Abuse | Medium | High | 10 | Identity / IAM | Cloud / SaaS Tenant Blast Radius | T1548 | Cloud / SaaS Tenant Blast Radius; CWE: CWE-1317; CWE-269; CWE-732 |
| 51 | CAPEC-592 | Stored XSS | Very High | High | 10 | Public Internet / Edge | Rare but High Impact |  | Rare but High Impact; CWE: CWE-79 |
| 52 | CAPEC-591 | Reflected XSS | Very High | High | 10 | Public Internet / Edge | Rare but High Impact |  | Rare but High Impact; CWE: CWE-79 |
| 53 | CAPEC-575 | Account Footprinting | Low | Low | 7.5 | Cloud Control Plane | Cloud / SaaS Tenant Blast Radius | T1087 | Cloud / SaaS Tenant Blast Radius; CWE: CWE-200 |
| 54 | CAPEC-439 | Manipulation During Distribution | Unknown | Unknown | 7.5 | Identity / IAM | Telemetry Gap / Evasion | T1195 | Telemetry Gap / Evasion; CWE: CWE-1269 |
| 55 | CAPEC-438 | Modification During Manufacture | Unknown | Unknown | 7.5 | Identity / IAM | Cloud / SaaS Tenant Blast Radius | T1195 | Cloud / SaaS Tenant Blast Radius |
| 56 | CAPEC-70 | Try Common or Default Usernames and Passwords | High | Medium | 9.38 | Identity / IAM | Identity / MFA Bypass | T1078.001 | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-308; CWE-309; CWE-521; CWE-654; CWE-798 |
| 57 | CAPEC-137 | Parameter Injection | Medium | Medium | 4.17 | Public Internet / Edge | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-88 |
| 58 | CAPEC-35 | Leverage Executable Code in Non-Executable Files | Very High | High | 10 | Data / Storage | Rare but High Impact | T1027.006; T1027.009; T1564.009 | Rare but High Impact; CWE: CWE-270; CWE-272; CWE-282; CWE-59; CWE-94; CWE-95; CWE-96; CWE-97 |
| 59 | CAPEC-158 | Sniffing Network Traffic | Medium | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1040; T1111 | Identity / MFA Bypass; CWE: CWE-311 |
| 60 | CAPEC-681 | Exploitation of Improperly Controlled Hardware Security Identifiers | Very High | Medium | 10 | Data / Storage | Exploit Chain / Multi-Step |  | Exploit Chain / Multi-Step; CWE: CWE-1259; CWE-1267; CWE-1270; CWE-1294; CWE-1302 |
| 61 | CAPEC-479 | Malicious Root Certificate | Low | Low | 7.5 | Public Internet / Edge | Telemetry Gap / Evasion | T1553.004 | Telemetry Gap / Evasion; CWE: CWE-284 |
| 62 | CAPEC-676 | NoSQL Injection | High | High | 7.5 | Public Internet / Edge | Rare but High Impact |  | Rare but High Impact; CWE: CWE-1286; CWE-943 |
| 63 | CAPEC-245 | XSS Using Doubled Characters | Medium | Unknown | 3.33 | Public Internet / Edge | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-85 |
| 64 | CAPEC-160 | Exploit Script-Based APIs | Medium | Unknown | 3.33 | Public Internet / Edge | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-346 |
| 65 | CAPEC-107 | Cross Site Tracing | Very High | Medium | 8.33 | Public Internet / Edge | Identity / MFA Bypass |  | Identity / MFA Bypass; CWE: CWE-648; CWE-693 |
| 66 | CAPEC-19 | Embedding Scripts within Scripts | High | High | 10 | Identity / IAM | Rare but High Impact | T1027.009; T1546.004; T1546.016 | Rare but High Impact; CWE: CWE-284 |
| 67 | CAPEC-545 | Pull Data from System Resources | Unknown | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1005; T1555.001 | Identity / MFA Bypass; CWE: CWE-1239; CWE-1243; CWE-1258; CWE-1266; CWE-1272; CWE-1278; CWE-1323; CWE-1330 |
| 68 | CAPEC-25 | Forced Deadlock | High | Low | 10 | Cloud Control Plane | Cloud / SaaS Tenant Blast Radius | T1499.004 | Cloud / SaaS Tenant Blast Radius; CWE: CWE-1322; CWE-412; CWE-567; CWE-662; CWE-667; CWE-833 |
| 69 | CAPEC-655 | Avoid Security Tool Identification by Adding Data | High | High | 10 | Data / Storage | Rare but High Impact | T1027.001 | Rare but High Impact |
| 70 | CAPEC-187 | Malicious Automated Software Update via Redirection | High | High | 10 | Identity / IAM | Supply Chain / Trusted Dependency | T1072 | Supply Chain / Trusted Dependency; CWE: CWE-494 |

## Layer 2 Correlation Hints

- Treat same user, source IP, destination IP, host, session ID, request ID, transaction ID, object ID, or time window as correlation keys.
- Treat overlapping ATT&CK technique, CAPEC pattern, CWE, edge case, or affected banking surface as pattern correlation keys.
- A single-agent hit is still forwarded. Layer 2 decides whether it is 1-of-3, 2-of-3, or 3-of-3 consensus.
- Layer 2 computes risk deterministically from the mapped base threat score and asset criticality multiplier.
- Auto-containment requires BFT consensus, meaning at least 2 of 3 agents flag a threat, and `final_risk_score >= 8.5`; a single-agent hit can raise analyst-visible severity but cannot trigger automated containment by itself.
- Unknown or zero-day-like behavior should be emitted with `unknown_or_novel_abnormality` and the best available evidence.

## Agent Prompt Reference

Use `agent_b/agent_b_ebanking_api_web_ueba_system_prompt.md` for Agent B.
