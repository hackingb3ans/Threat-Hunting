#### SentinelOne

```
(src.process.name contains:anycase 'nltest' or src.process.displayName contains:anycase 'nltest') AND (src.process.cmdline contains:anycase 'domain_trusts' OR tgt.process.cmdline contains:anycase 'domain_trusts')
```

#### Techniques:
T1482 - Domain Trust Discovery
https://attack.mitre.org/techniques/T1482/
T1059.001 -  Command and Scripting Interpreter: PowerShell 
https://attack.mitre.org/techniques/T1059/001/
