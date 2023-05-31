Enumeration
```bash
nmap -sV -Pn 10.10.11.202
```

![[Pasted image 20230312235218.png]]

SMB Enumerate
```bash
smbmap -u 'guest' -p '' -H 10.10.11.202
```

![[Pasted image 20230312235546.png]]

Download File From Public
```bash
smbclient //<IP>/<SHARE> -U <USER> -c "prompt OFF;recurse ON;mget *"
```

Referrence
[OSCP personal cheatsheet (liodeus.github.io)](https://liodeus.github.io/2020/09/18/OSCP-personal-cheatsheet.html#smb---445)

