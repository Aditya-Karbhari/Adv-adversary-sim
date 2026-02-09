# Credential Dumping Detection

## Description
Detects credential dumping activity using known tools or suspicious LSASS access.

## Log Source
- Sysmon Event ID 10
- Security Event Logs
- Winlogbeat

## KQL Query
```kql
process.name : ("mimikatz.exe" or "procdump.exe") 
