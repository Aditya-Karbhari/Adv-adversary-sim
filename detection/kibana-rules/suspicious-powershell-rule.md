# Suspicious PowerShell Execution

## Description
Detects potentially malicious PowerShell execution patterns.

## Log Source
- PowerShell Operational Logs
- Sysmon Event ID 1

## KQL Query
```kql
event.code : 4104 and powershell.command_line : ("Invoke-Mimikatz" or "IEX")
