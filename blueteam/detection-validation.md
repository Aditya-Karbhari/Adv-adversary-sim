# Detection Validation Mapping

This section maps each simulated attack technique to its corresponding log source, detection rule, and alert outcome.

| Attack Technique        | Log Source                     | Detection Rule               | Alert Outcome |
|------------------------|--------------------------------|------------------------------|---------------|
| SSH Brute Force        | audit.log / auth.log           | ssh-bruteforce-rule          | Triggered     |
| C2 Beaconing           | Sysmon Event ID 3              | c2-beaconing-rule            | Triggered     |
| Credential Dumping     | Sysmon Event ID 10             | credential-dumping-rule      | Triggered     |
| PowerShell Abuse       | PowerShell Operational Logs    | suspicious-powershell-rule  | Triggered     |
| AD Enumeration         | Windows Security Logs          | N/A                          | Missed        |

## Validation Result
- Behavioral detections proved more reliable than signature-based checks.
- ATT&CK-mapped rules improved traceability and reporting.
