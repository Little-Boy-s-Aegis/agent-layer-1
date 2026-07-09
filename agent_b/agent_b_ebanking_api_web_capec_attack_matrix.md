# Agent B CAPEC + MITRE ATT&CK Watch Matrix

Generated: scoped runtime rewrite from local Layer 1 package references

Agent: Agent B

This file is a Layer 1 watchlist source. It is not an exploit guide and does not authorize containment. Layer 1 uses it to map observed behavior to ATT&CK/CAPEC/CWE labels and form non-scoring attack-pattern prediction hints before emitting structured JSON to the deterministic Layer 2 orchestrator.

## Scope

- Input: sanitized, normalized telemetry from Layer 0 preprocessing.
- Output: read-only JSON finding for Layer 2 correlation.
- Layer 1 does not compute risk score, priority tier, routing, or auto-containment.
- Layer 2 independently verifies Layer 1 findings from logs/context, then performs deterministic scoring, OPA policy checks, and playbook execution.

## Primary Surfaces

API / Web / WAF, Session / Token, Payment / Transaction, Customer Data, Fraud Workflow, UEBA / Behavior

## Included Matrix Size

- ATT&CK rows included here: 68
- CAPEC rows included here: 212
- ATT&CK source boundary: `agent_b/surface_context_matrix.md`
- CAPEC source boundary: `agent_b/capec_attack_pattern_prediction_reference.md`

## MITRE ATT&CK Matrix Vectors

| rank | attack_id | attack_vector | tactics | surface | edge_case | related_capec | watch_focus |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | T1657 | Financial Theft | Impact | Payment / Transaction | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Process; File; Logon Session; Application Log |
| 2 | T1071.001 | Web Protocols | Command and Control | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Network Traffic; Process |
| 3 | T1567.002 | Exfiltration to Cloud Storage | Exfiltration | Customer Data | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Network Traffic; Process; File |
| 4 | T1114.002 | Remote Email Collection | Collection | Customer Data | Session / Token / Workflow Abuse | CAPEC-555 | Session / Token / Workflow Abuse; Watch: Command; Logon Session; Network Traffic; Application Log |
| 5 | T1185 | Browser Session Hijacking | Collection | API / Web / WAF; Session / Token | Session / Token / Workflow Abuse | CAPEC-593; CAPEC-662 | Session / Token / Workflow Abuse; Watch: Process; User Account; Network Traffic; Module; Logon Session |
| 6 | T1567 | Exfiltration Over Web Service | Exfiltration | API / Web / WAF | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Network Traffic; Process; File; Application Log |
| 7 | T1213.006 | Databases | Collection | Customer Data | API / SaaS Blast Radius |  | API / SaaS Blast Radius; Watch: Network Traffic; Process; File; Cloud Storage; Cloud Service; Application Log |
| 8 | T1213 | Data from Information Repositories | Collection | Customer Data | API / SaaS Blast Radius | CAPEC-150 | API / SaaS Blast Radius; Watch: Command; Process; Network Traffic; Cloud Service; Cloud Storage; File; Application Log; Network Share |
| 9 | T1567.001 | Exfiltration to Code Repository | Exfiltration | Customer Data | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Network Traffic; Process; File |
| 10 | T1491.002 | External Defacement | Impact | API / Web / WAF | API / SaaS Blast Radius |  | API / SaaS Blast Radius; Watch: Network Traffic; Process; File; Cloud Storage; Logon Session |
| 11 | T1567.004 | Exfiltration Over Webhook | Exfiltration | API / Web / WAF | API / SaaS Blast Radius |  | API / SaaS Blast Radius; Watch: Command; Network Traffic; Process; File; Application Log |
| 12 | T1499.003 | Application Exhaustion Flood | Impact | API / Web / WAF | API / SaaS Blast Radius | CAPEC-130 | API / SaaS Blast Radius; Watch: Network Traffic; Process; Sensor Health; Cloud Service; Application Log |
| 13 | T1499.002 | Service Exhaustion Flood | Impact | API / Web / WAF | Destructive / Ransomware | CAPEC-469; CAPEC-482; CAPEC-488; CAPEC-489; CAPEC-528 | Destructive / Ransomware; Watch: Process; Network Traffic; Firewall; Sensor Health; Application Log |
| 14 | T1491 | Defacement | Impact | API / Web / WAF | API / SaaS Blast Radius | CAPEC-148 | API / SaaS Blast Radius; Watch: Network Traffic; Process; File; Cloud Storage; Application Log |
| 15 | T1505.003 | Web Shell | Persistence | API / Web / WAF | Session / Token / Workflow Abuse | CAPEC-650 | Session / Token / Workflow Abuse; Watch: Network Traffic; Process; File; Logon Session |
| 16 | T1539 | Steal Web Session Cookie | Credential Access | API / Web / WAF; Session / Token | Session / Token / Workflow Abuse | CAPEC-21; CAPEC-31 | Session / Token / Workflow Abuse; Watch: Process; File; Logon Session; User Account; Application Log |
| 17 | T1114.001 | Local Email Collection | Collection | Customer Data | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; File; Network Traffic |
| 18 | T1071 | Application Layer Protocol | Command and Control | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Network Traffic; Process |
| 19 | T1056.004 | Credential API Hooking | Collection; Credential Access | API / Web / WAF | Session / Token / Workflow Abuse | CAPEC-383 | Session / Token / Workflow Abuse; Watch: Process; Module; File |
| 20 | T1530 | Data from Cloud Storage | Collection | Customer Data | Session / Token / Workflow Abuse | CAPEC-150 | Session / Token / Workflow Abuse; Watch: Network Traffic; User Account; Cloud Storage |
| 21 | T1213.002 | Sharepoint | Collection | Customer Data | API / SaaS Blast Radius |  | API / SaaS Blast Radius; Watch: Logon Session; Cloud Service; Application Log |
| 22 | T1213.003 | Code Repositories | Collection | Customer Data | API / SaaS Blast Radius |  | API / SaaS Blast Radius; Watch: Logon Session; Cloud Service; Application Log |
| 23 | T1213.005 | Messaging Applications | Collection | Customer Data | API / SaaS Blast Radius |  | API / SaaS Blast Radius; Watch: Logon Session; Application Log |
| 24 | T1056.003 | Web Portal Capture | Collection; Credential Access | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Network Traffic; File |
| 25 | T1213.001 | Confluence | Collection | Customer Data | API / SaaS Blast Radius |  | API / SaaS Blast Radius; Watch: Network Traffic; Logon Session; Application Log |
| 26 | T1667 | Email Bombing | Impact | Customer Data | Destructive / Ransomware |  | Destructive / Ransomware; Watch: File; Application Log |
| 27 | T1496.003 | SMS Pumping | Impact | Payment / Transaction | API / SaaS Blast Radius |  | API / SaaS Blast Radius; Watch: User Account; Application Log |
| 28 | T1213.004 | Customer Relationship Management Software | Collection | Customer Data | API / SaaS Blast Radius |  | API / SaaS Blast Radius; Watch: Logon Session; Application Log |
| 29 | T1528 | Steal Application Access Token | Credential Access | Session / Token | Session / Token / Workflow Abuse | CAPEC-21 | Session / Token / Workflow Abuse; Watch: Cloud Service; Cloud Storage; File; User Account; Application Log |
| 30 | T1564.008 | Email Hiding Rules | Stealth | Customer Data | Living-off-the-Land |  | Living-off-the-Land; Watch: Command; Process; File; Application Log |
| 31 | T1606.001 | Web Cookies | Credential Access | API / Web / WAF; Session / Token | Session / Token / Workflow Abuse | CAPEC-464 | Session / Token / Workflow Abuse; Watch: Web Credential; Network Traffic; File; Logon Session |
| 32 | T1606 | Forge Web Credentials | Credential Access | API / Web / WAF | Session / Token / Workflow Abuse | CAPEC-196 | Session / Token / Workflow Abuse; Watch: Process; Network Traffic; Web Credential; File; Logon Session |
| 33 | T1563 | Remote Service Session Hijacking | Lateral Movement | Session / Token | Session / Token / Workflow Abuse | CAPEC-593 | Session / Token / Workflow Abuse; Watch: Command; Network Traffic; Process; Logon Session |
| 34 | T1114 | Email Collection | Collection | Customer Data | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse; Watch: Command; Process; Network Traffic; File; Logon Session; Application Log; Network Share |
| 35 | T1114.003 | Email Forwarding Rule | Collection | Customer Data | API / SaaS Blast Radius |  | API / SaaS Blast Radius; Watch: Command; Process; File; Cloud Service; Application Log |
| 36 | T1659 | Content Injection | Initial Access; Command and Control | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Process; File; Network Traffic |
| 37 | T1552.005 | Cloud Instance Metadata API | Credential Access | API / Web / WAF; Customer Data | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Network Traffic; Cloud Service |
| 38 | T1550.001 | Application Access Token | Lateral Movement | Session / Token | Session / Token / Workflow Abuse | CAPEC-593 | Session / Token / Workflow Abuse; Watch: Web Credential; User Account |
| 39 | T1134.003 | Make and Impersonate Token | Stealth; Privilege Escalation | Session / Token | Session / Token / Workflow Abuse | CAPEC-196 | Session / Token / Workflow Abuse; Watch: Process; Logon Session |
| 40 | T1098.002 | Additional Email Delegate Permissions | Persistence; Privilege Escalation | Customer Data | API / SaaS Blast Radius |  | API / SaaS Blast Radius; Watch: Process; User Account; Application Log |
| 41 | T1550.004 | Web Session Cookie | Lateral Movement | API / Web / WAF; Session / Token | Session / Token / Workflow Abuse | CAPEC-60 | Session / Token / Workflow Abuse; Watch: Web Credential; Logon Session; User Account |
| 42 | T1095 | Non-Application Layer Protocol | Command and Control | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Network Traffic |
| 43 | T1190 | Exploit Public-Facing Application | Initial Access | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; Module; Application Log |
| 44 | T1102 | Web Service | Command and Control | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Network Traffic |
| 45 | T1566.002 | Spearphishing Link | Initial Access | API / Web / WAF | Zero-Day / Unknown Exploit | CAPEC-163 | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; Application Log |
| 46 | T1217 | Browser Information Discovery | Discovery | API / Web / WAF | Insider / Trusted Access | CAPEC-169 | Insider / Trusted Access; Watch: Command; Process; File |
| 47 | T1087.003 | Email Account | Discovery | Customer Data | API / SaaS Blast Radius |  | API / SaaS Blast Radius; Watch: Command; Process; User Account; Application Log |
| 48 | T1566 | Phishing | Initial Access | API / Web / WAF | Session / Token / Workflow Abuse | CAPEC-98 | Session / Token / Workflow Abuse; Watch: Process; File; Logon Session; Application Log |
| 49 | T1221 | Template Injection | Stealth | API / Web / WAF | Zero-Day / Unknown Exploit | CAPEC-636 | Zero-Day / Unknown Exploit; Watch: Process; Network Traffic |
| 50 | T1059.009 | Cloud API | Execution | API / Web / WAF | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse; Watch: Command; User Account; Cloud Service |
| 51 | T1505.001 | SQL Stored Procedures | Persistence | API / Web / WAF | Living-off-the-Land |  | Living-off-the-Land; Watch: Process; Script; Module |
| 52 | T1036.012 | Browser Fingerprint | Stealth | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Network Traffic; Process |
| 53 | T1566.001 | Spearphishing Attachment | Initial Access | API / Web / WAF | Zero-Day / Unknown Exploit | CAPEC-163 | Zero-Day / Unknown Exploit; Watch: Process; Network Traffic; File; Application Log |
| 54 | T1134.001 | Token Impersonation/Theft | Stealth; Privilege Escalation | Session / Token | Session / Token / Workflow Abuse | CAPEC-60 | Session / Token / Workflow Abuse; Watch: Process |
| 55 | T1553.005 | Mark-of-the-Web Bypass | Defense Impairment | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: File |
| 56 | T1566.003 | Spearphishing via Service | Initial Access | API / Web / WAF | Zero-Day / Unknown Exploit | CAPEC-163 | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; File; Application Log |
| 57 | T1674 | Input Injection | Execution | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Drive; Process; Command; Script |
| 58 | T1027.007 | Dynamic API Resolution | Stealth | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Process; Module |
| 59 | T1619 | Cloud Storage Object Discovery | Discovery | Customer Data | API / SaaS Blast Radius |  | API / SaaS Blast Radius; Watch: Cloud Storage |
| 60 | T1566.004 | Spearphishing Voice | Initial Access | API / Web / WAF | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse; Watch: Application Log |
| 61 | T1684.002 | Email Spoofing | Stealth | Customer Data | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Application Log |
| 62 | T1599.001 | Network Address Translation Traversal | Defense Impairment | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Network Traffic |
| 63 | T1437.001 | Web Protocols | Command and Control | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 64 | T1660 | Phishing | Initial Access | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 65 | T1516 | Input Injection | Defense Evasion; Impact | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 66 | T1437 | Application Layer Protocol | Command and Control | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 67 | T1481 | Web Service | Command and Control | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 68 | T1635 | Steal Application Access Token | Credential Access | Session / Token | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse |

## CAPEC Attack Pattern Matrix

| rank | capec_id | attack_pattern | surface | edge_case | related_attack | watch_focus |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | CAPEC-150 | Collect Data from Common Resource Locations | Customer Data; API / Web / WAF | API / SaaS Blast Radius | T1003; T1119; T1213; T1530; T1555; T1602 | API / SaaS Blast Radius; CWE: CWE-1239; CWE-1258; CWE-1266; CWE-1272; CWE-1323; CWE-1330; CWE-552 |
| 2 | CAPEC-636 | Hiding Malicious Data or Code within Files | API / Web / WAF | Zero-Day / Unknown Exploit | T1001.002; T1027.003; T1027.004; T1218.001; T1221 | Zero-Day / Unknown Exploit; CWE: CWE-506 |
| 3 | CAPEC-593 | Session Hijacking | API / Web / WAF; Session / Token | Session / Token / Workflow Abuse | T1185; T1550.001; T1563 | Session / Token / Workflow Abuse; CWE: CWE-287 |
| 4 | CAPEC-482 | TCP Flood | API / Web / WAF | Destructive / Ransomware | T1498.001; T1499.001; T1499.002 | Destructive / Ransomware; CWE: CWE-770 |
| 5 | CAPEC-654 | Credential Prompt Impersonation | API / Web / WAF | Zero-Day / Unknown Exploit | T1056; T1548.004 | Zero-Day / Unknown Exploit; CWE: CWE-1021 |
| 6 | CAPEC-634 | Probe Audio and Video Peripherals | API / Web / WAF | Zero-Day / Unknown Exploit | T1123; T1125 | Zero-Day / Unknown Exploit; CWE: CWE-267 |
| 7 | CAPEC-528 | XML Flood | API / Web / WAF | Destructive / Ransomware | T1498.001; T1499.002 | Destructive / Ransomware; CWE: CWE-770 |
| 8 | CAPEC-125 | Flooding | API / Web / WAF | Destructive / Ransomware | T1498.001; T1499 | Destructive / Ransomware; CWE: CWE-404; CWE-770 |
| 9 | CAPEC-662 | Adversary in the Browser (AiTB) | API / Web / WAF; Session / Token | Session / Token / Workflow Abuse | T1185 | Session / Token / Workflow Abuse; CWE: CWE-300; CWE-494 |
| 10 | CAPEC-569 | Collect Data as Provided by Users | API / Web / WAF | Zero-Day / Unknown Exploit | T1056 | Zero-Day / Unknown Exploit |
| 11 | CAPEC-489 | SSL Flood | API / Web / WAF | Destructive / Ransomware | T1499.002 | Destructive / Ransomware; CWE: CWE-770 |
| 12 | CAPEC-488 | HTTP Flood | API / Web / WAF | Destructive / Ransomware | T1499.002 | Destructive / Ransomware; CWE: CWE-770 |
| 13 | CAPEC-469 | HTTP DoS | API / Web / WAF | Destructive / Ransomware | T1499.002 | Destructive / Ransomware; CWE: CWE-770; CWE-772 |
| 14 | CAPEC-227 | Sustained Client Engagement | API / Web / WAF | Destructive / Ransomware | T1499 | Destructive / Ransomware; CWE: CWE-400 |
| 15 | CAPEC-204 | Lifting Sensitive Data Embedded in Cache | Customer Data; Session / Token | Telemetry Gap / Evasion | T1005 | Telemetry Gap / Evasion; CWE: CWE-1239; CWE-1258; CWE-311; CWE-524 |
| 16 | CAPEC-148 | Content Spoofing | API / Web / WAF | API / SaaS Blast Radius | T1491 | API / SaaS Blast Radius; CWE: CWE-345 |
| 17 | CAPEC-131 | Resource Leak Exposure | API / Web / WAF | Destructive / Ransomware | T1499 | Destructive / Ransomware; CWE: CWE-404 |
| 18 | CAPEC-130 | Excessive Allocation | API / Web / WAF | API / SaaS Blast Radius | T1499.003 | API / SaaS Blast Radius; CWE: CWE-1325; CWE-404; CWE-770 |
| 19 | CAPEC-77 | Manipulating User-Controlled Variables | API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-1321; CWE-15; CWE-285; CWE-302; CWE-473; CWE-94; CWE-96 |
| 20 | CAPEC-44 | Overflow Binary Resource File | Session / Token | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-119; CWE-120; CWE-697 |
| 21 | CAPEC-163 | Spear Phishing | API / Web / WAF | Zero-Day / Unknown Exploit | T1534; T1566.001; T1566.002; T1566.003; T1598.001; T1598.002; T1598.003 | Zero-Day / Unknown Exploit; CWE: CWE-451 |
| 22 | CAPEC-21 | Exploitation of Trusted Identifiers | Session / Token; API / Web / WAF | Session / Token / Workflow Abuse | T1134; T1528; T1539 | Session / Token / Workflow Abuse; CWE: CWE-290; CWE-302; CWE-346; CWE-384; CWE-539; CWE-6; CWE-602; CWE-642; CWE-664 |
| 23 | CAPEC-542 | Targeted Malware | API / Web / WAF | Telemetry Gap / Evasion | T1027; T1587.001 | Telemetry Gap / Evasion |
| 24 | CAPEC-478 | Modification of Windows Service Configuration | API / Web / WAF | Zero-Day / Unknown Exploit | T1543.003; T1574.011 | Zero-Day / Unknown Exploit; CWE: CWE-284 |
| 25 | CAPEC-650 | Upload a Web Shell to a Web Server | API / Web / WAF | Session / Token / Workflow Abuse | T1505.003 | Session / Token / Workflow Abuse; CWE: CWE-287; CWE-553 |
| 26 | CAPEC-57 | Utilizing REST's Trust in the System Resource to Obtain Sensitive Data | Customer Data; API / Web / WAF | Session / Token / Workflow Abuse | T1040 | Session / Token / Workflow Abuse; CWE: CWE-287; CWE-300; CWE-693 |
| 27 | CAPEC-543 | Counterfeit Websites | API / Web / WAF | Telemetry Gap / Evasion | T1036.005 | Telemetry Gap / Evasion |
| 28 | CAPEC-31 | Accessing/Intercepting/Modifying HTTP Cookies | API / Web / WAF; Session / Token | Session / Token / Workflow Abuse | T1539 | Session / Token / Workflow Abuse; CWE: CWE-113; CWE-20; CWE-302; CWE-311; CWE-315; CWE-384; CWE-472; CWE-539; CWE-565; CWE-602; CWE-642 |
| 29 | CAPEC-267 | Leverage Alternate Encoding | API / Web / WAF | Telemetry Gap / Evasion | T1027 | Telemetry Gap / Evasion; CWE: CWE-172; CWE-173; CWE-180; CWE-181; CWE-20; CWE-692; CWE-697; CWE-73; CWE-74 |
| 30 | CAPEC-177 | Create files with the same name as files protected with a higher classification | API / Web / WAF | Telemetry Gap / Evasion | T1036 | Telemetry Gap / Evasion; CWE: CWE-706 |
| 31 | CAPEC-666 | BlueSmacking | API / Web / WAF | API / SaaS Blast Radius | T1498.001; T1499.001 | API / SaaS Blast Radius; CWE: CWE-404 |
| 32 | CAPEC-481 | Contradictory Destinations in Traffic Routing Schemes | API / Web / WAF | Telemetry Gap / Evasion | T1090.004 | Telemetry Gap / Evasion; CWE: CWE-923 |
| 33 | CAPEC-383 | Harvesting Information via API Event Monitoring | API / Web / WAF | Session / Token / Workflow Abuse | T1056.004 | Session / Token / Workflow Abuse; CWE: CWE-311; CWE-319; CWE-419; CWE-602 |
| 34 | CAPEC-2 | Inducing Account Lockout | Session / Token | Session / Token / Workflow Abuse | T1531 | Session / Token / Workflow Abuse; CWE: CWE-645 |
| 35 | CAPEC-681 | Exploitation of Improperly Controlled Hardware Security Identifiers | Session / Token | Exploit Chain / Multi-Step |  | Exploit Chain / Multi-Step; CWE: CWE-1259; CWE-1267; CWE-1270; CWE-1294; CWE-1302 |
| 36 | CAPEC-663 | Exploitation of Transient Instruction Execution | Customer Data; API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-1037; CWE-1264; CWE-1303 |
| 37 | CAPEC-237 | Escaping a Sandbox by Calling Code in Another Language | API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-693 |
| 38 | CAPEC-35 | Leverage Executable Code in Non-Executable Files | API / Web / WAF | Rare but High Impact | T1027.006; T1027.009; T1564.009 | Rare but High Impact; CWE: CWE-270; CWE-272; CWE-282; CWE-59; CWE-94; CWE-95; CWE-96; CWE-97 |
| 39 | CAPEC-196 | Session Credential Falsification through Forging | Session / Token; API / Web / WAF | Session / Token / Workflow Abuse | T1134.002; T1134.003; T1606 | Session / Token / Workflow Abuse; CWE: CWE-384; CWE-664 |
| 40 | CAPEC-660 | Root/Jailbreak Detection Evasion via Hooking | API / Web / WAF | Telemetry Gap / Evasion | T1055 | Telemetry Gap / Evasion; CWE: CWE-829 |
| 41 | CAPEC-657 | Malicious Automated Software Update via Spoofing | API / Web / WAF | Supply Chain / Trusted Dependency | T1072 | Supply Chain / Trusted Dependency; CWE: CWE-494 |
| 42 | CAPEC-633 | Token Impersonation | Session / Token; API / Web / WAF | Session / Token / Workflow Abuse | T1134 | Session / Token / Workflow Abuse; CWE: CWE-1270; CWE-287 |
| 43 | CAPEC-480 | Escaping Virtualization | API / Web / WAF | Rare but High Impact | T1611 | Rare but High Impact; CWE: CWE-693 |
| 44 | CAPEC-464 | Evercookie | API / Web / WAF; Session / Token | Session / Token / Workflow Abuse | T1606.001 | Session / Token / Workflow Abuse; CWE: CWE-359 |
| 45 | CAPEC-251 | Local Code Inclusion | API / Web / WAF | Telemetry Gap / Evasion | T1055 | Telemetry Gap / Evasion; CWE: CWE-829 |
| 46 | CAPEC-83 | XPath Injection | Customer Data; API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-20; CWE-707; CWE-74; CWE-91 |
| 47 | CAPEC-8 | Buffer Overflow in an API Call | API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-118; CWE-119; CWE-120; CWE-20; CWE-680; CWE-697; CWE-733; CWE-74 |
| 48 | CAPEC-656 | Voice Phishing | API / Web / WAF | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse |
| 49 | CAPEC-59 | Session Credential Falsification through Prediction | Payment / Transaction; Session / Token | Rare but High Impact |  | Rare but High Impact; CWE: CWE-200; CWE-285; CWE-290; CWE-330; CWE-331; CWE-346; CWE-384; CWE-488; CWE-539; CWE-6; CWE-693 |
| 50 | CAPEC-48 | Passing Local Filenames to Functions That Expect a URL | Session / Token | Rare but High Impact |  | Rare but High Impact; CWE: CWE-241; CWE-706 |
| 51 | CAPEC-229 | Serialized Data Parameter Blowup | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-770 |
| 52 | CAPEC-201 | Serialized Data External Linking | API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-829 |
| 53 | CAPEC-136 | LDAP Injection | API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-20; CWE-77; CWE-90 |
| 54 | CAPEC-86 | XSS Through HTTP Headers | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-80 |
| 55 | CAPEC-84 | XQuery Injection | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-707; CWE-74 |
| 56 | CAPEC-76 | Manipulating Web Input to File System Calls | API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-15; CWE-22; CWE-23; CWE-272; CWE-285; CWE-346; CWE-348; CWE-59; CWE-73; CWE-74; CWE-77 |
| 57 | CAPEC-67 | String Format Overflow in syslog() | API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-120; CWE-134; CWE-20; CWE-680; CWE-697; CWE-74 |
| 58 | CAPEC-63 | Cross-Site Scripting (XSS) | Session / Token; API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-20; CWE-79 |
| 59 | CAPEC-62 | Cross Site Request Forgery | Session / Token; API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-1275; CWE-306; CWE-352; CWE-664; CWE-732 |
| 60 | CAPEC-592 | Stored XSS | API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-79 |
| 61 | CAPEC-591 | Reflected XSS | Session / Token; API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-79 |
| 62 | CAPEC-588 | DOM-Based XSS | Session / Token; API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-20; CWE-79; CWE-83 |
| 63 | CAPEC-51 | Poison Web Service Registry | API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-285; CWE-693; CWE-74 |
| 64 | CAPEC-275 | DNS Rebinding | Session / Token; API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-350 |
| 65 | CAPEC-23 | File Content Injection | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-20 |
| 66 | CAPEC-18 | XSS Targeting Non-Script Elements | API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-80 |
| 67 | CAPEC-126 | Path Traversal | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-22 |
| 68 | CAPEC-110 | SQL Injection through SOAP Parameter Tampering | Customer Data; API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-20; CWE-89 |
| 69 | CAPEC-60 | Reusing Session IDs (aka Session Replay) | Session / Token; API / Web / WAF | Session / Token / Workflow Abuse | T1134.001; T1550.004 | Session / Token / Workflow Abuse; CWE: CWE-200; CWE-285; CWE-290; CWE-294; CWE-346; CWE-384; CWE-488; CWE-539; CWE-664; CWE-732 |
| 70 | CAPEC-17 | Using Malicious Files | API / Web / WAF | Living-off-the-Land | T1574.005; T1574.010 | Living-off-the-Land; CWE: CWE-270; CWE-272; CWE-282; CWE-285; CWE-59; CWE-693; CWE-732 |
| 71 | CAPEC-30 | Hijacking a Privileged Thread of Execution | API / Web / WAF | Telemetry Gap / Evasion | T1055.003 | Telemetry Gap / Evasion; CWE: CWE-270 |
| 72 | CAPEC-1 | Accessing Functionality Not Properly Constrained by ACLs | API / Web / WAF | Rare but High Impact | T1574.010 | Rare but High Impact; CWE: CWE-1191; CWE-1193; CWE-1220; CWE-1297; CWE-1311; CWE-1314; CWE-1315; CWE-1318; CWE-1320; CWE-1321; CWE-1327; CWE-276; CWE-285; CWE-434; CWE-693; CWE-732 |
| 73 | CAPEC-47 | Buffer Overflow via Parameter Expansion | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-118; CWE-119; CWE-120; CWE-130; CWE-131; CWE-20; CWE-680; CWE-697; CWE-74 |
| 74 | CAPEC-230 | Serialized Data with Nested Payloads | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-112; CWE-20; CWE-674; CWE-770 |
| 75 | CAPEC-16 | Dictionary-based Password Attack | Session / Token | Exploit Chain / Multi-Step |  | Exploit Chain / Multi-Step; CWE: CWE-262; CWE-263; CWE-307; CWE-308; CWE-309; CWE-521; CWE-654 |
| 76 | CAPEC-470 | Expanding Control over the Operating System from the Database | Customer Data; API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-250; CWE-89 |
| 77 | CAPEC-138 | Reflection Injection | API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-470 |
| 78 | CAPEC-108 | Command Line Execution through SQL Injection | Customer Data; API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-114; CWE-20; CWE-74; CWE-78; CWE-89 |
| 79 | CAPEC-107 | Cross Site Tracing | Session / Token; API / Web / WAF | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse; CWE: CWE-648; CWE-693 |
| 80 | CAPEC-169 | Footprinting | API / Web / WAF | Insider / Trusted Access | T1217; T1592; T1595 | Insider / Trusted Access; CWE: CWE-200 |
| 81 | CAPEC-98 | Phishing | API / Web / WAF | Session / Token / Workflow Abuse | T1566; T1598 | Session / Token / Workflow Abuse; CWE: CWE-451 |
| 82 | CAPEC-698 | Install Malicious Extension | API / Web / WAF | Session / Token / Workflow Abuse | T1176; T1505.004 | Session / Token / Workflow Abuse; CWE: CWE-507; CWE-829 |
| 83 | CAPEC-575 | Account Footprinting | Customer Data | API / SaaS Blast Radius | T1087 | API / SaaS Blast Radius; CWE: CWE-200 |
| 84 | CAPEC-497 | File Discovery | API / Web / WAF | Rare but High Impact | T1083 | Rare but High Impact; CWE: CWE-200 |
| 85 | CAPEC-479 | Malicious Root Certificate | Session / Token; API / Web / WAF | Telemetry Gap / Evasion | T1553.004 | Telemetry Gap / Evasion; CWE: CWE-284 |
| 86 | CAPEC-95 | WSDL Scanning | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-538 |
| 87 | CAPEC-87 | Forceful Browsing | API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-285; CWE-425; CWE-693 |
| 88 | CAPEC-73 | User-Controlled Filename | Session / Token; API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-116; CWE-184; CWE-20; CWE-348; CWE-350; CWE-697; CWE-86; CWE-96 |
| 89 | CAPEC-7 | Blind SQL Injection | Customer Data; API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-20; CWE-209; CWE-697; CWE-707; CWE-74; CWE-89 |
| 90 | CAPEC-676 | NoSQL Injection | API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-1286; CWE-943 |
| 91 | CAPEC-664 | Server Side Request Forgery | Customer Data; API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-20; CWE-918 |
| 92 | CAPEC-66 | SQL Injection | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-1286; CWE-89 |
| 93 | CAPEC-58 | Restful Privilege Elevation | API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-267; CWE-269 |
| 94 | CAPEC-510 | SaaS User Request Forgery | Session / Token | API / SaaS Blast Radius |  | API / SaaS Blast Radius; CWE: CWE-346 |
| 95 | CAPEC-41 | Using Meta-characters in E-mail Headers to Inject Malicious Payloads | Session / Token; API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-150; CWE-697; CWE-88 |
| 96 | CAPEC-39 | Manipulating Opaque Client-based Data Tokens | Session / Token | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse; CWE: CWE-233; CWE-285; CWE-302; CWE-315; CWE-353; CWE-384; CWE-472; CWE-539; CWE-565 |
| 97 | CAPEC-32 | XSS Through HTTP Query Strings | Session / Token; API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-80 |
| 98 | CAPEC-256 | SOAP Array Overflow | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-805 |
| 99 | CAPEC-244 | XSS Targeting URI Placeholders | Session / Token; API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-83 |
| 100 | CAPEC-199 | XSS Using Alternate Syntax | API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-87 |
| 101 | CAPEC-193 | PHP Remote File Inclusion | API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-80; CWE-98 |
| 102 | CAPEC-174 | Flash Parameter Injection | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-88 |
| 103 | CAPEC-164 | Mobile Phishing | API / Web / WAF | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse; CWE: CWE-451 |
| 104 | CAPEC-12 | Choosing Message Identifier | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-201; CWE-306 |
| 105 | CAPEC-111 | JSON Hijacking (aka JavaScript Hijacking) | Session / Token; API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-345; CWE-346; CWE-352 |
| 106 | CAPEC-102 | Session Sidejacking | Session / Token | Destructive / Ransomware |  | Destructive / Ransomware; CWE: CWE-294; CWE-319; CWE-522; CWE-523; CWE-614 |
| 107 | CAPEC-101 | Server Side Include (SSI) Injection | API / Web / WAF | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse; CWE: CWE-20; CWE-74; CWE-97 |
| 108 | CAPEC-11 | Cause Web Server Misclassification | API / Web / WAF | Zero-Day / Unknown Exploit | T1036.006 | Zero-Day / Unknown Exploit; CWE: CWE-430 |
| 109 | CAPEC-81 | Web Server Logs Tampering | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-116; CWE-117; CWE-150; CWE-20; CWE-221; CWE-276; CWE-279; CWE-75; CWE-93; CWE-96 |
| 110 | CAPEC-701 | Browser in the Middle (BiTM) | Session / Token; API / Web / WAF | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse; CWE: CWE-294; CWE-345 |
| 111 | CAPEC-34 | HTTP Response Splitting | API / Web / WAF | Insider / Trusted Access |  | Insider / Trusted Access; CWE: CWE-113; CWE-138; CWE-436; CWE-74 |
| 112 | CAPEC-33 | HTTP Request Smuggling | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-444 |
| 113 | CAPEC-3 | Using Leading 'Ghost' Character Sequences to Bypass Input Filters | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-172; CWE-173; CWE-179; CWE-180; CWE-181; CWE-183; CWE-184; CWE-20; CWE-41; CWE-697; CWE-707; CWE-74 |
| 114 | CAPEC-279 | SOAP Manipulation | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-707 |
| 115 | CAPEC-273 | HTTP Response Smuggling | API / Web / WAF | Insider / Trusted Access |  | Insider / Trusted Access; CWE: CWE-436; CWE-444; CWE-74 |
| 116 | CAPEC-178 | Cross-Site Flashing | Session / Token | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-601 |
| 117 | CAPEC-14 | Client-side Injection-induced Buffer Overflow | Session / Token; API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-118; CWE-119; CWE-120; CWE-20; CWE-353; CWE-680; CWE-697; CWE-74 |
| 118 | CAPEC-113 | Interface Manipulation | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-1192 |
| 119 | CAPEC-105 | HTTP Request Splitting | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-113; CWE-138; CWE-436; CWE-74 |
| 120 | CAPEC-104 | Cross Zone Scripting | Session / Token; API / Web / WAF | Exploit Chain / Multi-Step |  | Exploit Chain / Multi-Step; CWE: CWE-116; CWE-20; CWE-250; CWE-285; CWE-638 |
| 121 | CAPEC-600 | Credential Stuffing | Session / Token | Session / Token / Workflow Abuse | T1110.004 | Session / Token / Workflow Abuse; CWE: CWE-262; CWE-263; CWE-307; CWE-308; CWE-309; CWE-522; CWE-654 |
| 122 | CAPEC-565 | Password Spraying | Session / Token; API / Web / WAF | Session / Token / Workflow Abuse | T1110.003 | Session / Token / Workflow Abuse; CWE: CWE-262; CWE-263; CWE-307; CWE-308; CWE-309; CWE-521; CWE-654 |
| 123 | CAPEC-141 | Cache Poisoning | Customer Data; Session / Token; API / Web / WAF | Session / Token / Workflow Abuse | T1557.002 | Session / Token / Workflow Abuse; CWE: CWE-345; CWE-346; CWE-348; CWE-349 |
| 124 | CAPEC-587 | Cross Frame Scripting (XFS) | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-1021 |
| 125 | CAPEC-468 | Generic Cross-Browser Cross-Domain Theft | Session / Token | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse; CWE: CWE-149; CWE-177; CWE-707; CWE-838 |
| 126 | CAPEC-466 | Leveraging Active Adversary in the Middle Attacks to Bypass Same Origin Policy | Session / Token; API / Web / WAF | API / SaaS Blast Radius |  | API / SaaS Blast Radius; CWE: CWE-300 |
| 127 | CAPEC-461 | Web Services API Signature Forgery Leveraging Hash Function Extension Weakness | Session / Token; API / Web / WAF | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse; CWE: CWE-290; CWE-328 |
| 128 | CAPEC-388 | Application API Button Hijacking | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-311; CWE-345; CWE-346; CWE-471; CWE-602 |
| 129 | CAPEC-386 | Application API Navigation Remapping | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-311; CWE-345; CWE-346; CWE-471; CWE-602 |
| 130 | CAPEC-385 | Transaction or Event Tampering via Application API Manipulation | Payment / Transaction; API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-311; CWE-345; CWE-346; CWE-471; CWE-602 |
| 131 | CAPEC-250 | XML Injection | Customer Data; API / Web / WAF | Insider / Trusted Access |  | Insider / Trusted Access; CWE: CWE-20; CWE-707; CWE-74; CWE-91 |
| 132 | CAPEC-226 | Session Credential Falsification through Manipulation | Session / Token | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse; CWE: CWE-472; CWE-565 |
| 133 | CAPEC-221 | Data Serialization External Entities Blowup | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-611 |
| 134 | CAPEC-219 | XML Routing Detour Attacks | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-441; CWE-610 |
| 135 | CAPEC-195 | Principal Spoof | API / Web / WAF | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse |
| 136 | CAPEC-182 | Flash Injection | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-184; CWE-20; CWE-697 |
| 137 | CAPEC-173 | Action Spoofing | API / Web / WAF | Rare but High Impact |  | Rare but High Impact; CWE: CWE-451 |
| 138 | CAPEC-146 | XML Schema Poisoning | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-15; CWE-472 |
| 139 | CAPEC-109 | Object Relational Mapping Injection | Customer Data; API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-20; CWE-564; CWE-89 |
| 140 | CAPEC-416 | Manipulate Human Behavior | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit |
| 141 | CAPEC-137 | Parameter Injection | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-88 |
| 142 | CAPEC-700 | Network Boundary Bridging | API / Web / WAF | Telemetry Gap / Evasion | T1599 | Telemetry Gap / Evasion |
| 143 | CAPEC-632 | Homograph Attack via Homoglyphs | API / Web / WAF | AI-Scaled Social Engineering |  | AI-Scaled Social Engineering; CWE: CWE-1007 |
| 144 | CAPEC-630 | TypoSquatting | API / Web / WAF | API / SaaS Blast Radius |  | API / SaaS Blast Radius |
| 145 | CAPEC-611 | BitSquatting | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit |
| 146 | CAPEC-597 | Absolute Path Traversal | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-36 |
| 147 | CAPEC-596 | TCP RST Injection | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-940 |
| 148 | CAPEC-594 | Traffic Injection | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-940 |
| 149 | CAPEC-585 | DNS Domain Seizure | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 150 | CAPEC-563 | Add Malicious File to Shared Webroot | Session / Token; API / Web / WAF | Exploit Chain / Multi-Step |  | Exploit Chain / Multi-Step; CWE: CWE-284 |
| 151 | CAPEC-503 | WebView Exposure | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-284 |
| 152 | CAPEC-500 | WebView Injection | Session / Token; API / Web / WAF | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse; CWE: CWE-749; CWE-940 |
| 153 | CAPEC-496 | ICMP Fragmentation | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-404; CWE-770 |
| 154 | CAPEC-495 | UDP Fragmentation | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-404; CWE-770 |
| 155 | CAPEC-494 | TCP Fragmentation | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-404; CWE-770 |
| 156 | CAPEC-493 | SOAP Array Blowup | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-770 |
| 157 | CAPEC-487 | ICMP Flood | Session / Token; API / Web / WAF | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse; CWE: CWE-770 |
| 158 | CAPEC-486 | UDP Flood | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-770 |
| 159 | CAPEC-462 | Cross-Domain Search Timing | Session / Token; API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-208; CWE-352; CWE-385 |
| 160 | CAPEC-460 | HTTP Parameter Pollution (HPP) | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-147; CWE-235; CWE-88 |
| 161 | CAPEC-278 | Web Services Protocol Manipulation | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-707 |
| 162 | CAPEC-277 | Data Interchange Protocol Manipulation | Session / Token; API / Web / WAF | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse; CWE: CWE-707 |
| 163 | CAPEC-276 | Inter-component Protocol Manipulation | Session / Token | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse; CWE: CWE-707 |
| 164 | CAPEC-274 | HTTP Verb Tampering | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-302; CWE-654 |
| 165 | CAPEC-272 | Protocol Manipulation | Session / Token | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse |
| 166 | CAPEC-247 | XSS Using Invalid Characters | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-86 |
| 167 | CAPEC-245 | XSS Using Doubled Characters | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-85 |
| 168 | CAPEC-243 | XSS Targeting HTML Attributes | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-83 |
| 169 | CAPEC-218 | Spoofing of UDDI/ebXML Messages | Payment / Transaction; API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-345 |
| 170 | CAPEC-216 | Communication Channel Manipulation | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-306 |
| 171 | CAPEC-209 | XSS Using MIME Type Mismatch | Session / Token; API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-20; CWE-646; CWE-79 |
| 172 | CAPEC-198 | XSS Targeting Error Pages | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-81 |
| 173 | CAPEC-183 | IMAP/SMTP Command Injection | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-77 |
| 174 | CAPEC-179 | Calling Micro-Services Directly | API / Web / WAF | Supply Chain / Trusted Dependency |  | Supply Chain / Trusted Dependency |
| 175 | CAPEC-160 | Exploit Script-Based APIs | Session / Token; API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-346 |
| 176 | CAPEC-147 | XML Ping of the Death | Payment / Transaction; API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-400; CWE-770 |
| 177 | CAPEC-140 | Bypassing of Intermediate Forms in Multiple-Form Sets | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-372 |
| 178 | CAPEC-134 | Email Injection | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-150 |
| 179 | CAPEC-133 | Try All Common Switches | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-912 |
| 180 | CAPEC-61 | Session Fixation | Payment / Transaction; Session / Token | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse; CWE: CWE-384; CWE-664; CWE-732 |
| 181 | CAPEC-330 | ICMP Error Message Echoing Integrity Probe | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-200 |
| 182 | CAPEC-329 | ICMP Error Message Quoting Probe | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-200 |
| 183 | CAPEC-318 | IP 'ID' Echoed Byte-Order Probe | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-200 |
| 184 | CAPEC-85 | AJAX Footprinting | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-113; CWE-116; CWE-184; CWE-20; CWE-348; CWE-692; CWE-79; CWE-86; CWE-96 |
| 185 | CAPEC-54 | Query System for Information | API / Web / WAF | Insider / Trusted Access |  | Insider / Trusted Access; CWE: CWE-209 |
| 186 | CAPEC-517 | Documentation Alteration to Circumvent Dial-down | Customer Data; API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 187 | CAPEC-414 | Pretexting via Delivery Person | API / Web / WAF | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse |
| 188 | CAPEC-389 | Content Spoofing Via Application API Manipulation | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-353 |
| 189 | CAPEC-170 | Web Application Fingerprinting | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-497 |
| 190 | CAPEC-331 | ICMP IP Total Length Field Probe | API / Web / WAF | Supply Chain / Trusted Dependency |  | Supply Chain / Trusted Dependency; CWE: CWE-204 |
| 191 | CAPEC-327 | TCP Options Probe | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-200 |
| 192 | CAPEC-326 | TCP Initial Window Size Probe | Session / Token | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse; CWE: CWE-200 |
| 193 | CAPEC-320 | TCP Timestamp Probe | API / Web / WAF | Supply Chain / Trusted Dependency |  | Supply Chain / Trusted Dependency; CWE: CWE-200 |
| 194 | CAPEC-407 | Pretexting | Customer Data | Zero-Day / Unknown Exploit | T1589 | Zero-Day / Unknown Exploit |
| 195 | CAPEC-142 | DNS Cache Poisoning | Customer Data | Rare but High Impact | T1584.002 | Rare but High Impact; CWE: CWE-345; CWE-346; CWE-348; CWE-349; CWE-350 |
| 196 | CAPEC-507 | Physical Theft | Session / Token | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse |
| 197 | CAPEC-472 | Browser Fingerprinting | Session / Token; API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-200 |
| 198 | CAPEC-467 | Cross Site Identification | Session / Token | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse; CWE: CWE-352; CWE-359 |
| 199 | CAPEC-427 | Influence via Psychological Principles | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 200 | CAPEC-415 | Pretexting via Phone | API / Web / WAF | AI-Scaled Social Engineering |  | AI-Scaled Social Engineering |
| 201 | CAPEC-413 | Pretexting via Tech Support | API / Web / WAF | AI-Scaled Social Engineering |  | AI-Scaled Social Engineering |
| 202 | CAPEC-412 | Pretexting via Customer Service | Customer Data; API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 203 | CAPEC-384 | Application API Message Manipulation via Man-in-the-Middle | API / Web / WAF | Exploit Chain / Multi-Step |  | Exploit Chain / Multi-Step; CWE: CWE-311; CWE-345; CWE-346; CWE-471; CWE-602 |
| 204 | CAPEC-308 | UDP Scan | Session / Token | Session / Token / Workflow Abuse |  | Session / Token / Workflow Abuse; CWE: CWE-200 |
| 205 | CAPEC-304 | TCP Null Scan | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-200 |
| 206 | CAPEC-303 | TCP Xmas Scan | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-200 |
| 207 | CAPEC-302 | TCP FIN Scan | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-200 |
| 208 | CAPEC-290 | Enumerate Mail Exchange (MX) Records | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-200 |
| 209 | CAPEC-228 | DTD Injection | API / Web / WAF | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-829 |
| 210 | CAPEC-189 | Black Box Reverse Engineering | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-1255; CWE-1300; CWE-203 |
| 211 | CAPEC-144 | Detect Unpublicized Web Services | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-425 |
| 212 | CAPEC-143 | Detect Unpublicized Web Pages | API / Web / WAF | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-425 |
