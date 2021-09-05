## Nebula Graph

Ref https://github.com/vkill/VPS/blob/main/NebulaGraph.md

### Install server

Require [debtap](https://github.com/vkill/Archlinux/blob/master/DebPackage.md#debtap)

```
wget https://github.com/vesoft-inc/nebula-graph/releases/download/v2.5.0/nebula-graph-2.5.0.ubuntu2004.amd64.deb

sudo debtap -u nebula-graph-2.5.0.ubuntu2004.amd64.deb

debtap nebula-graph-2.5.0.ubuntu2004.amd64.deb
:: Enter Packager name:
nebula-graph

sudo pacman -U nebula-graph-2.5.0-1-x86_64.pkg.tar.zst

/usr/local/nebula/bin/nebula-graphd --version
```

### Install console

```
wget https://github.com/vesoft-inc/nebula-console/releases/download/v2.5.0/nebula-console-linux-amd64-v2.5.0

sudo mv nebula-console-linux-amd64-v2.5.0 /usr/local/bin/nebula-console
sudo chmod +x /usr/local/bin/nebula-console

/usr/local/bin/nebula-console -v
```
