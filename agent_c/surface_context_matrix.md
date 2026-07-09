# Layer 1 Surface Context Matrix

Filtered for Agent C: ATM Endpoint, Identity / IAM, MFA / SSO, PAM / Privileged Identity, Kerberos / AD, HSM / Crypto Boundary surfaces only.
This file is context only and does not provide runtime risk scores.

| rank | attack_id | attack_vector | surface |
| --- | --- | --- | --- |
| 1 | T1003.001 | LSASS Memory | Kerberos / AD |
| 2 | T1068 | Exploitation for Privilege Escalation | PAM / Privileged Identity |
| 3 | T1552.001 | Credentials In Files | Identity / IAM |
| 4 | T1136.001 | Local Account | Identity / IAM |
| 5 | T1078.002 | Domain Accounts | Identity / IAM; PAM / Privileged Identity |
| 6 | T1025 | Data from Removable Media | ATM Endpoint |
| 7 | T1056.004 | Credential API Hooking | Identity / IAM |
| 8 | T1078 | Valid Accounts | Identity / IAM |
| 9 | T1555 | Credentials from Password Stores | Identity / IAM |
| 10 | T1003.002 | Security Account Manager | Identity / IAM; Kerberos / AD |
| 11 | T1134 | Access Token Manipulation | Identity / IAM |
| 12 | T1003.003 | NTDS | Kerberos / AD |
| 13 | T1003 | OS Credential Dumping | Identity / IAM |
| 14 | T1550.002 | Pass the Hash | Kerberos / AD |
| 15 | T1484.001 | Group Policy Modification | PAM / Privileged Identity |
| 16 | T1136.002 | Domain Account | Identity / IAM; PAM / Privileged Identity |
| 17 | T1111 | Multi-Factor Authentication Interception | Identity / IAM; MFA / SSO |
| 18 | T1098 | Account Manipulation | Identity / IAM |
| 19 | T1550.003 | Pass the Ticket | Kerberos / AD |
| 20 | T1556 | Modify Authentication Process | Identity / IAM; MFA / SSO |
| 21 | T1552.006 | Group Policy Preferences | PAM / Privileged Identity |
| 22 | T1552 | Unsecured Credentials | Identity / IAM |
| 23 | T1136 | Create Account | Identity / IAM |
| 24 | T1649 | Steal or Forge Authentication Certificates | Identity / IAM; HSM Adjacent |
| 25 | T1556.006 | Multi-Factor Authentication | Identity / IAM; MFA / SSO |
| 26 | T1547.012 | Print Processors | MFA / SSO |
| 27 | T1484.002 | Trust Modification | PAM / Privileged Identity |
| 28 | T1556.007 | Hybrid Identity | Identity / IAM |
| 29 | T1556.001 | Domain Controller Authentication | Identity / IAM; PAM / Privileged Identity; Kerberos / AD |
| 30 | T1547.008 | LSASS Driver | Kerberos / AD; ATM Endpoint |
| 31 | T1558 | Steal or Forge Kerberos Tickets | Kerberos / AD |
| 32 | T1495 | Firmware Corruption | ATM Endpoint |
| 33 | T1078.003 | Local Accounts | Identity / IAM |
| 34 | T1555.004 | Windows Credential Manager | Identity / IAM |
| 35 | T1555.005 | Password Managers | Identity / IAM |
| 36 | T1552.002 | Credentials in Registry | Identity / IAM |
| 37 | T1558.003 | Kerberoasting | Kerberos / AD |
| 38 | T1003.005 | Cached Domain Credentials | Identity / IAM; PAM / Privileged Identity |
| 39 | T1558.001 | Golden Ticket | Kerberos / AD |
| 40 | T1110.002 | Password Cracking | Identity / IAM |
| 41 | T1558.002 | Silver Ticket | Kerberos / AD |
| 42 | T1556.002 | Password Filter DLL | Identity / IAM |
| 43 | T1621 | Multi-Factor Authentication Request Generation | Identity / IAM; MFA / SSO |
| 44 | T1556.004 | Network Device Authentication | Identity / IAM |
| 45 | T1556.003 | Pluggable Authentication Modules | Identity / IAM |
| 46 | T1546.001 | Change Default File Association | MFA / SSO |
| 47 | T1542.002 | Component Firmware | ATM Endpoint |
| 48 | T1098.001 | Additional Cloud Credentials | Identity / IAM |
| 49 | T1606.002 | SAML Tokens | MFA / SSO |
| 50 | T1547.002 | Authentication Package | Identity / IAM |
| 51 | T1212 | Exploitation for Credential Access | Identity / IAM |
| 52 | T1207 | Rogue Domain Controller | PAM / Privileged Identity; Kerberos / AD |
| 53 | T1092 | Communication Through Removable Media | ATM Endpoint |
| 54 | T1087.001 | Local Account | Identity / IAM |
| 55 | T1087.002 | Domain Account | Identity / IAM; PAM / Privileged Identity |
| 56 | T1201 | Password Policy Discovery | Identity / IAM |
| 57 | T1553.004 | Install Root Certificate | HSM Adjacent |
| 58 | T1542.001 | System Firmware | ATM Endpoint |
| 59 | T1091 | Replication Through Removable Media | ATM Endpoint |
| 60 | T1187 | Forced Authentication | Identity / IAM |
| 61 | T1110.003 | Password Spraying | Identity / IAM |
| 62 | T1110.001 | Password Guessing | Identity / IAM |
| 63 | T1110.004 | Credential Stuffing | Identity / IAM |
| 64 | T1615 | Group Policy Discovery | PAM / Privileged Identity |
| 65 | T1652 | Device Driver Discovery | ATM Endpoint |
| 66 | T1404 | Exploitation for Privilege Escalation | PAM / Privileged Identity |
| 67 | T0859 | Valid Accounts | Identity / IAM |
| 68 | T1694.002 | Hardcoded Credentials | Identity / IAM |
| 69 | T1458 | Replication Through Removable Media | ATM Endpoint |
| 70 | T0890 | Exploitation for Privilege Escalation | PAM / Privileged Identity |
| 71 | T0847 | Replication Through Removable Media | ATM Endpoint |
| 72 | T1693.001 | System Firmware | ATM Endpoint |
| 73 | T0800 | Activate Firmware Update Mode | ATM Endpoint |
| 74 | T1694.001 | Default Credentials | Identity / IAM |
| 75 | T1694 | Insecure Credentials | Identity / IAM |
| 76 | T1693.002 | Module Firmware | ATM Endpoint |
| 77 | T1693 | Modify Firmware | ATM Endpoint |
| 78 | T1634 | Credentials from Password Store | Identity / IAM |
| 79 | T0892 | Change Credential | Identity / IAM |
