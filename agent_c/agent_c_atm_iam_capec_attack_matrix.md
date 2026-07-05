# Agent C CAPEC + MITRE ATT&CK Watch Matrix

Generated: 2026-07-04T20:59:48

Agent: Adversarial AI ATM Endpoint & IAM Agent

ATM endpoint, ATM network edge, IAM, MFA, PAM, identity abuse, credential misuse, obfuscation, and adversarial evasion monitoring.

This file is a Layer 1 watchlist source. It is not an exploit guide and does not authorize containment. Layer 1 uses it to map observations to ATT&CK/CAPEC/CWE labels, predict likely next steps, and emit structured JSON to the deterministic Layer 2 orchestrator.

## Scope

- Input: sanitized, normalized telemetry from Layer 0 preprocessing.
- Output: read-only JSON finding for Layer 2 correlation.
- Layer 1 does not compute risk score, priority tier, routing, or auto-containment.
- Layer 2 performs BFT consensus, deterministic scoring, OPA policy checks, and playbook execution.

## Primary Surfaces

Identity / IAM, Endpoint / User, ICS / OT, Network / Perimeter, Server / Workload, Data / Storage

## Primary Evidence Fields

- user, account type, role/group, and authentication method
- ATM terminal ID, endpoint hostname, process path, signer, and hash
- MFA event, token/ticket indicator, and session ID
- PAM checkout or change ticket context
- obfuscation, masquerading, bypass, or disabled-control indicator

## Included Matrix Size

- Relevant ATT&CK candidates found: 854
- ATT&CK rows included here: 90
- Relevant CAPEC candidates found: 262
- CAPEC rows included here: 70
- CAPEC IDs directly linked from included ATT&CK rows: 38

## Included ATT&CK ID Set

- T1078.002, T1078, T1556, T1003.001, T1550.003, T1078.003, T1056.001, T1040, T1556.006, T1550.002, T1134, T1091, T1548.002, T1558.003
- T1055, T1558.001, T1003.003, T1557, T1556.001, T1556.008, T1542, T1558, T1556.002, T1556.003, T1556.005, T1053.005, T1027, T1542.001
- T1547.008, T1547.001, T1556.007, T1546.011, T1078.001, T1621, T1111, T1546.008, T1110.003, T1490, T1547.013, T1486, T1480.001, T1134.002
- T0859, T1098, T1197, T1547.006, T1200, T1110, T1547, T1546.018, T1205.002, T1546, T1484.002, T1563, T1078.004, T1134.003
- T1556.004, T1480, T1003.002, T1561.002, T1484.001, T1563.002, T1543.004, T1555.004, T1547.014, T1176, T1543.003, T1112, T1036, T1056.002
- T1136.002, T1021.006, T1557.001, T1552, T1484, T1542.005, T1558.002, T1563.001, T1543.002, T1505.004, T1205, T1555.003, T1547.012, T1134.005
- T1098.001, T1003.008, T1547.009, T1497.002, T1564.003, T1003

## Included CAPEC ID Set

- CAPEC-652, CAPEC-644, CAPEC-645, CAPEC-509, CAPEC-578, CAPEC-560, CAPEC-665, CAPEC-697, CAPEC-2, CAPEC-561, CAPEC-65, CAPEC-196, CAPEC-70, CAPEC-552
- CAPEC-203, CAPEC-633, CAPEC-485, CAPEC-206, CAPEC-568, CAPEC-565, CAPEC-98, CAPEC-55, CAPEC-569, CAPEC-555, CAPEC-593, CAPEC-21, CAPEC-654, CAPEC-158
- CAPEC-474, CAPEC-653, CAPEC-600, CAPEC-402, CAPEC-647, CAPEC-31, CAPEC-651, CAPEC-691, CAPEC-638, CAPEC-37, CAPEC-473, CAPEC-122, CAPEC-49, CAPEC-60
- CAPEC-150, CAPEC-639, CAPEC-545, CAPEC-59, CAPEC-648, CAPEC-270, CAPEC-660, CAPEC-233, CAPEC-457, CAPEC-640, CAPEC-115, CAPEC-656, CAPEC-102, CAPEC-50
- CAPEC-226, CAPEC-195, CAPEC-151, CAPEC-163, CAPEC-94, CAPEC-57, CAPEC-191, CAPEC-383, CAPEC-68, CAPEC-609, CAPEC-551, CAPEC-464, CAPEC-16, CAPEC-471

## MITRE ATT&CK Matrix Vectors

| rank | attack_id | attack_vector | tactics | global_score_ref | grade_ref | surface | edge_case | related_capec | watch_focus |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | T1078.002 | Domain Accounts | Stealth; Persistence; Privilege Escalation; Initial Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Logon Session; Process; Network Traffic; User Account |
| 2 | T1078 | Valid Accounts | Stealth; Persistence; Privilege Escalation; Initial Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-560 | Identity / MFA Bypass; Watch: Process; Logon Session; User Account |
| 3 | T1556 | Modify Authentication Process | Defense Impairment; Persistence; Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-665 | Identity / MFA Bypass; Watch: Process; User Account; Windows Registry; File; Module; Cloud Service |
| 4 | T1003.001 | LSASS Memory | Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; User Account; Windows Registry; File |
| 5 | T1550.003 | Pass the Ticket | Lateral Movement | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-645 | Identity / MFA Bypass; Watch: Process; Active Directory; Module; Logon Session; User Account |
| 6 | T1078.003 | Local Accounts | Stealth; Persistence; Privilege Escalation; Initial Access | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Logon Session; User Account |
| 7 | T1056.001 | Keylogging | Collection; Credential Access | 10 | Critical | Data / Storage | Identity / MFA Bypass | CAPEC-568 | Identity / MFA Bypass; Watch: Process; Firmware; Network Traffic; Windows Registry; File; Service |
| 8 | T1040 | Network Sniffing | Credential Access; Discovery | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-158; CAPEC-57; CAPEC-65 | Identity / MFA Bypass; Watch: Command; Network Traffic; Process; Service; User Account; Cloud Service |
| 9 | T1556.006 | Multi-Factor Authentication | Defense Impairment; Persistence; Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-578 | Identity / MFA Bypass; Watch: User Account; Active Directory; File; Script; Application Log; Cloud Service |
| 10 | T1550.002 | Pass the Hash | Lateral Movement | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-644 | Identity / MFA Bypass; Watch: Process; Logon Session; Network Traffic; Active Directory |
| 11 | T1134 | Access Token Manipulation | Stealth; Privilege Escalation | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-21; CAPEC-633 | Identity / MFA Bypass; Watch: Process; Active Directory; Logon Session |
| 12 | T1091 | Replication Through Removable Media | Lateral Movement; Initial Access | 6.25 | Medium High | Network / Perimeter | Zero-Day / Unknown Exploit | CAPEC-457 | Zero-Day / Unknown Exploit; Watch: Drive; Process; File |
| 13 | T1548.002 | Bypass User Account Control | Privilege Escalation | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; Windows Registry; Module; Logon Session |
| 14 | T1558.003 | Kerberoasting | Credential Access | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-509 | Identity / MFA Bypass; Watch: Process; Logon Session; Active Directory |
| 15 | T1055 | Process Injection | Stealth; Privilege Escalation | 7.5 | Critical | Server / Workload | Telemetry Gap / Evasion | CAPEC-251; CAPEC-660 | Telemetry Gap / Evasion; Watch: Process; Module; File |
| 16 | T1558.001 | Golden Ticket | Credential Access | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; Logon Session; Active Directory |
| 17 | T1003.003 | NTDS | Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Volume; Process; File |
| 18 | T1557 | Adversary-in-the-Middle | Credential Access; Collection | 10 | Critical | Public Internet / Edge | Identity / MFA Bypass | CAPEC-94 | Identity / MFA Bypass; Watch: Network Traffic; File; Windows Registry; Application Log |
| 19 | T1556.001 | Domain Controller Authentication | Defense Impairment; Persistence; Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; Logon Session; File; Module |
| 20 | T1556.008 | Network Provider DLL | Defense Impairment; Persistence; Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; File; Windows Registry; Module |
| 21 | T1542 | Pre-OS Boot | Stealth; Persistence | 7.5 | Critical | Server / Workload | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Firmware; Drive; Process; File |
| 22 | T1558 | Steal or Forge Kerberos Tickets | Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-652 | Identity / MFA Bypass; Watch: Process; Logon Session; Active Directory; File |
| 23 | T1556.002 | Password Filter DLL | Defense Impairment; Persistence; Credential Access | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: File; Windows Registry; Module |
| 24 | T1556.003 | Pluggable Authentication Modules | Defense Impairment; Persistence; Credential Access | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; Logon Session; File |
| 25 | T1556.005 | Reversible Encryption | Defense Impairment; Persistence; Credential Access | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Command; Process; Active Directory |
| 26 | T1053.005 | Scheduled Task | Execution; Persistence; Privilege Escalation | 10 | Critical | Identity / IAM | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; Windows Registry; Scheduled Job; File |
| 27 | T1027 | Obfuscated Files or Information | Stealth | 10 | Critical | ESXi / Hypervisor | Telemetry Gap / Evasion | CAPEC-267; CAPEC-542 | Telemetry Gap / Evasion; Watch: Command; Network Traffic; Process; File |
| 28 | T1542.001 | System Firmware | Stealth; Persistence | 7.5 | Critical | Server / Workload | Supply Chain / Trusted Dependency | CAPEC-532 | Supply Chain / Trusted Dependency; Watch: Firmware; Drive; Process; File |
| 29 | T1547.008 | LSASS Driver | Persistence; Privilege Escalation | 10 | Critical | Identity / IAM | Living-off-the-Land |  | Living-off-the-Land; Watch: File; Windows Registry; Module; Driver |
| 30 | T1547.001 | Registry Run Keys / Startup Folder | Persistence; Privilege Escalation | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-270 | Identity / MFA Bypass; Watch: Process; File; Windows Registry |
| 31 | T1556.007 | Hybrid Identity | Defense Impairment; Persistence; Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: User Account; Active Directory; Module; Logon Session; Application Log; Cloud Service |
| 32 | T1546.011 | Application Shimming | Privilege Escalation; Persistence | 10 | Critical | Identity / IAM | Living-off-the-Land |  | Living-off-the-Land; Watch: Process; File; Windows Registry; Module |
| 33 | T1078.001 | Default Accounts | Stealth; Persistence; Privilege Escalation; Initial Access | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-70 | Identity / MFA Bypass; Watch: Logon Session; User Account |
| 34 | T1621 | Multi-Factor Authentication Request Generation | Credential Access | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Logon Session; User Account; Application Log |
| 35 | T1111 | Multi-Factor Authentication Interception | Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-158; CAPEC-609; CAPEC-651 | Identity / MFA Bypass; Watch: Process; Windows Registry; Driver; Logon Session |
| 36 | T1546.008 | Accessibility Features | Privilege Escalation; Persistence | 6.25 | Medium High | Server / Workload | Zero-Day / Unknown Exploit | CAPEC-558 | Zero-Day / Unknown Exploit; Watch: File; Process; Windows Registry |
| 37 | T1110.003 | Password Spraying | Credential Access | 5.62 | Medium High | Identity / IAM | Identity / MFA Bypass | CAPEC-565 | Identity / MFA Bypass; Watch: User Account |
| 38 | T1490 | Inhibit System Recovery | Impact | 10 | Critical | Cloud Control Plane | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Process; Windows Registry; Service; File; Snapshot; Cloud Storage |
| 39 | T1547.013 | XDG Autostart Entries | Persistence; Privilege Escalation | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; File; Logon Session |
| 40 | T1486 | Data Encrypted for Impact | Impact | 10 | Critical | Cloud Control Plane | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Command; Process; File; Cloud Storage |
| 41 | T1480.001 | Environmental Keying | Stealth | 10 | Critical | Data / Storage | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Process; Command; Network Traffic; WMI; Module; File; Logon Session |
| 42 | T1134.002 | Create Process with Token | Stealth; Privilege Escalation | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-196 | Identity / MFA Bypass; Watch: Process; Active Directory; Logon Session |
| 43 | T0859 | Valid Accounts | Persistence; Lateral Movement | 0 | Low | ICS / OT | Air-Gapped / ICS Safety |  | Air-Gapped / ICS Safety |
| 44 | T1098 | Account Manipulation | Persistence; Privilege Escalation | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; User Account; Active Directory; File |
| 45 | T1197 | BITS Jobs | Stealth; Persistence; Execution | 7.5 | Critical | Network / Perimeter | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Process; Network Traffic; Service |
| 46 | T1547.006 | Kernel Modules and Extensions | Persistence; Privilege Escalation | 7.5 | Critical | Server / Workload | Exploit Chain / Multi-Step | CAPEC-552 | Exploit Chain / Multi-Step; Watch: Command; Kernel; Process; File |
| 47 | T1200 | Hardware Additions | Initial Access | 5.0 | Medium High | Public Internet / Edge | Zero-Day / Unknown Exploit | CAPEC-440 | Zero-Day / Unknown Exploit; Watch: Drive; Process; Network Traffic; Module; File; Driver; Application Log |
| 48 | T1110 | Brute Force | Credential Access | 6.75 | Medium High | Identity / IAM | Identity / MFA Bypass | CAPEC-112 | Identity / MFA Bypass; Watch: User Account |
| 49 | T1547 | Boot or Logon Autostart Execution | Persistence; Privilege Escalation | 10 | Critical | Identity / IAM | Living-off-the-Land | CAPEC-564 | Living-off-the-Land; Watch: Process; File; Windows Registry; Service |
| 50 | T1546.018 | Python Startup Hooks | Persistence; Privilege Escalation | 6.25 | Medium High | Network / Perimeter | Exploit Chain / Multi-Step |  | Exploit Chain / Multi-Step; Watch: Process; File; Network Traffic |
| 51 | T1205.002 | Socket Filters | Stealth; Persistence; Command and Control | 10 | Critical | Network / Perimeter | Living-off-the-Land |  | Living-off-the-Land; Watch: Network Traffic; Process; Module; Driver; Service |
| 52 | T1546 | Event Triggered Execution | Privilege Escalation; Persistence | 10 | Critical | Identity / IAM | Cloud / SaaS Tenant Blast Radius |  | Cloud / SaaS Tenant Blast Radius; Watch: Command; Network Traffic; Process; Windows Registry; WMI; Scheduled Job; File; Script; Cloud Service |
| 53 | T1484.002 | Trust Modification | Defense Impairment; Privilege Escalation | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Command; User Account; Process; Active Directory; Application Log |
| 54 | T1563 | Remote Service Session Hijacking | Lateral Movement | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-593 | Identity / MFA Bypass; Watch: Command; Network Traffic; Process; Logon Session |
| 55 | T1078.004 | Cloud Accounts | Stealth; Persistence; Privilege Escalation; Initial Access | 9.38 | Critical | Public Internet / Edge | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Logon Session; User Account |
| 56 | T1134.003 | Make and Impersonate Token | Stealth; Privilege Escalation | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-196 | Identity / MFA Bypass; Watch: Process; Logon Session |
| 57 | T1556.004 | Network Device Authentication | Defense Impairment; Persistence; Credential Access | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: File; User Account |
| 58 | T1480 | Execution Guardrails | Stealth | 10 | Critical | ESXi / Hypervisor | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Process; Network Traffic; Windows Registry; WMI; Module; File; Logon Session; User Account |
| 59 | T1003.002 | Security Account Manager | Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: File; Process; Windows Registry |
| 60 | T1561.002 | Disk Structure Wipe | Impact | 10 | Critical | Identity / IAM | Destructive / Ransomware |  | Destructive / Ransomware; Watch: Drive; Command; Process; User Account; Driver |
| 61 | T1484.001 | Group Policy Modification | Defense Impairment; Privilege Escalation | 10 | Critical | Identity / IAM | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: User Account; Process; File; Active Directory |
| 62 | T1563.002 | RDP Hijacking | Lateral Movement | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; Service; Logon Session; Network Traffic |
| 63 | T1543.004 | Launch Daemon | Persistence; Privilege Escalation | 6.25 | Medium High | Server / Workload | Supply Chain / Trusted Dependency | CAPEC-564 | Supply Chain / Trusted Dependency; Watch: Service; Process; File |
| 64 | T1555.004 | Windows Credential Manager | Credential Access | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; File |
| 65 | T1547.014 | Active Setup | Persistence; Privilege Escalation | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-270 | Identity / MFA Bypass; Watch: Logon Session; Process; Windows Registry |
| 66 | T1176 | Software Extensions | Persistence | 7.5 | Critical | Network / Perimeter | Zero-Day / Unknown Exploit | CAPEC-698 | Zero-Day / Unknown Exploit; Watch: Command; Process; Network Traffic; Windows Registry; File |
| 67 | T1543.003 | Windows Service | Persistence; Privilege Escalation | 9.0 | Critical | Server / Workload | Zero-Day / Unknown Exploit | CAPEC-478 | Zero-Day / Unknown Exploit; Watch: Windows Registry; Process; Service; Driver |
| 68 | T1112 | Modify Registry | Defense Impairment; Persistence | 10 | Critical | Identity / IAM | Telemetry Gap / Evasion | CAPEC-203 | Telemetry Gap / Evasion; Watch: Process; Windows Registry |
| 69 | T1036 | Masquerading | Stealth | 10 | Critical | ESXi / Hypervisor | Cloud / SaaS Tenant Blast Radius | CAPEC-177 | Cloud / SaaS Tenant Blast Radius; Watch: Command; Process; File; Service; Image |
| 70 | T1056.002 | GUI Input Capture | Collection; Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Command; Process; Script |
| 71 | T1136.002 | Domain Account | Persistence | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Command; User Account; Process; Logon Session |
| 72 | T1021.006 | Windows Remote Management | Lateral Movement | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; Logon Session; Service; Network Traffic |
| 73 | T1557.001 | Name Resolution Poisoning and SMB Relay | Credential Access; Collection | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Windows Registry; Network Traffic; Service |
| 74 | T1552 | Unsecured Credentials | Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Command; Network Traffic; Process; Windows Registry; File; Cloud Service; User Account; Application Log |
| 75 | T1484 | Domain or Tenant Policy Modification | Defense Impairment; Privilege Escalation | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; File; Active Directory; User Account; Application Log |
| 76 | T1542.005 | TFTP Boot | Stealth; Persistence | 6.25 | Medium High | Network / Perimeter | Living-off-the-Land |  | Living-off-the-Land; Watch: Command; Firmware; Network Traffic |
| 77 | T1558.002 | Silver Ticket | Credential Access | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; Logon Session; Active Directory |
| 78 | T1563.001 | SSH Hijacking | Lateral Movement | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; Logon Session; Network Traffic |
| 79 | T1543.002 | Systemd Service | Persistence; Privilege Escalation | 7.5 | Critical | Server / Workload | Exploit Chain / Multi-Step |  | Exploit Chain / Multi-Step; Watch: Command; Process; File; Service |
| 80 | T1505.004 | IIS Components | Persistence | 7.5 | Critical | Server / Workload | Exploit Chain / Multi-Step | CAPEC-698 | Exploit Chain / Multi-Step; Watch: Process; File; Module; Service; Application Log |
| 81 | T1205 | Traffic Signaling | Stealth; Persistence; Command and Control | 8.33 | Critical | Network / Perimeter | Exploit Chain / Multi-Step |  | Exploit Chain / Multi-Step; Watch: Command; Network Traffic; Process |
| 82 | T1555.003 | Credentials from Web Browsers | Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; File |
| 83 | T1547.012 | Print Processors | Persistence; Privilege Escalation | 10 | Critical | Identity / IAM | Living-off-the-Land |  | Living-off-the-Land; Watch: Process; File; Windows Registry; Module |
| 84 | T1134.005 | SID-History Injection | Stealth; Privilege Escalation | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: User Account; Active Directory; Process |
| 85 | T1098.001 | Additional Cloud Credentials | Persistence; Privilege Escalation | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: User Account; Active Directory |
| 86 | T1003.008 | /etc/passwd and /etc/shadow | Credential Access | 9.38 | Critical | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; File |
| 87 | T1547.009 | Shortcut Modification | Persistence; Privilege Escalation | 7.5 | Critical | Server / Workload | Exploit Chain / Multi-Step | CAPEC-132 | Exploit Chain / Multi-Step; Watch: File; Process |
| 88 | T1497.002 | User Activity Based Checks | Stealth; Discovery | 7.5 | Critical | Server / Workload | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Process; Command; File; Logon Session |
| 89 | T1564.003 | Hidden Window | Stealth | 9.0 | Critical | Server / Workload | Living-off-the-Land |  | Living-off-the-Land; Watch: Command; Process; Windows Registry; File |
| 90 | T1003 | OS Credential Dumping | Credential Access | 10 | Critical | Identity / IAM | Identity / MFA Bypass | CAPEC-150 | Identity / MFA Bypass; Watch: Process; Active Directory; File |

## CAPEC Attack Pattern Matrix

| rank | capec_id | attack_pattern | severity_ref | likelihood_ref | global_score_ref | surface | edge_case | related_attack | watch_focus |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | CAPEC-652 | Use of Known Kerberos Credentials | High | Medium | 10 | Identity / IAM | Identity / MFA Bypass | T1558 | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-294; CWE-307; CWE-308; CWE-309; CWE-522; CWE-654; CWE-836 |
| 2 | CAPEC-644 | Use of Captured Hashes (Pass The Hash) | High | Medium | 10 | Identity / IAM | Identity / MFA Bypass | T1550.002 | Identity / MFA Bypass; CWE: CWE-294; CWE-308; CWE-522; CWE-836 |
| 3 | CAPEC-645 | Use of Captured Tickets (Pass The Ticket) | High | Low | 10 | Identity / IAM | Identity / MFA Bypass | T1550.003 | Identity / MFA Bypass; CWE: CWE-294; CWE-308; CWE-522 |
| 4 | CAPEC-509 | Kerberoasting | High | Unknown | 9.38 | Identity / IAM | Identity / MFA Bypass | T1558.003 | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-294; CWE-308; CWE-309; CWE-521; CWE-522 |
| 5 | CAPEC-578 | Disable Security Software | Medium | Medium | 10 | Identity / IAM | Identity / MFA Bypass | T1556.006 | Identity / MFA Bypass; CWE: CWE-284 |
| 6 | CAPEC-560 | Use of Known Domain Credentials | High | High | 10 | Identity / IAM | Identity / MFA Bypass | T1078 | Identity / MFA Bypass; CWE: CWE-1273; CWE-262; CWE-263; CWE-307; CWE-308; CWE-309; CWE-522; CWE-654 |
| 7 | CAPEC-665 | Exploitation of Thunderbolt Protection Flaws | Very High | Low | 10 | Identity / IAM | Identity / MFA Bypass | T1211; T1542.002; T1556 | Identity / MFA Bypass; CWE: CWE-1188; CWE-288; CWE-345; CWE-353; CWE-862 |
| 8 | CAPEC-697 | DHCP Spoofing | High | Low | 10 | Identity / IAM | Identity / MFA Bypass | T1557.003 | Identity / MFA Bypass; CWE: CWE-923 |
| 9 | CAPEC-2 | Inducing Account Lockout | Medium | High | 10 | Identity / IAM | Identity / MFA Bypass | T1531 | Identity / MFA Bypass; CWE: CWE-645 |
| 10 | CAPEC-561 | Windows Admin Shares with Stolen Credentials | Unknown | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1021.002 | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-294; CWE-308; CWE-309; CWE-521; CWE-522 |
| 11 | CAPEC-65 | Sniff Application Code | High | Low | 10 | Identity / IAM | Identity / MFA Bypass | T1040 | Identity / MFA Bypass; CWE: CWE-311; CWE-318; CWE-319; CWE-693 |
| 12 | CAPEC-196 | Session Credential Falsification through Forging | Medium | Medium | 10 | Identity / IAM | Identity / MFA Bypass | T1134.002; T1134.003; T1606 | Identity / MFA Bypass; CWE: CWE-384; CWE-664 |
| 13 | CAPEC-70 | Try Common or Default Usernames and Passwords | High | Medium | 9.38 | Identity / IAM | Identity / MFA Bypass | T1078.001 | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-308; CWE-309; CWE-521; CWE-654; CWE-798 |
| 14 | CAPEC-552 | Install Rootkit | High | Medium | 10 | Identity / IAM | Telemetry Gap / Evasion | T1014; T1542.003; T1547.006 | Telemetry Gap / Evasion; CWE: CWE-284 |
| 15 | CAPEC-203 | Manipulate Registry Information | Medium | Unknown | 10 | Identity / IAM | Telemetry Gap / Evasion | T1112; T1647 | Telemetry Gap / Evasion; CWE: CWE-15 |
| 16 | CAPEC-633 | Token Impersonation | Medium | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1134 | Identity / MFA Bypass; CWE: CWE-1270; CWE-287 |
| 17 | CAPEC-485 | Signature Spoofing by Key Recreation | High | Low | 10 | Identity / IAM | Identity / MFA Bypass | T1552.004 | Identity / MFA Bypass; CWE: CWE-330 |
| 18 | CAPEC-206 | Signing Malicious Code | Very High | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1553.002 | Identity / MFA Bypass; CWE: CWE-732 |
| 19 | CAPEC-568 | Capture Credentials via Keylogger | High | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1056.001 | Identity / MFA Bypass |
| 20 | CAPEC-565 | Password Spraying | High | High | 5.62 | Identity / IAM | Identity / MFA Bypass | T1110.003 | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-307; CWE-308; CWE-309; CWE-521; CWE-654 |
| 21 | CAPEC-98 | Phishing | Very High | High | 7.5 | Identity / IAM | Identity / MFA Bypass | T1566; T1598 | Identity / MFA Bypass; CWE: CWE-451 |
| 22 | CAPEC-55 | Rainbow Table Password Cracking | Medium | Medium | 9.38 | Identity / IAM | Identity / MFA Bypass | T1110.002 | Identity / MFA Bypass; CWE: CWE-261; CWE-262; CWE-263; CWE-308; CWE-309; CWE-521; CWE-654; CWE-916 |
| 23 | CAPEC-569 | Collect Data as Provided by Users | Unknown | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1056 | Identity / MFA Bypass |
| 24 | CAPEC-555 | Remote Services with Stolen Credentials | Very High | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1021; T1114.002; T1133 | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-294; CWE-308; CWE-309; CWE-521; CWE-522 |
| 25 | CAPEC-593 | Session Hijacking | Very High | High | 10 | Identity / IAM | Identity / MFA Bypass | T1185; T1550.001; T1563 | Identity / MFA Bypass; CWE: CWE-287 |
| 26 | CAPEC-21 | Exploitation of Trusted Identifiers | High | High | 10 | Identity / IAM | Identity / MFA Bypass | T1134; T1528; T1539 | Identity / MFA Bypass; CWE: CWE-290; CWE-302; CWE-346; CWE-384; CWE-539; CWE-6; CWE-602; CWE-642; CWE-664 |
| 27 | CAPEC-654 | Credential Prompt Impersonation | High | Medium | 10 | Identity / IAM | Identity / MFA Bypass | T1056; T1548.004 | Identity / MFA Bypass; CWE: CWE-1021 |
| 28 | CAPEC-158 | Sniffing Network Traffic | Medium | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1040; T1111 | Identity / MFA Bypass; CWE: CWE-311 |
| 29 | CAPEC-474 | Signature Spoofing by Key Theft | High | Medium | 10 | Identity / IAM | Identity / MFA Bypass | T1552.004 | Identity / MFA Bypass; CWE: CWE-522 |
| 30 | CAPEC-653 | Use of Known Operating System Credentials | High | High | 10 | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-307; CWE-308; CWE-309; CWE-522; CWE-654 |
| 31 | CAPEC-600 | Credential Stuffing | High | High | 5.62 | Identity / IAM | Identity / MFA Bypass | T1110.004 | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-307; CWE-308; CWE-309; CWE-522; CWE-654 |
| 32 | CAPEC-402 | Bypassing ATA Password Security | Unknown | Unknown | 5.0 | Identity / IAM | Insider / Trusted Access |  | Insider / Trusted Access; CWE: CWE-285 |
| 33 | CAPEC-647 | Collect Data from Registries | Medium | Medium | 10 | Identity / IAM | Identity / MFA Bypass | T1005; T1012; T1552.002 | Identity / MFA Bypass; CWE: CWE-285 |
| 34 | CAPEC-31 | Accessing/Intercepting/Modifying HTTP Cookies | High | High | 10 | Identity / IAM | Identity / MFA Bypass | T1539 | Identity / MFA Bypass; CWE: CWE-113; CWE-20; CWE-302; CWE-311; CWE-315; CWE-384; CWE-472; CWE-539; CWE-565; CWE-602; CWE-642 |
| 35 | CAPEC-651 | Eavesdropping | Medium | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1111 | Identity / MFA Bypass; CWE: CWE-200 |
| 36 | CAPEC-691 | Spoof Open-Source Software Metadata | High | Medium | 7.5 | Identity / IAM | Supply Chain / Trusted Dependency | T1195.001; T1195.002 | Supply Chain / Trusted Dependency; CWE: CWE-494 |
| 37 | CAPEC-638 | Altered Component Firmware | Very High | Low | 9.38 | Identity / IAM | Zero-Day / Unknown Exploit | T1542.002 | Zero-Day / Unknown Exploit |
| 38 | CAPEC-37 | Retrieve Embedded Sensitive Data | Very High | High | 10 | Identity / IAM | Identity / MFA Bypass | T1005; T1552.004 | Identity / MFA Bypass; CWE: CWE-1239; CWE-1258; CWE-1266; CWE-1272; CWE-1278; CWE-1301; CWE-1330; CWE-226; CWE-311; CWE-312; CWE-314; CWE-315; CWE-318; CWE-525 |
| 39 | CAPEC-473 | Signature Spoof | Unknown | Unknown | 10 | Identity / IAM | Telemetry Gap / Evasion | T1036.001; T1553.002 | Telemetry Gap / Evasion; CWE: CWE-20; CWE-290; CWE-327 |
| 40 | CAPEC-122 | Privilege Abuse | Medium | High | 10 | Identity / IAM | Cloud / SaaS Tenant Blast Radius | T1548 | Cloud / SaaS Tenant Blast Radius; CWE: CWE-1317; CWE-269; CWE-732 |
| 41 | CAPEC-49 | Password Brute Forcing | High | Medium | 5.62 | Identity / IAM | Identity / MFA Bypass | T1110.001 | Identity / MFA Bypass; CWE: CWE-257; CWE-262; CWE-263; CWE-307; CWE-308; CWE-309; CWE-521; CWE-654 |
| 42 | CAPEC-60 | Reusing Session IDs (aka Session Replay) | High | High | 9.38 | Identity / IAM | Identity / MFA Bypass | T1134.001; T1550.004 | Identity / MFA Bypass; CWE: CWE-200; CWE-285; CWE-290; CWE-294; CWE-346; CWE-384; CWE-488; CWE-539; CWE-664; CWE-732 |
| 43 | CAPEC-150 | Collect Data from Common Resource Locations | Medium | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1003; T1119; T1213; T1530; T1555; T1602 | Identity / MFA Bypass; CWE: CWE-1239; CWE-1258; CWE-1266; CWE-1272; CWE-1323; CWE-1330; CWE-552 |
| 44 | CAPEC-639 | Probe System Files | Medium | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1039; T1552.001; T1552.003; T1552.004; T1552.006 | Identity / MFA Bypass; CWE: CWE-552 |
| 45 | CAPEC-545 | Pull Data from System Resources | Unknown | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1005; T1555.001 | Identity / MFA Bypass; CWE: CWE-1239; CWE-1243; CWE-1258; CWE-1266; CWE-1272; CWE-1278; CWE-1323; CWE-1330 |
| 46 | CAPEC-59 | Session Credential Falsification through Prediction | High | High | 10 | Identity / IAM | Rare but High Impact |  | Rare but High Impact; CWE: CWE-200; CWE-285; CWE-290; CWE-330; CWE-331; CWE-346; CWE-384; CWE-488; CWE-539; CWE-6; CWE-693 |
| 47 | CAPEC-648 | Collect Data from Screen Capture | Medium | Medium | 10 | Identity / IAM | Zero-Day / Unknown Exploit | T1113; T1513 | Zero-Day / Unknown Exploit; CWE: CWE-267 |
| 48 | CAPEC-270 | Modification of Registry Run Keys | Medium | Medium | 10 | Identity / IAM | Insider / Trusted Access | T1547.001; T1547.014 | Insider / Trusted Access; CWE: CWE-15 |
| 49 | CAPEC-660 | Root/Jailbreak Detection Evasion via Hooking | Very High | Medium | 10 | Identity / IAM | Telemetry Gap / Evasion | T1055 | Telemetry Gap / Evasion; CWE: CWE-829 |
| 50 | CAPEC-233 | Privilege Escalation | Unknown | Unknown | 10 | Identity / IAM | Cloud / SaaS Tenant Blast Radius | T1548 | Cloud / SaaS Tenant Blast Radius; CWE: CWE-1264; CWE-1311; CWE-269 |
| 51 | CAPEC-457 | USB Memory Attacks | High | Low | 8.33 | Network / Perimeter | Air-Gapped / ICS Safety | T1091; T1092 | Air-Gapped / ICS Safety; CWE: CWE-1299 |
| 52 | CAPEC-640 | Inclusion of Code in Existing Process | High | Low | 10 | ICS / OT | Air-Gapped / ICS Safety | T1505.005; T1574.006; T1574.013; T1620 | Air-Gapped / ICS Safety; CWE: CWE-114; CWE-829 |
| 53 | CAPEC-115 | Authentication Bypass | Medium | Unknown | 10 | Identity / IAM | Cloud / SaaS Tenant Blast Radius | T1548 | Cloud / SaaS Tenant Blast Radius; CWE: CWE-287 |
| 54 | CAPEC-656 | Voice Phishing | High | High | 10 | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass |
| 55 | CAPEC-102 | Session Sidejacking | High | High | 7.5 | Network / Perimeter | Destructive / Ransomware |  | Destructive / Ransomware; CWE: CWE-294; CWE-319; CWE-522; CWE-523; CWE-614 |
| 56 | CAPEC-50 | Password Recovery Exploitation | High | Medium | 9.38 | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; CWE: CWE-522; CWE-640 |
| 57 | CAPEC-226 | Session Credential Falsification through Manipulation | Medium | Unknown | 5.0 | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; CWE: CWE-472; CWE-565 |
| 58 | CAPEC-195 | Principal Spoof | Medium | Unknown | 5.0 | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass |
| 59 | CAPEC-151 | Identity Spoofing | Medium | Medium | 6.25 | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; CWE: CWE-287 |
| 60 | CAPEC-163 | Spear Phishing | High | High | 10 | Identity / IAM | Cloud / SaaS Tenant Blast Radius | T1534; T1566.001; T1566.002; T1566.003; T1598.001; T1598.002; T1598.003 | Cloud / SaaS Tenant Blast Radius; CWE: CWE-451 |
| 61 | CAPEC-94 | Adversary in the Middle (AiTM) | Very High | High | 10 | Identity / IAM | Identity / MFA Bypass | T1557 | Identity / MFA Bypass; CWE: CWE-287; CWE-290; CWE-294; CWE-300; CWE-593 |
| 62 | CAPEC-57 | Utilizing REST's Trust in the System Resource to Obtain Sensitive Data | Very High | Medium | 10 | Identity / IAM | Identity / MFA Bypass | T1040 | Identity / MFA Bypass; CWE: CWE-287; CWE-300; CWE-693 |
| 63 | CAPEC-191 | Read Sensitive Constants Within an Executable | Low | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1552.001 | Identity / MFA Bypass; CWE: CWE-798 |
| 64 | CAPEC-383 | Harvesting Information via API Event Monitoring | Low | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1056.004 | Identity / MFA Bypass; CWE: CWE-311; CWE-319; CWE-419; CWE-602 |
| 65 | CAPEC-68 | Subvert Code-signing Facilities | Very High | Low | 10 | Identity / IAM | Telemetry Gap / Evasion | T1553.002 | Telemetry Gap / Evasion; CWE: CWE-1326; CWE-325; CWE-328 |
| 66 | CAPEC-609 | Cellular Traffic Intercept | Low | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1111 | Identity / MFA Bypass; CWE: CWE-311 |
| 67 | CAPEC-551 | Modify Existing Service | Unknown | Unknown | 10 | Identity / IAM | Telemetry Gap / Evasion | T1543 | Telemetry Gap / Evasion; CWE: CWE-284; CWE-522 |
| 68 | CAPEC-464 | Evercookie | Medium | Unknown | 10 | Identity / IAM | Identity / MFA Bypass | T1606.001 | Identity / MFA Bypass; CWE: CWE-359 |
| 69 | CAPEC-16 | Dictionary-based Password Attack | High | Medium | 9.38 | Identity / IAM | Exploit Chain / Multi-Step |  | Exploit Chain / Multi-Step; CWE: CWE-262; CWE-263; CWE-307; CWE-308; CWE-309; CWE-521; CWE-654 |
| 70 | CAPEC-471 | Search Order Hijacking | Medium | Unknown | 10 | Data / Storage | Telemetry Gap / Evasion | T1574.001; T1574.004; T1574.008 | Telemetry Gap / Evasion; CWE: CWE-427 |

## Layer 2 Correlation Hints

- Treat same user, source IP, destination IP, host, session ID, request ID, transaction ID, object ID, or time window as correlation keys.
- Treat overlapping ATT&CK technique, CAPEC pattern, CWE, edge case, or affected banking surface as pattern correlation keys.
- A single-agent hit is still forwarded. Layer 2 decides whether it is 1-of-3, 2-of-3, or 3-of-3 consensus.
- Layer 2 computes risk deterministically from the mapped base threat score and asset criticality multiplier.
- Auto-containment requires BFT consensus, meaning at least 2 of 3 agents flag a threat, and `final_risk_score >= 8.5`; a single-agent hit can raise analyst-visible severity but cannot trigger automated containment by itself.
- Unknown or zero-day-like behavior should be emitted with `unknown_or_novel_abnormality` and the best available evidence.

## Agent Prompt Reference

Use `agent_c/agent_c_atm_iam_adversarial_system_prompt.md` for Agent C.
