# Layer 1 Surface Context Matrix

Layer 1 surface context table for observation mapping and blast-radius hints.
This file is context only and does not provide runtime risk scores.

| rank | attack_id | attack_vector | surface_context |
| --- | --- | --- | --- |
| 1 | T1105 | Ingress Tool Transfer | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 2 | T1573.001 | Symmetric Cryptography | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 3 | T1056.001 | Keylogging | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 4 | T1132.001 | Standard Encoding | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 5 | T1074.001 | Local Data Staging | Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 6 | T1573.002 | Asymmetric Cryptography | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 7 | T1486 | Data Encrypted for Impact | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 8 | T1560.001 | Archive via Utility | SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 9 | T1119 | Automated Collection | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; Mobile |
| 10 | T1090 | Proxy | Public Internet / Edge; Network / Perimeter; Server / Workload; Endpoint / User; ESXi / Hypervisor; Mobile; ICS / OT |
| 11 | T1560 | Archive Collected Data | SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 12 | T1490 | Inhibit System Recovery | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor; Mobile |
| 13 | T1489 | Service Stop | Public Internet / Edge; Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 14 | T1485 | Data Destruction | Public Internet / Edge; Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 15 | T1048.003 | Exfiltration Over Unencrypted Non-C2 Protocol | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile; ICS / OT |
| 16 | T1657 | Financial Theft | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 17 | T1071.001 | Web Protocols | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 18 | T1005 | Data from Local System | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 19 | T1041 | Exfiltration Over C2 Channel | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 20 | T1113 | Screen Capture | Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 21 | T1571 | Non-Standard Port | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 22 | T1102.002 | Bidirectional Communication | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 23 | T1071.004 | DNS | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 24 | T1567.002 | Exfiltration to Cloud Storage | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 25 | T1560.003 | Archive via Custom Method | SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 26 | T1572 | Protocol Tunneling | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 27 | T1125 | Video Capture | Public Internet / Edge; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 28 | T1090.003 | Multi-hop Proxy | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 29 | T1090.001 | Internal Proxy | Public Internet / Edge; Network / Perimeter; Server / Workload; Endpoint / User; ESXi / Hypervisor; Mobile |
| 30 | T1529 | System Shutdown/Reboot | Public Internet / Edge; Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile; ICS / OT |
| 31 | T1001.003 | Protocol or Service Impersonation | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 32 | T1561.002 | Disk Structure Wipe | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 33 | T1132.002 | Non-Standard Encoding | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 34 | T1114.002 | Remote Email Collection | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 35 | T1561.001 | Disk Content Wipe | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 36 | T1573 | Encrypted Channel | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 37 | T1560.002 | Archive via Library | SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 38 | T1185 | Browser Session Hijacking | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 39 | T1491.001 | Internal Defacement | Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 40 | T1496.001 | Compute Hijacking | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 41 | T1074.002 | Remote Data Staging | Public Internet / Edge; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 42 | T1567 | Exfiltration Over Web Service | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 43 | T1056 | Input Capture | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 44 | T1074 | Data Staged | Public Internet / Edge; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 45 | T1048 | Exfiltration Over Alternative Protocol | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor; Mobile; ICS / OT |
| 46 | T1132 | Data Encoding | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 47 | T1213.006 | Databases | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 48 | T1048.002 | Exfiltration Over Asymmetric Encrypted Non-C2 Protocol | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; ICS / OT |
| 49 | T1665 | Hide Infrastructure | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User; ESXi / Hypervisor; Mobile |
| 50 | T1537 | Transfer Data to Cloud Account | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 51 | T1499 | Endpoint Denial of Service | Public Internet / Edge; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; Mobile |
| 52 | T1213 | Data from Information Repositories | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; Mobile |
| 53 | T1567.001 | Exfiltration to Code Repository | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 54 | T1491.002 | External Defacement | Public Internet / Edge; Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 55 | T1567.004 | Exfiltration Over Webhook | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 56 | T1499.004 | Application or System Exploitation | Public Internet / Edge; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 57 | T1011.001 | Exfiltration Over Bluetooth | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 58 | T1567.003 | Exfiltration to Text Storage Sites | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 59 | T1561 | Disk Wipe | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 60 | T1499.003 | Application Exhaustion Flood | Public Internet / Edge; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 61 | T1499.002 | Service Exhaustion Flood | Public Internet / Edge; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 62 | T1498.002 | Reflection Amplification | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 63 | T1496 | Resource Hijacking | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; Mobile |
| 64 | T1491 | Defacement | Public Internet / Edge; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 65 | T1052 | Exfiltration Over Physical Medium | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 66 | T1011 | Exfiltration Over Other Network Medium | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 67 | T1036.005 | Match Legitimate Resource Name or Location | Cloud Control Plane; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 68 | T1053.005 | Scheduled Task | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 69 | T1027 | Obfuscated Files or Information | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 70 | T1685 | Disable or Modify Tools | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor; Mobile |
| 71 | T1574.001 | DLL | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 72 | T1003.001 | LSASS Memory | Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 73 | T1548.002 | Bypass User Account Control | Identity / IAM; Server / Workload; Endpoint / User |
| 74 | T1505.003 | Web Shell | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 75 | T1036 | Masquerading | Cloud Control Plane; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 76 | T1480 | Execution Guardrails | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 77 | T1068 | Exploitation for Privilege Escalation | Public Internet / Edge; Identity / IAM; Cloud Control Plane; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 78 | T1552.001 | Credentials In Files | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 79 | T1133 | External Remote Services | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 80 | T1136.001 | Local Account | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor; Mobile |
| 81 | T1539 | Steal Web Session Cookie | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 82 | T1040 | Network Sniffing | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor; Mobile |
| 83 | T1210 | Exploitation of Remote Services | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 84 | T1078.002 | Domain Accounts | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; ESXi / Hypervisor |
| 85 | T1021.004 | SSH | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User; ESXi / Hypervisor |
| 86 | T1123 | Audio Capture | Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 87 | T1071.002 | File Transfer Protocols | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 88 | T1568.002 | Domain Generation Algorithms | Public Internet / Edge; Network / Perimeter; Server / Workload; Endpoint / User; ESXi / Hypervisor; ICS / OT |
| 89 | T1025 | Data from Removable Media | SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 90 | T1090.002 | External Proxy | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User; ESXi / Hypervisor; Mobile; ICS / OT |
| 91 | T1114.001 | Local Email Collection | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 92 | T1568 | Dynamic Resolution | Public Internet / Edge; Network / Perimeter; Server / Workload; Endpoint / User; ESXi / Hypervisor; ICS / OT |
| 93 | T1001.001 | Junk Data | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 94 | T1071 | Application Layer Protocol | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 95 | T1056.002 | GUI Input Capture | Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 96 | T1104 | Multi-Stage Channels | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; ICS / OT |
| 97 | T1001 | Data Obfuscation | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 98 | T1056.004 | Credential API Hooking | Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 99 | T1039 | Data from Network Shared Drive | SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 100 | T1001.002 | Steganography | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 101 | T1530 | Data from Cloud Storage | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; Mobile |
| 102 | T1213.002 | Sharepoint | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 103 | T1102.003 | One-Way Communication | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 104 | T1557.001 | Name Resolution Poisoning and SMB Relay | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 105 | T1052.001 | Exfiltration over USB | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 106 | T1568.001 | Fast Flux DNS | Public Internet / Edge; Network / Perimeter; Server / Workload; Endpoint / User; ESXi / Hypervisor |
| 107 | T1531 | Account Access Removal | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 108 | T1213.003 | Code Repositories | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 109 | T1565.002 | Transmitted Data Manipulation | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 110 | T1090.004 | Domain Fronting | Public Internet / Edge; Network / Perimeter; Server / Workload; Endpoint / User; ESXi / Hypervisor |
| 111 | T1213.005 | Messaging Applications | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 112 | T1056.003 | Web Portal Capture | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 113 | T1565.001 | Stored Data Manipulation | SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 114 | T1498 | Network Denial of Service | Public Internet / Edge; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; Mobile |
| 115 | T1602.002 | Network Device Configuration Dump | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 116 | T1565 | Data Manipulation | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 117 | T1213.001 | Confluence | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Data / Storage; Containers / Kubernetes |
| 118 | T1667 | Email Bombing | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 119 | T1568.003 | DNS Calculation | Public Internet / Edge; Network / Perimeter; Server / Workload; Endpoint / User; ESXi / Hypervisor |
| 120 | T1565.003 | Runtime Data Manipulation | Server / Workload; Data / Storage; Endpoint / User |
| 121 | T1498.001 | Direct Network Flood | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 122 | T1496.004 | Cloud Service Hijacking | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; Mobile |
| 123 | T1496.003 | SMS Pumping | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; Mobile |
| 124 | T1496.002 | Bandwidth Hijacking | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 125 | T1213.004 | Customer Relationship Management Software | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Data / Storage; Containers / Kubernetes; Mobile |
| 126 | T1048.001 | Exfiltration Over Symmetric Encrypted Non-C2 Protocol | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; ICS / OT |
| 127 | T1140 | Deobfuscate/Decode Files or Information | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 128 | T1070.004 | File Deletion | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 129 | T1547.001 | Registry Run Keys / Startup Folder | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User |
| 130 | T1112 | Modify Registry | Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 131 | T1555.003 | Credentials from Web Browsers | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 132 | T1021.002 | SMB/Windows Admin Shares | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 133 | T1070.006 | Timestomp | Cloud Control Plane; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 134 | T1021.001 | Remote Desktop Protocol | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User |
| 135 | T1078 | Valid Accounts | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor; Mobile |
| 136 | T1570 | Lateral Tool Transfer | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 137 | T1555 | Credentials from Password Stores | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; Mobile |
| 138 | T1027.015 | Compression | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 139 | T1070 | Indicator Removal | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor; Mobile |
| 140 | T1027.001 | Binary Padding | Public Internet / Edge; Server / Workload; Data / Storage; Endpoint / User |
| 141 | T1027.011 | Fileless Storage | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 142 | T1003.002 | Security Account Manager | Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 143 | T1686 | Disable or Modify System Firewall | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 144 | T1027.003 | Steganography | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 145 | T1134 | Access Token Manipulation | Public Internet / Edge; Identity / IAM; Cloud Control Plane; Server / Workload; Data / Storage; Endpoint / User |
| 146 | T1003.003 | NTDS | Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 147 | T1027.009 | Embedded Payloads | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 148 | T1554 | Compromise Host Software Binary | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 149 | T1003 | OS Credential Dumping | Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 150 | T1550.002 | Pass the Hash | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 151 | T1070.009 | Clear Persistence | Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 152 | T1484.001 | Group Policy Modification | Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 153 | T1222.001 | Windows Permissions | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User |
| 154 | T1480.001 | Environmental Keying | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 155 | T1136.002 | Domain Account | Identity / IAM; SaaS / Office / Email; Server / Workload; Endpoint / User |
| 156 | T1072 | Software Deployment Tools | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; Containers / Kubernetes; Mobile |
| 157 | T1021.006 | Windows Remote Management | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User |
| 158 | T1564 | Hide Artifacts | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 159 | T1543 | Create or Modify System Process | Identity / IAM; Cloud Control Plane; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 160 | T1534 | Internal Spearphishing | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; Mobile |
| 161 | T1176.001 | Browser Extensions | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 162 | T1111 | Multi-Factor Authentication Interception | Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 163 | T1098 | Account Manipulation | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor; Mobile |
| 164 | T1037.004 | RC Scripts | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 165 | T1037 | Boot or Logon Initialization Scripts | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 166 | T1021 | Remote Services | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 167 | T1564.005 | Hidden File System | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 168 | T1550.003 | Pass the Ticket | Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 169 | T1547 | Boot or Logon Autostart Execution | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 170 | T1528 | Steal Application Access Token | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 171 | T1218.001 | Compiled HTML File | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 172 | T1053.002 | At | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User |
| 173 | T1037.001 | Logon Script (Windows) | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User |
| 174 | T1611 | Escape to Host | Public Internet / Edge; Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 175 | T1556 | Modify Authentication Process | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; Mobile |
| 176 | T1552.006 | Group Policy Preferences | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 177 | T1552 | Unsecured Credentials | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; Mobile |
| 178 | T1546.011 | Application Shimming | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 179 | T1137.001 | Office Template Macros | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 180 | T1136 | Create Account | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor; Mobile |
| 181 | T1649 | Steal or Forge Authentication Certificates | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 182 | T1564.006 | Run Virtual Instance | Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 183 | T1564.002 | Hidden Users | Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 184 | T1556.006 | Multi-Factor Authentication | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 185 | T1547.012 | Print Processors | Identity / IAM; Cloud Control Plane; Server / Workload; Data / Storage; Endpoint / User |
| 186 | T1546 | Event Triggered Execution | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 187 | T1484.002 | Trust Modification | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Endpoint / User |
| 188 | T1021.003 | Distributed Component Object Model | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 189 | T1564.008 | Email Hiding Rules | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 190 | T1563.002 | RDP Hijacking | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User |
| 191 | T1556.007 | Hybrid Identity | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Endpoint / User; Containers / Kubernetes; Mobile |
| 192 | T1556.001 | Domain Controller Authentication | Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 193 | T1548 | Abuse Elevation Control Mechanism | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 194 | T1547.008 | LSASS Driver | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User |
| 195 | T1137 | Office Application Startup | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 196 | T1558 | Steal or Forge Kerberos Tickets | Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 197 | T1552.007 | Container API | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Endpoint / User; Containers / Kubernetes |
| 198 | T1550 | Use Alternate Authentication Material | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; Containers / Kubernetes |
| 199 | T1548.006 | TCC Manipulation | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 200 | T1222 | File and Directory Permissions Modification | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 201 | T1218.014 | MMC | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 202 | T1137.002 | Office Test | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 203 | T1053 | Scheduled Task/Job | Public Internet / Edge; Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor; Mobile |
| 204 | T1687 | Exploitation for Defense Impairment | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; Containers / Kubernetes |
| 205 | T1684 | Social Engineering | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 206 | T1606.001 | Web Cookies | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 207 | T1606 | Forge Web Credentials | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 208 | T1578 | Modify Cloud Compute Infrastructure | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Containers / Kubernetes; ESXi / Hypervisor |
| 209 | T1563 | Remote Service Session Hijacking | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User |
| 210 | T1556.008 | Network Provider DLL | Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 211 | T1547.003 | Time Providers | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 212 | T1543.005 | Container Service | Identity / IAM; Cloud Control Plane; Server / Workload; Endpoint / User; Containers / Kubernetes |
| 213 | T1535 | Unused/Unsupported Cloud Regions | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 214 | T1505 | Server Software Component | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; ESXi / Hypervisor; Mobile |
| 215 | T1484 | Domain or Tenant Policy Modification | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 216 | T1219 | Remote Access Tools | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 217 | T1219.002 | Remote Desktop Software | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 218 | T1557 | Adversary-in-the-Middle | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 219 | T1114 | Email Collection | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 220 | T1114.003 | Email Forwarding Rule | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 221 | T1205.002 | Socket Filters | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 222 | T1659 | Content Injection | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 223 | T1495 | Firmware Corruption | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 224 | T1497.003 | Time Based Checks | Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 225 | T1622 | Debugger Evasion | Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 226 | T1003.004 | LSA Secrets | Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 227 | T1684.001 | Impersonation | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; Containers / Kubernetes |
| 228 | T1078.003 | Local Accounts | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor; Mobile |
| 229 | T1564.004 | NTFS File Attributes | Public Internet / Edge; Server / Workload; Data / Storage; Endpoint / User |
| 230 | T1078.004 | Cloud Accounts | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; Mobile |
| 231 | T1053.003 | Cron | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 232 | T1555.004 | Windows Credential Manager | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 233 | T1134.002 | Create Process with Token | Identity / IAM; Server / Workload; Endpoint / User |
| 234 | T1555.001 | Keychain | Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 235 | T1080 | Taint Shared Content | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 236 | T1555.005 | Password Managers | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 237 | T1070.003 | Clear Command History | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 238 | T1021.005 | VNC | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 239 | T1690 | Prevent Command History Logging | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 240 | T1574.006 | Dynamic Linker Hijacking | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ICS / OT |
| 241 | T1552.002 | Credentials in Registry | Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 242 | T1027.004 | Compile After Delivery | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 243 | T1558.003 | Kerberoasting | Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 244 | T1542.003 | Bootkit | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 245 | T1036.001 | Invalid Code Signature | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User |
| 246 | T1003.005 | Cached Domain Credentials | Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 247 | T1679 | Selective Exclusion | Server / Workload; Data / Storage; Endpoint / User |
| 248 | T1547.013 | XDG Autostart Entries | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User |
| 249 | T1553.001 | Gatekeeper Bypass | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 250 | T1098.004 | SSH Authorized Keys | Public Internet / Edge; Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor; Mobile |
| 251 | T1078.001 | Default Accounts | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor; Mobile |
| 252 | T1558.001 | Golden Ticket | Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 253 | T1552.005 | Cloud Instance Metadata API | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 254 | T1550.001 | Application Access Token | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 255 | T1134.003 | Make and Impersonate Token | Identity / IAM; Server / Workload; Endpoint / User |
| 256 | T1110.002 | Password Cracking | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 257 | T1003.006 | DCSync | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 258 | T1558.002 | Silver Ticket | Identity / IAM; SaaS / Office / Email; Server / Workload; Endpoint / User |
| 259 | T1556.002 | Password Filter DLL | Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 260 | T1548.003 | Sudo and Sudo Caching | Identity / IAM; Cloud Control Plane; Server / Workload; Data / Storage; Endpoint / User |
| 261 | T1027.012 | LNK Icon Smuggling | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 262 | T1621 | Multi-Factor Authentication Request Generation | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Endpoint / User; Containers / Kubernetes; Mobile |
| 263 | T1556.004 | Network Device Authentication | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 264 | T1547.015 | Login Items | Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 265 | T1547.005 | Security Support Provider | Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 266 | T1136.003 | Cloud Account | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 267 | T1098.002 | Additional Email Delegate Permissions | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User |
| 268 | T1055.013 | Process Doppelgänging | Identity / IAM; Cloud Control Plane; Server / Workload; Data / Storage; Endpoint / User |
| 269 | T1027.006 | HTML Smuggling | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 270 | T1021.007 | Cloud Services | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 271 | T1003.007 | Proc Filesystem | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 272 | T1685.002 | Disable or Modify Cloud Log | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 273 | T1647 | Plist File Modification | Server / Workload; Data / Storage; Endpoint / User |
| 274 | T1564.009 | Resource Forking | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 275 | T1556.009 | Conditional Access Policies | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; Mobile |
| 276 | T1556.003 | Pluggable Authentication Modules | Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 277 | T1546.001 | Change Default File Association | Identity / IAM; Server / Workload; Endpoint / User |
| 278 | T1542.002 | Component Firmware | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 279 | T1505.006 | vSphere Installation Bundles | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 280 | T1211 | Exploitation for Stealth | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 281 | T1134.005 | SID-History Injection | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User |
| 282 | T1098.005 | Device Registration | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 283 | T1098.001 | Additional Cloud Credentials | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; Containers / Kubernetes; Mobile |
| 284 | T1606.002 | SAML Tokens | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Endpoint / User; Containers / Kubernetes |
| 285 | T1574.010 | Services File Permissions Weakness | Public Internet / Edge; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 286 | T1564.012 | File/Path Exclusions | Public Internet / Edge; Server / Workload; Data / Storage; Endpoint / User |
| 287 | T1563.001 | SSH Hijacking | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 288 | T1558.005 | Ccache Files | Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 289 | T1558.004 | AS-REP Roasting | Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 290 | T1555.002 | Securityd Memory | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 291 | T1552.008 | Chat Messages | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 292 | T1552.003 | Shell History | Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 293 | T1550.004 | Web Session Cookie | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 294 | T1548.004 | Elevated Execution with Prompt | Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 295 | T1547.014 | Active Setup | Identity / IAM; Server / Workload; Endpoint / User |
| 296 | T1547.002 | Authentication Package | Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User |
| 297 | T1546.013 | PowerShell Profile | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 298 | T1546.009 | AppCert DLLs | Identity / IAM; Cloud Control Plane; Server / Workload; Endpoint / User |
| 299 | T1546.002 | Screensaver | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 300 | T1212 | Exploitation for Credential Access | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 301 | T1207 | Rogue Domain Controller | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 302 | T1003.008 | /etc/passwd and /etc/shadow | Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 303 | T1671 | Cloud Application Integration | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 304 | T1668 | Exclusive Control | Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 305 | T1612 | Build Image on Host | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User; Containers / Kubernetes |
| 306 | T1564.013 | Bind Mounts | Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 307 | T1564.007 | VBA Stomping | Public Internet / Edge; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 308 | T1556.005 | Reversible Encryption | Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 309 | T1553.003 | SIP and Trust Provider Hijacking | Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 310 | T1548.005 | Temporary Elevated Cloud Access | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Endpoint / User; Containers / Kubernetes |
| 311 | T1547.007 | Re-opened Applications | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User |
| 312 | T1546.014 | Emond | Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 313 | T1525 | Implant Internal Image | Public Internet / Edge; Identity / IAM; Cloud Control Plane; Server / Workload; Endpoint / User; Containers / Kubernetes |
| 314 | T1053.007 | Container Orchestration Job | Public Internet / Edge; Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User; Containers / Kubernetes |
| 315 | T1037.003 | Network Logon Script | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 316 | T1027.017 | SVG Smuggling | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 317 | T1021.008 | Direct Cloud VM Connections | Public Internet / Edge; Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 318 | T1082 | System Information Discovery | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor; Mobile |
| 319 | T1027.013 | Encrypted/Encoded File | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 320 | T1543.003 | Windows Service | Public Internet / Edge; Identity / IAM; Cloud Control Plane; Server / Workload; Endpoint / User |
| 321 | T1095 | Non-Application Layer Protocol | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 322 | T1218.011 | Rundll32 | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 323 | T1124 | System Time Discovery | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 324 | T1018 | Remote System Discovery | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 325 | T1564.003 | Hidden Window | Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 326 | T1059.004 | Unix Shell | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User; ESXi / Hypervisor; Mobile |
| 327 | T1059.006 | Python | Public Internet / Edge; Network / Perimeter; Server / Workload; Endpoint / User; ESXi / Hypervisor; Mobile |
| 328 | T1008 | Fallback Channels | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 329 | T1190 | Exploit Public-Facing Application | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor; Mobile |
| 330 | T1518 | Software Discovery | Public Internet / Edge; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor; Mobile |
| 331 | T1102 | Web Service | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 332 | T1189 | Drive-by Compromise | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 333 | T1102.001 | Dead Drop Resolver | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 334 | T1020 | Automated Exfiltration | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 335 | T1071.003 | Mail Protocols | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 336 | T1205 | Traffic Signaling | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 337 | T1029 | Scheduled Transfer | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 338 | T1205.001 | Port Knocking | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 339 | T1092 | Communication Through Removable Media | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 340 | T1557.004 | Evil Twin | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 341 | T1219.001 | IDE Tunneling | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 342 | T1071.005 | Publish/Subscribe Protocols | Public Internet / Edge; Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 343 | T1602.001 | SNMP (MIB Dump) | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 344 | T1557.003 | DHCP Spoofing | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 345 | T1499.001 | OS Exhaustion Flood | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 346 | T1083 | File and Directory Discovery | Public Internet / Edge; Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 347 | T1057 | Process Discovery | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 348 | T1016 | System Network Configuration Discovery | Public Internet / Edge; Network / Perimeter; Server / Workload; Endpoint / User; ESXi / Hypervisor; Mobile |
| 349 | T1518.001 | Security Software Discovery | Public Internet / Edge; Cloud Control Plane; Server / Workload; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 350 | T1680 | Local Storage Discovery | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 351 | T1049 | System Network Connections Discovery | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor; Mobile |
| 352 | T1036.004 | Masquerade Task or Service | Server / Workload; Endpoint / User |
| 353 | T1055 | Process Injection | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 354 | T1566.002 | Spearphishing Link | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; Mobile |
| 355 | T1497.001 | System Checks | Network / Perimeter; Server / Workload; Endpoint / User; ESXi / Hypervisor; Mobile |
| 356 | T1055.001 | Dynamic-link Library Injection | Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 357 | T1046 | Network Service Discovery | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User; Containers / Kubernetes; Mobile |
| 358 | T1027.010 | Command Obfuscation | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User |
| 359 | T1087.001 | Local Account | Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 360 | T1564.001 | Hidden Files and Directories | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 361 | T1087.002 | Domain Account | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User |
| 362 | T1120 | Peripheral Device Discovery | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 363 | T1115 | Clipboard Data | SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 364 | T1218.010 | Regsvr32 | Public Internet / Edge; Network / Perimeter; Server / Workload; Endpoint / User |
| 365 | T1620 | Reflective Code Loading | Server / Workload; Data / Storage; Endpoint / User; ICS / OT |
| 366 | T1482 | Domain Trust Discovery | Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User |
| 367 | T1014 | Rootkit | Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 368 | T1547.009 | Shortcut Modification | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 369 | T1218.007 | Msiexec | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 370 | T1218.005 | Mshta | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 371 | T1614 | System Location Discovery | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 372 | T1217 | Browser Information Discovery | Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 373 | T1016.001 | Internet Connection Discovery | Public Internet / Edge; Network / Perimeter; Server / Workload; Endpoint / User; ESXi / Hypervisor |
| 374 | T1030 | Data Transfer Size Limits | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 375 | T1552.004 | Private Keys | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 376 | T1686.003 | Windows Host Firewall | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 377 | T1197 | BITS Jobs | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 378 | T1543.002 | Systemd Service | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 379 | T1087.003 | Email Account | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Endpoint / User |
| 380 | T1566 | Phishing | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 381 | T1574 | Hijack Execution Flow | Server / Workload; Data / Storage; Endpoint / User |
| 382 | T1087 | Account Discovery | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 383 | T1497.002 | User Activity Based Checks | Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 384 | T1201 | Password Policy Discovery | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; Containers / Kubernetes; Mobile |
| 385 | T1218.004 | InstallUtil | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 386 | T1553.004 | Install Root Certificate | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 387 | T1195.001 | Compromise Software Dependencies and Development Tools | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 388 | T1195 | Supply Chain Compromise | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 389 | T1070.005 | Network Share Connection Removal | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User |
| 390 | T1610 | Deploy Container | Public Internet / Edge; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; Containers / Kubernetes |
| 391 | T1218.003 | CMSTP | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 392 | T1204 | User Execution | Public Internet / Edge; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 393 | T1137.006 | Add-ins | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 394 | T1070.008 | Clear Mailbox Data | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 395 | T1686.002 | Network Device Firewall | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 396 | T1685.001 | Disable or Modify Windows Event Log | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 397 | T1547.006 | Kernel Modules and Extensions | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 398 | T1542.001 | System Firmware | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 399 | T1505.004 | IIS Components | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 400 | T1127.001 | MSBuild | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 401 | T1070.007 | Clear Network Connection History and Configurations | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 402 | T1574.012 | COR_PROFILER | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User |
| 403 | T1553 | Subvert Trust Controls | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 404 | T1218.002 | Control Panel | Public Internet / Edge; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 405 | T1137.004 | Outlook Home Page | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Endpoint / User |
| 406 | T1685.004 | Disable or Modify Linux Audit System Log | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 407 | T1677 | Poisoned Pipeline Execution | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 408 | T1538 | Cloud Service Dashboard | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 409 | T1505.002 | Transport Agent | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 410 | T1218.015 | Electron Applications | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 411 | T1218.013 | Mavinject | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 412 | T1218.012 | Verclsid | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User |
| 413 | T1218.009 | Regsvcs/Regasm | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 414 | T1216.001 | PubPrn | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 415 | T1204.003 | Malicious Image | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User; Containers / Kubernetes |
| 416 | T1137.005 | Outlook Rules | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Endpoint / User |
| 417 | T1137.003 | Outlook Forms | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Endpoint / User |
| 418 | T1059.013 | Container CLI/API | Public Internet / Edge; Cloud Control Plane; Server / Workload; Endpoint / User; Containers / Kubernetes |
| 419 | T1027.018 | Invisible Unicode | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 420 | T1547.010 | Port Monitors | Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 421 | T1542 | Pre-OS Boot | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 422 | T1505.005 | Terminal Services DLL | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ICS / OT |
| 423 | T1485.001 | Lifecycle-Triggered Deletion | Public Internet / Edge; Cloud Control Plane; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 424 | T1216 | System Script Proxy Execution | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 425 | T1176 | Software Extensions | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 426 | T1127 | Trusted Developer Utilities Proxy Execution | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 427 | T1020.001 | Traffic Duplication | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; Mobile |
| 428 | T1110 | Brute Force | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor; Mobile |
| 429 | T1055.012 | Process Hollowing | Identity / IAM; Cloud Control Plane; Server / Workload; Data / Storage; Endpoint / User |
| 430 | T1685.005 | Clear Windows Event Logs | Public Internet / Edge; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 431 | T1059 | Command and Scripting Interpreter | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor; Mobile |
| 432 | T1091 | Replication Through Removable Media | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 433 | T1497 | Virtualization/Sandbox Evasion | Server / Workload; Endpoint / User; ESXi / Hypervisor |
| 434 | T1546.003 | Windows Management Instrumentation Event Subscription | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User |
| 435 | T1543.001 | Launch Agent | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User |
| 436 | T1678 | Delay Execution | Public Internet / Edge; Cloud Control Plane; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 437 | T1222.002 | Linux and Mac Permissions | Server / Workload; Data / Storage; Endpoint / User |
| 438 | T1055.002 | Portable Executable Injection | Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 439 | T1547.004 | Winlogon Helper DLL | Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User |
| 440 | T1055.004 | Asynchronous Procedure Call | Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User |
| 441 | T1546.015 | Component Object Model Hijacking | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User |
| 442 | T1199 | Trusted Relationship | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; Containers / Kubernetes |
| 443 | T1069 | Permission Groups Discovery | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 444 | T1036.003 | Rename Legitimate Utilities | Server / Workload; Data / Storage; Endpoint / User |
| 445 | T1654 | Log Enumeration | Public Internet / Edge; Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 446 | T1543.004 | Launch Daemon | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User |
| 447 | T1221 | Template Injection | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 448 | T1685.006 | Clear Linux or Mac System Logs | Public Internet / Edge; Identity / IAM; Server / Workload; Data / Storage; Endpoint / User |
| 449 | T1564.011 | Ignore Process Interrupts | Network / Perimeter; Server / Workload; Endpoint / User |
| 450 | T1688 | Safe Mode Boot | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 451 | T1546.008 | Accessibility Features | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 452 | T1546.004 | Unix Shell Configuration Modification | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 453 | T1673 | Virtual Machine Discovery | Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 454 | T1609 | Container Administration Command | Cloud Control Plane; Server / Workload; Endpoint / User; Containers / Kubernetes |
| 455 | T1553.006 | Code Signing Policy Modification | Public Internet / Edge; Server / Workload; Data / Storage; Endpoint / User |
| 456 | T1526 | Cloud Service Discovery | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 457 | T1087.004 | Cloud Account | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; Containers / Kubernetes |
| 458 | T1059.009 | Cloud API | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 459 | T1036.007 | Double File Extension | Public Internet / Edge; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 460 | T1036.002 | Right-to-Left Override | Public Internet / Edge; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 461 | T1651 | Cloud Administration Command | Public Internet / Edge; Identity / IAM; Cloud Control Plane; Server / Workload; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 462 | T1580 | Cloud Infrastructure Discovery | Public Internet / Edge; Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 463 | T1574.007 | Path Interception by PATH Environment Variable | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 464 | T1546.010 | AppInit DLLs | Identity / IAM; Cloud Control Plane; Server / Workload; Endpoint / User |
| 465 | T1202 | Indirect Command Execution | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 466 | T1059.012 | Hypervisor CLI | Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 467 | T1055.003 | Thread Execution Hijacking | Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User |
| 468 | T1613 | Container and Resource Discovery | Public Internet / Edge; Cloud Control Plane; Server / Workload; Containers / Kubernetes |
| 469 | T1220 | XSL Script Processing | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 470 | T1218.008 | Odbcconf | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 471 | T1187 | Forced Authentication | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 472 | T1069.003 | Cloud Groups | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Endpoint / User; Containers / Kubernetes |
| 473 | T1059.008 | Network Device CLI | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 474 | T1006 | Direct Volume Access | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 475 | T1689 | Downgrade Attack | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 476 | T1653 | Power Settings | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 477 | T1574.009 | Path Interception by Unquoted Path | Server / Workload; Data / Storage; Endpoint / User |
| 478 | T1574.008 | Path Interception by Search Order Hijacking | Server / Workload; Data / Storage; Endpoint / User |
| 479 | T1548.001 | Setuid and Setgid | Identity / IAM; Cloud Control Plane; Server / Workload; Data / Storage; Endpoint / User |
| 480 | T1546.016 | Installer Packages | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User |
| 481 | T1546.012 | Image File Execution Options Injection | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 482 | T1218 | System Binary Proxy Execution | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 483 | T1055.005 | Thread Local Storage | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 484 | T1036.006 | Space after Filename | Public Internet / Edge; Server / Workload; Data / Storage; Endpoint / User |
| 485 | T1027.008 | Stripped Payloads | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 486 | T1685.003 | Modify or Spoof Tool UI | Server / Workload; Endpoint / User |
| 487 | T1648 | Serverless Execution | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 488 | T1601.001 | Patch System Image | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 489 | T1601 | Modify System Image | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 490 | T1574.014 | AppDomainManager | Server / Workload; Data / Storage; Endpoint / User |
| 491 | T1574.005 | Executable Installer File Permissions Weakness | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 492 | T1546.017 | Udev Rules | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 493 | T1546.007 | Netsh Helper DLL | Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User |
| 494 | T1505.001 | SQL Stored Procedures | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User |
| 495 | T1176.002 | IDE Extensions | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 496 | T1070.010 | Relocate Malware | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 497 | T1055.015 | ListPlanting | Identity / IAM; Cloud Control Plane; Server / Workload; Endpoint / User |
| 498 | T1037.005 | Startup Items | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User |
| 499 | T1036.012 | Browser Fingerprint | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User |
| 500 | T1027.014 | Polymorphic Code | Server / Workload; Data / Storage; Endpoint / User |
| 501 | T1601.002 | Downgrade System Image | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 502 | T1600.002 | Disable Crypto Hardware | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 503 | T1600.001 | Reduce Key Space | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 504 | T1600 | Weaken Encryption | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 505 | T1574.011 | Services Registry Permissions Weakness | Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User |
| 506 | T1564.014 | Extended Attributes | Server / Workload; Data / Storage; Endpoint / User |
| 507 | T1546.018 | Python Startup Hooks | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 508 | T1546.006 | LC_LOAD_DYLIB Addition | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User |
| 509 | T1546.005 | Trap | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User |
| 510 | T1542.005 | TFTP Boot | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 511 | T1542.004 | ROMMONkit | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 512 | T1216.002 | SyncAppvPublishingServer | Network / Perimeter; Server / Workload; Endpoint / User; ESXi / Hypervisor |
| 513 | T1127.003 | JamPlus | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 514 | T1127.002 | ClickOnce | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 515 | T1055.014 | VDSO Hijacking | Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User |
| 516 | T1055.009 | Proc Memory | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 517 | T1053.006 | Systemd Timers | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User |
| 518 | T1037.002 | Login Hook | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User |
| 519 | T1566.001 | Spearphishing Attachment | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 520 | T1059.005 | Visual Basic | Public Internet / Edge; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User |
| 521 | T1135 | Network Share Discovery | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 522 | T1569.002 | Service Execution | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User |
| 523 | T1059.007 | JavaScript | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 524 | T1203 | Exploitation for Client Execution | Public Internet / Edge; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 525 | T1134.001 | Token Impersonation/Theft | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 526 | T1110.003 | Password Spraying | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor; Mobile |
| 527 | T1110.001 | Password Guessing | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor; Mobile |
| 528 | T1098.007 | Additional Local or Domain Groups | Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 529 | T1036.010 | Masquerade Account Name | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 530 | T1555.006 | Cloud Secrets Management Stores | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 531 | T1553.005 | Mark-of-the-Web Bypass | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 532 | T1134.004 | Parent PID Spoofing | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User |
| 533 | T1110.004 | Credential Stuffing | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor; Mobile |
| 534 | T1098.003 | Additional Cloud Roles | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 535 | T1578.003 | Delete Cloud Instance | Public Internet / Edge; Cloud Control Plane; Server / Workload; Containers / Kubernetes; ESXi / Hypervisor |
| 536 | T1578.002 | Create Cloud Instance | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Containers / Kubernetes; ESXi / Hypervisor |
| 537 | T1686.001 | Cloud Firewall | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 538 | T1578.001 | Create Snapshot | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Containers / Kubernetes; ESXi / Hypervisor |
| 539 | T1666 | Modify Cloud Resource Hierarchy | Public Internet / Edge; Identity / IAM; Cloud Control Plane; Server / Workload; Endpoint / User; Containers / Kubernetes |
| 540 | T1578.005 | Modify Cloud Compute Configurations | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 541 | T1578.004 | Revert Cloud Instance | Public Internet / Edge; Cloud Control Plane; Server / Workload; Data / Storage; Containers / Kubernetes; ESXi / Hypervisor |
| 542 | T1098.006 | Additional Container Cluster Roles | Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Endpoint / User; Containers / Kubernetes |
| 543 | T1059.003 | Windows Command Shell | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 544 | T1033 | System Owner/User Discovery | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 545 | T1106 | Native API | Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 546 | T1059.001 | PowerShell | Public Internet / Edge; Server / Workload; Endpoint / User |
| 547 | T1204.002 | Malicious File | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 548 | T1047 | Windows Management Instrumentation | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 549 | T1012 | Query Registry | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 550 | T1204.001 | Malicious Link | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 551 | T1007 | System Service Discovery | Server / Workload; Endpoint / User |
| 552 | T1129 | Shared Modules | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 553 | T1566.003 | Spearphishing via Service | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 554 | T1559 | Inter-Process Communication | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 555 | T1195.002 | Compromise Software Supply Chain | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 556 | T1615 | Group Policy Discovery | Public Internet / Edge; Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 557 | T1569.001 | Launchctl | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 558 | T1059.011 | Lua | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 559 | T1652 | Device Driver Discovery | Public Internet / Edge; Cloud Control Plane; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 560 | T1204.004 | Malicious Copy and Paste | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 561 | T1557.002 | ARP Cache Poisoning | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 562 | T1674 | Input Injection | Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 563 | T1569.003 | Systemctl | Server / Workload; Data / Storage; Endpoint / User |
| 564 | T1200 | Hardware Additions | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 565 | T1602 | Data from Configuration Repository | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 566 | T1569 | System Services | Server / Workload; Data / Storage; Endpoint / User |
| 567 | T1219.003 | Remote Access Hardware | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 568 | T1195.003 | Compromise Hardware Supply Chain | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 569 | T1614.001 | System Language Discovery | Cloud Control Plane; Server / Workload; Data / Storage; Endpoint / User |
| 570 | T1010 | Application Window Discovery | Cloud Control Plane; Server / Workload; Data / Storage; Endpoint / User |
| 571 | T1069.002 | Domain Groups | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User |
| 572 | T1559.001 | Component Object Model | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User |
| 573 | T1559.002 | Dynamic Data Exchange | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 574 | T1059.010 | AutoHotKey & AutoIT | Public Internet / Edge; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 575 | T1016.002 | Wi-Fi Discovery | Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 576 | T1669 | Wi-Fi Networks | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 577 | T1518.002 | Backup Software Discovery | Server / Workload; Data / Storage; Endpoint / User |
| 578 | T1204.005 | Malicious Library | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 579 | T1559.003 | XPC Services | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User |
| 580 | T1553.002 | Code Signing | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User |
| 581 | T1027.007 | Dynamic API Resolution | Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 582 | T1619 | Cloud Storage Object Discovery | Public Internet / Edge; Cloud Control Plane; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes |
| 583 | T1675 | ESXi Administration Command | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 584 | T1574.013 | KernelCallbackTable | Cloud Control Plane; Server / Workload; Data / Storage; Endpoint / User; ICS / OT |
| 585 | T1564.010 | Process Argument Spoofing | Cloud Control Plane; Server / Workload; Data / Storage; Endpoint / User |
| 586 | T1055.011 | Extra Window Memory Injection | Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 587 | T1036.009 | Break Process Trees | Cloud Control Plane; Server / Workload; Endpoint / User |
| 588 | T1599 | Network Boundary Bridging | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Mobile |
| 589 | T1566.004 | Spearphishing Voice | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Endpoint / User |
| 590 | T1055.008 | Ptrace System Calls | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 591 | T1036.011 | Overwrite Process Arguments | Server / Workload; Data / Storage; Endpoint / User |
| 592 | T1684.002 | Email Spoofing | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 593 | T1599.001 | Network Address Translation Traversal | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 594 | T1027.016 | Junk Code Insertion | Server / Workload; Data / Storage; Endpoint / User |
| 595 | T1480.002 | Mutual Exclusion | Cloud Control Plane; Server / Workload; Data / Storage; Endpoint / User |
| 596 | T1036.008 | Masquerade File Type | Server / Workload; Data / Storage; Endpoint / User |
| 597 | T1027.005 | Indicator Removal from Tools | Public Internet / Edge; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 598 | T1574.004 | Dylib Hijacking | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 599 | T1069.001 | Local Groups | Server / Workload; Endpoint / User |
| 600 | T1059.002 | AppleScript | Server / Workload; Endpoint / User |
| 601 | T1027.002 | Software Packing | Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 602 | T1598.003 | Spearphishing Link | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 603 | T1585.001 | Social Media Accounts | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User |
| 604 | T1583 | Acquire Infrastructure | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload |
| 605 | T1588.004 | Digital Certificates | Public Internet / Edge; Identity / IAM; Network / Perimeter; Data / Storage |
| 606 | T1598 | Phishing for Information | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Data / Storage; Endpoint / User |
| 607 | T1585 | Establish Accounts | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; Containers / Kubernetes |
| 608 | T1598.002 | Spearphishing Attachment | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Endpoint / User |
| 609 | T1587 | Develop Capabilities | Public Internet / Edge; Network / Perimeter; Server / Workload; Endpoint / User |
| 610 | T1586.001 | Social Media Accounts | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 611 | T1598.001 | Spearphishing Service | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User |
| 612 | T1588 | Obtain Capabilities | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 613 | T1586 | Compromise Accounts | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User |
| 614 | T1584 | Compromise Infrastructure | Public Internet / Edge; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Mobile |
| 615 | T1588.002 | Tool | Network / Perimeter; Endpoint / User |
| 616 | T1583.001 | Domains | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 617 | T1583.006 | Web Services | Public Internet / Edge; SaaS / Office / Email; Server / Workload; Data / Storage |
| 618 | T1608.001 | Upload Malware | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Containers / Kubernetes; ESXi / Hypervisor |
| 619 | T1587.001 | Malware | Public Internet / Edge; Network / Perimeter; Server / Workload; Endpoint / User |
| 620 | T1588.001 | Malware | Public Internet / Edge; Network / Perimeter; Server / Workload; Endpoint / User |
| 621 | T1583.003 | Virtual Private Server | Public Internet / Edge; Cloud Control Plane; Server / Workload; Containers / Kubernetes; ESXi / Hypervisor |
| 622 | T1589.002 | Email Addresses | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 623 | T1595.002 | Vulnerability Scanning | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage |
| 624 | T1589 | Gather Victim Identity Information | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 625 | T1584.004 | Server | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload |
| 626 | T1608.004 | Drive-by Target | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 627 | T1584.001 | Domains | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User |
| 628 | T1583.004 | Server | Public Internet / Edge; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload |
| 629 | T1594 | Search Victim-Owned Websites | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Data / Storage; Endpoint / User |
| 630 | T1584.006 | Web Services | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 631 | T1587.003 | Digital Certificates | Public Internet / Edge; Identity / IAM; Network / Perimeter; Data / Storage |
| 632 | T1584.008 | Network Devices | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Mobile |
| 633 | T1608.005 | Link Target | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Endpoint / User |
| 634 | T1592.002 | Software | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 635 | T1608.002 | Upload Tool | Public Internet / Edge; Network / Perimeter; Server / Workload; Endpoint / User |
| 636 | T1598.004 | Spearphishing Voice | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter |
| 637 | T1595.003 | Wordlist Scanning | Public Internet / Edge; Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 638 | T1595.001 | Scanning IP Blocks | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage |
| 639 | T1584.003 | Virtual Private Server | Public Internet / Edge; Cloud Control Plane; Server / Workload; Containers / Kubernetes; ESXi / Hypervisor |
| 640 | T1584.002 | DNS Server | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage |
| 641 | T1583.008 | Malvertising | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User |
| 642 | T1608.006 | SEO Poisoning | Public Internet / Edge; SaaS / Office / Email; Endpoint / User |
| 643 | T1608.003 | Install Digital Certificate | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 644 | T1608 | Stage Capabilities | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 645 | T1592.004 | Client Configurations | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ESXi / Hypervisor |
| 646 | T1592 | Gather Victim Host Information | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 647 | T1595 | Active Scanning | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage |
| 648 | T1592.001 | Hardware | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 649 | T1584.007 | Serverless | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User; ICS / OT |
| 650 | T1583.007 | Serverless | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User; ICS / OT |
| 651 | T1588.003 | Code Signing Certificates | Endpoint / User |
| 652 | T1587.002 | Code Signing Certificates | Endpoint / User |
| 653 | T1636.004 | SMS Messages | Cloud Control Plane; SaaS / Office / Email; Data / Storage; Endpoint / User; Mobile |
| 654 | T1430 | Location Tracking | Public Internet / Edge; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 655 | T1636.003 | Contact List | SaaS / Office / Email; Data / Storage; Endpoint / User; Mobile |
| 656 | T1426 | System Information Discovery | Endpoint / User; Mobile |
| 657 | T1533 | Data from Local System | Identity / IAM; SaaS / Office / Email; Data / Storage; Endpoint / User; Mobile |
| 658 | T1429 | Audio Capture | SaaS / Office / Email; Data / Storage; Endpoint / User; Mobile |
| 659 | T1418 | Software Discovery | Endpoint / User; Mobile |
| 660 | T1437.001 | Web Protocols | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 661 | T1422 | System Network Configuration Discovery | Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 662 | T1406 | Obfuscated Files or Information | Network / Perimeter; Data / Storage; Endpoint / User; Mobile |
| 663 | T1655.001 | Match Legitimate Name or Location | Data / Storage; Endpoint / User; Mobile |
| 664 | T1512 | Video Capture | Cloud Control Plane; SaaS / Office / Email; Data / Storage; Endpoint / User; Mobile |
| 665 | T1636.002 | Call Log | Cloud Control Plane; SaaS / Office / Email; Data / Storage; Endpoint / User; Mobile |
| 666 | T1407 | Download New Code at Runtime | Public Internet / Edge; Endpoint / User; Mobile |
| 667 | T1582 | SMS Control | Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 668 | T1409 | Stored Application Data | SaaS / Office / Email; Data / Storage; Endpoint / User; Mobile |
| 669 | T1417.002 | GUI Input Capture | Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Data / Storage; Endpoint / User; Mobile |
| 670 | T1646 | Exfiltration Over C2 Channel | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 671 | T1513 | Screen Capture | Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 672 | T1628.001 | Suppress Application Icon | Endpoint / User; Mobile |
| 673 | T1624.001 | Broadcast Receivers | Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 674 | T1417.001 | Keylogging | Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 675 | T1630.002 | File Deletion | SaaS / Office / Email; Data / Storage; Endpoint / User; Mobile |
| 676 | T1585.002 | Email Accounts | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload |
| 677 | T1422.001 | Internet Connection Discovery | Public Internet / Edge; Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 678 | T1644 | Out of Band Data | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 679 | T1420 | File and Directory Discovery | Public Internet / Edge; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 680 | T1404 | Exploitation for Privilege Escalation | Public Internet / Edge; Identity / IAM; Server / Workload; Endpoint / User; Mobile |
| 681 | T1660 | Phishing | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 682 | T1616 | Call Control | SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 683 | T1643 | Generate Traffic from Victim | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 684 | T1633.001 | System Checks | Network / Perimeter; Endpoint / User; ESXi / Hypervisor; Mobile |
| 685 | T1544 | Ingress Tool Transfer | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 686 | T1586.002 | Email Accounts | Public Internet / Edge; Identity / IAM; SaaS / Office / Email |
| 687 | T1517 | Access Notifications | Identity / IAM; SaaS / Office / Email; Data / Storage; Endpoint / User; Mobile |
| 688 | T1516 | Input Injection | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 689 | T1532 | Archive Collected Data | SaaS / Office / Email; Network / Perimeter; Data / Storage; Endpoint / User; Mobile |
| 690 | T1629.003 | Disable or Modify Tools | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 691 | T1424 | Process Discovery | Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 692 | T1422.002 | Wi-Fi Discovery | Identity / IAM; Network / Perimeter; Endpoint / User; Mobile |
| 693 | T1575 | Native API | Cloud Control Plane; Server / Workload; Endpoint / User; Mobile |
| 694 | T1632.001 | Code Signing Policy Modification | Data / Storage; Endpoint / User; Mobile |
| 695 | T1629.001 | Prevent Application Removal | Cloud Control Plane; Data / Storage; Endpoint / User; Mobile |
| 696 | T1626.001 | Device Administrator Permissions | Identity / IAM; Cloud Control Plane; Server / Workload; Endpoint / User; Mobile |
| 697 | T1645 | Compromise Client Software Binary | Identity / IAM; Server / Workload; Endpoint / User; Mobile |
| 698 | T1509 | Non-Standard Port | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 699 | T1453 | Abuse Accessibility Features | Identity / IAM; SaaS / Office / Email; Data / Storage; Endpoint / User; Mobile |
| 700 | T1421 | System Network Connections Discovery | Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 701 | T1630.001 | Uninstall Malicious Application | Cloud Control Plane; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 702 | T1623.001 | Unix Shell | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 703 | T1591 | Gather Victim Org Information | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Data / Storage |
| 704 | T1521.002 | Asymmetric Cryptography | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 705 | T0869 | Standard Application Layer Protocol | Network / Perimeter; Server / Workload; Mobile; ICS / OT |
| 706 | T0828 | Loss of Productivity and Revenue | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 707 | T1636.001 | Calendar Entries | SaaS / Office / Email; Data / Storage; Endpoint / User; Mobile |
| 708 | T1628.002 | User Evasion | Endpoint / User; Mobile |
| 709 | T1593 | Search Open Websites/Domains | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage |
| 710 | T1541 | Foreground Persistence | Identity / IAM; Cloud Control Plane; Server / Workload; Endpoint / User; Mobile |
| 711 | T1406.002 | Software Packing | Data / Storage; Endpoint / User; Mobile |
| 712 | T0865 | Spearphishing Attachment | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Endpoint / User; ICS / OT |
| 713 | T1655 | Masquerading | Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 714 | T1642 | Endpoint Denial of Service | Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 715 | T1603 | Scheduled Task/Job | Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 716 | T1589.001 | Credentials | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 717 | T1584.005 | Botnet | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload |
| 718 | T1521.001 | Symmetric Cryptography | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 719 | T1481.001 | Dead Drop Resolver | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 720 | T1474.003 | Compromise Software Supply Chain | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Data / Storage; Endpoint / User; Mobile |
| 721 | T1456 | Drive-By Compromise | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Endpoint / User; Mobile |
| 722 | T1414 | Clipboard Data | Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Data / Storage; Endpoint / User; Mobile |
| 723 | T0888 | Remote System Information Discovery | Cloud Control Plane; Network / Perimeter; Server / Workload; ICS / OT |
| 724 | T0881 | Service Stop | Server / Workload; Data / Storage; Endpoint / User; ICS / OT |
| 725 | T0867 | Lateral Tool Transfer | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ICS / OT |
| 726 | T0817 | Drive-by Compromise | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; ICS / OT |
| 727 | T1662 | Data Destruction | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 728 | T1637.001 | Domain Generation Algorithms | Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 729 | T1636.005 | Accounts | Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 730 | T1593.003 | Code Repositories | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 731 | T1591.004 | Identify Roles | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Data / Storage |
| 732 | T1590.004 | Network Topology | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Mobile |
| 733 | T1481.002 | Bidirectional Communication | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 734 | T1461 | Lockscreen Bypass | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 735 | T1437 | Application Layer Protocol | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 736 | T1398 | Boot or Logon Initialization Scripts | Identity / IAM; Server / Workload; Endpoint / User; Mobile |
| 737 | T0882 | Theft of Operational Information | Server / Workload; Data / Storage; ICS / OT |
| 738 | T0866 | Exploitation of Remote Services | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; ICS / OT |
| 739 | T0863 | User Execution | Public Internet / Edge; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; ICS / OT |
| 740 | T0859 | Valid Accounts | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 741 | T0853 | Scripting | Server / Workload; Endpoint / User; ICS / OT |
| 742 | T0849 | Masquerading | Data / Storage; Endpoint / User; ICS / OT |
| 743 | T0843 | Program Download | Cloud Control Plane; Network / Perimeter; Endpoint / User; ICS / OT |
| 744 | T0836 | Modify Parameter | Endpoint / User; Mobile; ICS / OT |
| 745 | T0829 | Loss of View | Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ICS / OT |
| 746 | T0814 | Denial of Service | Public Internet / Edge; Network / Perimeter; Server / Workload; Endpoint / User; Mobile; ICS / OT |
| 747 | T0809 | Data Destruction | Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 748 | T0807 | Command-Line Interface | Server / Workload; Endpoint / User; Mobile; ICS / OT |
| 749 | T0801 | Monitor Process State | SaaS / Office / Email; Network / Perimeter; Data / Storage; Endpoint / User; ICS / OT |
| 750 | T1692.001 | Command Message | Network / Perimeter; Server / Workload; Endpoint / User; Mobile; ICS / OT |
| 751 | T1639.001 | Exfiltration Over Unencrypted Non-C2 Protocol | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 752 | T1638 | Adversary-in-the-Middle | SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 753 | T1634.001 | Keychain | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 754 | T1631.001 | Ptrace System Calls | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 755 | T1629.002 | Device Lockout | Data / Storage; Endpoint / User; Mobile |
| 756 | T1627.001 | Geofencing | Cloud Control Plane; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 757 | T1625.001 | System Runtime API Hijacking | Identity / IAM; Cloud Control Plane; Server / Workload; Endpoint / User; Mobile |
| 758 | T1617 | Hooking | Public Internet / Edge; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 759 | T1593.001 | Social Media | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 760 | T1591.002 | Business Relationships | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage |
| 761 | T1590.005 | IP Addresses | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage |
| 762 | T1590 | Gather Victim Network Information | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Data / Storage |
| 763 | T1589.003 | Employee Names | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Data / Storage |
| 764 | T1588.007 | Artificial Intelligence | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Data / Storage; Endpoint / User |
| 765 | T1588.006 | Vulnerabilities | Public Internet / Edge; Server / Workload; Data / Storage |
| 766 | T1587.004 | Exploits | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User |
| 767 | T1583.005 | Botnet | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 768 | T1583.002 | DNS Server | Public Internet / Edge; Network / Perimeter; Server / Workload; Endpoint / User |
| 769 | T1577 | Compromise Application Executable | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 770 | T1471 | Data Encrypted for Impact | Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 771 | T1418.001 | Security Software Discovery | Endpoint / User; Mobile |
| 772 | T1417 | Input Capture | Identity / IAM; SaaS / Office / Email; Network / Perimeter; Data / Storage; Endpoint / User; Mobile |
| 773 | T0893 | Data from Local System | SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 774 | T0886 | Remote Services | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 775 | T0885 | Commonly Used Port | Public Internet / Edge; Network / Perimeter; Server / Workload; ICS / OT |
| 776 | T0884 | Connection Proxy | Network / Perimeter; Server / Workload; ICS / OT |
| 777 | T0862 | Supply Chain Compromise | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Mobile; ICS / OT |
| 778 | T0858 | Change Operating Mode | Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 779 | T0846.001 | Port Scan | Public Internet / Edge; Network / Perimeter; Server / Workload; Mobile; ICS / OT |
| 780 | T0846 | Remote System Discovery | Network / Perimeter; Server / Workload; ICS / OT |
| 781 | T0842 | Network Sniffing | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ICS / OT |
| 782 | T0834 | Native API | Cloud Control Plane; Server / Workload; Endpoint / User; Mobile; ICS / OT |
| 783 | T0821 | Modify Controller Tasking | Cloud Control Plane; Server / Workload; Endpoint / User; ICS / OT |
| 784 | T0806 | Brute Force I/O | Endpoint / User; ICS / OT |
| 785 | T0802 | Automated Collection | SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 786 | T1694.002 | Hardcoded Credentials | Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User; Mobile; ICS / OT |
| 787 | T1683.002 | Audio-Visual Content | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User |
| 788 | T1683.001 | Written Content | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User |
| 789 | T1682 | Query Public AI Services | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage |
| 790 | T1681 | Search Threat Vendor Data | Public Internet / Edge; Network / Perimeter; Data / Storage; Endpoint / User |
| 791 | T1676 | Linked Devices | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 792 | T1670 | Virtualization Solution | Identity / IAM; Data / Storage; Endpoint / User; ESXi / Hypervisor; Mobile |
| 793 | T1664 | Exploitation for Initial Access | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Endpoint / User; Mobile |
| 794 | T1663 | Remote Access Software | Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 795 | T1658 | Exploitation for Client Execution | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 796 | T1641.001 | Transmitted Data Manipulation | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 797 | T1633 | Virtualization/Sandbox Evasion | Endpoint / User; ESXi / Hypervisor; Mobile |
| 798 | T1631 | Process Injection | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 799 | T1630 | Indicator Removal on Host | Network / Perimeter; Data / Storage; Endpoint / User; Mobile |
| 800 | T1629 | Impair Defenses | Endpoint / User; Mobile |
| 801 | T1627 | Execution Guardrails | Endpoint / User; Mobile |
| 802 | T1624 | Event Triggered Execution | Identity / IAM; Server / Workload; Endpoint / User; Mobile |
| 803 | T1623 | Command and Scripting Interpreter | Server / Workload; Endpoint / User; Mobile |
| 804 | T1604 | Proxy Through Victim | Public Internet / Edge; Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 805 | T1596.005 | Scan Databases | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage |
| 806 | T1596 | Search Open Technical Databases | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage |
| 807 | T1590.001 | Domain Properties | Public Internet / Edge; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 808 | T1588.005 | Exploits | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload |
| 809 | T1586.003 | Cloud Accounts | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User |
| 810 | T1521 | Encrypted Channel | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 811 | T1458 | Replication Through Removable Media | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 812 | T1451 | SIM Card Swap | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Data / Storage; Endpoint / User; Mobile |
| 813 | T1428 | Exploitation of Remote Services | Public Internet / Edge; Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 814 | T0890 | Exploitation for Privilege Escalation | Public Internet / Edge; Identity / IAM; Server / Workload; Endpoint / User; ICS / OT |
| 815 | T0889 | Modify Program | Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User; Mobile; ICS / OT |
| 816 | T0874 | Hooking | Identity / IAM; Cloud Control Plane; Network / Perimeter; Server / Workload; Endpoint / User; ICS / OT |
| 817 | T0872 | Indicator Removal on Host | Mobile; ICS / OT |
| 818 | T0861 | Point & Tag Identification | SaaS / Office / Email; Data / Storage; Endpoint / User; ICS / OT |
| 819 | T0852 | Screen Capture | SaaS / Office / Email; Network / Perimeter; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 820 | T0847 | Replication Through Removable Media | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Endpoint / User; Mobile; ICS / OT |
| 821 | T0845 | Program Upload | SaaS / Office / Email; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 822 | T0840 | Network Connection Enumeration | Network / Perimeter; Mobile; ICS / OT |
| 823 | T0835 | Manipulate I/O Image | Public Internet / Edge; Data / Storage; Endpoint / User; ICS / OT |
| 824 | T0832 | Manipulation of View | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; ICS / OT |
| 825 | T0831 | Manipulation of Control | Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 826 | T0827 | Loss of Control | SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; ICS / OT |
| 827 | T1695.003 | Wi-Fi | Network / Perimeter; Server / Workload; Mobile; ICS / OT |
| 828 | T1695.002 | Ethernet | Network / Perimeter; Server / Workload; Mobile; ICS / OT |
| 829 | T1695.001 | Serial COM | Network / Perimeter; Server / Workload; Mobile; ICS / OT |
| 830 | T1693.001 | System Firmware | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User; Mobile; ICS / OT |
| 831 | T1691.002 | Reporting Message | Network / Perimeter; Data / Storage; Endpoint / User; ICS / OT |
| 832 | T1691.001 | Command Message | Network / Perimeter; Server / Workload; Mobile; ICS / OT |
| 833 | T1661 | Application Versioning | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Endpoint / User; Mobile |
| 834 | T1650 | Acquire Access | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 835 | T1640 | Account Access Removal | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 836 | T1639 | Exfiltration Over Alternative Protocol | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 837 | T1628.003 | Conceal Multimedia Files | Public Internet / Edge; Data / Storage; Endpoint / User; Mobile |
| 838 | T1625 | Hijack Execution Flow | Identity / IAM; Server / Workload; Endpoint / User; Mobile |
| 839 | T1597.002 | Purchase Technical Data | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 840 | T1597 | Search Closed Sources | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 841 | T1593.002 | Search Engines | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User |
| 842 | T1591.001 | Determine Physical Locations | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Data / Storage |
| 843 | T1590.006 | Network Security Appliances | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage |
| 844 | T1585.003 | Cloud Accounts | Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage |
| 845 | T1521.003 | SSL Pinning | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 846 | T1481.003 | One-Way Communication | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 847 | T1481 | Web Service | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 848 | T1474.001 | Compromise Software Dependencies and Development Tools | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Data / Storage; Endpoint / User; Mobile |
| 849 | T1464 | Network Denial of Service | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 850 | T1430.002 | Impersonate SS7 Nodes | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 851 | T1423 | Network Service Scanning | Public Internet / Edge; Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 852 | T1406.001 | Steganography | Data / Storage; Endpoint / User; Mobile |
| 853 | T0883 | Internet Accessible Device | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Mobile; ICS / OT |
| 854 | T0880 | Loss of Safety | Server / Workload; Data / Storage; Endpoint / User; ICS / OT |
| 855 | T0877 | I/O Image | Public Internet / Edge; Cloud Control Plane; SaaS / Office / Email; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 856 | T0873.001 | Siemens Project File Format | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User; ICS / OT |
| 857 | T0871 | Execution through API | Cloud Control Plane; Server / Workload; Endpoint / User; Mobile; ICS / OT |
| 858 | T0868 | Detect Operating Mode | SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 859 | T0851 | Rootkit | Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 860 | T0846.003 | Multicast Discovery | Network / Perimeter; Endpoint / User; Mobile; ICS / OT |
| 861 | T0846.002 | Broadcast Discovery | Identity / IAM; Network / Perimeter; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 862 | T0843.001 | Download All | Network / Perimeter; Endpoint / User; ICS / OT |
| 863 | T0837 | Loss of Protection | Server / Workload; Data / Storage; Endpoint / User; ICS / OT |
| 864 | T0830 | Adversary-in-the-Middle | SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Mobile; ICS / OT |
| 865 | T0826 | Loss of Availability | Server / Workload; Data / Storage; Endpoint / User; ICS / OT |
| 866 | T0822 | External Remote Services | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; ICS / OT |
| 867 | T0820 | Exploitation for Evasion | Public Internet / Edge; Server / Workload; Mobile; ICS / OT |
| 868 | T0819 | Exploit Public-Facing Application | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; ICS / OT |
| 869 | T0816 | Device Restart/Shutdown | Public Internet / Edge; Network / Perimeter; Server / Workload; Endpoint / User; Mobile; ICS / OT |
| 870 | T0815 | Denial of View | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 871 | T0813 | Denial of Control | SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 872 | T0811 | Data from Information Repositories | Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 873 | T0800 | Activate Firmware Update Mode | Endpoint / User; Mobile; ICS / OT |
| 874 | T1695 | Block Communications | Network / Perimeter; Server / Workload; Endpoint / User; Mobile; ICS / OT |
| 875 | T1694.001 | Default Credentials | Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User; Mobile; ICS / OT |
| 876 | T1694 | Insecure Credentials | Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User; Mobile; ICS / OT |
| 877 | T1693.002 | Module Firmware | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User; Mobile; ICS / OT |
| 878 | T1693 | Modify Firmware | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User; Mobile; ICS / OT |
| 879 | T1692.002 | Reporting Message | Network / Perimeter; Data / Storage; Endpoint / User; ICS / OT |
| 880 | T1692 | Unauthorized Message | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 881 | T1691 | Block Operational Technology Message | Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 882 | T1683 | Generate Content | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User |
| 883 | T1641 | Data Manipulation | Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 884 | T1637 | Dynamic Resolution | Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 885 | T1636 | Protected User Data | SaaS / Office / Email; Data / Storage; Endpoint / User; Mobile |
| 886 | T1635.001 | URI Hijacking | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Data / Storage; Endpoint / User; Mobile |
| 887 | T1635 | Steal Application Access Token | Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 888 | T1634 | Credentials from Password Store | Identity / IAM; SaaS / Office / Email; Data / Storage; Endpoint / User; Mobile |
| 889 | T1632 | Subvert Trust Controls | Endpoint / User; Mobile |
| 890 | T1630.003 | Disguise Root/Jailbreak Indicators | Endpoint / User; Mobile |
| 891 | T1628 | Hide Artifacts | Endpoint / User; Mobile |
| 892 | T1626 | Abuse Elevation Control Mechanism | Identity / IAM; Server / Workload; Endpoint / User; Mobile |
| 893 | T1597.001 | Threat Intel Vendors | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage |
| 894 | T1596.004 | CDNs | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage |
| 895 | T1596.003 | Digital Certificates | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage |
| 896 | T1596.002 | WHOIS | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage |
| 897 | T1596.001 | DNS/Passive DNS | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage |
| 898 | T1592.003 | Firmware | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage |
| 899 | T1591.003 | Identify Business Tempo | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Data / Storage |
| 900 | T1590.003 | Network Trust Dependencies | Public Internet / Edge; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage |
| 901 | T1590.002 | DNS | Public Internet / Edge; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage |
| 902 | T1477 | Exploit via Radio Interfaces | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; Mobile |
| 903 | T1476 | Deliver Malicious App via Other Means | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Endpoint / User; Mobile |
| 904 | T1475 | Deliver Malicious App via Authorized App Store | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 905 | T1474.002 | Compromise Hardware Supply Chain | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Data / Storage; Endpoint / User; Mobile |
| 906 | T1474 | Supply Chain Compromise | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Data / Storage; Endpoint / User; Mobile |
| 907 | T1470 | Obtain Device Cloud Backups | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 908 | T1469 | Remotely Wipe Data Without Authorization | Public Internet / Edge; Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 909 | T1449 | Exploit SS7 to Redirect Phone Calls/SMS | Public Internet / Edge; Identity / IAM; Network / Perimeter; Server / Workload; Endpoint / User; Mobile; ICS / OT |
| 910 | T1444 | Masquerade as Legitimate Application | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Endpoint / User; Mobile |
| 911 | T1436 | Commonly Used Port | Public Internet / Edge; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 912 | T1430.001 | Remote Device Management Services | Cloud Control Plane; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 913 | T1427 | Attack PC via USB Connection | Network / Perimeter; Data / Storage; Endpoint / User; Mobile |
| 914 | T1413 | Access Sensitive Data in Device Logs | Identity / IAM; SaaS / Office / Email; Data / Storage; Endpoint / User; Mobile |
| 915 | T1405 | Exploit TEE Vulnerability | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Mobile |
| 916 | T1403 | Modify Cached Executable Code | Identity / IAM; Server / Workload; Endpoint / User; Mobile |
| 917 | T1399 | Modify Trusted Execution Environment | Identity / IAM; Server / Workload; Endpoint / User; Mobile |
| 918 | T0895 | Autorun Image | Server / Workload; Endpoint / User; ESXi / Hypervisor; Mobile; ICS / OT |
| 919 | T0894 | System Binary Proxy Execution | Cloud Control Plane; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 920 | T0892 | Change Credential | Identity / IAM; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 921 | T0887 | Wireless Sniffing | SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Mobile; ICS / OT |
| 922 | T0879 | Damage to Property | SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 923 | T0878 | Alarm Suppression | Network / Perimeter; Mobile; ICS / OT |
| 924 | T0875 | Change Program State | Server / Workload; Endpoint / User; Mobile; ICS / OT |
| 925 | T0873 | Project File Infection | Identity / IAM; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 926 | T0870 | Detect Program State | SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; ICS / OT |
| 927 | T0864 | Transient Cyber Asset | Public Internet / Edge; Identity / IAM; Cloud Control Plane; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; Mobile; ICS / OT |
| 928 | T0860 | Wireless Compromise | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Mobile; ICS / OT |
| 929 | T0854 | Serial Connection Enumeration | Network / Perimeter; Server / Workload; Endpoint / User; Mobile; ICS / OT |
| 930 | T0850 | Role Identification | SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 931 | T0848 | Rogue Master | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Endpoint / User; Mobile; ICS / OT |
| 932 | T0844 | Program Organization Units | Network / Perimeter; Server / Workload; Endpoint / User; Mobile; ICS / OT |
| 933 | T0843.003 | Program Append | Network / Perimeter; Endpoint / User; ICS / OT |
| 934 | T0843.002 | Online Edit | Network / Perimeter; Endpoint / User; ICS / OT |
| 935 | T0841 | Network Service Scanning | Public Internet / Edge; Network / Perimeter; Server / Workload; Endpoint / User; Mobile; ICS / OT |
| 936 | T0838 | Modify Alarm Settings | Network / Perimeter; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 937 | T0833 | Modify Control Logic | Identity / IAM; Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 938 | T0825 | Location Identification | SaaS / Office / Email; Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 939 | T0824 | I/O Module Discovery | Network / Perimeter; Server / Workload; Endpoint / User; Mobile; ICS / OT |
| 940 | T0823 | Graphical User Interface | Network / Perimeter; Server / Workload; Endpoint / User; Mobile; ICS / OT |
| 941 | T0818 | Engineering Workstation Compromise | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Endpoint / User; ICS / OT |
| 942 | T0810 | Data Historian Compromise | Public Internet / Edge; Identity / IAM; SaaS / Office / Email; Network / Perimeter; Server / Workload; Data / Storage; Endpoint / User; Mobile; ICS / OT |
| 943 | T0808 | Control Device Identification | Server / Workload; Endpoint / User; Mobile; ICS / OT |
