# Layer 1 Edge-Case Matrix

Filtered for Agent C: scoped runtime edge cases only.
This file is context only and does not provide runtime risk scores.

| rank | attack_id | attack_vector | edge_case | edge_case_flags | prediction_context |
| --- | --- | --- | --- | --- | --- |
| 1 | T1003.001 | LSASS Memory | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Process; User Account; Windows Registry; File |
| 2 | T1068 | Exploitation for Privilege Escalation | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Process; Container; Module; Driver; Logon Session |
| 3 | T1552.001 | Credentials In Files | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Command; Process; Network Traffic; File; Logon Session |
| 4 | T1136.001 | Local Account | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Command; Process; File; User Account |
| 5 | T1078.002 | Domain Accounts | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Logon Session; Process; Network Traffic; User Account |
| 6 | T1025 | Data from Removable Media | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Drive; Process; File |
| 7 | T1056.004 | Credential API Hooking | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Process; Module; File |
| 8 | T1078 | Valid Accounts | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Process; Logon Session; User Account |
| 9 | T1555 | Credentials from Password Stores | Identity Blast Radius | Identity Blast Radius | Identity Blast Radius; Watch: Process; Cloud Service; File |
| 10 | T1003.002 | Security Account Manager | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: File; Process; Windows Registry |
| 11 | T1134 | Access Token Manipulation | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Process; Active Directory; Logon Session |
| 12 | T1003.003 | NTDS | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Volume; Process; File |
| 13 | T1003 | OS Credential Dumping | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Process; Active Directory; File |
| 14 | T1550.002 | Pass the Hash | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Process; Logon Session; Network Traffic; Active Directory |
| 15 | T1484.001 | Group Policy Modification | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: User Account; Process; File; Active Directory |
| 16 | T1136.002 | Domain Account | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Command; User Account; Process; Logon Session |
| 17 | T1111 | Multi-Factor Authentication Interception | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Process; Windows Registry; Driver; Logon Session |
| 18 | T1098 | Account Manipulation | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Process; User Account; Active Directory; File |
| 19 | T1550.003 | Pass the Ticket | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Process; Active Directory; Module; Logon Session; User Account |
| 20 | T1556 | Modify Authentication Process | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Process; User Account; Windows Registry; File; Module; Cloud Service |
| 21 | T1552.006 | Group Policy Preferences | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Process; File; Script; Network Share |
| 22 | T1552 | Unsecured Credentials | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Command; Network Traffic; Process; Windows Registry; File; Cloud Service; User Account; Application Log |
| 23 | T1136 | Create Account | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Command; User Account; Process; File |
| 24 | T1649 | Steal or Forge Authentication Certificates | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Command; Active Directory; File; Windows Registry; Application Log |
| 25 | T1556.006 | Multi-Factor Authentication | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: User Account; Active Directory; File; Script; Application Log; Cloud Service |
| 26 | T1547.012 | Print Processors | Living-off-the-Land | Living-off-the-Land | Living-off-the-Land; Watch: Process; File; Windows Registry; Module |
| 27 | T1484.002 | Trust Modification | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Command; User Account; Process; Active Directory; Application Log |
| 28 | T1556.007 | Hybrid Identity | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: User Account; Active Directory; Module; Logon Session; Application Log; Cloud Service |
| 29 | T1556.001 | Domain Controller Authentication | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Process; Logon Session; File; Module |
| 30 | T1547.008 | LSASS Driver | Living-off-the-Land | Living-off-the-Land | Living-off-the-Land; Watch: File; Windows Registry; Module; Driver |
| 31 | T1558 | Steal or Forge Kerberos Tickets | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Process; Logon Session; Active Directory; File |
| 32 | T1495 | Firmware Corruption | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: Firmware; Process; Network Traffic; Driver |
| 33 | T1078.003 | Local Accounts | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Logon Session; User Account |
| 34 | T1555.004 | Windows Credential Manager | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Process; File |
| 35 | T1555.005 | Password Managers | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Process; File |
| 36 | T1552.002 | Credentials in Registry | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Process; Windows Registry |
| 37 | T1558.003 | Kerberoasting | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Process; Logon Session; Active Directory |
| 38 | T1003.005 | Cached Domain Credentials | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Process; File |
| 39 | T1558.001 | Golden Ticket | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Process; Logon Session; Active Directory |
| 40 | T1110.002 | Password Cracking | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Process; File; User Account |
| 41 | T1558.002 | Silver Ticket | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Process; Logon Session; Active Directory |
| 42 | T1556.002 | Password Filter DLL | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: File; Windows Registry; Module |
| 43 | T1621 | Multi-Factor Authentication Request Generation | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Logon Session; User Account; Application Log |
| 44 | T1556.004 | Network Device Authentication | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: File; User Account |
| 45 | T1556.003 | Pluggable Authentication Modules | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Process; Logon Session; File |
| 46 | T1546.001 | Change Default File Association | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Process; Logon Session; Windows Registry |
| 47 | T1542.002 | Component Firmware | Exploit Chain / Multi-Step | Exploit Chain / Multi-Step | Exploit Chain / Multi-Step; Watch: Firmware; Driver |
| 48 | T1098.001 | Additional Cloud Credentials | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: User Account; Active Directory |
| 49 | T1606.002 | SAML Tokens | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Logon Session; User Account |
| 50 | T1547.002 | Authentication Package | Living-off-the-Land | Living-off-the-Land | Living-off-the-Land; Watch: Windows Registry; Module |
| 51 | T1212 | Exploitation for Credential Access | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Process; User Account; Application Log |
| 52 | T1207 | Rogue Domain Controller | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Network Traffic; Active Directory |
| 53 | T1092 | Communication Through Removable Media | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Drive; Process; File |
| 54 | T1087.001 | Local Account | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Process; User Account; File |
| 55 | T1087.002 | Domain Account | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Command; Process; Network Traffic |
| 56 | T1201 | Password Policy Discovery | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Command; Process; User Account; Active Directory |
| 57 | T1553.004 | Install Root Certificate | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Command; Process; File; Windows Registry |
| 58 | T1542.001 | System Firmware | Supply Chain / Trusted Dependency | Supply Chain / Trusted Dependency | Supply Chain / Trusted Dependency; Watch: Firmware; Drive; Process; File |
| 59 | T1091 | Replication Through Removable Media | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Drive; Process; File |
| 60 | T1187 | Forced Authentication | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: Network Traffic; File |
| 61 | T1110.003 | Password Spraying | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: User Account |
| 62 | T1110.001 | Password Guessing | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: User Account |
| 63 | T1110.004 | Credential Stuffing | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass; Watch: User Account |
| 64 | T1615 | Group Policy Discovery | Living-off-the-Land | Living-off-the-Land | Living-off-the-Land; Watch: Command; Active Directory; Process; Network Traffic |
| 65 | T1652 | Device Driver Discovery | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Command; Process; Windows Registry; File |
| 66 | T1404 | Exploitation for Privilege Escalation | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit |
| 67 | T0859 | Valid Accounts | ATM / HSM Safety | ATM / HSM Safety | ATM / HSM Safety |
| 68 | T1694.002 | Hardcoded Credentials | ATM / HSM Safety | ATM / HSM Safety | ATM / HSM Safety |
| 69 | T1458 | Replication Through Removable Media | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 70 | T0890 | Exploitation for Privilege Escalation | ATM / HSM Safety | ATM / HSM Safety | ATM / HSM Safety |
| 71 | T0847 | Replication Through Removable Media | ATM / HSM Safety | ATM / HSM Safety | ATM / HSM Safety |
| 72 | T1693.001 | System Firmware | ATM / HSM Safety | ATM / HSM Safety | ATM / HSM Safety |
| 73 | T0800 | Activate Firmware Update Mode | ATM / HSM Safety | ATM / HSM Safety | ATM / HSM Safety |
| 74 | T1694.001 | Default Credentials | ATM / HSM Safety | ATM / HSM Safety | ATM / HSM Safety |
| 75 | T1694 | Insecure Credentials | ATM / HSM Safety | ATM / HSM Safety | ATM / HSM Safety |
| 76 | T1693.002 | Module Firmware | ATM / HSM Safety | ATM / HSM Safety | ATM / HSM Safety |
| 77 | T1693 | Modify Firmware | ATM / HSM Safety | ATM / HSM Safety | ATM / HSM Safety |
| 78 | T1634 | Credentials from Password Store | Identity / MFA Bypass | Identity / MFA Bypass | Identity / MFA Bypass |
| 79 | T0892 | Change Credential | ATM / HSM Safety | ATM / HSM Safety | ATM / HSM Safety |
