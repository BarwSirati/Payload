SMB Enumerate
```bash
smbmap -u 'guest' -p '' -H 10.10.11.202
```

Download File From Public
```bash
smbclient //<IP>/<SHARE> -U <USER> -c "prompt OFF;recurse ON;mget *"
```
