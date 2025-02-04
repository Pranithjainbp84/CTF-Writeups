# Blue Team CTF: Log Analysis Challenge

## 🕵️ Incident:
Detected a brute-force attack using SIEM logs.

## 🔎 Investigation:
1. **Filtered Event Logs** for multiple failed logins.
2. **Identified Source IPs** linked to multiple failed attempts.
3. **Correlated with Threat Feeds** using VirusTotal API.

## 🛡️ Mitigation:
- Blocked the attacker’s IPs.
- Enabled MFA for the affected accounts.
