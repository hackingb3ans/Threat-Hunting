#### SentinelOne

```
(src.process.name = "SystemSettings.exe" AND tgt.process.name = "SystemSettingsAdminFlows.exe") AND (#cmdline contains:anycase 'Disable' OR cmdScript.content contains:anycase 'Disable')
```

#### Techniques:
T1562.001 - Impair Defenses: Disable or Modify Tools
https://attack.mitre.org/techniques/T1562/001/
T1059.003 - Command and Scripting Interpreter: Windows Command Shell
https://attack.mitre.org/techniques/T1059/003/
