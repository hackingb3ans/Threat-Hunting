#### SentinelOne
```
(#cmdline contains:anycase 'schtasks' AND #cmdline contains:anycase ('create', 'write')) AND #cmdline contains:anycase ('split', 'splitloader') OR task.name contains:anycase ('split', 'splitloader')
```

#### Google Chronicle
```
(
    (principal.process.command_line = /(?i)schtasks/ nocase OR target.process.command_line = /(?i)schtasks/ nocase)
    AND
    (principal.process.command_line = /(?i)(create|write)/ nocase OR target.process.command_line = /(?i)(create|write)/ nocase)
)
AND
(principal.process.command_line = /(?i)(split|splitloader)/ nocase OR target.process.command_line = /(?i)(split|splitloader)/ nocase)
```

#### Crowd Strike
```
(CommandLine = /(?i)schtasks/ AND CommandLine = /(?i)(create|write)/ AND CommandLine = /(?i)(split|splitloader)/) OR #event_simpleName=ScheduledTaskRegistered AND ("split" OR "splitloader")
```

#### Techniques:
T1053.005 -  Scheduled Task/Job: Scheduled Task 
https://attack.mitre.org/techniques/T1053/005/
T1059.001 -  Command and Scripting Interpreter: PowerShell
https://attack.mitre.org/techniques/T1059/001/
