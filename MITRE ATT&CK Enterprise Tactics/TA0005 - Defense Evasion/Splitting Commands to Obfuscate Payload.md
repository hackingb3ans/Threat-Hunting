#### SentinelOne
```
(src.process.cmdline contains:anycase 'System.IO.StreamReader' AND src.process.cmdline contains:anycase 'System.IO.Compression.GzipStream' AND src.process.cmdline contains:anycase 'System.IO.MemoryStream') OR (tgt.process.cmdline contains:anycase 'System.IO.StreamReader' AND tgt.process.cmdline contains:anycase 'System.IO.Compression.GzipStream' AND tgt.process.cmdline contains:anycase 'System.IO.MemoryStream') OR (cmdScript.content contains:anycase 'System.IO.StreamReader' AND cmdScript.content contains:anycase 'System.IO.Compression.GzipStream' AND cmdScript.content contains:anycase 'System.IO.MemoryStream') 
| group enco=count() by cmdScript.content, src.process.cmdline, tgt.process.cmdline, src.process.user, endpoint.name | sort -enco	 
```

#### Techniques:
T1027 - Obfuscated Files or Information | https://attack.mitre.org/techniques/T1027/
T1059.001 -  Command and Scripting Interpreter: PowerShell | https://attack.mitre.org/techniques/T1059/001/
T1059.003 -  Command and Scripting Interpreter: Windows Command Shell | https://attack.mitre.org/techniques/T1059/003/
