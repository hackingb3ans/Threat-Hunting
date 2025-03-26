#### SentinelOne
```
#cmdline matches:anycase '(?i)reg add HKEY_LOCAL_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Services\\\\LanmanServer\\\\Parameters' OR cmdScript.content matches:anycase '(?i)reg add HKEY_LOCAL_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Services\\\\LanmanServer\\\\Parameters' OR registry.value matches:anycase '(?i)reg add HKEY_LOCAL_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Services\\\\LanmanServer\\\\Parameters'
```

#### Techniques:
T1021.002 - Remote Services: SMB/Windows Admin Shares | https://attack.mitre.org/techniques/T1021/002/
T1112 - Modify Registry | https://attack.mitre.org/techniques/T1112/
