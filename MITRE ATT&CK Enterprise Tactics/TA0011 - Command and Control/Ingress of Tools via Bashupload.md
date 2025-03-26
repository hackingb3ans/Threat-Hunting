#### SentinelOne
```
url.address contains:anycase ('bashupload') OR (src.process.cmdline contains:anycase 'certutil' AND src.process.cmdline contains:anycase 'bashupload')
| group urlv=count() by src.process.name, src.process.user, url.address, src.process.cmdline | sort -urlv
```

#### Google Chronicle
```
target.url = /bashupload/ nocase
(principal.process.command_line = /certutil/ nocase AND principal.process.command_line = /bashupload/ nocase)
security_result.rule_name != "LONI DNS NTP"
```

#### Crowd Strike
```
DomainName = /(?i)bashupload/ OR (CommandLine = /(?i)certutil/ AND CommandLine = /(?i)bashupload/)
```

#### Techniques:
T1105 - Ingress Tool Transfer | https://attack.mitre.org/techniques/T1105/
T1140 - Deobfuscate/Decode Files or Information | https://attack.mitre.org/techniques/T1140/
T1505.003 - Server Software Component: Web Shell | https://attack.mitre.org/techniques/T1505/003/
T1059.001 - Command and Scripting Interpreter: PowerShell | https://attack.mitre.org/techniques/T1059/001/
