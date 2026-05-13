## Numa

### Install

```shell
yay -S numa-git

sudo numa install
```

```shell
sudo systemctl stop systemd-resolved
sudo systemctl stop systemd-resolved-varlink.socket
sudo systemctl stop systemd-resolved-monitor.socket

sudo systemctl disable systemd-resolved
sudo systemctl disable systemd-resolved-monitor.socket
sudo systemctl disable systemd-resolved-varlink.socket

sudo systemctl start numa
sudo systemctl enable numa

sudo journalctl -t numa -f
```

```shell
sudo vim /etc/numa.toml
[upstream]
address = ["114.114.114.114"]

sudo systemctl restart numa
```

```shell
sudo vim /etc/resolv.conf
nameserver 127.0.0.1
search numa
```

```shell
dig @127.0.0.1 numa.numa
dig numa.numa
```

```shell
open http://numa.numa
```

### Configurate

```shell
sudo vim /etc/numa.toml
[[services]]
name = "frontend"
target_port = 5173

sudo systemctl restart numa
```

