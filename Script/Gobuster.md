Search Directory
```bash
gobuster dir -u 10.10.11.210 -w /usr/share/wordlists/dirb/common.txt
```

Find SubDomain
```bash
gobuster vhost -u {url} -w {wordlist}  --append-domain -t 100
```





