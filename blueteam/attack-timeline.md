# Attack Timeline

This timeline documents the end-to-end adversary activity executed during the simulation and the corresponding defensive observations in ELK.

| Attack Step              | Time (UTC)          | Detection Log Source        | Alert Triggered |
|--------------------------|---------------------|-----------------------------|-----------------|
| Initial Access (Payload) | 2026-02-01 10:12:04 | Sysmon Event ID 1           | Yes             |
| C2 Beacon Established    | 2026-02-01 10:12:15 | Sysmon Event ID 3           | Yes             |
| Command Execution        | 2026-02-01 10:13:01 | PowerShell 4104             | Yes             |
| Credential Dump Attempt  | 2026-02-01 10:15:22 | Sysmon Event ID 10          | Yes             |
| Lateral Movement Attempt | 2026-02-01 10:18:40 | Security Event Log          | Partial         |
| Persistence Mechanism    | 2026-02-01 10:20:05 | Registry Modification Log  | No              |

## Observations
- Most attacker actions were detected within seconds.
- Persistence-related activity required additional tuning.
