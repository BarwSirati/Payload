Upgrading Simple Shells to Fully Interactive TTYs
```bash
python -c 'import pty; pty.spawn("/bin/bash")' # On victim 
ctrl -Z 
stty raw -echo;fg 
export TERM=xterm 
# your terminal type 
# echo $TERM stty rows 29 columns 96 
# your current terminal rows and columns 
# stty -a
```

Alternative ways to spawn a TTY shell (proper terminal)
```bash
/usr/bin/script -qc /bin/bash /dev/null 
/usr/bin/expect -c "spawn bash; interact"
```

zsh to bash
```bash
ps -p $$ 
# check your current shell 
exec bash --login 
# change to bash shell
```

