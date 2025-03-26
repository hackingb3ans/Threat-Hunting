#### SentinelOne
```
(#cmdline contains:anycase 'procdump' AND #cmdline contains:anycase 'lsass') OR (#cmdline contains:anycase 'rundll32' AND #cmdline contains:anycase 'comsvcs' AND #cmdline contains:anycase 'MiniDump')
```

#### Google Chronicle
```
(
    (
        principal.process.command_line = /(?i)procdump/ nocase AND
        principal.process.command_line = /(?i)lsass/ nocase 
    )
    OR
    (
        target.process.command_line = /(?i)procdump/ nocase AND
        target.process.command_line = /(?i)lsass/ nocase 

    )
)
OR
(
    (
        principal.process.command_line = /(?i)rundll32/ nocase AND
        principal.process.command_line = /(?i)comsvcs/ nocase AND
        principal.process.command_line = /(?i)MiniDump/ nocase
    )
OR
    (
        target.process.command_line = /(?i)rundll32/ nocase AND
        target.process.command_line = /(?i)comsvcs/ nocase AND
        target.process.command_line = /(?i)MiniDump/ nocase       
    )
)
```

#### Crowd Strike
```
(CommandLine = /(?i)procdump/ AND CommandLine = /(?i)lsass/)
OR
(CommandLine = /(?i)rundll32/ AND CommandLine = /(?i)comsvcs/ AND CommandLine = /(?i)MiniDump/)
```

#### Techniques:
T1003.001 -  OS Credential Dumping: LSASS Memory
https://attack.mitre.org/techniques/T1003/001/
T1059.001 -  Command and Scripting Interpreter: PowerShell
https://attack.mitre.org/techniques/T1059/001/
