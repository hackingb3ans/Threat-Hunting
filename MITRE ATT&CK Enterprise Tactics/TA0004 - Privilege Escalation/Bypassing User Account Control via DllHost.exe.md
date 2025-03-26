#### SentinelOne
```
src.process.name contains:anycase 'dllhost.exe' AND (#cmdline contains:anycase '3E5FC7F9-9A51-4367-9063-A120244FBEC7' OR #cmdline contains:anycase 'D2E7041B-2927-42FB-8E9F-7CE93B6DC937')
```

#### Techniques:
T1548.002 -  Abuse Elevation Control Mechanism: Bypass User Account Control 
https://attack.mitre.org/techniques/T1548/002/
T1559.001 -  Inter-Process Communication: Component Object Model
https://attack.mitre.org/techniques/T1559/001/

#### Further Explanation:
The adversary is attempting to bypass Windows UAC via the ICMLuaUtil Elevated COM interface [1].

[1] https://www.elastic.co/guide/en/security/current/uac-bypass-via-icmluautil-elevated-com-interface.html
