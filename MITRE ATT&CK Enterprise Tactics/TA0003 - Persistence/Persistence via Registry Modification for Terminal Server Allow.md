#### SentinelOne
```
#cmdline matches:anycase '\"HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Control\\\\Terminal Server\"' OR cmdScript.content matches:anycase '\"HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Control\\\\Terminal Server\"' OR registry.value matches:anycase '\"HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Control\\\\Terminal Server\"'
```

#### Techniques:
T1547.001 - Boot or Logon Autostart Execution: Registry Run Keys / Startup Folder | https://attack.mitre.org/techniques/T1547/001/
T1112 - Modify Registry | https://attack.mitre.org/techniques/T1112/
T1021.001 - Remote Services: Remote Desktop Protocol | https://attack.mitre.org/techniques/T1021/001/
