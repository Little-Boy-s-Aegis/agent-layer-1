# Layer 1 Edge-Case Matrix

Filtered for Agent A: scoped runtime edge cases only.
This file is context only and does not provide runtime risk scores.

| rank | attack_id | attack_vector | edge_case | edge_case_flags | prediction_context |
| --- | --- | --- | --- | --- | --- |
| 1 | T1105 | Ingress Tool Transfer | Living-off-the-Land | Living-off-the-Land | Living-off-the-Land; Watch: Command; Process; Network Traffic; File |
| 2 | T1074.001 | Local Data Staging | Server / Workload Blast Radius | Server / Workload Blast Radius | Server / Workload Blast Radius; Watch: Command; Process; Snapshot; File |
| 3 | T1486 | Data Encrypted for Impact | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: Command; Process; File |
| 4 | T1560.001 | Archive via Utility | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: Command; Process; File; Module |
| 5 | T1090 | Proxy | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Command; Process; Network Traffic; Firewall |
| 6 | T1560 | Archive Collected Data | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: Command; Process; File; Module |
| 7 | T1490 | Inhibit System Recovery | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: Command; Process; Windows Registry; Service; File; Snapshot |
| 8 | T1489 | Service Stop | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: Process; Service; File |
| 9 | T1485 | Data Destruction | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: Command; Process; File; Volume |
| 10 | T1048.003 | Exfiltration Over Unencrypted Non-C2 Protocol | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: Command; Network Traffic; Process; File |
| 11 | T1041 | Exfiltration Over C2 Channel | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; File |
| 12 | T1571 | Non-Standard Port | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; Application Log |
| 13 | T1071.004 | DNS | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process |
| 14 | T1560.003 | Archive via Custom Method | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: Process; Command; File |
| 15 | T1572 | Protocol Tunneling | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; Application Log |
| 16 | T1090.003 | Multi-hop Proxy | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Firmware; Network Traffic; Process |
| 17 | T1090.001 | Internal Proxy | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Command; Network Traffic; Process; Firewall; Service |
| 18 | T1529 | System Shutdown/Reboot | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: Command; Process; Sensor Health |
| 19 | T1001.003 | Protocol or Service Impersonation | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process |
| 20 | T1573 | Encrypted Channel | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; Module; Application Log |
| 21 | T1560.002 | Archive via Library | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: Command; Process; File; Module |
| 22 | T1074 | Data Staged | Server / Workload Blast Radius | Server / Workload Blast Radius | Server / Workload Blast Radius; Watch: Command; Process; File |
| 23 | T1048 | Exfiltration Over Alternative Protocol | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: Command; Network Traffic; Process; File |
| 24 | T1048.002 | Exfiltration Over Asymmetric Encrypted Non-C2 Protocol | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: Command; Network Traffic; Process; File |
| 25 | T1499 | Endpoint Denial of Service | Server / Workload Blast Radius | Server / Workload Blast Radius | Server / Workload Blast Radius; Watch: Process; Instance; Sensor Health; Application Log; Network Traffic |
| 26 | T1011.001 | Exfiltration Over Bluetooth | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: Command; Process; Network Traffic; File |
| 27 | T1561 | Disk Wipe | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: Drive; Command; Process; User Account; Driver |
| 28 | T1499.002 | Service Exhaustion Flood | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: Process; Network Traffic; Firewall; Sensor Health; Application Log |
| 29 | T1496 | Resource Hijacking | Server / Workload Blast Radius | Server / Workload Blast Radius | Server / Workload Blast Radius; Watch: Network Traffic; Process; Instance; Sensor Health; Application Log |
| 30 | T1052 | Exfiltration Over Physical Medium | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: Drive; Command; Process; File |
| 31 | T1011 | Exfiltration Over Other Network Medium | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: Command; Network Traffic; Process; File; Sensor Health |
| 32 | T1053.005 | Scheduled Task | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Process; Windows Registry; Scheduled Job; File |
| 33 | T1027 | Obfuscated Files or Information | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Command; Network Traffic; Process; File |
| 34 | T1574.001 | DLL | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Process; Windows Registry; Module; File |
| 35 | T1003.001 | LSASS Memory | Credential Artifact Abuse | Credential Artifact Abuse | Credential Artifact Abuse; Watch: Process; User Account; Windows Registry; File |
| 36 | T1036 | Masquerading | Server / Workload Blast Radius | Server / Workload Blast Radius | Server / Workload Blast Radius; Watch: Command; Process; File; Service; Image |
| 37 | T1068 | Exploitation for Privilege Escalation | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Process; Container; Module; Driver |
| 38 | T1552.001 | Credentials In Files | Credential Artifact Abuse | Credential Artifact Abuse | Credential Artifact Abuse; Watch: Command; Process; Network Traffic; File |
| 39 | T1133 | External Remote Services | Credential Artifact Abuse | Credential Artifact Abuse | Credential Artifact Abuse; Watch: Network Traffic; User Account; Application Log |
| 40 | T1040 | Network Sniffing | Credential Artifact Abuse | Credential Artifact Abuse | Credential Artifact Abuse; Watch: Command; Network Traffic; Process; Service; User Account |
| 41 | T1210 | Exploitation of Remote Services | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Process; Network Traffic; Module; File; Application Log |
| 42 | T1021.004 | SSH | Credential Artifact Abuse | Credential Artifact Abuse | Credential Artifact Abuse; Watch: Command; Network Traffic; Process |
| 43 | T1071.002 | File Transfer Protocols | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Command; Network Traffic; Process |
| 44 | T1025 | Data from Removable Media | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Drive; Process; File |
| 45 | T1090.002 | External Proxy | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; Firewall |
| 46 | T1001 | Data Obfuscation | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Network Traffic; Process |
| 47 | T1039 | Data from Network Shared Drive | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: File; Drive; Network Share |
| 48 | T1557.001 | Name Resolution Poisoning and SMB Relay | Credential Artifact Abuse | Credential Artifact Abuse | Credential Artifact Abuse; Watch: Windows Registry; Network Traffic; Service |
| 49 | T1052.001 | Exfiltration over USB | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: Drive; Process; File |
| 50 | T1568.001 | Fast Flux DNS | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Process; Network Traffic |
| 51 | T1498 | Network Denial of Service | Server / Workload Blast Radius | Server / Workload Blast Radius | Server / Workload Blast Radius; Watch: Process; Network Traffic |
| 52 | T1602.002 | Network Device Configuration Dump | Credential Artifact Abuse | Credential Artifact Abuse | Credential Artifact Abuse; Watch: Command; Network Traffic; User Account |
| 53 | T1568.003 | DNS Calculation | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Process; Network Traffic |
| 54 | T1498.001 | Direct Network Flood | Server / Workload Blast Radius | Server / Workload Blast Radius | Server / Workload Blast Radius; Watch: Process; Sensor Health; Network Traffic |
| 55 | T1048.001 | Exfiltration Over Symmetric Encrypted Non-C2 Protocol | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: Command; Network Traffic; Process |
| 56 | T1140 | Deobfuscate/Decode Files or Information | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Process; File; Command |
| 57 | T1547.001 | Registry Run Keys / Startup Folder | Credential Artifact Abuse | Credential Artifact Abuse | Credential Artifact Abuse; Watch: Process; File; Windows Registry |
| 58 | T1112 | Modify Registry | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Process; Windows Registry |
| 59 | T1021.002 | SMB/Windows Admin Shares | Credential Artifact Abuse | Credential Artifact Abuse | Credential Artifact Abuse; Watch: Process; Network Traffic |
| 60 | T1570 | Lateral Tool Transfer | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Command; Process; File; Network Share |
| 61 | T1555 | Credentials from Password Stores | Server / Workload Blast Radius | Server / Workload Blast Radius | Server / Workload Blast Radius; Watch: Process; File |
| 62 | T1070 | Indicator Removal | Server / Workload Blast Radius | Server / Workload Blast Radius | Server / Workload Blast Radius; Watch: File; Windows Registry; Scheduled Job; Application Log |
| 63 | T1003.002 | Security Account Manager | Credential Artifact Abuse | Credential Artifact Abuse | Credential Artifact Abuse; Watch: File; Process; Windows Registry |
| 64 | T1003 | OS Credential Dumping | Credential Artifact Abuse | Credential Artifact Abuse | Credential Artifact Abuse; Watch: Process; File |
| 65 | T1222.001 | Windows Permissions | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Command; Process; WMI; File |
| 66 | T1021.006 | Windows Remote Management | Credential Artifact Abuse | Credential Artifact Abuse | Credential Artifact Abuse; Watch: Process; Service; Network Traffic |
| 67 | T1564 | Hide Artifacts | Living-off-the-Land | Living-off-the-Land | Living-off-the-Land; Watch: Command; Process; Windows Registry; File; Application Log |
| 68 | T1543 | Create or Modify System Process | Exploit Chain / Multi-Step | Exploit Chain / Multi-Step | Exploit Chain / Multi-Step; Watch: Command; Process; Windows Registry; File; Container; Service |
| 69 | T1037.004 | RC Scripts | Living-off-the-Land | Living-off-the-Land | Living-off-the-Land; Watch: Command; Process; File; Script |
| 70 | T1037 | Boot or Logon Initialization Scripts | Credential Artifact Abuse | Credential Artifact Abuse | Credential Artifact Abuse; Watch: Process; File; Windows Registry; Scheduled Job; Script; Service |
| 71 | T1021 | Remote Services | Credential Artifact Abuse | Credential Artifact Abuse | Credential Artifact Abuse; Watch: Command; Process; Network Traffic |
| 72 | T1547 | Boot or Logon Autostart Execution | Living-off-the-Land | Living-off-the-Land | Living-off-the-Land; Watch: Process; File; Windows Registry; Service |
| 73 | T1037.001 | Logon Script (Windows) | Credential Artifact Abuse | Credential Artifact Abuse | Credential Artifact Abuse; Watch: Process; Script; File |
| 74 | T1547.012 | Print Processors | Living-off-the-Land | Living-off-the-Land | Living-off-the-Land; Watch: Process; File; Windows Registry; Module |
| 75 | T1547.008 | LSASS Driver | Living-off-the-Land | Living-off-the-Land | Living-off-the-Land; Watch: File; Windows Registry; Module; Driver |
| 76 | T1053 | Scheduled Task/Job | Exploit Chain / Multi-Step | Exploit Chain / Multi-Step | Exploit Chain / Multi-Step; Watch: Command; Process; File; Scheduled Job |
| 77 | T1543.005 | Container Service | Server / Workload Blast Radius | Server / Workload Blast Radius | Server / Workload Blast Radius; Watch: Process; Service; Container; Pod |
| 78 | T1134.002 | Create Process with Token | Credential Artifact Abuse | Credential Artifact Abuse | Credential Artifact Abuse; Watch: Process |
| 79 | T1070.003 | Clear Command History | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Command; Process; File |
| 80 | T1690 | Prevent Command History Logging | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Command; Process |
| 81 | T1552.002 | Credentials in Registry | Credential Artifact Abuse | Credential Artifact Abuse | Credential Artifact Abuse; Watch: Process; Windows Registry |
| 82 | T1098.004 | SSH Authorized Keys | Credential Artifact Abuse | Credential Artifact Abuse | Credential Artifact Abuse; Watch: Command; Process; File |
| 83 | T1055.013 | Process Doppelgänging | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Process; File |
| 84 | T1574.010 | Services File Permissions Weakness | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: File; Process; Service |
| 85 | T1546.013 | PowerShell Profile | Credential Artifact Abuse | Credential Artifact Abuse | Credential Artifact Abuse; Watch: Command; Process; File |
| 86 | T1546.009 | AppCert DLLs | Credential Artifact Abuse | Credential Artifact Abuse | Credential Artifact Abuse; Watch: Process; Windows Registry; Module |
| 87 | T1053.007 | Container Orchestration Job | Exploit Chain / Multi-Step | Exploit Chain / Multi-Step | Exploit Chain / Multi-Step; Watch: Network Traffic; Scheduled Job; Container |
| 88 | T1543.003 | Windows Service | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Windows Registry; Process; Service; Driver |
| 89 | T1218.011 | Rundll32 | Living-off-the-Land | Living-off-the-Land | Living-off-the-Land; Watch: Process; File; Network Traffic; Module |
| 90 | T1020 | Automated Exfiltration | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Process; Network Traffic; Scheduled Job |
| 91 | T1092 | Communication Through Removable Media | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Drive; Process; File |
| 92 | T1057 | Process Discovery | Living-off-the-Land | Living-off-the-Land | Living-off-the-Land; Watch: Process; Command; File |
| 93 | T1016 | System Network Configuration Discovery | Living-off-the-Land | Living-off-the-Land | Living-off-the-Land; Watch: Command; Process |
| 94 | T1049 | System Network Connections Discovery | Server / Workload Blast Radius | Server / Workload Blast Radius | Server / Workload Blast Radius; Watch: Command; Process; Network Traffic |
| 95 | T1036.004 | Masquerade Task or Service | Living-off-the-Land | Living-off-the-Land | Living-off-the-Land; Watch: Scheduled Job; Process; Service |
| 96 | T1055 | Process Injection | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Process; Module; File |
| 97 | T1046 | Network Service Discovery | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Process; Network Traffic |
| 98 | T1027.010 | Command Obfuscation | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Command; Process |
| 99 | T1686.003 | Windows Host Firewall | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Process; Network Traffic; Windows Registry; Service |
| 100 | T1543.002 | Systemd Service | Exploit Chain / Multi-Step | Exploit Chain / Multi-Step | Exploit Chain / Multi-Step; Watch: Command; Process; File; Service |
| 101 | T1070.005 | Network Share Connection Removal | Credential Artifact Abuse | Credential Artifact Abuse | Credential Artifact Abuse; Watch: Command; Process; Network Traffic |
| 102 | T1610 | Deploy Container | Server / Workload Blast Radius | Server / Workload Blast Radius | Server / Workload Blast Radius; Watch: Container; Process; Network Traffic; Application Log |
| 103 | T1686.002 | Network Device Firewall | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Firewall; Command; Network Traffic |
| 104 | T1685.001 | Disable or Modify Windows Event Log | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Process; Windows Registry; Service; Application Log |
| 105 | T1070.007 | Clear Network Connection History and Configurations | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Command; Network Traffic; Process; Windows Registry; File; Firewall |
| 106 | T1685.004 | Disable or Modify Linux Audit System Log | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Command; File; Service; Process |
| 107 | T1505.005 | Terminal Services DLL | Credential Artifact Abuse | Credential Artifact Abuse | Credential Artifact Abuse; Watch: Process; File; Windows Registry; Module |
| 108 | T1216 | System Script Proxy Execution | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Command; Process; Module; File |
| 109 | T1127 | Trusted Developer Utilities Proxy Execution | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Process; Network Traffic; Module; File |
| 110 | T1055.012 | Process Hollowing | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Process |
| 111 | T1685.005 | Clear Windows Event Logs | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Process; File; Application Log |
| 112 | T1059 | Command and Scripting Interpreter | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Command; Process; User Account |
| 113 | T1091 | Replication Through Removable Media | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Drive; Process; File |
| 114 | T1546.003 | Windows Management Instrumentation Event Subscription | Living-off-the-Land | Living-off-the-Land | Living-off-the-Land; Watch: Process; WMI; Module |
| 115 | T1222.002 | Linux and Mac Permissions | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Command; File; Process |
| 116 | T1547.004 | Winlogon Helper DLL | Living-off-the-Land | Living-off-the-Land | Living-off-the-Land; Watch: Process; Windows Registry; Module |
| 117 | T1685.006 | Clear Linux or Mac System Logs | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Process; File |
| 118 | T1564.011 | Ignore Process Interrupts | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Command; Process |
| 119 | T1609 | Container Administration Command | Server / Workload Blast Radius | Server / Workload Blast Radius | Server / Workload Blast Radius; Watch: Command; Process |
| 120 | T1546.010 | AppInit DLLs | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Process; Windows Registry; Module |
| 121 | T1202 | Indirect Command Execution | Living-off-the-Land | Living-off-the-Land | Living-off-the-Land; Watch: Process; File; Network Traffic |
| 122 | T1613 | Container and Resource Discovery | Server / Workload Blast Radius | Server / Workload Blast Radius | Server / Workload Blast Radius; Watch: Container; Pod |
| 123 | T1220 | XSL Script Processing | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Process; Module |
| 124 | T1059.008 | Network Device CLI | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Command; Network Traffic; User Account |
| 125 | T1218 | System Binary Proxy Execution | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Process; Network Traffic; Module |
| 126 | T1546.007 | Netsh Helper DLL | Living-off-the-Land | Living-off-the-Land | Living-off-the-Land; Watch: Process; Windows Registry; Module |
| 127 | T1574.011 | Services Registry Permissions Weakness | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Process; Windows Registry; Service |
| 128 | T1135 | Network Share Discovery | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Command; Process; Network Traffic; Named Pipe |
| 129 | T1569.002 | Service Execution | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Windows Registry; Process; Network Traffic; Service |
| 130 | T1059.007 | JavaScript | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Command; Process; Script; Module |
| 131 | T1036.010 | Masquerade Account Name | Server / Workload Blast Radius | Server / Workload Blast Radius | Server / Workload Blast Radius; Watch: User Account |
| 132 | T1098.006 | Additional Container Cluster Roles | Credential Artifact Abuse | Credential Artifact Abuse | Credential Artifact Abuse; Watch: User Account |
| 133 | T1059.003 | Windows Command Shell | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Process; Script; Module |
| 134 | T1059.001 | PowerShell | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Command; Process; Module |
| 135 | T1047 | Windows Management Instrumentation | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Process; Network Traffic; WMI |
| 136 | T1012 | Query Registry | Living-off-the-Land | Living-off-the-Land | Living-off-the-Land; Watch: Command; Process; Windows Registry |
| 137 | T1007 | System Service Discovery | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Command; Process |
| 138 | T1566.003 | Spearphishing via Service | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; File; Application Log |
| 139 | T1559 | Inter-Process Communication | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Process; Script; File; Named Pipe |
| 140 | T1652 | Device Driver Discovery | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Command; Process; Windows Registry; File |
| 141 | T1569 | System Services | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Windows Registry; Process; Service; File |
| 142 | T1669 | Wi-Fi Networks | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Network Traffic; Firewall; User Account |
| 143 | T1559.003 | XPC Services | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Process; Named Pipe |
| 144 | T1675 | ESXi Administration Command | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Application Log |
| 145 | T1564.010 | Process Argument Spoofing | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Process |
| 146 | T1036.009 | Break Process Trees | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Process |
| 147 | T1599 | Network Boundary Bridging | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Network Traffic |
| 148 | T1036.011 | Overwrite Process Arguments | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Process |
| 149 | T1599.001 | Network Address Translation Traversal | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Network Traffic |
| 150 | T1036.008 | Masquerade File Type | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Process; File |
| 151 | T1027.005 | Indicator Removal from Tools | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Process; File; Application Log |
| 152 | T1059.002 | AppleScript | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Process |
| 153 | T1422 | System Network Configuration Discovery | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 154 | T1406 | Obfuscated Files or Information | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 155 | T1646 | Exfiltration Over C2 Channel | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 156 | T1404 | Exploitation for Privilege Escalation | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit |
| 157 | T1544 | Ingress Tool Transfer | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 158 | T1532 | Archive Collected Data | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware |
| 159 | T1424 | Process Discovery | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 160 | T1509 | Non-Standard Port | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 161 | T1421 | System Network Connections Discovery | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 162 | T1655 | Masquerading | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 163 | T1642 | Endpoint Denial of Service | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware |
| 164 | T1603 | Scheduled Task/Job | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 165 | T0881 | Service Stop | Rare but High Impact | Rare but High Impact | Rare but High Impact |
| 166 | T0867 | Lateral Tool Transfer | Rare but High Impact | Rare but High Impact | Rare but High Impact |
| 167 | T1662 | Data Destruction | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware |
| 168 | T1398 | Boot or Logon Initialization Scripts | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 169 | T0866 | Exploitation of Remote Services | Rare but High Impact | Rare but High Impact | Rare but High Impact |
| 170 | T0853 | Scripting | Rare but High Impact | Rare but High Impact | Rare but High Impact |
| 171 | T0849 | Masquerading | Rare but High Impact | Rare but High Impact | Rare but High Impact |
| 172 | T0814 | Denial of Service | Rare but High Impact | Rare but High Impact | Rare but High Impact |
| 173 | T0809 | Data Destruction | Rare but High Impact | Rare but High Impact | Rare but High Impact |
| 174 | T0807 | Command-Line Interface | Rare but High Impact | Rare but High Impact | Rare but High Impact |
| 175 | T0801 | Monitor Process State | Rare but High Impact | Rare but High Impact | Rare but High Impact |
| 176 | T1692.001 | Command Message | Rare but High Impact | Rare but High Impact | Rare but High Impact |
| 177 | T1639.001 | Exfiltration Over Unencrypted Non-C2 Protocol | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware |
| 178 | T1471 | Data Encrypted for Impact | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware |
| 179 | T0886 | Remote Services | Rare but High Impact | Rare but High Impact | Rare but High Impact |
| 180 | T0884 | Connection Proxy | Rare but High Impact | Rare but High Impact | Rare but High Impact |
| 181 | T0842 | Network Sniffing | Rare but High Impact | Rare but High Impact | Rare but High Impact |
| 182 | T1631 | Process Injection | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 183 | T1630 | Indicator Removal on Host | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 184 | T1623 | Command and Scripting Interpreter | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 185 | T1604 | Proxy Through Victim | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 186 | T1521 | Encrypted Channel | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 187 | T1458 | Replication Through Removable Media | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 188 | T1428 | Exploitation of Remote Services | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 189 | T0890 | Exploitation for Privilege Escalation | Rare but High Impact | Rare but High Impact | Rare but High Impact |
| 190 | T0872 | Indicator Removal on Host | Rare but High Impact | Rare but High Impact | Rare but High Impact |
| 191 | T0847 | Replication Through Removable Media | Rare but High Impact | Rare but High Impact | Rare but High Impact |
| 192 | T0840 | Network Connection Enumeration | Rare but High Impact | Rare but High Impact | Rare but High Impact |
| 193 | T1691.001 | Command Message | Rare but High Impact | Rare but High Impact | Rare but High Impact |
| 194 | T1639 | Exfiltration Over Alternative Protocol | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware |
| 195 | T1464 | Network Denial of Service | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware |
| 196 | T1423 | Network Service Scanning | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 197 | T0822 | External Remote Services | Rare but High Impact | Rare but High Impact | Rare but High Impact |
| 198 | T1628 | Hide Artifacts | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 199 | T1444 | Masquerade as Legitimate Application | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 200 | T1430.001 | Remote Device Management Services | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 201 | T0894 | System Binary Proxy Execution | Rare but High Impact | Rare but High Impact | Rare but High Impact |
| 202 | T0841 | Network Service Scanning | Rare but High Impact | Rare but High Impact | Rare but High Impact |
