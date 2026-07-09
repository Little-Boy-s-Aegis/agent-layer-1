# Layer 1 Surface Context Matrix

Filtered for Agent A: Endpoint / EDR, Internal Network, Server / Workload surfaces only.
This file is context only and does not provide runtime risk scores.

| rank | attack_id | attack_vector | surface |
| --- | --- | --- | --- |
| 1 | T1105 | Ingress Tool Transfer | Endpoint / EDR |
| 2 | T1074.001 | Local Data Staging | Endpoint / EDR |
| 3 | T1486 | Data Encrypted for Impact | Endpoint / EDR |
| 4 | T1560.001 | Archive via Utility | Endpoint / EDR |
| 5 | T1090 | Proxy | Internal Network |
| 6 | T1560 | Archive Collected Data | Endpoint / EDR |
| 7 | T1490 | Inhibit System Recovery | Server / Workload |
| 8 | T1489 | Service Stop | Server / Workload |
| 9 | T1485 | Data Destruction | Endpoint / EDR |
| 10 | T1048.003 | Exfiltration Over Unencrypted Non-C2 Protocol | Internal Network |
| 11 | T1041 | Exfiltration Over C2 Channel | Internal Network |
| 12 | T1571 | Non-Standard Port | Internal Network |
| 13 | T1071.004 | DNS | Internal Network |
| 14 | T1560.003 | Archive via Custom Method | Endpoint / EDR |
| 15 | T1572 | Protocol Tunneling | Internal Network |
| 16 | T1090.003 | Multi-hop Proxy | Internal Network |
| 17 | T1090.001 | Internal Proxy | Internal Network |
| 18 | T1529 | System Shutdown/Reboot | Endpoint / EDR |
| 19 | T1001.003 | Protocol or Service Impersonation | Server / Workload |
| 20 | T1573 | Encrypted Channel | Endpoint / EDR |
| 21 | T1560.002 | Archive via Library | Endpoint / EDR |
| 22 | T1074 | Data Staged | Endpoint / EDR |
| 23 | T1048 | Exfiltration Over Alternative Protocol | Endpoint / EDR |
| 24 | T1048.002 | Exfiltration Over Asymmetric Encrypted Non-C2 Protocol | Internal Network |
| 25 | T1499 | Endpoint Denial of Service | Endpoint / EDR; Server / Workload |
| 26 | T1011.001 | Exfiltration Over Bluetooth | Endpoint / EDR |
| 27 | T1561 | Disk Wipe | Endpoint / EDR |
| 28 | T1499.002 | Service Exhaustion Flood | Server / Workload |
| 29 | T1496 | Resource Hijacking | Endpoint / EDR |
| 30 | T1052 | Exfiltration Over Physical Medium | Endpoint / EDR |
| 31 | T1011 | Exfiltration Over Other Network Medium | Internal Network |
| 32 | T1053.005 | Scheduled Task | Server / Workload |
| 33 | T1027 | Obfuscated Files or Information | Endpoint / EDR |
| 34 | T1574.001 | DLL | Endpoint / EDR |
| 35 | T1003.001 | LSASS Memory | Endpoint / EDR |
| 36 | T1036 | Masquerading | Endpoint / EDR |
| 37 | T1068 | Exploitation for Privilege Escalation | Endpoint / EDR |
| 38 | T1552.001 | Credentials In Files | Endpoint / EDR |
| 39 | T1133 | External Remote Services | Internal Network; Server / Workload |
| 40 | T1040 | Network Sniffing | Internal Network |
| 41 | T1210 | Exploitation of Remote Services | Internal Network; Server / Workload |
| 42 | T1021.004 | SSH | Internal Network |
| 43 | T1071.002 | File Transfer Protocols | Internal Network; Endpoint / EDR |
| 44 | T1025 | Data from Removable Media | Endpoint / EDR |
| 45 | T1090.002 | External Proxy | Internal Network |
| 46 | T1001 | Data Obfuscation | Endpoint / EDR |
| 47 | T1039 | Data from Network Shared Drive | Internal Network |
| 48 | T1557.001 | Name Resolution Poisoning and SMB Relay | Internal Network |
| 49 | T1052.001 | Exfiltration over USB | Endpoint / EDR |
| 50 | T1568.001 | Fast Flux DNS | Internal Network |
| 51 | T1498 | Network Denial of Service | Internal Network; Server / Workload |
| 52 | T1602.002 | Network Device Configuration Dump | Internal Network |
| 53 | T1568.003 | DNS Calculation | Internal Network |
| 54 | T1498.001 | Direct Network Flood | Internal Network |
| 55 | T1048.001 | Exfiltration Over Symmetric Encrypted Non-C2 Protocol | Internal Network |
| 56 | T1140 | Deobfuscate/Decode Files or Information | Endpoint / EDR |
| 57 | T1547.001 | Registry Run Keys / Startup Folder | Endpoint / EDR |
| 58 | T1112 | Modify Registry | Endpoint / EDR |
| 59 | T1021.002 | SMB/Windows Admin Shares | Internal Network |
| 60 | T1570 | Lateral Tool Transfer | Endpoint / EDR |
| 61 | T1555 | Credentials from Password Stores | Endpoint / EDR |
| 62 | T1070 | Indicator Removal | Endpoint / EDR |
| 63 | T1003.002 | Security Account Manager | Endpoint / EDR |
| 64 | T1003 | OS Credential Dumping | Endpoint / EDR |
| 65 | T1222.001 | Windows Permissions | Endpoint / EDR |
| 66 | T1021.006 | Windows Remote Management | Endpoint / EDR |
| 67 | T1564 | Hide Artifacts | Endpoint / EDR |
| 68 | T1543 | Create or Modify System Process | Endpoint / EDR |
| 69 | T1037.004 | RC Scripts | Endpoint / EDR |
| 70 | T1037 | Boot or Logon Initialization Scripts | Endpoint / EDR; Server / Workload |
| 71 | T1021 | Remote Services | Internal Network; Server / Workload |
| 72 | T1547 | Boot or Logon Autostart Execution | Server / Workload |
| 73 | T1037.001 | Logon Script (Windows) | Endpoint / EDR; Server / Workload |
| 74 | T1547.012 | Print Processors | Endpoint / EDR |
| 75 | T1547.008 | LSASS Driver | Endpoint / EDR |
| 76 | T1053 | Scheduled Task/Job | Server / Workload |
| 77 | T1543.005 | Container Service | Server / Workload |
| 78 | T1134.002 | Create Process with Token | Endpoint / EDR |
| 79 | T1070.003 | Clear Command History | Endpoint / EDR |
| 80 | T1690 | Prevent Command History Logging | Endpoint / EDR |
| 81 | T1552.002 | Credentials in Registry | Endpoint / EDR |
| 82 | T1098.004 | SSH Authorized Keys | Internal Network |
| 83 | T1055.013 | Process Doppelgänging | Endpoint / EDR |
| 84 | T1574.010 | Services File Permissions Weakness | Endpoint / EDR; Server / Workload |
| 85 | T1546.013 | PowerShell Profile | Endpoint / EDR |
| 86 | T1546.009 | AppCert DLLs | Endpoint / EDR |
| 87 | T1053.007 | Container Orchestration Job | Server / Workload |
| 88 | T1543.003 | Windows Service | Server / Workload |
| 89 | T1218.011 | Rundll32 | Endpoint / EDR |
| 90 | T1020 | Automated Exfiltration | Endpoint / EDR |
| 91 | T1092 | Communication Through Removable Media | Endpoint / EDR |
| 92 | T1057 | Process Discovery | Endpoint / EDR |
| 93 | T1016 | System Network Configuration Discovery | Internal Network |
| 94 | T1049 | System Network Connections Discovery | Internal Network |
| 95 | T1036.004 | Masquerade Task or Service | Endpoint / EDR; Server / Workload |
| 96 | T1055 | Process Injection | Endpoint / EDR |
| 97 | T1046 | Network Service Discovery | Internal Network; Server / Workload |
| 98 | T1027.010 | Command Obfuscation | Endpoint / EDR |
| 99 | T1686.003 | Windows Host Firewall | Endpoint / EDR |
| 100 | T1543.002 | Systemd Service | Server / Workload |
| 101 | T1070.005 | Network Share Connection Removal | Internal Network |
| 102 | T1610 | Deploy Container | Server / Workload |
| 103 | T1686.002 | Network Device Firewall | Internal Network |
| 104 | T1685.001 | Disable or Modify Windows Event Log | Endpoint / EDR |
| 105 | T1070.007 | Clear Network Connection History and Configurations | Internal Network |
| 106 | T1685.004 | Disable or Modify Linux Audit System Log | Endpoint / EDR |
| 107 | T1505.005 | Terminal Services DLL | Endpoint / EDR; Server / Workload |
| 108 | T1216 | System Script Proxy Execution | Internal Network; Endpoint / EDR |
| 109 | T1127 | Trusted Developer Utilities Proxy Execution | Internal Network |
| 110 | T1055.012 | Process Hollowing | Endpoint / EDR |
| 111 | T1685.005 | Clear Windows Event Logs | Endpoint / EDR |
| 112 | T1059 | Command and Scripting Interpreter | Endpoint / EDR |
| 113 | T1091 | Replication Through Removable Media | Endpoint / EDR |
| 114 | T1546.003 | Windows Management Instrumentation Event Subscription | Endpoint / EDR |
| 115 | T1222.002 | Linux and Mac Permissions | Endpoint / EDR |
| 116 | T1547.004 | Winlogon Helper DLL | Endpoint / EDR |
| 117 | T1685.006 | Clear Linux or Mac System Logs | Endpoint / EDR |
| 118 | T1564.011 | Ignore Process Interrupts | Endpoint / EDR |
| 119 | T1609 | Container Administration Command | Endpoint / EDR; Server / Workload |
| 120 | T1546.010 | AppInit DLLs | Endpoint / EDR |
| 121 | T1202 | Indirect Command Execution | Endpoint / EDR |
| 122 | T1613 | Container and Resource Discovery | Server / Workload |
| 123 | T1220 | XSL Script Processing | Endpoint / EDR |
| 124 | T1059.008 | Network Device CLI | Internal Network |
| 125 | T1218 | System Binary Proxy Execution | Internal Network |
| 126 | T1546.007 | Netsh Helper DLL | Endpoint / EDR |
| 127 | T1574.011 | Services Registry Permissions Weakness | Endpoint / EDR; Server / Workload |
| 128 | T1135 | Network Share Discovery | Internal Network |
| 129 | T1569.002 | Service Execution | Server / Workload |
| 130 | T1059.007 | JavaScript | Endpoint / EDR |
| 131 | T1036.010 | Masquerade Account Name | Endpoint / EDR |
| 132 | T1098.006 | Additional Container Cluster Roles | Server / Workload |
| 133 | T1059.003 | Windows Command Shell | Endpoint / EDR |
| 134 | T1059.001 | PowerShell | Endpoint / EDR |
| 135 | T1047 | Windows Management Instrumentation | Endpoint / EDR |
| 136 | T1012 | Query Registry | Endpoint / EDR |
| 137 | T1007 | System Service Discovery | Server / Workload |
| 138 | T1566.003 | Spearphishing via Service | Server / Workload |
| 139 | T1559 | Inter-Process Communication | Endpoint / EDR |
| 140 | T1652 | Device Driver Discovery | Endpoint / EDR |
| 141 | T1569 | System Services | Server / Workload |
| 142 | T1669 | Wi-Fi Networks | Internal Network |
| 143 | T1559.003 | XPC Services | Server / Workload |
| 144 | T1675 | ESXi Administration Command | Endpoint / EDR; Server / Workload |
| 145 | T1564.010 | Process Argument Spoofing | Endpoint / EDR |
| 146 | T1036.009 | Break Process Trees | Endpoint / EDR |
| 147 | T1599 | Network Boundary Bridging | Internal Network |
| 148 | T1036.011 | Overwrite Process Arguments | Endpoint / EDR |
| 149 | T1599.001 | Network Address Translation Traversal | Internal Network |
| 150 | T1036.008 | Masquerade File Type | Endpoint / EDR |
| 151 | T1027.005 | Indicator Removal from Tools | Endpoint / EDR |
| 152 | T1059.002 | AppleScript | Endpoint / EDR |
| 153 | T1422 | System Network Configuration Discovery | Internal Network |
| 154 | T1406 | Obfuscated Files or Information | Endpoint / EDR |
| 155 | T1646 | Exfiltration Over C2 Channel | Internal Network |
| 156 | T1404 | Exploitation for Privilege Escalation | Endpoint / EDR |
| 157 | T1544 | Ingress Tool Transfer | Endpoint / EDR |
| 158 | T1532 | Archive Collected Data | Endpoint / EDR |
| 159 | T1424 | Process Discovery | Endpoint / EDR |
| 160 | T1509 | Non-Standard Port | Internal Network |
| 161 | T1421 | System Network Connections Discovery | Internal Network |
| 162 | T1655 | Masquerading | Endpoint / EDR |
| 163 | T1642 | Endpoint Denial of Service | Endpoint / EDR; Server / Workload |
| 164 | T1603 | Scheduled Task/Job | Server / Workload |
| 165 | T0881 | Service Stop | Server / Workload |
| 166 | T0867 | Lateral Tool Transfer | Endpoint / EDR |
| 167 | T1662 | Data Destruction | Endpoint / EDR |
| 168 | T1398 | Boot or Logon Initialization Scripts | Endpoint / EDR; Server / Workload |
| 169 | T0866 | Exploitation of Remote Services | Internal Network; Server / Workload |
| 170 | T0853 | Scripting | Endpoint / EDR |
| 171 | T0849 | Masquerading | Endpoint / EDR |
| 172 | T0814 | Denial of Service | Server / Workload |
| 173 | T0809 | Data Destruction | Endpoint / EDR |
| 174 | T0807 | Command-Line Interface | Endpoint / EDR |
| 175 | T0801 | Monitor Process State | Endpoint / EDR |
| 176 | T1692.001 | Command Message | Endpoint / EDR |
| 177 | T1639.001 | Exfiltration Over Unencrypted Non-C2 Protocol | Internal Network |
| 178 | T1471 | Data Encrypted for Impact | Endpoint / EDR |
| 179 | T0886 | Remote Services | Internal Network; Server / Workload |
| 180 | T0884 | Connection Proxy | Internal Network |
| 181 | T0842 | Network Sniffing | Internal Network |
| 182 | T1631 | Process Injection | Endpoint / EDR |
| 183 | T1630 | Indicator Removal on Host | Endpoint / EDR |
| 184 | T1623 | Command and Scripting Interpreter | Endpoint / EDR |
| 185 | T1604 | Proxy Through Victim | Internal Network |
| 186 | T1521 | Encrypted Channel | Endpoint / EDR |
| 187 | T1458 | Replication Through Removable Media | Endpoint / EDR |
| 188 | T1428 | Exploitation of Remote Services | Internal Network; Server / Workload |
| 189 | T0890 | Exploitation for Privilege Escalation | Endpoint / EDR |
| 190 | T0872 | Indicator Removal on Host | Endpoint / EDR |
| 191 | T0847 | Replication Through Removable Media | Endpoint / EDR |
| 192 | T0840 | Network Connection Enumeration | Internal Network |
| 193 | T1691.001 | Command Message | Endpoint / EDR |
| 194 | T1639 | Exfiltration Over Alternative Protocol | Endpoint / EDR |
| 195 | T1464 | Network Denial of Service | Internal Network; Server / Workload |
| 196 | T1423 | Network Service Scanning | Internal Network; Server / Workload |
| 197 | T0822 | External Remote Services | Internal Network; Server / Workload |
| 198 | T1628 | Hide Artifacts | Endpoint / EDR |
| 199 | T1444 | Masquerade as Legitimate Application | Endpoint / EDR |
| 200 | T1430.001 | Remote Device Management Services | Server / Workload |
| 201 | T0894 | System Binary Proxy Execution | Internal Network |
| 202 | T0841 | Network Service Scanning | Internal Network; Server / Workload |
