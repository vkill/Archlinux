## Nebula Graph

Ref https://github.com/vkill/VPS/blob/main/NebulaGraph.md

### Install server

Require [debtap](https://github.com/vkill/Archlinux/blob/master/DebPackage.md#debtap)

```
wget https://github.com/vesoft-inc/nebula-graph/releases/download/v2.0.0/nebula-graph-2.0.0.ubuntu2004.amd64.deb

sudo debtap -u nebula-graph-2.0.0.ubuntu2004.amd64.deb

debtap nebula-graph-2.0.0.ubuntu2004.amd64.deb
:: Enter Packager name:
nebula-graph

sudo pacman -U nebula-graph-2.0.0-1-x86_64.pkg.tar.zst
```

### Install console

```
wget https://github.com/vesoft-inc/nebula-console/releases/download/v2.0.0-ga/nebula-console-linux-amd64-v2.0.0-ga

sudo mv nebula-console-linux-amd64-v2.0.0-ga /usr/local/bin/nebula-console
sudo chmod +x /usr/local/bin/nebula-console
```
