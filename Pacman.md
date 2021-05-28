## pacman

### Mirror

https://archlinux.org/mirrorlist/

```
cp /etc/pacman.d/mirrorlist /etc/pacman.d/mirrorlist.bak
echo 'Server = http://mirrors.163.com/archlinux/$repo/os/$arch' > /etc/pacman.d/mirrorlist
echo 'Server = https://mirrors.bfsu.edu.cn/archlinux/$repo/os/$arch' >> /etc/pacman.d/mirrorlist
```

### AUR

```
# Fix `==> ERROR: Cannot find the fakeroot binary.`

sudo pacman -S base-devel
```

### archlinuxcn repo

https://mirrors.163.com/.help/archlinux-cn.html

https://mirrors.bfsu.edu.cn/help/archlinuxcn/

```
sudo vim /etc/pacman.conf

[archlinuxcn]
SigLevel = Optional TrustedOnly
Server = http://mirrors.163.com/archlinux-cn/$arch
Server = https://mirrors.bfsu.edu.cn/archlinuxcn/$arch
```

```
sudo pacman -Sy archlinuxcn-keyring
```

```
# Require archlinuxcn repo
sudo pacman -S yaourt

echo 'AURURL="https://aur.tuna.tsinghua.edu.cn"' | sudo tee -a /etc/yaourtrc
```

```
yaourt -S downgrade
```

### arch4edu repo

```
sudo vim /etc/pacman.conf

[arch4edu]
SigLevel = Optional TrustAll
Server = http://mirrors.tuna.tsinghua.edu.cn/arch4edu/$arch
```

```
yaourt -Sy arch4edu-keyring
```

### Tips

```
# Removing unused packages
sudo pacman -Rns $(sudo pacman -Qtdq)
```
