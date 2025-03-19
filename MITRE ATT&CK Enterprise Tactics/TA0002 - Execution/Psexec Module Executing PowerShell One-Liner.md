#### Sentinel One XDR

```
#cmdline matches:anycase '(?i)\%comspec\% \/b \/c start \/b \/min powershell \-nop \-w hidden \-encodedcommand' OR cmdScript.content matches:anycase '(?i)\%comspec\% \/b \/c start \/b \/min powershell \-nop \-w hidden \-encodedcommand'
```
#### Techniques
T1059.001 - Command and Scripting Interpreter: PowerShell | https://attack.mitre.org/techniques/T1059/001/
T1059.003 - Command and Scripting Interpreter: Windows Command Shell | https://attack.mitre.org/techniques/T1059/003/
T1027.010 - Obfuscated Files or Information: Command Obfuscation | https://attack.mitre.org/techniques/T1027/010/
