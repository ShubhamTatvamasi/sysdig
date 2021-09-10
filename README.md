# sysdig

install sysdig:
```bash
curl -s https://s3.amazonaws.com/download.draios.com/stable/install-sysdig | sudo bash
```

filter sysdig output:
```bash
sudo sysdig evt.type=write and proc.name=bash or proc.name=zsh
```

write output to file:
```bash
sudo sysdig -G 10800 -W 72 -w dump.scap
```

