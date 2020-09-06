## Proxy

### shadowsocks

```
sudo pacman -S shadowsocks-libev

sudo pacman -S shadowsocks-v2ray-plugin
```

```
sudo mkdir /etc/shadowsocks
```

```
sudo vim /etc/shadowsocks/1086.json

{
    "server": "x.x.x.x",
    "server_port": 443,
    "local_address": "0.0.0.0",
    "local_port": 1086,
    "password": "xxx",
    "timeout": 300,
    "method": "xchacha20-ietf-poly1305",
    "fast_open": true,
    "plugin": "v2ray-plugin",
    "plugin_opts": "xxx"
}
```

```
sudo systemctl start shadowsocks-libev@1086

sudo journalctl --no-pager -f -u shadowsocks-libev@1086

sudo systemctl enable shadowsocks-libev@1086
```

### trojan

```
sudo pacman -S trojan
```

```
sudo cp /etc/trojan/config.json /etc/trojan/1081.json

sudo systemctl start trojan@1081

sudo journalctl --no-pager -f -u trojan@1081

sudo systemctl enable trojan@1081
```

### v2ray

```
sudo pacman -S v2ray
```

### proxychains

```
sudo psudo pacman -S proxychains-ng
```

```
sudo vim /etc/proxychains.conf

socks5 127.0.0.1 1081
```

### polipo

```
sudo pacman -S polipo
```

```
sudo vim /etc/polipo/config

proxyAddress=0.0.0.0
proxyPort=8118
socksParentProxy=127.0.0.1:1081
socksProxyType=socks5
```

```
sudo systemctl start polipo
sudo journalctl --no-pager -f -u polipo

sudo systemctl enable polipo
```
