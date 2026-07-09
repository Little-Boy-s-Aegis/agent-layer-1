# Agent A CAPEC + MITRE ATT&CK Watch Matrix

Generated: scoped runtime rewrite from local Layer 1 package references

Agent: Agent A

This file is a Layer 1 watchlist source. It is not an exploit guide and does not authorize containment. Layer 1 uses it to map observed behavior to ATT&CK/CAPEC/CWE labels and form non-scoring attack-pattern prediction hints before emitting structured JSON to the deterministic Layer 2 orchestrator.

## Scope

- Input: sanitized, normalized telemetry from Layer 0 preprocessing.
- Output: read-only JSON finding for Layer 2 correlation.
- Layer 1 does not compute risk score, priority tier, routing, or auto-containment.
- Layer 2 independently verifies Layer 1 findings from logs/context, then performs deterministic scoring, OPA policy checks, and playbook execution.

## Primary Surfaces

Endpoint / EDR, Internal Network, Server / Workload

## Included Matrix Size

- ATT&CK rows included here: 202
- CAPEC rows included here: 183
- ATT&CK source boundary: `agent_a/surface_context_matrix.md`
- CAPEC source boundary: `agent_a/capec_attack_pattern_prediction_reference.md`

## MITRE ATT&CK Matrix Vectors

| rank | attack_id | attack_vector | tactics | surface | edge_case | related_capec | watch_focus |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | T1105 | Ingress Tool Transfer | Command and Control | Endpoint / EDR | Living-off-the-Land |  | Living-off-the-Land; Watch: Command; Process; Network Traffic; File |
| 2 | T1074.001 | Local Data Staging | Collection | Endpoint / EDR | Server / Workload Blast Radius |  | Server / Workload Blast Radius; Watch: Command; Process; Snapshot; File |
| 3 | T1486 | Data Encrypted for Impact | Impact | Endpoint / EDR | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Process; File |
| 4 | T1560.001 | Archive via Utility | Collection | Endpoint / EDR | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Process; File; Module |
| 5 | T1090 | Proxy | Command and Control | Internal Network | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Process; Network Traffic; Firewall |
| 6 | T1560 | Archive Collected Data | Collection | Endpoint / EDR | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Process; File; Module |
| 7 | T1490 | Inhibit System Recovery | Impact | Server / Workload | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Process; Windows Registry; Service; File; Snapshot |
| 8 | T1489 | Service Stop | Impact | Server / Workload | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Process; Service; File |
| 9 | T1485 | Data Destruction | Impact | Endpoint / EDR | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Process; File; Volume |
| 10 | T1048.003 | Exfiltration Over Unencrypted Non-C2 Protocol | Exfiltration | Internal Network | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Network Traffic; Process; File |
| 11 | T1041 | Exfiltration Over C2 Channel | Exfiltration | Internal Network | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; File |
| 12 | T1571 | Non-Standard Port | Command and Control | Internal Network | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; Application Log |
| 13 | T1071.004 | DNS | Command and Control | Internal Network | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process |
| 14 | T1560.003 | Archive via Custom Method | Collection | Endpoint / EDR | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Process; Command; File |
| 15 | T1572 | Protocol Tunneling | Command and Control | Internal Network | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; Application Log |
| 16 | T1090.003 | Multi-hop Proxy | Command and Control | Internal Network | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Firmware; Network Traffic; Process |
| 17 | T1090.001 | Internal Proxy | Command and Control | Internal Network | Zero-Day / Unknown Exploit | CAPEC-465 | Zero-Day / Unknown Exploit; Watch: Command; Network Traffic; Process; Firewall; Service |
| 18 | T1529 | System Shutdown/Reboot | Impact | Endpoint / EDR | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Process; Sensor Health |
| 19 | T1001.003 | Protocol or Service Impersonation | Command and Control | Server / Workload | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process |
| 20 | T1573 | Encrypted Channel | Command and Control | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; Module; Application Log |
| 21 | T1560.002 | Archive via Library | Collection | Endpoint / EDR | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Process; File; Module |
| 22 | T1074 | Data Staged | Collection | Endpoint / EDR | Server / Workload Blast Radius |  | Server / Workload Blast Radius; Watch: Command; Process; File |
| 23 | T1048 | Exfiltration Over Alternative Protocol | Exfiltration | Endpoint / EDR | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Network Traffic; Process; File |
| 24 | T1048.002 | Exfiltration Over Asymmetric Encrypted Non-C2 Protocol | Exfiltration | Internal Network | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Network Traffic; Process; File |
| 25 | T1499 | Endpoint Denial of Service | Impact | Endpoint / EDR; Server / Workload | Server / Workload Blast Radius | CAPEC-125; CAPEC-131; CAPEC-227 | Server / Workload Blast Radius; Watch: Process; Instance; Sensor Health; Application Log; Network Traffic |
| 26 | T1011.001 | Exfiltration Over Bluetooth | Exfiltration | Endpoint / EDR | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Process; Network Traffic; File |
| 27 | T1561 | Disk Wipe | Impact | Endpoint / EDR | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Drive; Command; Process; User Account; Driver |
| 28 | T1499.002 | Service Exhaustion Flood | Impact | Server / Workload | Destructive / Ransomware | CAPEC-482; CAPEC-489; CAPEC-528 | Destructive / Ransomware; Watch: Process; Network Traffic; Firewall; Sensor Health; Application Log |
| 29 | T1496 | Resource Hijacking | Impact | Endpoint / EDR | Server / Workload Blast Radius |  | Server / Workload Blast Radius; Watch: Network Traffic; Process; Instance; Sensor Health; Application Log |
| 30 | T1052 | Exfiltration Over Physical Medium | Exfiltration | Endpoint / EDR | Destructive / Ransomware | CAPEC-675 | Destructive / Ransomware; Watch: Drive; Command; Process; File |
| 31 | T1011 | Exfiltration Over Other Network Medium | Exfiltration | Internal Network | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Network Traffic; Process; File; Sensor Health |
| 32 | T1053.005 | Scheduled Task | Execution; Persistence; Privilege Escalation | Server / Workload | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; Windows Registry; Scheduled Job; File |
| 33 | T1027 | Obfuscated Files or Information | Stealth | Endpoint / EDR | Telemetry Gap / Evasion | CAPEC-267; CAPEC-542 | Telemetry Gap / Evasion; Watch: Command; Network Traffic; Process; File |
| 34 | T1574.001 | DLL | Stealth; Execution | Endpoint / EDR | Telemetry Gap / Evasion | CAPEC-471 | Telemetry Gap / Evasion; Watch: Process; Windows Registry; Module; File |
| 35 | T1003.001 | LSASS Memory | Credential Access | Endpoint / EDR | Credential Artifact Abuse |  | Credential Artifact Abuse; Watch: Process; User Account; Windows Registry; File |
| 36 | T1036 | Masquerading | Stealth | Endpoint / EDR | Server / Workload Blast Radius | CAPEC-177 | Server / Workload Blast Radius; Watch: Command; Process; File; Service; Image |
| 37 | T1068 | Exploitation for Privilege Escalation | Privilege Escalation | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; Container; Module; Driver |
| 38 | T1552.001 | Credentials In Files | Credential Access | Endpoint / EDR | Credential Artifact Abuse | CAPEC-191; CAPEC-639 | Credential Artifact Abuse; Watch: Command; Process; Network Traffic; File |
| 39 | T1133 | External Remote Services | Persistence; Initial Access | Internal Network; Server / Workload | Credential Artifact Abuse | CAPEC-555 | Credential Artifact Abuse; Watch: Network Traffic; User Account; Application Log |
| 40 | T1040 | Network Sniffing | Credential Access; Discovery | Internal Network | Credential Artifact Abuse | CAPEC-158; CAPEC-65 | Credential Artifact Abuse; Watch: Command; Network Traffic; Process; Service; User Account |
| 41 | T1210 | Exploitation of Remote Services | Lateral Movement | Internal Network; Server / Workload | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; Network Traffic; Module; File; Application Log |
| 42 | T1021.004 | SSH | Lateral Movement | Internal Network | Credential Artifact Abuse |  | Credential Artifact Abuse; Watch: Command; Network Traffic; Process |
| 43 | T1071.002 | File Transfer Protocols | Command and Control | Internal Network; Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Network Traffic; Process |
| 44 | T1025 | Data from Removable Media | Collection | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Drive; Process; File |
| 45 | T1090.002 | External Proxy | Command and Control | Internal Network | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; Firewall |
| 46 | T1001 | Data Obfuscation | Command and Control | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Network Traffic; Process |
| 47 | T1039 | Data from Network Shared Drive | Collection | Internal Network | Destructive / Ransomware | CAPEC-639 | Destructive / Ransomware; Watch: File; Drive; Network Share |
| 48 | T1557.001 | Name Resolution Poisoning and SMB Relay | Credential Access; Collection | Internal Network | Credential Artifact Abuse |  | Credential Artifact Abuse; Watch: Windows Registry; Network Traffic; Service |
| 49 | T1052.001 | Exfiltration over USB | Exfiltration | Endpoint / EDR | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Drive; Process; File |
| 50 | T1568.001 | Fast Flux DNS | Command and Control | Internal Network | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Process; Network Traffic |
| 51 | T1498 | Network Denial of Service | Impact | Internal Network; Server / Workload | Server / Workload Blast Radius |  | Server / Workload Blast Radius; Watch: Process; Network Traffic |
| 52 | T1602.002 | Network Device Configuration Dump | Collection | Internal Network | Credential Artifact Abuse |  | Credential Artifact Abuse; Watch: Command; Network Traffic; User Account |
| 53 | T1568.003 | DNS Calculation | Command and Control | Internal Network | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; Network Traffic |
| 54 | T1498.001 | Direct Network Flood | Impact | Internal Network | Server / Workload Blast Radius | CAPEC-125; CAPEC-482; CAPEC-528; CAPEC-666 | Server / Workload Blast Radius; Watch: Process; Sensor Health; Network Traffic |
| 55 | T1048.001 | Exfiltration Over Symmetric Encrypted Non-C2 Protocol | Exfiltration | Internal Network | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Network Traffic; Process |
| 56 | T1140 | Deobfuscate/Decode Files or Information | Stealth | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Process; File; Command |
| 57 | T1547.001 | Registry Run Keys / Startup Folder | Persistence; Privilege Escalation | Endpoint / EDR | Credential Artifact Abuse | CAPEC-270 | Credential Artifact Abuse; Watch: Process; File; Windows Registry |
| 58 | T1112 | Modify Registry | Defense Impairment; Persistence | Endpoint / EDR | Telemetry Gap / Evasion | CAPEC-203 | Telemetry Gap / Evasion; Watch: Process; Windows Registry |
| 59 | T1021.002 | SMB/Windows Admin Shares | Lateral Movement | Internal Network | Credential Artifact Abuse | CAPEC-561 | Credential Artifact Abuse; Watch: Process; Network Traffic |
| 60 | T1570 | Lateral Tool Transfer | Lateral Movement | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Process; File; Network Share |
| 61 | T1555 | Credentials from Password Stores | Credential Access | Endpoint / EDR | Server / Workload Blast Radius | CAPEC-150 | Server / Workload Blast Radius; Watch: Process; File |
| 62 | T1070 | Indicator Removal | Stealth | Endpoint / EDR | Server / Workload Blast Radius | CAPEC-268 | Server / Workload Blast Radius; Watch: File; Windows Registry; Scheduled Job; Application Log |
| 63 | T1003.002 | Security Account Manager | Credential Access | Endpoint / EDR | Credential Artifact Abuse |  | Credential Artifact Abuse; Watch: File; Process; Windows Registry |
| 64 | T1003 | OS Credential Dumping | Credential Access | Endpoint / EDR | Credential Artifact Abuse | CAPEC-150 | Credential Artifact Abuse; Watch: Process; File |
| 65 | T1222.001 | Windows Permissions | Defense Impairment | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Command; Process; WMI; File |
| 66 | T1021.006 | Windows Remote Management | Lateral Movement | Endpoint / EDR | Credential Artifact Abuse |  | Credential Artifact Abuse; Watch: Process; Service; Network Traffic |
| 67 | T1564 | Hide Artifacts | Stealth | Endpoint / EDR | Living-off-the-Land |  | Living-off-the-Land; Watch: Command; Process; Windows Registry; File; Application Log |
| 68 | T1543 | Create or Modify System Process | Persistence; Privilege Escalation | Endpoint / EDR | Exploit Chain / Multi-Step | CAPEC-550; CAPEC-551 | Exploit Chain / Multi-Step; Watch: Command; Process; Windows Registry; File; Container; Service |
| 69 | T1037.004 | RC Scripts | Persistence; Privilege Escalation | Endpoint / EDR | Living-off-the-Land |  | Living-off-the-Land; Watch: Command; Process; File; Script |
| 70 | T1037 | Boot or Logon Initialization Scripts | Persistence; Privilege Escalation | Endpoint / EDR; Server / Workload | Credential Artifact Abuse | CAPEC-564 | Credential Artifact Abuse; Watch: Process; File; Windows Registry; Scheduled Job; Script; Service |
| 71 | T1021 | Remote Services | Lateral Movement | Internal Network; Server / Workload | Credential Artifact Abuse | CAPEC-555 | Credential Artifact Abuse; Watch: Command; Process; Network Traffic |
| 72 | T1547 | Boot or Logon Autostart Execution | Persistence; Privilege Escalation | Server / Workload | Living-off-the-Land | CAPEC-564 | Living-off-the-Land; Watch: Process; File; Windows Registry; Service |
| 73 | T1037.001 | Logon Script (Windows) | Persistence; Privilege Escalation | Endpoint / EDR; Server / Workload | Credential Artifact Abuse |  | Credential Artifact Abuse; Watch: Process; Script; File |
| 74 | T1547.012 | Print Processors | Persistence; Privilege Escalation | Endpoint / EDR | Living-off-the-Land |  | Living-off-the-Land; Watch: Process; File; Windows Registry; Module |
| 75 | T1547.008 | LSASS Driver | Persistence; Privilege Escalation | Endpoint / EDR | Living-off-the-Land |  | Living-off-the-Land; Watch: File; Windows Registry; Module; Driver |
| 76 | T1053 | Scheduled Task/Job | Execution; Persistence; Privilege Escalation | Server / Workload | Exploit Chain / Multi-Step |  | Exploit Chain / Multi-Step; Watch: Command; Process; File; Scheduled Job |
| 77 | T1543.005 | Container Service | Persistence; Privilege Escalation | Server / Workload | Server / Workload Blast Radius |  | Server / Workload Blast Radius; Watch: Process; Service; Container; Pod |
| 78 | T1134.002 | Create Process with Token | Stealth; Privilege Escalation | Endpoint / EDR | Credential Artifact Abuse | CAPEC-196 | Credential Artifact Abuse; Watch: Process |
| 79 | T1070.003 | Clear Command History | Stealth | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Command; Process; File |
| 80 | T1690 | Prevent Command History Logging | Defense Impairment | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Command; Process |
| 81 | T1552.002 | Credentials in Registry | Credential Access | Endpoint / EDR | Credential Artifact Abuse | CAPEC-647 | Credential Artifact Abuse; Watch: Process; Windows Registry |
| 82 | T1098.004 | SSH Authorized Keys | Persistence; Privilege Escalation | Internal Network | Credential Artifact Abuse |  | Credential Artifact Abuse; Watch: Command; Process; File |
| 83 | T1055.013 | Process Doppelgänging | Stealth; Privilege Escalation | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; File |
| 84 | T1574.010 | Services File Permissions Weakness | Stealth; Execution | Endpoint / EDR; Server / Workload | Zero-Day / Unknown Exploit | CAPEC-1; CAPEC-17; CAPEC-180 | Zero-Day / Unknown Exploit; Watch: File; Process; Service |
| 85 | T1546.013 | PowerShell Profile | Privilege Escalation; Persistence | Endpoint / EDR | Credential Artifact Abuse |  | Credential Artifact Abuse; Watch: Command; Process; File |
| 86 | T1546.009 | AppCert DLLs | Privilege Escalation; Persistence | Endpoint / EDR | Credential Artifact Abuse |  | Credential Artifact Abuse; Watch: Process; Windows Registry; Module |
| 87 | T1053.007 | Container Orchestration Job | Execution; Persistence; Privilege Escalation | Server / Workload | Exploit Chain / Multi-Step |  | Exploit Chain / Multi-Step; Watch: Network Traffic; Scheduled Job; Container |
| 88 | T1543.003 | Windows Service | Persistence; Privilege Escalation | Server / Workload | Zero-Day / Unknown Exploit | CAPEC-478 | Zero-Day / Unknown Exploit; Watch: Windows Registry; Process; Service; Driver |
| 89 | T1218.011 | Rundll32 | Stealth | Endpoint / EDR | Living-off-the-Land |  | Living-off-the-Land; Watch: Process; File; Network Traffic; Module |
| 90 | T1020 | Automated Exfiltration | Exfiltration | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; Network Traffic; Scheduled Job |
| 91 | T1092 | Communication Through Removable Media | Command and Control | Endpoint / EDR | Zero-Day / Unknown Exploit | CAPEC-457 | Zero-Day / Unknown Exploit; Watch: Drive; Process; File |
| 92 | T1057 | Process Discovery | Discovery | Endpoint / EDR | Living-off-the-Land | CAPEC-573 | Living-off-the-Land; Watch: Process; Command; File |
| 93 | T1016 | System Network Configuration Discovery | Discovery | Internal Network | Living-off-the-Land | CAPEC-309 | Living-off-the-Land; Watch: Command; Process |
| 94 | T1049 | System Network Connections Discovery | Discovery | Internal Network | Server / Workload Blast Radius | CAPEC-309 | Server / Workload Blast Radius; Watch: Command; Process; Network Traffic |
| 95 | T1036.004 | Masquerade Task or Service | Stealth | Endpoint / EDR; Server / Workload | Living-off-the-Land | CAPEC-504 | Living-off-the-Land; Watch: Scheduled Job; Process; Service |
| 96 | T1055 | Process Injection | Stealth; Privilege Escalation | Endpoint / EDR | Telemetry Gap / Evasion | CAPEC-251; CAPEC-660 | Telemetry Gap / Evasion; Watch: Process; Module; File |
| 97 | T1046 | Network Service Discovery | Discovery | Internal Network; Server / Workload | Zero-Day / Unknown Exploit | CAPEC-300 | Zero-Day / Unknown Exploit; Watch: Process; Network Traffic |
| 98 | T1027.010 | Command Obfuscation | Stealth | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Process |
| 99 | T1686.003 | Windows Host Firewall | Defense Impairment | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Process; Network Traffic; Windows Registry; Service |
| 100 | T1543.002 | Systemd Service | Persistence; Privilege Escalation | Server / Workload | Exploit Chain / Multi-Step |  | Exploit Chain / Multi-Step; Watch: Command; Process; File; Service |
| 101 | T1070.005 | Network Share Connection Removal | Stealth | Internal Network | Credential Artifact Abuse |  | Credential Artifact Abuse; Watch: Command; Process; Network Traffic |
| 102 | T1610 | Deploy Container | Execution | Server / Workload | Server / Workload Blast Radius |  | Server / Workload Blast Radius; Watch: Container; Process; Network Traffic; Application Log |
| 103 | T1686.002 | Network Device Firewall | Defense Impairment | Internal Network | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Firewall; Command; Network Traffic |
| 104 | T1685.001 | Disable or Modify Windows Event Log | Defense Impairment | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Process; Windows Registry; Service; Application Log |
| 105 | T1070.007 | Clear Network Connection History and Configurations | Stealth | Internal Network | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Command; Network Traffic; Process; Windows Registry; File; Firewall |
| 106 | T1685.004 | Disable or Modify Linux Audit System Log | Defense Impairment | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Command; File; Service; Process |
| 107 | T1505.005 | Terminal Services DLL | Persistence | Endpoint / EDR; Server / Workload | Credential Artifact Abuse | CAPEC-558; CAPEC-640; CAPEC-642 | Credential Artifact Abuse; Watch: Process; File; Windows Registry; Module |
| 108 | T1216 | System Script Proxy Execution | Stealth | Internal Network; Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Command; Process; Module; File |
| 109 | T1127 | Trusted Developer Utilities Proxy Execution | Stealth; Execution | Internal Network | Zero-Day / Unknown Exploit | CAPEC-670 | Zero-Day / Unknown Exploit; Watch: Process; Network Traffic; Module; File |
| 110 | T1055.012 | Process Hollowing | Stealth; Privilege Escalation | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Process |
| 111 | T1685.005 | Clear Windows Event Logs | Defense Impairment | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Process; File; Application Log |
| 112 | T1059 | Command and Scripting Interpreter | Execution | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Process; User Account |
| 113 | T1091 | Replication Through Removable Media | Lateral Movement; Initial Access | Endpoint / EDR | Zero-Day / Unknown Exploit | CAPEC-457 | Zero-Day / Unknown Exploit; Watch: Drive; Process; File |
| 114 | T1546.003 | Windows Management Instrumentation Event Subscription | Privilege Escalation; Persistence | Endpoint / EDR | Living-off-the-Land |  | Living-off-the-Land; Watch: Process; WMI; Module |
| 115 | T1222.002 | Linux and Mac Permissions | Defense Impairment | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Command; File; Process |
| 116 | T1547.004 | Winlogon Helper DLL | Persistence; Privilege Escalation | Endpoint / EDR | Living-off-the-Land | CAPEC-579 | Living-off-the-Land; Watch: Process; Windows Registry; Module |
| 117 | T1685.006 | Clear Linux or Mac System Logs | Defense Impairment | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Process; File |
| 118 | T1564.011 | Ignore Process Interrupts | Stealth | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Command; Process |
| 119 | T1609 | Container Administration Command | Execution | Endpoint / EDR; Server / Workload | Server / Workload Blast Radius |  | Server / Workload Blast Radius; Watch: Command; Process |
| 120 | T1546.010 | AppInit DLLs | Privilege Escalation; Persistence | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; Windows Registry; Module |
| 121 | T1202 | Indirect Command Execution | Stealth | Endpoint / EDR | Living-off-the-Land |  | Living-off-the-Land; Watch: Process; File; Network Traffic |
| 122 | T1613 | Container and Resource Discovery | Discovery | Server / Workload | Server / Workload Blast Radius |  | Server / Workload Blast Radius; Watch: Container; Pod |
| 123 | T1220 | XSL Script Processing | Stealth | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Process; Module |
| 124 | T1059.008 | Network Device CLI | Execution | Internal Network | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Network Traffic; User Account |
| 125 | T1218 | System Binary Proxy Execution | Stealth | Internal Network | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Process; Network Traffic; Module |
| 126 | T1546.007 | Netsh Helper DLL | Privilege Escalation; Persistence | Endpoint / EDR | Living-off-the-Land |  | Living-off-the-Land; Watch: Process; Windows Registry; Module |
| 127 | T1574.011 | Services Registry Permissions Weakness | Stealth; Execution | Endpoint / EDR; Server / Workload | Zero-Day / Unknown Exploit | CAPEC-478 | Zero-Day / Unknown Exploit; Watch: Process; Windows Registry; Service |
| 128 | T1135 | Network Share Discovery | Discovery | Internal Network | Zero-Day / Unknown Exploit | CAPEC-643 | Zero-Day / Unknown Exploit; Watch: Command; Process; Network Traffic; Named Pipe |
| 129 | T1569.002 | Service Execution | Execution | Server / Workload | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Windows Registry; Process; Network Traffic; Service |
| 130 | T1059.007 | JavaScript | Execution | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Process; Script; Module |
| 131 | T1036.010 | Masquerade Account Name | Stealth | Endpoint / EDR | Server / Workload Blast Radius |  | Server / Workload Blast Radius; Watch: User Account |
| 132 | T1098.006 | Additional Container Cluster Roles | Persistence; Privilege Escalation | Server / Workload | Credential Artifact Abuse |  | Credential Artifact Abuse; Watch: User Account |
| 133 | T1059.003 | Windows Command Shell | Execution | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; Script; Module |
| 134 | T1059.001 | PowerShell | Execution | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Process; Module |
| 135 | T1047 | Windows Management Instrumentation | Execution | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; Network Traffic; WMI |
| 136 | T1012 | Query Registry | Discovery | Endpoint / EDR | Living-off-the-Land | CAPEC-647 | Living-off-the-Land; Watch: Command; Process; Windows Registry |
| 137 | T1007 | System Service Discovery | Discovery | Server / Workload | Zero-Day / Unknown Exploit | CAPEC-574 | Zero-Day / Unknown Exploit; Watch: Command; Process |
| 138 | T1566.003 | Spearphishing via Service | Initial Access | Server / Workload | Zero-Day / Unknown Exploit | CAPEC-163 | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; File; Application Log |
| 139 | T1559 | Inter-Process Communication | Execution | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; Script; File; Named Pipe |
| 140 | T1652 | Device Driver Discovery | Discovery | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Process; Windows Registry; File |
| 141 | T1569 | System Services | Execution | Server / Workload | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Windows Registry; Process; Service; File |
| 142 | T1669 | Wi-Fi Networks | Initial Access | Internal Network | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Network Traffic; Firewall; User Account |
| 143 | T1559.003 | XPC Services | Execution | Server / Workload | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; Named Pipe |
| 144 | T1675 | ESXi Administration Command | Execution | Endpoint / EDR; Server / Workload | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Application Log |
| 145 | T1564.010 | Process Argument Spoofing | Stealth | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Process |
| 146 | T1036.009 | Break Process Trees | Stealth | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Process |
| 147 | T1599 | Network Boundary Bridging | Defense Impairment | Internal Network | Telemetry Gap / Evasion | CAPEC-700 | Telemetry Gap / Evasion; Watch: Network Traffic |
| 148 | T1036.011 | Overwrite Process Arguments | Stealth | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Process |
| 149 | T1599.001 | Network Address Translation Traversal | Defense Impairment | Internal Network | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Network Traffic |
| 150 | T1036.008 | Masquerade File Type | Stealth | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Process; File |
| 151 | T1027.005 | Indicator Removal from Tools | Stealth | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; File; Application Log |
| 152 | T1059.002 | AppleScript | Execution | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process |
| 153 | T1422 | System Network Configuration Discovery | Discovery | Internal Network | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 154 | T1406 | Obfuscated Files or Information | Defense Evasion | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 155 | T1646 | Exfiltration Over C2 Channel | Exfiltration | Internal Network | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 156 | T1404 | Exploitation for Privilege Escalation | Privilege Escalation | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit |
| 157 | T1544 | Ingress Tool Transfer | Command and Control | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 158 | T1532 | Archive Collected Data | Collection | Endpoint / EDR | Destructive / Ransomware |  | Destructive / Ransomware |
| 159 | T1424 | Process Discovery | Discovery | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 160 | T1509 | Non-Standard Port | Command and Control | Internal Network | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 161 | T1421 | System Network Connections Discovery | Discovery | Internal Network | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 162 | T1655 | Masquerading | Defense Evasion | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 163 | T1642 | Endpoint Denial of Service | Impact | Endpoint / EDR; Server / Workload | Destructive / Ransomware |  | Destructive / Ransomware |
| 164 | T1603 | Scheduled Task/Job | Execution; Persistence | Server / Workload | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 165 | T0881 | Service Stop | Inhibit Response Function | Server / Workload | Rare but High Impact |  | Rare but High Impact |
| 166 | T0867 | Lateral Tool Transfer | Lateral Movement | Endpoint / EDR | Rare but High Impact |  | Rare but High Impact |
| 167 | T1662 | Data Destruction | Impact | Endpoint / EDR | Destructive / Ransomware |  | Destructive / Ransomware |
| 168 | T1398 | Boot or Logon Initialization Scripts | Persistence | Endpoint / EDR; Server / Workload | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 169 | T0866 | Exploitation of Remote Services | Initial Access; Lateral Movement | Internal Network; Server / Workload | Rare but High Impact |  | Rare but High Impact |
| 170 | T0853 | Scripting | Execution | Endpoint / EDR | Rare but High Impact |  | Rare but High Impact |
| 171 | T0849 | Masquerading | Evasion | Endpoint / EDR | Rare but High Impact |  | Rare but High Impact |
| 172 | T0814 | Denial of Service | Inhibit Response Function | Server / Workload | Rare but High Impact |  | Rare but High Impact |
| 173 | T0809 | Data Destruction | Inhibit Response Function | Endpoint / EDR | Rare but High Impact |  | Rare but High Impact |
| 174 | T0807 | Command-Line Interface | Execution | Endpoint / EDR | Rare but High Impact |  | Rare but High Impact |
| 175 | T0801 | Monitor Process State | Collection | Endpoint / EDR | Rare but High Impact |  | Rare but High Impact |
| 176 | T1692.001 | Command Message | Evasion; Impair Process Control | Endpoint / EDR | Rare but High Impact |  | Rare but High Impact |
| 177 | T1639.001 | Exfiltration Over Unencrypted Non-C2 Protocol | Exfiltration | Internal Network | Destructive / Ransomware |  | Destructive / Ransomware |
| 178 | T1471 | Data Encrypted for Impact | Impact | Endpoint / EDR | Destructive / Ransomware |  | Destructive / Ransomware |
| 179 | T0886 | Remote Services | Initial Access; Lateral Movement | Internal Network; Server / Workload | Rare but High Impact |  | Rare but High Impact |
| 180 | T0884 | Connection Proxy | Command and Control | Internal Network | Rare but High Impact |  | Rare but High Impact |
| 181 | T0842 | Network Sniffing | Discovery | Internal Network | Rare but High Impact |  | Rare but High Impact |
| 182 | T1631 | Process Injection | Defense Evasion; Privilege Escalation | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 183 | T1630 | Indicator Removal on Host | Defense Evasion | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 184 | T1623 | Command and Scripting Interpreter | Execution | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 185 | T1604 | Proxy Through Victim | Defense Evasion | Internal Network | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 186 | T1521 | Encrypted Channel | Command and Control | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 187 | T1458 | Replication Through Removable Media | Initial Access; Lateral Movement | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 188 | T1428 | Exploitation of Remote Services | Lateral Movement | Internal Network; Server / Workload | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 189 | T0890 | Exploitation for Privilege Escalation | Privilege Escalation | Endpoint / EDR | Rare but High Impact |  | Rare but High Impact |
| 190 | T0872 | Indicator Removal on Host | Evasion | Endpoint / EDR | Rare but High Impact |  | Rare but High Impact |
| 191 | T0847 | Replication Through Removable Media | Initial Access | Endpoint / EDR | Rare but High Impact |  | Rare but High Impact |
| 192 | T0840 | Network Connection Enumeration | Discovery | Internal Network | Rare but High Impact |  | Rare but High Impact |
| 193 | T1691.001 | Command Message | Inhibit Response Function | Endpoint / EDR | Rare but High Impact |  | Rare but High Impact |
| 194 | T1639 | Exfiltration Over Alternative Protocol | Exfiltration | Endpoint / EDR | Destructive / Ransomware |  | Destructive / Ransomware |
| 195 | T1464 | Network Denial of Service | Impact | Internal Network; Server / Workload | Destructive / Ransomware |  | Destructive / Ransomware |
| 196 | T1423 | Network Service Scanning | Discovery | Internal Network; Server / Workload | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 197 | T0822 | External Remote Services | Initial Access | Internal Network; Server / Workload | Rare but High Impact |  | Rare but High Impact |
| 198 | T1628 | Hide Artifacts | Defense Evasion | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 199 | T1444 | Masquerade as Legitimate Application | Initial Access; Defense Evasion | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 200 | T1430.001 | Remote Device Management Services | Collection; Discovery | Server / Workload | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 201 | T0894 | System Binary Proxy Execution | Evasion | Internal Network | Rare but High Impact |  | Rare but High Impact |
| 202 | T0841 | Network Service Scanning | Discovery | Internal Network; Server / Workload | Rare but High Impact |  | Rare but High Impact |

## CAPEC Attack Pattern Matrix

| rank | capec_id | attack_pattern | surface | edge_case | related_attack | watch_focus |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | CAPEC-150 | Collect Data from Common Resource Locations | Endpoint / EDR; Internal Network | Credential Artifact Abuse | T1003; T1119; T1213; T1530; T1555; T1602 | Credential Artifact Abuse; CWE: CWE-1239; CWE-1258; CWE-1266; CWE-1272; CWE-1323; CWE-1330; CWE-552 |
| 2 | CAPEC-639 | Probe System Files | Internal Network; Endpoint / EDR | Destructive / Ransomware | T1039; T1552.001; T1552.003; T1552.004; T1552.006 | Destructive / Ransomware; CWE: CWE-552 |
| 3 | CAPEC-636 | Hiding Malicious Data or Code within Files | Endpoint / EDR; Internal Network | Telemetry Gap / Evasion | T1001.002; T1027.003; T1027.004; T1218.001; T1221 | Telemetry Gap / Evasion; CWE: CWE-506 |
| 4 | CAPEC-555 | Remote Services with Stolen Credentials | Internal Network; Server / Workload; Endpoint / EDR | Credential Artifact Abuse | T1021; T1114.002; T1133 | Credential Artifact Abuse; CWE: CWE-262; CWE-263; CWE-294; CWE-308; CWE-309; CWE-521; CWE-522 |
| 5 | CAPEC-647 | Collect Data from Registries | Endpoint / EDR | Living-off-the-Land | T1005; T1012; T1552.002 | Living-off-the-Land; CWE: CWE-285 |
| 6 | CAPEC-482 | TCP Flood | Internal Network; Server / Workload; Endpoint / EDR | Server / Workload Blast Radius | T1498.001; T1499.001; T1499.002 | Server / Workload Blast Radius; CWE: CWE-770 |
| 7 | CAPEC-634 | Probe Audio and Video Peripherals | Endpoint / EDR | Zero-Day / Unknown Exploit | T1123; T1125 | Zero-Day / Unknown Exploit; CWE: CWE-267 |
| 8 | CAPEC-545 | Pull Data from System Resources | Endpoint / EDR | Server / Workload Blast Radius | T1005; T1555.001 | Server / Workload Blast Radius; CWE: CWE-1239; CWE-1243; CWE-1258; CWE-1266; CWE-1272; CWE-1278; CWE-1323; CWE-1330 |
| 9 | CAPEC-125 | Flooding | Internal Network; Server / Workload; Endpoint / EDR | Server / Workload Blast Radius | T1498.001; T1499 | Server / Workload Blast Radius; CWE: CWE-404; CWE-770 |
| 10 | CAPEC-94 | Adversary in the Middle (AiTM) | Internal Network | Credential Artifact Abuse | T1557 | Credential Artifact Abuse; CWE: CWE-287; CWE-290; CWE-294; CWE-300; CWE-593 |
| 11 | CAPEC-675 | Retrieve Data from Decommissioned Devices | Endpoint / EDR | Destructive / Ransomware | T1052 | Destructive / Ransomware; CWE: CWE-1266 |
| 12 | CAPEC-490 | Amplification | Internal Network; Server / Workload | Server / Workload Blast Radius | T1498.002 | Server / Workload Blast Radius; CWE: CWE-770 |
| 13 | CAPEC-489 | SSL Flood | Endpoint / EDR; Server / Workload | Server / Workload Blast Radius | T1499.002 | Server / Workload Blast Radius; CWE: CWE-770 |
| 14 | CAPEC-465 | Transparent Proxy Abuse | Internal Network | Zero-Day / Unknown Exploit | T1090.001 | Zero-Day / Unknown Exploit; CWE: CWE-441 |
| 15 | CAPEC-25 | Forced Deadlock | Endpoint / EDR; Server / Workload | Server / Workload Blast Radius | T1499.004 | Server / Workload Blast Radius; CWE: CWE-1322; CWE-412; CWE-567; CWE-662; CWE-667; CWE-833 |
| 16 | CAPEC-227 | Sustained Client Engagement | Endpoint / EDR; Server / Workload | Server / Workload Blast Radius | T1499 | Server / Workload Blast Radius; CWE: CWE-400 |
| 17 | CAPEC-148 | Content Spoofing | Internal Network; Endpoint / EDR | Server / Workload Blast Radius | T1491 | Server / Workload Blast Radius; CWE: CWE-345 |
| 18 | CAPEC-131 | Resource Leak Exposure | Endpoint / EDR; Server / Workload | Server / Workload Blast Radius | T1499 | Server / Workload Blast Radius; CWE: CWE-404 |
| 19 | CAPEC-130 | Excessive Allocation | Endpoint / EDR; Server / Workload | Server / Workload Blast Radius | T1499.003 | Server / Workload Blast Radius; CWE: CWE-1325; CWE-404; CWE-770 |
| 20 | CAPEC-75 | Manipulating Writeable Configuration Files | Endpoint / EDR | Rare but High Impact |  | Rare but High Impact; CWE: CWE-346; CWE-349; CWE-353; CWE-354; CWE-77; CWE-99 |
| 21 | CAPEC-44 | Overflow Binary Resource File | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-119; CWE-120; CWE-697 |
| 22 | CAPEC-163 | Spear Phishing | Server / Workload | Zero-Day / Unknown Exploit | T1534; T1566.001; T1566.002; T1566.003; T1598.001; T1598.002; T1598.003 | Zero-Day / Unknown Exploit; CWE: CWE-451 |
| 23 | CAPEC-640 | Inclusion of Code in Existing Process | Endpoint / EDR; Server / Workload | Credential Artifact Abuse | T1505.005; T1574.006; T1574.013; T1620 | Credential Artifact Abuse; CWE: CWE-114; CWE-829 |
| 24 | CAPEC-642 | Replace Binaries | Endpoint / EDR; Server / Workload | Credential Artifact Abuse | T1505.005; T1554; T1574.005 | Credential Artifact Abuse; CWE: CWE-732 |
| 25 | CAPEC-471 | Search Order Hijacking | Endpoint / EDR | Telemetry Gap / Evasion | T1574.001; T1574.004; T1574.008 | Telemetry Gap / Evasion; CWE: CWE-427 |
| 26 | CAPEC-21 | Exploitation of Trusted Identifiers | Endpoint / EDR | Credential Artifact Abuse | T1134; T1528; T1539 | Credential Artifact Abuse; CWE: CWE-290; CWE-302; CWE-346; CWE-384; CWE-539; CWE-6; CWE-602; CWE-642; CWE-664 |
| 27 | CAPEC-542 | Targeted Malware | Endpoint / EDR | Zero-Day / Unknown Exploit | T1027; T1587.001 | Zero-Day / Unknown Exploit |
| 28 | CAPEC-478 | Modification of Windows Service Configuration | Endpoint / EDR; Server / Workload | Zero-Day / Unknown Exploit | T1543.003; T1574.011 | Zero-Day / Unknown Exploit; CWE: CWE-284 |
| 29 | CAPEC-158 | Sniffing Network Traffic | Internal Network | Credential Artifact Abuse | T1040; T1111 | Credential Artifact Abuse; CWE: CWE-311 |
| 30 | CAPEC-65 | Sniff Application Code | Internal Network | Credential Artifact Abuse | T1040 | Credential Artifact Abuse; CWE: CWE-311; CWE-318; CWE-319; CWE-693 |
| 31 | CAPEC-616 | Establish Rogue Location | Endpoint / EDR | Server / Workload Blast Radius | T1036.005 | Server / Workload Blast Radius; CWE: CWE-200 |
| 32 | CAPEC-267 | Leverage Alternate Encoding | Endpoint / EDR | Zero-Day / Unknown Exploit | T1027 | Zero-Day / Unknown Exploit; CWE: CWE-172; CWE-173; CWE-180; CWE-181; CWE-20; CWE-692; CWE-697; CWE-73; CWE-74 |
| 33 | CAPEC-191 | Read Sensitive Constants Within an Executable | Endpoint / EDR | Credential Artifact Abuse | T1552.001 | Credential Artifact Abuse; CWE: CWE-798 |
| 34 | CAPEC-177 | Create files with the same name as files protected with a higher classification | Endpoint / EDR; Server / Workload | Telemetry Gap / Evasion | T1036 | Telemetry Gap / Evasion; CWE: CWE-706 |
| 35 | CAPEC-666 | BlueSmacking | Internal Network; Server / Workload; Endpoint / EDR | Server / Workload Blast Radius | T1498.001; T1499.001 | Server / Workload Blast Radius; CWE: CWE-404 |
| 36 | CAPEC-697 | DHCP Spoofing | Internal Network; Server / Workload | Credential Artifact Abuse | T1557.003 | Credential Artifact Abuse; CWE: CWE-923 |
| 37 | CAPEC-481 | Contradictory Destinations in Traffic Routing Schemes | Internal Network | Zero-Day / Unknown Exploit | T1090.004 | Zero-Day / Unknown Exploit; CWE: CWE-923 |
| 38 | CAPEC-2 | Inducing Account Lockout | Server / Workload | Credential Artifact Abuse | T1531 | Credential Artifact Abuse; CWE: CWE-645 |
| 39 | CAPEC-175 | Code Inclusion | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-829 |
| 40 | CAPEC-564 | Run Software at Logon | Endpoint / EDR; Server / Workload; Internal Network | Living-off-the-Land | T1037; T1543.001; T1543.004; T1547 | Living-off-the-Land; CWE: CWE-284 |
| 41 | CAPEC-665 | Exploitation of Thunderbolt Protection Flaws | Endpoint / EDR; Internal Network | Credential Artifact Abuse | T1211; T1542.002; T1556 | Credential Artifact Abuse; CWE: CWE-1188; CWE-288; CWE-345; CWE-353; CWE-862 |
| 42 | CAPEC-552 | Install Rootkit | Server / Workload | Living-off-the-Land | T1014; T1542.003; T1547.006 | Living-off-the-Land; CWE: CWE-284 |
| 43 | CAPEC-35 | Leverage Executable Code in Non-Executable Files | Endpoint / EDR | Telemetry Gap / Evasion | T1027.006; T1027.009; T1564.009 | Telemetry Gap / Evasion; CWE: CWE-270; CWE-272; CWE-282; CWE-59; CWE-94; CWE-95; CWE-96; CWE-97 |
| 44 | CAPEC-19 | Embedding Scripts within Scripts | Endpoint / EDR | Telemetry Gap / Evasion | T1027.009; T1546.004; T1546.016 | Telemetry Gap / Evasion; CWE: CWE-284 |
| 45 | CAPEC-670 | Software Development Tools Maliciously Altered | Internal Network | Zero-Day / Unknown Exploit | T1127; T1195.001 | Zero-Day / Unknown Exploit |
| 46 | CAPEC-558 | Replace Trusted Executable | Endpoint / EDR; Server / Workload | Credential Artifact Abuse | T1505.005; T1546.008 | Credential Artifact Abuse; CWE: CWE-284 |
| 47 | CAPEC-473 | Signature Spoof | Endpoint / EDR | Server / Workload Blast Radius | T1036.001; T1553.002 | Server / Workload Blast Radius; CWE: CWE-20; CWE-290; CWE-327 |
| 48 | CAPEC-270 | Modification of Registry Run Keys | Server / Workload; Endpoint / EDR | Living-off-the-Land | T1547.001; T1547.014 | Living-off-the-Land; CWE: CWE-15 |
| 49 | CAPEC-203 | Manipulate Registry Information | Endpoint / EDR | Telemetry Gap / Evasion | T1112; T1647 | Telemetry Gap / Evasion; CWE: CWE-15 |
| 50 | CAPEC-660 | Root/Jailbreak Detection Evasion via Hooking | Endpoint / EDR | Telemetry Gap / Evasion | T1055 | Telemetry Gap / Evasion; CWE: CWE-829 |
| 51 | CAPEC-655 | Avoid Security Tool Identification by Adding Data | Endpoint / EDR | Telemetry Gap / Evasion | T1027.001 | Telemetry Gap / Evasion |
| 52 | CAPEC-651 | Eavesdropping | Internal Network | Credential Artifact Abuse | T1111 | Credential Artifact Abuse; CWE: CWE-200 |
| 53 | CAPEC-633 | Token Impersonation | Endpoint / EDR | Credential Artifact Abuse | T1134 | Credential Artifact Abuse; CWE: CWE-1270; CWE-287 |
| 54 | CAPEC-578 | Disable Security Software | Endpoint / EDR | Credential Artifact Abuse | T1556.006 | Credential Artifact Abuse; CWE: CWE-284 |
| 55 | CAPEC-572 | Artificially Inflate File Sizes | Endpoint / EDR | Telemetry Gap / Evasion | T1027.001 | Telemetry Gap / Evasion |
| 56 | CAPEC-561 | Windows Admin Shares with Stolen Credentials | Internal Network; Server / Workload | Credential Artifact Abuse | T1021.002 | Credential Artifact Abuse; CWE: CWE-262; CWE-263; CWE-294; CWE-308; CWE-309; CWE-521; CWE-522 |
| 57 | CAPEC-560 | Use of Known Domain Credentials | Server / Workload | Credential Artifact Abuse | T1078 | Credential Artifact Abuse; CWE: CWE-1273; CWE-262; CWE-263; CWE-307; CWE-308; CWE-309; CWE-522; CWE-654 |
| 58 | CAPEC-551 | Modify Existing Service | Endpoint / EDR; Server / Workload | Exploit Chain / Multi-Step | T1543 | Exploit Chain / Multi-Step; CWE: CWE-284; CWE-522 |
| 59 | CAPEC-550 | Install New Service | Endpoint / EDR; Server / Workload | Exploit Chain / Multi-Step | T1543 | Exploit Chain / Multi-Step; CWE: CWE-284 |
| 60 | CAPEC-480 | Escaping Virtualization | Server / Workload | Rare but High Impact | T1611 | Rare but High Impact; CWE: CWE-693 |
| 61 | CAPEC-448 | Embed Virus into DLL | Endpoint / EDR | Telemetry Gap / Evasion | T1027.009 | Telemetry Gap / Evasion; CWE: CWE-506 |
| 62 | CAPEC-268 | Audit Log Manipulation | Endpoint / EDR; Internal Network | Telemetry Gap / Evasion | T1070 | Telemetry Gap / Evasion; CWE: CWE-117 |
| 63 | CAPEC-251 | Local Code Inclusion | Endpoint / EDR | Telemetry Gap / Evasion | T1055 | Telemetry Gap / Evasion; CWE: CWE-829 |
| 64 | CAPEC-132 | Symlink Attack | Server / Workload | Living-off-the-Land | T1547.009 | Living-off-the-Land; CWE: CWE-59 |
| 65 | CAPEC-93 | Log Injection-Tampering-Forging | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-117; CWE-150; CWE-75 |
| 66 | CAPEC-79 | Using Slashes in Alternate Encoding | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-173; CWE-180; CWE-181; CWE-185; CWE-20; CWE-200; CWE-22; CWE-697; CWE-707; CWE-73; CWE-74 |
| 67 | CAPEC-653 | Use of Known Operating System Credentials | Server / Workload | Credential Artifact Abuse |  | Credential Artifact Abuse; CWE: CWE-262; CWE-263; CWE-307; CWE-308; CWE-309; CWE-522; CWE-654 |
| 68 | CAPEC-6 | Argument Injection | Server / Workload | Rare but High Impact |  | Rare but High Impact; CWE: CWE-146; CWE-184; CWE-185; CWE-697; CWE-74; CWE-78 |
| 69 | CAPEC-46 | Overflow Variables and Tags | Endpoint / EDR | Rare but High Impact |  | Rare but High Impact; CWE: CWE-118; CWE-119; CWE-120; CWE-20; CWE-680; CWE-697; CWE-733; CWE-74 |
| 70 | CAPEC-45 | Buffer Overflow via Symbolic Links | Endpoint / EDR | Rare but High Impact |  | Rare but High Impact; CWE: CWE-118; CWE-119; CWE-120; CWE-20; CWE-285; CWE-302; CWE-680; CWE-697; CWE-74 |
| 71 | CAPEC-29 | Leveraging Time-of-Check and Time-of-Use (TOCTOU) Race Conditions | Endpoint / EDR | Rare but High Impact |  | Rare but High Impact; CWE: CWE-362; CWE-366; CWE-367; CWE-368; CWE-370; CWE-662; CWE-663; CWE-665; CWE-691 |
| 72 | CAPEC-26 | Leveraging Race Conditions | Endpoint / EDR | Rare but High Impact |  | Rare but High Impact; CWE: CWE-1223; CWE-1254; CWE-1298; CWE-362; CWE-363; CWE-366; CWE-368; CWE-370; CWE-662; CWE-665; CWE-667; CWE-689 |
| 73 | CAPEC-242 | Code Injection | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-94 |
| 74 | CAPEC-229 | Serialized Data Parameter Blowup | Server / Workload; Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-770 |
| 75 | CAPEC-201 | Serialized Data External Linking | Endpoint / EDR | Rare but High Impact |  | Rare but High Impact; CWE: CWE-829 |
| 76 | CAPEC-15 | Command Delimiters | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-138; CWE-140; CWE-146; CWE-154; CWE-157; CWE-184; CWE-185; CWE-697; CWE-77; CWE-78; CWE-93 |
| 77 | CAPEC-275 | DNS Rebinding | Internal Network; Server / Workload | Rare but High Impact |  | Rare but High Impact; CWE: CWE-350 |
| 78 | CAPEC-23 | File Content Injection | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-20 |
| 79 | CAPEC-126 | Path Traversal | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-22 |
| 80 | CAPEC-38 | Leveraging/Manipulating Configuration File Search Paths | Endpoint / EDR | Rare but High Impact | T1574.007; T1574.009 | Rare but High Impact; CWE: CWE-426; CWE-427 |
| 81 | CAPEC-17 | Using Malicious Files | Endpoint / EDR; Server / Workload | Zero-Day / Unknown Exploit | T1574.005; T1574.010 | Zero-Day / Unknown Exploit; CWE: CWE-270; CWE-272; CWE-282; CWE-285; CWE-59; CWE-693; CWE-732 |
| 82 | CAPEC-649 | Adding a Space to a File Extension | Endpoint / EDR | Server / Workload Blast Radius | T1036.006 | Server / Workload Blast Radius; CWE: CWE-46 |
| 83 | CAPEC-638 | Altered Component Firmware | Endpoint / EDR | Zero-Day / Unknown Exploit | T1542.002 | Zero-Day / Unknown Exploit |
| 84 | CAPEC-579 | Replace Winlogon Helper DLL | Server / Workload; Endpoint / EDR | Living-off-the-Land | T1547.004 | Living-off-the-Land; CWE: CWE-15 |
| 85 | CAPEC-562 | Modify Shared File | Endpoint / EDR | Server / Workload Blast Radius | T1080 | Server / Workload Blast Radius; CWE: CWE-284 |
| 86 | CAPEC-556 | Replace File Extension Handlers | Endpoint / EDR | Exploit Chain / Multi-Step | T1546.001 | Exploit Chain / Multi-Step; CWE: CWE-284 |
| 87 | CAPEC-30 | Hijacking a Privileged Thread of Execution | Endpoint / EDR | Telemetry Gap / Evasion | T1055.003 | Telemetry Gap / Evasion; CWE: CWE-270 |
| 88 | CAPEC-180 | Exploiting Incorrectly Configured Access Control Security Levels | Endpoint / EDR; Server / Workload | Zero-Day / Unknown Exploit | T1574.010 | Zero-Day / Unknown Exploit; CWE: CWE-1190; CWE-1191; CWE-1193; CWE-1220; CWE-1268; CWE-1280; CWE-1297; CWE-1311; CWE-1315; CWE-1318; CWE-1320; CWE-1321; CWE-732 |
| 89 | CAPEC-165 | File Manipulation | Endpoint / EDR | Server / Workload Blast Radius | T1036.003 | Server / Workload Blast Radius |
| 90 | CAPEC-690 | Metadata Spoofing | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 91 | CAPEC-604 | Wi-Fi Jamming | Internal Network | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 92 | CAPEC-441 | Malicious Logic Insertion | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-284 |
| 93 | CAPEC-27 | Leveraging Race Conditions via Symbolic Links | Endpoint / EDR | Exploit Chain / Multi-Step |  | Exploit Chain / Multi-Step; CWE: CWE-367; CWE-61; CWE-662; CWE-667; CWE-689 |
| 94 | CAPEC-313 | Passive OS Fingerprinting | Internal Network; Server / Workload | Server / Workload Blast Radius | T1082 | Server / Workload Blast Radius; CWE: CWE-200 |
| 95 | CAPEC-292 | Host Discovery | Internal Network | Telemetry Gap / Evasion | T1018 | Telemetry Gap / Evasion; CWE: CWE-200 |
| 96 | CAPEC-457 | USB Memory Attacks | Endpoint / EDR | Zero-Day / Unknown Exploit | T1091; T1092 | Zero-Day / Unknown Exploit; CWE: CWE-1299 |
| 97 | CAPEC-309 | Network Topology Mapping | Internal Network | Telemetry Gap / Evasion | T1016; T1049; T1590 | Telemetry Gap / Evasion; CWE: CWE-200 |
| 98 | CAPEC-98 | Phishing | Server / Workload | Zero-Day / Unknown Exploit | T1566; T1598 | Zero-Day / Unknown Exploit; CWE: CWE-451 |
| 99 | CAPEC-677 | Server Motherboard Compromise | Server / Workload; Endpoint / EDR | Supply Chain / Trusted Dependency | T1195.003 | Supply Chain / Trusted Dependency |
| 100 | CAPEC-646 | Peripheral Footprinting | Internal Network; Endpoint / EDR | Destructive / Ransomware | T1120 | Destructive / Ransomware; CWE: CWE-200 |
| 101 | CAPEC-637 | Collect Data from Clipboard | Endpoint / EDR | Zero-Day / Unknown Exploit | T1115 | Zero-Day / Unknown Exploit; CWE: CWE-267 |
| 102 | CAPEC-577 | Owner Footprinting | Endpoint / EDR | Zero-Day / Unknown Exploit | T1033 | Zero-Day / Unknown Exploit; CWE: CWE-200 |
| 103 | CAPEC-573 | Process Footprinting | Endpoint / EDR | Living-off-the-Land | T1057 | Living-off-the-Land; CWE: CWE-200 |
| 104 | CAPEC-511 | Infiltration of Software Development Environment | Endpoint / EDR | Rare but High Impact | T1195.001 | Rare but High Impact |
| 105 | CAPEC-504 | Task Impersonation | Endpoint / EDR; Server / Workload | Server / Workload Blast Radius | T1036.004 | Server / Workload Blast Radius; CWE: CWE-1021 |
| 106 | CAPEC-497 | File Discovery | Internal Network; Endpoint / EDR | Rare but High Impact | T1083 | Rare but High Impact; CWE: CWE-200 |
| 107 | CAPEC-446 | Malicious Logic Insertion into Product via Inclusion of Third-Party Component | Endpoint / EDR | Supply Chain / Trusted Dependency | T1195 | Supply Chain / Trusted Dependency |
| 108 | CAPEC-445 | Malicious Logic Insertion into Product Software via Configuration Management Manipulation | Endpoint / EDR | Supply Chain / Trusted Dependency | T1195.001 | Supply Chain / Trusted Dependency |
| 109 | CAPEC-439 | Manipulation During Distribution | Server / Workload | Telemetry Gap / Evasion | T1195 | Telemetry Gap / Evasion; CWE: CWE-1269 |
| 110 | CAPEC-300 | Port Scanning | Internal Network; Server / Workload | Zero-Day / Unknown Exploit | T1046 | Zero-Day / Unknown Exploit; CWE: CWE-200 |
| 111 | CAPEC-127 | Directory Indexing | Endpoint / EDR | Rare but High Impact | T1083 | Rare but High Impact; CWE: CWE-276; CWE-285; CWE-288; CWE-424; CWE-425; CWE-693; CWE-732 |
| 112 | CAPEC-9 | Buffer Overflow in Local Command-Line Utilities | Endpoint / EDR | Exploit Chain / Multi-Step |  | Exploit Chain / Multi-Step; CWE: CWE-118; CWE-119; CWE-120; CWE-20; CWE-680; CWE-697; CWE-733; CWE-74 |
| 113 | CAPEC-641 | DLL Side-Loading | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-706 |
| 114 | CAPEC-536 | Data Injected During Configuration | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-284 |
| 115 | CAPEC-271 | Schema Poisoning | Server / Workload | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-15 |
| 116 | CAPEC-174 | Flash Parameter Injection | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-88 |
| 117 | CAPEC-139 | Relative Path Traversal | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-23 |
| 118 | CAPEC-635 | Alternative Execution Due to Deceptive Filenames | Endpoint / EDR | Server / Workload Blast Radius | T1036.007 | Server / Workload Blast Radius; CWE: CWE-162 |
| 119 | CAPEC-601 | Jamming | Server / Workload | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 120 | CAPEC-586 | Object Injection | Internal Network; Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-502 |
| 121 | CAPEC-549 | Local Execution of Code | Endpoint / EDR | Destructive / Ransomware |  | Destructive / Ransomware; CWE: CWE-829 |
| 122 | CAPEC-4 | Using Alternative IP Address Encodings | Internal Network | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-173; CWE-291 |
| 123 | CAPEC-155 | Screen Temporary Files for Sensitive Information | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-377 |
| 124 | CAPEC-643 | Identify Shared Files/Directories on System | Internal Network | Zero-Day / Unknown Exploit | T1135 | Zero-Day / Unknown Exploit; CWE: CWE-200; CWE-267 |
| 125 | CAPEC-678 | System Build Data Maliciously Altered | Endpoint / EDR | Supply Chain / Trusted Dependency | T1195.002 | Supply Chain / Trusted Dependency |
| 126 | CAPEC-669 | Alteration of a Software Update | Endpoint / EDR | Supply Chain / Trusted Dependency | T1195.002 | Supply Chain / Trusted Dependency |
| 127 | CAPEC-574 | Services Footprinting | Server / Workload | Zero-Day / Unknown Exploit | T1007 | Zero-Day / Unknown Exploit; CWE: CWE-200 |
| 128 | CAPEC-141 | Cache Poisoning | Internal Network | Credential Artifact Abuse | T1557.002 | Credential Artifact Abuse; CWE: CWE-345; CWE-346; CWE-348; CWE-349 |
| 129 | CAPEC-606 | Weakening of Cellular Encryption | Internal Network | Destructive / Ransomware |  | Destructive / Ransomware; CWE: CWE-757 |
| 130 | CAPEC-590 | IP Address Blocking | Server / Workload | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-300 |
| 131 | CAPEC-582 | Route Disabling | Internal Network | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 132 | CAPEC-548 | Contaminate Resource | Internal Network | Destructive / Ransomware |  | Destructive / Ransomware |
| 133 | CAPEC-533 | Malicious Manual Software Update | Internal Network; Endpoint / EDR | Supply Chain / Trusted Dependency |  | Supply Chain / Trusted Dependency; CWE: CWE-494 |
| 134 | CAPEC-499 | Android Intent Intercept | Server / Workload | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-925 |
| 135 | CAPEC-491 | Quadratic Data Expansion | Server / Workload | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-770 |
| 136 | CAPEC-263 | Force Use of Corrupted Files | Server / Workload; Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-829 |
| 137 | CAPEC-253 | Remote Code Inclusion | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-829 |
| 138 | CAPEC-221 | Data Serialization External Entities Blowup | Server / Workload; Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-611 |
| 139 | CAPEC-200 | Removal of filters: Input filters, output filters, data masking | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 140 | CAPEC-194 | Fake the Source of Data | Server / Workload | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-287 |
| 141 | CAPEC-181 | Flash File Overlay | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-1021 |
| 142 | CAPEC-176 | Configuration/Environment Manipulation | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-1233; CWE-1234; CWE-1304; CWE-1328; CWE-15 |
| 143 | CAPEC-168 | Windows ::DATA Alternate Data Stream | Endpoint / EDR | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-212; CWE-69 |
| 144 | CAPEC-161 | Infrastructure Manipulation | Internal Network; Server / Workload | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-923 |
| 145 | CAPEC-149 | Explore for Predictable Temporary File Names | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-377 |
| 146 | CAPEC-661 | Root/Jailbreak Detection Evasion via Debugging | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-489 |
| 147 | CAPEC-529 | Malware-Directed Internal Reconnaissance | Internal Network; Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 148 | CAPEC-700 | Network Boundary Bridging | Internal Network | Telemetry Gap / Evasion | T1599 | Telemetry Gap / Evasion |
| 149 | CAPEC-598 | DNS Spoofing | Internal Network | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 150 | CAPEC-594 | Traffic Injection | Internal Network | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-940 |
| 151 | CAPEC-589 | DNS Blocking | Internal Network; Server / Workload | Destructive / Ransomware |  | Destructive / Ransomware; CWE: CWE-300 |
| 152 | CAPEC-585 | DNS Domain Seizure | Internal Network; Server / Workload | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 153 | CAPEC-584 | BGP Route Disabling | Internal Network | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 154 | CAPEC-583 | Disabling Network Hardware | Internal Network; Server / Workload | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 155 | CAPEC-495 | UDP Fragmentation | Internal Network; Server / Workload | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-404; CWE-770 |
| 156 | CAPEC-494 | TCP Fragmentation | Internal Network | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-404; CWE-770 |
| 157 | CAPEC-487 | ICMP Flood | Internal Network; Server / Workload | Credential Artifact Abuse |  | Credential Artifact Abuse; CWE: CWE-770 |
| 158 | CAPEC-486 | UDP Flood | Internal Network; Server / Workload | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-770 |
| 159 | CAPEC-202 | Create Malicious Client | Server / Workload | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-602 |
| 160 | CAPEC-179 | Calling Micro-Services Directly | Server / Workload | Supply Chain / Trusted Dependency |  | Supply Chain / Trusted Dependency |
| 161 | CAPEC-167 | White Box Reverse Engineering | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-1323 |
| 162 | CAPEC-157 | Sniffing Attacks | Internal Network | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-311 |
| 163 | CAPEC-117 | Interception | Internal Network | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-319 |
| 164 | CAPEC-452 | Infected Hardware | Endpoint / EDR | Supply Chain / Trusted Dependency |  | Supply Chain / Trusted Dependency |
| 165 | CAPEC-190 | Reverse Engineer an Executable to Expose Assumed Hidden Functionality | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-912 |
| 166 | CAPEC-320 | TCP Timestamp Probe | Server / Workload | Supply Chain / Trusted Dependency |  | Supply Chain / Trusted Dependency; CWE: CWE-200 |
| 167 | CAPEC-142 | DNS Cache Poisoning | Internal Network; Server / Workload | Exploit Chain / Multi-Step | T1584.002 | Exploit Chain / Multi-Step; CWE: CWE-345; CWE-346; CWE-348; CWE-349; CWE-350 |
| 168 | CAPEC-618 | Cellular Broadcast Message Request | Internal Network | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-201 |
| 169 | CAPEC-615 | Evil Twin Wi-Fi Attack | Internal Network | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-300 |
| 170 | CAPEC-613 | WiFi SSID Tracking | Internal Network; Server / Workload | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-201; CWE-300 |
| 171 | CAPEC-458 | Flash Memory Attacks | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-1282 |
| 172 | CAPEC-394 | Using a Snap Gun Lock to Force a Lock | Endpoint / EDR | Supply Chain / Trusted Dependency |  | Supply Chain / Trusted Dependency |
| 173 | CAPEC-392 | Lock Bumping | Endpoint / EDR | Supply Chain / Trusted Dependency |  | Supply Chain / Trusted Dependency |
| 174 | CAPEC-310 | Scanning for Vulnerable Software | Internal Network; Server / Workload | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-200 |
| 175 | CAPEC-307 | TCP RPC Scan | Server / Workload | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-200 |
| 176 | CAPEC-297 | TCP ACK Ping | Server / Workload | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-200 |
| 177 | CAPEC-296 | ICMP Information Request | Internal Network | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-200 |
| 178 | CAPEC-294 | ICMP Address Mask Request | Internal Network | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-200 |
| 179 | CAPEC-293 | Traceroute Route Enumeration | Internal Network | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-200 |
| 180 | CAPEC-291 | DNS Zone Transfers | Internal Network; Server / Workload | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-200 |
| 181 | CAPEC-290 | Enumerate Mail Exchange (MX) Records | Internal Network; Server / Workload | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-200 |
| 182 | CAPEC-192 | Protocol Analysis | Internal Network | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-326 |
| 183 | CAPEC-189 | Black Box Reverse Engineering | Endpoint / EDR | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-1255; CWE-1300; CWE-203 |
