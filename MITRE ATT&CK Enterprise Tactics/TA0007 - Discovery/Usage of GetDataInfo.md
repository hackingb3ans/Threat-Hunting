#### SentinelOne
```
(#cmdline matches:anycase 'C:\\\\Users.*\\7z.exe' OR cmdScript.content matches:anycase 'C:\\\\Users.*\\7z.exe') OR ((#cmdline matches:anycase 'powershell\\.exe -executionpolicy remotesigned -File \\.\\\\Get-DataInfo\\.ps1' OR cmdScript.content matches:anycase 'powershell\\.exe -executionpolicy remotesigned -File \\.\\\\Get-DataInfo\\.ps1') OR #cmdline matches:anycase 'Get-DataInfo\\.ps1')
```

#### Techniques:
T1059.001 - Command and Scripting Interpreter: PowerShell | https://attack.mitre.org/techniques/T1059/001/
T1059.003 - Command and Scripting Interpreter: Windows Command Shell | https://attack.mitre.org/techniques/T1059/003/
T1005 - Data From Local System | https://attack.mitre.org/techniques/T1005/
T1560.001 - Archive Collected Data: Archive via Utility | https://attack.mitre.org/techniques/T1560/001/
