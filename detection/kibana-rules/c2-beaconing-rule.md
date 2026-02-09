# Command-and-Control Beaconing Detection

## Description
Detects periodic outbound network connections indicating C2 beaconing behavior.

## Log Source
- Sysmon Event ID 3
- Winlogbeat
- Filebeat (Linux process + network logs)

## KQL Query
```kql
process.name : "client.exe" or destination.port : 80
