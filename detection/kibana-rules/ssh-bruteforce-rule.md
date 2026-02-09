# SSH Brute Force Detection

## Description
Detects repeated failed SSH authentication attempts from a single source IP, indicating a brute-force attack.

## Log Source
- Filebeat
- Linux audit logs
- /var/log/auth.log
- /var/log/audit/audit.log

## KQL Query
```kql
event.original : "*sshd*" and event.original : "*res=failed*"
