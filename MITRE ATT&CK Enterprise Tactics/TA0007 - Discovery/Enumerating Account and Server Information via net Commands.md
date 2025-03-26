#### SentinelOne

```
(src.process.name contains:anycase 'net.exe' OR tgt.process.name contains:anycase 'net.exe' OR src.process.name contains:anycase 'net1.exe' OR tgt.process.name contains:anycase 'net1.exe') AND #cmdline matches:anycase '(?i)^net\\s+((group|localgroup)\\s+(domain computers|administrators$|domain admins)|net user)'
```

#### Techniques:

T1087.002 -  Account Discovery: Domain Account 
https://attack.mitre.org/techniques/T1087/002/
T1069.001 -  Permission Groups Discovery: Local Groups
https://attack.mitre.org/techniques/T1069/001/
T1069.002 -  Permission Groups Discovery: Domain Groups
https://attack.mitre.org/techniques/T1069/002/
