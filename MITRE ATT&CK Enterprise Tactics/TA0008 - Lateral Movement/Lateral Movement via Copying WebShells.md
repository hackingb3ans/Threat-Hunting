#### SentinelOne
```
(tgt.process.image.path contains:anycase 'HttpProxy' OR src.process.cmdline contains:anycase 'HttpProxy' OR tgt.process.cmdline contains:anycase 'HttpProxy') AND (src.process.cmdline contains:anycase 'copy')
| group wscpy=count() by src.process.cmdline, src.process.image.path | sort -wscpy
```

#### Google Chronicle
```
(target.process.file.full_path = /HttpProxy/ nocase OR principal.process.command_line = /HttpProxy/ nocase OR target.process.command_line = /HttpProxy/ nocase) AND principal.process.command_line = /copy/ nocase
```

#### Crowd Strike
```
(FilePath = /(?i)HttpProxy/ OR CommandLine = /(?i)HttProxy/) AND CommandLine = /(?i)copy/
```

#### Techniques:
T1570 - Lateral Tool Transfer | https://attack.mitre.org/techniques/T1570/
T1047 - Windows Management Instrumentation | https://attack.mitre.org/techniques/T1047/
T1059.003 - Command and Scripting Interpreter: Windows Command Shell | https://attack.mitre.org/techniques/T1059/003/
T1505.003 - Server Software Component: Web Shell | https://attack.mitre.org/techniques/T1505/003/
