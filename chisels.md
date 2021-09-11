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

list all files with top read/write:
```bash
sudo sysdig -c topfiles_bytes "not fd.name contains /proc"
sudo sysdig -c topfiles_bytes "not (fd.name contains /home/ubuntu/Download or fd.name contains /home/ubuntu/Documents)"
```

capture http request on your web server from specfic IP:
```bash
sudo sysdig -c httplog fd.cip=192.168.0.75
```

