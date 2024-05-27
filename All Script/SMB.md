SMB Enumerate
```bash
smbmap -u 'guest' -p '' -H '<target-ip>'
```

Download File From Public
```bash
smbclient //<IP>/<SHARE> -U <USER> -c "prompt OFF;recurse ON;mget *"
```
