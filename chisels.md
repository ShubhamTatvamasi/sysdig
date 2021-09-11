# Chisels

list all chisels:
```bash
sudo sysdig -cl
```

capture processes with network i/o slower slower than 15 miliseconds:
```bash
sudo sysdig -c netlower 15
```

spy on all data exchange between IP:
```bash
sudo sysdig spy_ip 192.168.0.75
```



