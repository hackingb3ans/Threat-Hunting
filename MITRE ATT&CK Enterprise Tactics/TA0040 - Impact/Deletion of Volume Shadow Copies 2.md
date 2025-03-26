#### SentinelOne
```
| filter (src.process.cmdline contains:anycase 'Delete Shadow' OR tgt.process.cmdline contains:anycase 'Delete Shadow' OR src.process.parent.cmdline contains:anycase 'Delete Shadow') OR ((src.process.cmdline contains:anycase '\bdel\b' OR tgt.process.cmdline contains:anycase '\bdel\b' OR src.process.parent.cmdline contains:anycase '\bdel\b') AND (src.process.cmdline contains:anycase '.bak' OR tgt.process.cmdline contains:anycase '.bak' OR src.process.parent.cmdline contains:anycase '.bak')) 
| group IM01=count() by src.process.user, src.process.name, src.process.parent.name, src.process.parent.cmdline, src.process.cmdline, tgt.process.cmdline, timestamp | sort -IM01 
```

#### Techniques:
T1490 - Inhibit System Recovery | https://attack.mitre.org/techniques/T1490/
T1489 - Service Stop | https://attack.mitre.org/techniques/T1489/
