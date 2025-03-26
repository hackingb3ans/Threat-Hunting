#### SentinelOne
```
event.type = 'Process Creation' AND src.process.name == 'rclone.exe' AND #cmdline contains ('mega.io', 'ftp')
```

#### Google Chronicle
```
metadata.event_type = "PROCESS_LAUNCH" AND 
target.process.file.full_path = /rclone\.exe$/ nocase AND
(target.process.command_line = /mega\.io/ nocase OR target.process.command_line = /ftp/ nocase)
```

#### Crowd Strike
```
event_simpleName=ProcessRollup2 ImageFileName="rclone.exe" AND 
(CommandLine CONTAINS "mega.io" OR CommandLine CONTAINS "ftp")
```

#### Techniques:
T1048.003 - Exfiltration Over Alternative Protocol: Exfiltration Over Unencrypted Non-C2 Protocol
https://attack.mitre.org/techniques/T1048/003/
T1567.002 - Exfiltration Over Web Service: Exfiltration to Cloud Storage
https://attack.mitre.org/techniques/T1567/002/
