## Nebula Graph

Ref https://low-orbit.net/arch-linux-how-to-install-deb-package

### Install debtap

```
yaourt -S debtap

sudo su - root
proxychains debtap -u
```

### Convert and install

```
wget https://github.com/vesoft-inc/nebula-graph/releases/download/v2.0.0-rc1/nebula-graph-2.0.0-rc1.ubuntu2004.amd64.deb

debtap nebula-graph-2.0.0-rc1.ubuntu2004.amd64.deb
:: Enter Packager name:
nebula-graph

sudo pacman -U nebula-graph-2.0.0rc1-1-x86_64.pkg.tar.zst
```
