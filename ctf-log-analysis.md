🕵️ Incident:

A brute-force attack was detected through SIEM logs, where there were several failed login attempts from multiple IP addresses on critical accounts.

🔎 Investigation:

- Step 1: Collected and filtered Windows Event Logs using the event ID for failed logins (4625) and successful logins (4624).
- Step 2: Identified IP addresses responsible for multiple failed login attempts.
- Step 3: Correlated the failed login events with successful logins and unusual activities (such as process executions or privilege escalation).
- Step 4: Used VirusTotal API to check if the suspicious IP addresses were linked to any known threat actors.
- Step 5: Used custom scripts to search for system and user anomalies in other logs like PowerShell logs and audit logs.

🛡️ Mitigation:
- Step 1: Blocked the suspicious IPs via the firewall and updated the system’s intrusion detection system (IDS) rules.
- Step 2: Enabled Multi-Factor Authentication (MFA) for all accounts involved in the suspicious logins.
- Step 3: Conducted a full malware scan and cleared any found artifacts on affected systems.
- Step 4: Reset passwords for accounts with potential compromise.
- Step 5: Implemented additional monitoring and alerting for brute-force attack patterns.
