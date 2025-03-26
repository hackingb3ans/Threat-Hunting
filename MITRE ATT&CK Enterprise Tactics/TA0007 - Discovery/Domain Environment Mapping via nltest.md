#### SentinelOne
```
(#cmdline contains:anycase 'nltest' OR src.process.parent.cmdline contains 'nltest') AND (#cmdline contains:anycase '/dclist' OR src.process.parent.cmdline contains:anycase '/dclist')
```

#### Google Chronicle
```
(target.process.command_line = /nltest/ nocase OR principal.process.command_line = /nltest/ nocase) AND

(target.process.command_line = /\/dclist/ nocase OR principal.process.command_line = /\/dclist/ nocase)
```

#### Crowd Strike
```
(CommandLine CONTAINS "nltest" OR ParentCommandLine CONTAINS "nltest") AND

(CommandLine CONTAINS "/dclist" OR ParentCommandLine CONTAINS "/dclist")
```

#### Techniques:
T1018 - Remote System Discovery
https://attack.mitre.org/techniques/T1018/
