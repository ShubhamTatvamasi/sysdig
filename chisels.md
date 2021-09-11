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
sudo sysdig -c httplog fd.cip=192.168.0.75 and fd.type=ipv4
```

capture all read/write on specfic file:
```bash
sudo sysdig -c echo_fds "fd.name contains /root/sysdig_lecture/service.conf"
```

capture top local ports:
```bash
sudo sysdig -c fdbytes_by fd.sport
```

