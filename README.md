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

read dump file:
```bash
sudo sysdig -r dump.scap0
```

get 300 system events and save to file:
```bash
sudo sysdig -n 300 -w sysdig-trace-file.scap
```

trace vim file changes:
```bash
sudo sysdig proc.name=vim -w vim-sysdig-trace-file.scap 
```

capture file names opened by vim:
```bash
sudo sysdig -p "%evt.arg.name" proc.name=vim
```

capture all directory changes by user:
```bash
sudo sysdig -p "%evt.arg.path" "evt.type=chdir and user.name=ubuntu"
```







