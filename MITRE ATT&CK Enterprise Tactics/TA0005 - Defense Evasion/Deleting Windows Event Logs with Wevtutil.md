#### SentinelOne
```
src.process.name contains:anycase 'wevtutil' AND #cmdline matches:anycase '(?i)cl \"(system|application|security)\"'
```

#### Techniques:
T1070.001 - Indicator Removal: Clear Windows Event Logs
https://attack.mitre.org/versions/v14/techniques/T1070/001/
T1562.002 - Impair Defenses: Disable Windows Event Logging
https://attack.mitre.org/techniques/T1562/002/
