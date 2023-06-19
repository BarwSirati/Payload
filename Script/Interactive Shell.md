```bash
/usr/bin/script -qc /bin/bash /dev/null 
ctrl -Z 
stty raw -echo;fg 
export TERM=xterm
```
