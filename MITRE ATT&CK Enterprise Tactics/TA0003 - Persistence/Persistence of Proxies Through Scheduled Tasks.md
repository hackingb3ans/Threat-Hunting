#### SentinelOne
```
task.name contains ('SystemBC', 'GhostSOCKS') OR (event.type = 'Registry Key Create' AND registry.value contains ('SystemBC', 'GhostSOCKS') AND registry.keyPath contains 'Run')
```

#### Google Chronicle
```
metadata.event_type = "SCHEDULED_TASK_CREATION" AND
(target.process.command_line = /SystemBC/ nocase OR
target.process.command_line = /GhostSOCKS/ nocase)
OR
(metadata.event_type = "REGISTRY_CREATION") AND
(target.registry.registry_value_name = /SystemBC/ nocase OR
target.registry.registry_value_name = /GhostSOCKS/ nocase) AND
target.registry.registry_key = /.*\\Run$/ nocase
```

#### Crowd Strike
```
CommandLine = /(?i)schtasks/ AND (CommandLine = /(?i)SystemBC/ OR CommandLine = /(?i)GhostSOCKS/)
```

#### Techniques:
T1547.001 - Boot or Logon Autostart Execution: Registry Run Keys / Startup Folder
https://attack.mitre.org/techniques/T1547/001/
T1053.005 - Scheduled Task/Job: Scheduled Task
https://attack.mitre.org/techniques/T1053/005/
