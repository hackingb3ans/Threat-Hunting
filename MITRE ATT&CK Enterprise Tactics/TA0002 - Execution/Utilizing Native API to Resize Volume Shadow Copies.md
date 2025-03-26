#### SentinelOne

```
(#cmdline matches:anycase 'DeviceIOControl' OR cmdScript.content matches:anycase 'DeviceIOControl') AND cmdScript.content matches:anycase '(?i)0x53C028'
```

#### Techniques:

T1106- Native API
https://attack.mitre.org/techniques/T1106/
T1490 - Inhibit System Recovery
https://attack.mitre.org/techniques/T1490/
T1059.003 - Command and Scripting Interpreter: Windows Command Shell
https://attack.mitre.org/techniques/T1059/003/
