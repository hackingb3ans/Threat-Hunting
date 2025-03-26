#### SentinelOne
```
event.category = 'registry' event.type='Registry Value Delete' AND registry.keyPath in ('HKCU\\Software\\Microsoft\\Windows\\CurrentVersion\\Policies', 'HKCU\\Software\\Microsoft\\WindowsSelfHost', 'HKCU\\Software\\Policies', 'HKLM\\Software\\Microsoft\\Policies', 'HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\Policies', 'HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\WindowsStore\\WindowsUpdate', 'HKLM\\Software\\Microsoft\\WindowsSelfHost', 'HKLM\\Software\\Policies', 'HKLM\\Software\\WOW6432Node\\Microsoft\\Policies', 'HKLM\\Software\\WOW6432Node\\Microsoft\\Windows\\CurrentVersion\\Policies', 'HKLM\\Software\\WOW6432Node\\Microsoft\\Windows\\CurrentVersion\\WindowsStore\\WindowsUpdate')
```

#### Techniques:
T1112 - Modify Registry
https://attack.mitre.org/techniques/T1112/
T1059 -  Command and Scripting Interpreter
https://attack.mitre.org/techniques/T1059/
