#### SentinelOne
```
(src.process.cmdline contains:anycase 'powershell -executionPolicy bypass -enc' OR tgt.process.cmdline contains:anycase 'powershell -executionPolicy bypass -enc') OR cmdScript.content contains:anycase 'powershell -executionPolicy bypass -enc' 
| group findings=count() by src.process.cmdline, tgt.process.cmdline, cmdScript.content, src.process.user, endpoint.name 
| sort -findings 
| filter findings <= 100 
```

#### Techniques:
T1027.013 -  Obfuscated Files or Information: Encrypted/Encoded File | https://attack.mitre.org/techniques/T1027/013/
T1059.001 -  Command and Scripting Interpreter: PowerShell | https://attack.mitre.org/techniques/T1059/001/
T1059.003 -  Command and Scripting Interpreter: Windows Command Shell | https://attack.mitre.org/techniques/T1059/003/
