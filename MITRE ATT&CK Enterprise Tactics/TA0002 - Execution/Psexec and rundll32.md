#### Sentinel One XDR
```
(src.process.name matches:anycase 'psexec' OR src.process.displayName matches:anycase 'psexec' OR file.path matches:anycase 'psexec' OR src.process.image.path matches:anycase 'psexec' OR src.process.cmdline matches:anycase 'psexec') AND (#cmdline matches:anycase 'rundll32' OR tgt.file.path matches:anycase 'rundll32')
```
#### Techniques
T1569.002 - System Services: Service Execution | https://attack.mitre.org/techniques/T1569/002/

T1021.002 - Remote Services: SMB/Windows Admin Shares | https://attack.mitre.org/techniques/T1021/002/

T1218.011 - System Binary Proxy Execution: Rundll32 | https://attack.mitre.org/techniques/T1218/011/
