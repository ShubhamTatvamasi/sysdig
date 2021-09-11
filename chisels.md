# Chisels

list all chisels:
```bash
sudo sysdig -cl
```

capture processes with network i/o slower slower than 15 miliseconds:
```bash
sudo sysdig -c netlower 15
```

spy on all data exchange between linux and IP:
```bash
sudo sysdig -c spy_ip 192.168.0.75
# This also applies on: spy_port spy_file spy_users
```



