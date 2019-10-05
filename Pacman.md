## pacman

### archlinuxcn repo

https://mirrors.163.com/.help/archlinux-cn.html

```
sudo vim /etc/pacman.conf

[archlinuxcn]
SigLevel = Optional TrustedOnly
Server = http://mirrors.163.com/archlinux-cn/$arch
```

```
sudo pacman -S archlinuxcn-keyring
```
