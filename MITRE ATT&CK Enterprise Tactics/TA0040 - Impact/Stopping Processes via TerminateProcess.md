#### SentinelOne
```
(#cmdline matches:anycase 'TerminateProcess' OR cmdScript.content matches:anycase 'TerminateProcess') src.process.parent.name != 'Code Helper (Plugin)' not(#cmdline contains:anycase 'ScreenConnect')
```

#### Techniques:
T1489 - Service Stop
https://attack.mitre.org/techniques/T1489/
T1106 - Native API
https://attack.mitre.org/techniques/T1106/
