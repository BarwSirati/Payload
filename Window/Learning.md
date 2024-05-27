find information of os
```powershell
Get-WmiObject -Class win32_OperatingSystem | select Version,BuildNumber
```

xfreerdp
```
xfreerdp /u:<username@domain> /p:<password> /v:<remote> /auto-reconnect-max-retries:0 /smart-sizing +clipboard
```

get-alias
```powershell
get-alias
```

Integrity Control Access Control List
```cmd
icacls <path> /grant user:<permisson>
```

- `F` : full access
- `D` :  delete access
- `N` :  no access
- `M` :  modify access
- `RX` :  read and execute access
- `R` :  read-only access
- `W` :  write-only access


