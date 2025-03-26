#### SentinelOne
```
#cmdline matches:anycase '(?i)\\/C \"(vssadmin|vssadmin\.exe|wmic|wmic.exe)\\s+(Delete Shadows|Shadowcopy)' OR cmdScript.content matches:anycase '(?i)\\/C \"(vssadmin|vssadmin\.exe|wmic|wmic.exe)\\s+(Delete Shadows|Shadowcopy)'
```

#### Techniques:
T1490 - Inhibit System Recovery | https://attack.mitre.org/techniques/T1490/
T1059.003 - Command and Scripting Interpreter: Windows Command Shell | https://attack.mitre.org/techniques/T1059/003/
