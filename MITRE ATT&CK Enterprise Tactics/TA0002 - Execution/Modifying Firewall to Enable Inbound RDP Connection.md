#### SentinelOne
```
| filter (src.process.cmdline contains:anycase "netsh advfirewall firewall add rule name" OR tgt.process.cmdline contains:anycase "netsh advfirewall firewall add rule name" OR cmdScript.content contains:anycase "netsh advfirewall firewall add rule name") AND (src.process.cmdline contains:anycase "dir=in" OR tgt.process.cmdline contains:anycase "dir=in" OR cmdScript.content contains:anycase "dir=in") AND (src.process.cmdline contains:anycase ("localport=3389", "localport=5504", "localport=5985", "localport=445") OR tgt.process.cmdline contains:anycase ("localport=3389", "localport=5504", "localport=5985", "localport=445") OR cmdScript.content contains:anycase ("localport=3389", "localport=5504", "localport=5985", "localport=445")) AND (src.process.cmdline contains:anycase "protocol=tcp" OR tgt.process.cmdline contains:anycase "protocol=tcp" OR cmdScript.content contains:anycase "protocol=tcp") 
| group netcount=count() by src.process.cmdline, tgt.process.cmdline, cmdScript.content, src.process.user, endpoint.name | sort -netcount 
```

#### Techniques:
T1562.004 - Impair Defenses: Disable or Modify System Firewall | https://attack.mitre.org/techniques/T1562/004/
T1059.001 -  Command and Scripting Interpreter: PowerShell | https://attack.mitre.org/techniques/T1059/001/
T1059.003 -  Command and Scripting Interpreter: Windows Command Shell | https://attack.mitre.org/techniques/T1059/003/
