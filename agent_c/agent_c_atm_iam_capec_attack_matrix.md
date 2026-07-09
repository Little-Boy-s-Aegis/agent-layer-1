# Agent C CAPEC + MITRE ATT&CK Watch Matrix

Generated: scoped runtime rewrite from local Layer 1 package references

Agent: Agent C

This file is a Layer 1 watchlist source. It is not an exploit guide and does not authorize containment. Layer 1 uses it to map observed behavior to ATT&CK/CAPEC/CWE labels and form non-scoring attack-pattern prediction hints before emitting structured JSON to the deterministic Layer 2 orchestrator.

## Scope

- Input: sanitized, normalized telemetry from Layer 0 preprocessing.
- Output: read-only JSON finding for Layer 2 correlation.
- Layer 1 does not compute risk score, priority tier, routing, or auto-containment.
- Layer 2 independently verifies Layer 1 findings from logs/context, then performs deterministic scoring, OPA policy checks, and playbook execution.

## Primary Surfaces

ATM Endpoint, Identity / IAM, MFA / SSO, PAM / Privileged Identity, Kerberos / AD, HSM / Crypto Boundary

## Included Matrix Size

- ATT&CK rows included here: 79
- CAPEC rows included here: 58
- ATT&CK source boundary: `agent_c/surface_context_matrix.md`
- CAPEC source boundary: `agent_c/capec_attack_pattern_prediction_reference.md`

## MITRE ATT&CK Matrix Vectors

| rank | attack_id | attack_vector | tactics | surface | edge_case | related_capec | watch_focus |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | T1003.001 | LSASS Memory | Credential Access | Kerberos / AD | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; User Account; Windows Registry; File |
| 2 | T1068 | Exploitation for Privilege Escalation | Privilege Escalation | PAM / Privileged Identity | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; Container; Module; Driver; Logon Session |
| 3 | T1552.001 | Credentials In Files | Credential Access | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Command; Process; Network Traffic; File; Logon Session |
| 4 | T1136.001 | Local Account | Persistence | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Command; Process; File; User Account |
| 5 | T1078.002 | Domain Accounts | Stealth; Persistence; Privilege Escalation; Initial Access | Identity / IAM; PAM / Privileged Identity | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Logon Session; Process; Network Traffic; User Account |
| 6 | T1025 | Data from Removable Media | Collection | ATM Endpoint | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Drive; Process; File |
| 7 | T1056.004 | Credential API Hooking | Collection; Credential Access | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; Module; File |
| 8 | T1078 | Valid Accounts | Stealth; Persistence; Privilege Escalation; Initial Access | Identity / IAM | Identity / MFA Bypass | CAPEC-560 | Identity / MFA Bypass; Watch: Process; Logon Session; User Account |
| 9 | T1555 | Credentials from Password Stores | Credential Access | Identity / IAM | Identity Blast Radius |  | Identity Blast Radius; Watch: Process; Cloud Service; File |
| 10 | T1003.002 | Security Account Manager | Credential Access | Identity / IAM; Kerberos / AD | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: File; Process; Windows Registry |
| 11 | T1134 | Access Token Manipulation | Stealth; Privilege Escalation | Identity / IAM | Identity / MFA Bypass | CAPEC-633 | Identity / MFA Bypass; Watch: Process; Active Directory; Logon Session |
| 12 | T1003.003 | NTDS | Credential Access | Kerberos / AD | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Volume; Process; File |
| 13 | T1003 | OS Credential Dumping | Credential Access | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; Active Directory; File |
| 14 | T1550.002 | Pass the Hash | Lateral Movement | Kerberos / AD | Identity / MFA Bypass | CAPEC-644 | Identity / MFA Bypass; Watch: Process; Logon Session; Network Traffic; Active Directory |
| 15 | T1484.001 | Group Policy Modification | Defense Impairment; Privilege Escalation | PAM / Privileged Identity | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: User Account; Process; File; Active Directory |
| 16 | T1136.002 | Domain Account | Persistence | Identity / IAM; PAM / Privileged Identity | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Command; User Account; Process; Logon Session |
| 17 | T1111 | Multi-Factor Authentication Interception | Credential Access | Identity / IAM; MFA / SSO | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; Windows Registry; Driver; Logon Session |
| 18 | T1098 | Account Manipulation | Persistence; Privilege Escalation | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; User Account; Active Directory; File |
| 19 | T1550.003 | Pass the Ticket | Lateral Movement | Kerberos / AD | Identity / MFA Bypass | CAPEC-645 | Identity / MFA Bypass; Watch: Process; Active Directory; Module; Logon Session; User Account |
| 20 | T1556 | Modify Authentication Process | Defense Impairment; Persistence; Credential Access | Identity / IAM; MFA / SSO | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; User Account; Windows Registry; File; Module; Cloud Service |
| 21 | T1552.006 | Group Policy Preferences | Credential Access | PAM / Privileged Identity | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; File; Script; Network Share |
| 22 | T1552 | Unsecured Credentials | Credential Access | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Command; Network Traffic; Process; Windows Registry; File; Cloud Service; User Account; Application Log |
| 23 | T1136 | Create Account | Persistence | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Command; User Account; Process; File |
| 24 | T1649 | Steal or Forge Authentication Certificates | Credential Access | Identity / IAM; HSM Adjacent | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Command; Active Directory; File; Windows Registry; Application Log |
| 25 | T1556.006 | Multi-Factor Authentication | Defense Impairment; Persistence; Credential Access | Identity / IAM; MFA / SSO | Identity / MFA Bypass | CAPEC-578 | Identity / MFA Bypass; Watch: User Account; Active Directory; File; Script; Application Log; Cloud Service |
| 26 | T1547.012 | Print Processors | Persistence; Privilege Escalation | MFA / SSO | Living-off-the-Land |  | Living-off-the-Land; Watch: Process; File; Windows Registry; Module |
| 27 | T1484.002 | Trust Modification | Defense Impairment; Privilege Escalation | PAM / Privileged Identity | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Command; User Account; Process; Active Directory; Application Log |
| 28 | T1556.007 | Hybrid Identity | Defense Impairment; Persistence; Credential Access | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: User Account; Active Directory; Module; Logon Session; Application Log; Cloud Service |
| 29 | T1556.001 | Domain Controller Authentication | Defense Impairment; Persistence; Credential Access | Identity / IAM; PAM / Privileged Identity; Kerberos / AD | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; Logon Session; File; Module |
| 30 | T1547.008 | LSASS Driver | Persistence; Privilege Escalation | Kerberos / AD; ATM Endpoint | Living-off-the-Land |  | Living-off-the-Land; Watch: File; Windows Registry; Module; Driver |
| 31 | T1558 | Steal or Forge Kerberos Tickets | Credential Access | Kerberos / AD | Identity / MFA Bypass | CAPEC-652 | Identity / MFA Bypass; Watch: Process; Logon Session; Active Directory; File |
| 32 | T1495 | Firmware Corruption | Impact | ATM Endpoint | Destructive / Ransomware | CAPEC-532 | Destructive / Ransomware; Watch: Firmware; Process; Network Traffic; Driver |
| 33 | T1078.003 | Local Accounts | Stealth; Persistence; Privilege Escalation; Initial Access | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Logon Session; User Account |
| 34 | T1555.004 | Windows Credential Manager | Credential Access | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; File |
| 35 | T1555.005 | Password Managers | Credential Access | Identity / IAM | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; File |
| 36 | T1552.002 | Credentials in Registry | Credential Access | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; Windows Registry |
| 37 | T1558.003 | Kerberoasting | Credential Access | Kerberos / AD | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; Logon Session; Active Directory |
| 38 | T1003.005 | Cached Domain Credentials | Credential Access | Identity / IAM; PAM / Privileged Identity | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; File |
| 39 | T1558.001 | Golden Ticket | Credential Access | Kerberos / AD | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; Logon Session; Active Directory |
| 40 | T1110.002 | Password Cracking | Credential Access | Identity / IAM | Identity / MFA Bypass | CAPEC-55 | Identity / MFA Bypass; Watch: Process; File; User Account |
| 41 | T1558.002 | Silver Ticket | Credential Access | Kerberos / AD | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; Logon Session; Active Directory |
| 42 | T1556.002 | Password Filter DLL | Defense Impairment; Persistence; Credential Access | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: File; Windows Registry; Module |
| 43 | T1621 | Multi-Factor Authentication Request Generation | Credential Access | Identity / IAM; MFA / SSO | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Logon Session; User Account; Application Log |
| 44 | T1556.004 | Network Device Authentication | Defense Impairment; Persistence; Credential Access | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: File; User Account |
| 45 | T1556.003 | Pluggable Authentication Modules | Defense Impairment; Persistence; Credential Access | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; Logon Session; File |
| 46 | T1546.001 | Change Default File Association | Privilege Escalation; Persistence | MFA / SSO | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Process; Logon Session; Windows Registry |
| 47 | T1542.002 | Component Firmware | Stealth; Persistence | ATM Endpoint | Exploit Chain / Multi-Step | CAPEC-638 | Exploit Chain / Multi-Step; Watch: Firmware; Driver |
| 48 | T1098.001 | Additional Cloud Credentials | Persistence; Privilege Escalation | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: User Account; Active Directory |
| 49 | T1606.002 | SAML Tokens | Credential Access | MFA / SSO | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Logon Session; User Account |
| 50 | T1547.002 | Authentication Package | Persistence; Privilege Escalation | Identity / IAM | Living-off-the-Land |  | Living-off-the-Land; Watch: Windows Registry; Module |
| 51 | T1212 | Exploitation for Credential Access | Credential Access | Identity / IAM | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; User Account; Application Log |
| 52 | T1207 | Rogue Domain Controller | Defense Impairment | PAM / Privileged Identity; Kerberos / AD | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; Watch: Network Traffic; Active Directory |
| 53 | T1092 | Communication Through Removable Media | Command and Control | ATM Endpoint | Zero-Day / Unknown Exploit | CAPEC-457 | Zero-Day / Unknown Exploit; Watch: Drive; Process; File |
| 54 | T1087.001 | Local Account | Discovery | Identity / IAM | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Process; User Account; File |
| 55 | T1087.002 | Domain Account | Discovery | Identity / IAM; PAM / Privileged Identity | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Process; Network Traffic |
| 56 | T1201 | Password Policy Discovery | Discovery | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Command; Process; User Account; Active Directory |
| 57 | T1553.004 | Install Root Certificate | Defense Impairment | HSM Adjacent | Telemetry Gap / Evasion | CAPEC-479 | Telemetry Gap / Evasion; Watch: Command; Process; File; Windows Registry |
| 58 | T1542.001 | System Firmware | Stealth; Persistence | ATM Endpoint | Supply Chain / Trusted Dependency | CAPEC-532 | Supply Chain / Trusted Dependency; Watch: Firmware; Drive; Process; File |
| 59 | T1091 | Replication Through Removable Media | Lateral Movement; Initial Access | ATM Endpoint | Zero-Day / Unknown Exploit | CAPEC-457 | Zero-Day / Unknown Exploit; Watch: Drive; Process; File |
| 60 | T1187 | Forced Authentication | Credential Access | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; Watch: Network Traffic; File |
| 61 | T1110.003 | Password Spraying | Credential Access | Identity / IAM | Identity / MFA Bypass | CAPEC-565 | Identity / MFA Bypass; Watch: User Account |
| 62 | T1110.001 | Password Guessing | Credential Access | Identity / IAM | Identity / MFA Bypass | CAPEC-49 | Identity / MFA Bypass; Watch: User Account |
| 63 | T1110.004 | Credential Stuffing | Credential Access | Identity / IAM | Identity / MFA Bypass | CAPEC-600 | Identity / MFA Bypass; Watch: User Account |
| 64 | T1615 | Group Policy Discovery | Discovery | PAM / Privileged Identity | Living-off-the-Land | CAPEC-576 | Living-off-the-Land; Watch: Command; Active Directory; Process; Network Traffic |
| 65 | T1652 | Device Driver Discovery | Discovery | ATM Endpoint | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; Watch: Command; Process; Windows Registry; File |
| 66 | T1404 | Exploitation for Privilege Escalation | Privilege Escalation | PAM / Privileged Identity | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit |
| 67 | T0859 | Valid Accounts | Persistence; Lateral Movement | Identity / IAM | ATM / HSM Safety |  | ATM / HSM Safety |
| 68 | T1694.002 | Hardcoded Credentials | Persistence; Lateral Movement | Identity / IAM | ATM / HSM Safety |  | ATM / HSM Safety |
| 69 | T1458 | Replication Through Removable Media | Initial Access; Lateral Movement | ATM Endpoint | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion |
| 70 | T0890 | Exploitation for Privilege Escalation | Privilege Escalation | PAM / Privileged Identity | ATM / HSM Safety |  | ATM / HSM Safety |
| 71 | T0847 | Replication Through Removable Media | Initial Access | ATM Endpoint | ATM / HSM Safety |  | ATM / HSM Safety |
| 72 | T1693.001 | System Firmware | Persistence; Inhibit Response Function; Impair Process Control | ATM Endpoint | ATM / HSM Safety |  | ATM / HSM Safety |
| 73 | T0800 | Activate Firmware Update Mode | Inhibit Response Function | ATM Endpoint | ATM / HSM Safety |  | ATM / HSM Safety |
| 74 | T1694.001 | Default Credentials | Persistence; Lateral Movement | Identity / IAM | ATM / HSM Safety |  | ATM / HSM Safety |
| 75 | T1694 | Insecure Credentials | Persistence; Lateral Movement | Identity / IAM | ATM / HSM Safety |  | ATM / HSM Safety |
| 76 | T1693.002 | Module Firmware | Persistence; Inhibit Response Function; Impair Process Control | ATM Endpoint | ATM / HSM Safety |  | ATM / HSM Safety |
| 77 | T1693 | Modify Firmware | Persistence; Inhibit Response Function; Impair Process Control | ATM Endpoint | ATM / HSM Safety |  | ATM / HSM Safety |
| 78 | T1634 | Credentials from Password Store | Credential Access | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass |
| 79 | T0892 | Change Credential | Inhibit Response Function | Identity / IAM | ATM / HSM Safety |  | ATM / HSM Safety |

## CAPEC Attack Pattern Matrix

| rank | capec_id | attack_pattern | surface | edge_case | related_attack | watch_focus |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | CAPEC-555 | Remote Services with Stolen Credentials | Identity / IAM | Identity / MFA Bypass | T1021; T1114.002; T1133 | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-294; CWE-308; CWE-309; CWE-521; CWE-522 |
| 2 | CAPEC-568 | Capture Credentials via Keylogger | Identity / IAM | Identity / MFA Bypass | T1056.001 | Identity / MFA Bypass |
| 3 | CAPEC-654 | Credential Prompt Impersonation | Identity / IAM | Identity / MFA Bypass | T1056; T1548.004 | Identity / MFA Bypass; CWE: CWE-1021 |
| 4 | CAPEC-532 | Altered Installed BIOS | ATM Endpoint | Destructive / Ransomware | T1495; T1542.001 | Destructive / Ransomware |
| 5 | CAPEC-163 | Spear Phishing | Identity / IAM | Identity Blast Radius | T1534; T1566.001; T1566.002; T1566.003; T1598.001; T1598.002; T1598.003 | Identity Blast Radius; CWE: CWE-451 |
| 6 | CAPEC-2 | Inducing Account Lockout | Identity / IAM | Identity / MFA Bypass | T1531 | Identity / MFA Bypass; CWE: CWE-645 |
| 7 | CAPEC-564 | Run Software at Logon | Identity / IAM; Kerberos / AD; ATM Endpoint; MFA / SSO | Living-off-the-Land | T1037; T1543.001; T1543.004; T1547 | Living-off-the-Land; CWE: CWE-284 |
| 8 | CAPEC-552 | Install Rootkit | PAM / Privileged Identity | Telemetry Gap / Evasion | T1014; T1542.003; T1547.006 | Telemetry Gap / Evasion; CWE: CWE-284 |
| 9 | CAPEC-473 | Signature Spoof | Identity / IAM | Telemetry Gap / Evasion | T1036.001; T1553.002 | Telemetry Gap / Evasion; CWE: CWE-20; CWE-290; CWE-327 |
| 10 | CAPEC-68 | Subvert Code-signing Facilities | PAM / Privileged Identity; Identity / IAM | Telemetry Gap / Evasion | T1553.002 | Telemetry Gap / Evasion; CWE: CWE-1326; CWE-325; CWE-328 |
| 11 | CAPEC-652 | Use of Known Kerberos Credentials | Kerberos / AD | Identity / MFA Bypass | T1558 | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-294; CWE-307; CWE-308; CWE-309; CWE-522; CWE-654; CWE-836 |
| 12 | CAPEC-645 | Use of Captured Tickets (Pass The Ticket) | Identity / IAM; Kerberos / AD | Identity / MFA Bypass | T1550.003 | Identity / MFA Bypass; CWE: CWE-294; CWE-308; CWE-522 |
| 13 | CAPEC-644 | Use of Captured Hashes (Pass The Hash) | Identity / IAM; Kerberos / AD | Identity / MFA Bypass | T1550.002 | Identity / MFA Bypass; CWE: CWE-294; CWE-308; CWE-522; CWE-836 |
| 14 | CAPEC-633 | Token Impersonation | Identity / IAM | Identity / MFA Bypass | T1134 | Identity / MFA Bypass; CWE: CWE-1270; CWE-287 |
| 15 | CAPEC-578 | Disable Security Software | Identity / IAM; MFA / SSO | Identity / MFA Bypass | T1556.006 | Identity / MFA Bypass; CWE: CWE-284 |
| 16 | CAPEC-561 | Windows Admin Shares with Stolen Credentials | PAM / Privileged Identity; Identity / IAM | Identity / MFA Bypass | T1021.002 | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-294; CWE-308; CWE-309; CWE-521; CWE-522 |
| 17 | CAPEC-560 | Use of Known Domain Credentials | Identity / IAM; PAM / Privileged Identity | Identity / MFA Bypass | T1078 | Identity / MFA Bypass; CWE: CWE-1273; CWE-262; CWE-263; CWE-307; CWE-308; CWE-309; CWE-522; CWE-654 |
| 18 | CAPEC-550 | Install New Service | PAM / Privileged Identity | Identity Blast Radius | T1543 | Identity Blast Radius; CWE: CWE-284 |
| 19 | CAPEC-485 | Signature Spoofing by Key Recreation | Identity / IAM | Identity / MFA Bypass | T1552.004 | Identity / MFA Bypass; CWE: CWE-330 |
| 20 | CAPEC-474 | Signature Spoofing by Key Theft | Identity / IAM | Identity / MFA Bypass | T1552.004 | Identity / MFA Bypass; CWE: CWE-522 |
| 21 | CAPEC-233 | Privilege Escalation | PAM / Privileged Identity | Identity Blast Radius | T1548 | Identity Blast Radius; CWE: CWE-1264; CWE-1311; CWE-269 |
| 22 | CAPEC-122 | Privilege Abuse | PAM / Privileged Identity; Identity / IAM | Identity Blast Radius | T1548 | Identity Blast Radius; CWE: CWE-1317; CWE-269; CWE-732 |
| 23 | CAPEC-115 | Authentication Bypass | MFA / SSO; PAM / Privileged Identity | Identity Blast Radius | T1548 | Identity Blast Radius; CWE: CWE-287 |
| 24 | CAPEC-114 | Authentication Abuse | Identity / IAM | Identity Blast Radius | T1548 | Identity Blast Radius; CWE: CWE-1244; CWE-287 |
| 25 | CAPEC-90 | Reflection Attack in Authentication Protocol | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; CWE: CWE-301; CWE-303 |
| 26 | CAPEC-656 | Voice Phishing | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass |
| 27 | CAPEC-653 | Use of Known Operating System Credentials | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-307; CWE-308; CWE-309; CWE-522; CWE-654 |
| 28 | CAPEC-508 | Shoulder Surfing | HSM Adjacent; Identity / IAM | Insider / Trusted Access |  | Insider / Trusted Access; CWE: CWE-200; CWE-359 |
| 29 | CAPEC-136 | LDAP Injection | Identity / IAM | Rare but High Impact |  | Rare but High Impact; CWE: CWE-20; CWE-77; CWE-90 |
| 30 | CAPEC-69 | Target Programs with Elevated Privileges | PAM / Privileged Identity | Rare but High Impact |  | Rare but High Impact; CWE: CWE-15; CWE-250 |
| 31 | CAPEC-70 | Try Common or Default Usernames and Passwords | Identity / IAM | Identity / MFA Bypass | T1078.001 | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-308; CWE-309; CWE-521; CWE-654; CWE-798 |
| 32 | CAPEC-638 | Altered Component Firmware | ATM Endpoint | Exploit Chain / Multi-Step | T1542.002 | Exploit Chain / Multi-Step |
| 33 | CAPEC-55 | Rainbow Table Password Cracking | Identity / IAM | Identity / MFA Bypass | T1110.002 | Identity / MFA Bypass; CWE: CWE-261; CWE-262; CWE-263; CWE-308; CWE-309; CWE-521; CWE-654; CWE-916 |
| 34 | CAPEC-30 | Hijacking a Privileged Thread of Execution | PAM / Privileged Identity | Exploit Chain / Multi-Step | T1055.003 | Exploit Chain / Multi-Step; CWE: CWE-270 |
| 35 | CAPEC-180 | Exploiting Incorrectly Configured Access Control Security Levels | Identity / IAM | Rare but High Impact | T1574.010 | Rare but High Impact; CWE: CWE-1190; CWE-1191; CWE-1193; CWE-1220; CWE-1268; CWE-1280; CWE-1297; CWE-1311; CWE-1315; CWE-1318; CWE-1320; CWE-1321; CWE-732 |
| 36 | CAPEC-50 | Password Recovery Exploitation | PAM / Privileged Identity; Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; CWE: CWE-522; CWE-640 |
| 37 | CAPEC-16 | Dictionary-based Password Attack | Identity / IAM | Exploit Chain / Multi-Step |  | Exploit Chain / Multi-Step; CWE: CWE-262; CWE-263; CWE-307; CWE-308; CWE-309; CWE-521; CWE-654 |
| 38 | CAPEC-457 | USB Memory Attacks | ATM Endpoint | Zero-Day / Unknown Exploit | T1091; T1092 | Zero-Day / Unknown Exploit; CWE: CWE-1299 |
| 39 | CAPEC-459 | Creating a Rogue Certification Authority Certificate | Kerberos / AD; Identity / IAM | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-290; CWE-295; CWE-327 |
| 40 | CAPEC-98 | Phishing | Identity / IAM | Identity / MFA Bypass | T1566; T1598 | Identity / MFA Bypass; CWE: CWE-451 |
| 41 | CAPEC-576 | Group Permission Footprinting | PAM / Privileged Identity | Living-off-the-Land | T1069; T1615 | Living-off-the-Land; CWE: CWE-200 |
| 42 | CAPEC-575 | Account Footprinting | Identity / IAM; PAM / Privileged Identity | Zero-Day / Unknown Exploit | T1087 | Zero-Day / Unknown Exploit; CWE: CWE-200 |
| 43 | CAPEC-479 | Malicious Root Certificate | HSM Adjacent | Telemetry Gap / Evasion | T1553.004 | Telemetry Gap / Evasion; CWE: CWE-284 |
| 44 | CAPEC-477 | Signature Spoofing by Mixing Signed and Unsigned Content | Identity / IAM | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-311; CWE-319; CWE-693 |
| 45 | CAPEC-476 | Signature Spoofing by Misrepresentation | Identity / IAM | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-290 |
| 46 | CAPEC-164 | Mobile Phishing | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; CWE: CWE-451 |
| 47 | CAPEC-112 | Brute Force | Identity / IAM | Identity / MFA Bypass | T1110 | Identity / MFA Bypass; CWE: CWE-326; CWE-330; CWE-521 |
| 48 | CAPEC-151 | Identity Spoofing | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass; CWE: CWE-287 |
| 49 | CAPEC-600 | Credential Stuffing | Identity / IAM | Identity / MFA Bypass | T1110.004 | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-307; CWE-308; CWE-309; CWE-522; CWE-654 |
| 50 | CAPEC-565 | Password Spraying | Identity / IAM | Identity / MFA Bypass | T1110.003 | Identity / MFA Bypass; CWE: CWE-262; CWE-263; CWE-307; CWE-308; CWE-309; CWE-521; CWE-654 |
| 51 | CAPEC-49 | Password Brute Forcing | Identity / IAM | Identity / MFA Bypass | T1110.001 | Identity / MFA Bypass; CWE: CWE-257; CWE-262; CWE-263; CWE-307; CWE-308; CWE-309; CWE-521; CWE-654 |
| 52 | CAPEC-626 | Smudge Attack | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass |
| 53 | CAPEC-475 | Signature Spoofing by Improper Validation | Identity / IAM | Zero-Day / Unknown Exploit |  | Zero-Day / Unknown Exploit; CWE: CWE-295; CWE-327; CWE-347 |
| 54 | CAPEC-402 | Bypassing ATA Password Security | Identity / IAM | Insider / Trusted Access |  | Insider / Trusted Access; CWE: CWE-285 |
| 55 | CAPEC-195 | Principal Spoof | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass |
| 56 | CAPEC-414 | Pretexting via Delivery Person | Identity / IAM | Identity / MFA Bypass |  | Identity / MFA Bypass |
| 57 | CAPEC-407 | Pretexting | Identity / IAM | Identity / MFA Bypass | T1589 | Identity / MFA Bypass |
| 58 | CAPEC-234 | Hijacking a privileged process | MFA / SSO; PAM / Privileged Identity | Telemetry Gap / Evasion |  | Telemetry Gap / Evasion; CWE: CWE-648; CWE-732 |
