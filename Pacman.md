## pacman

### Mirror

https://archlinux.org/mirrorlist/

```
sudo cp /etc/pacman.d/mirrorlist /etc/pacman.d/mirrorlist.bak
echo 'Server = https://mirrors.bfsu.edu.cn/archlinux/$repo/os/$arch' | sudo tee /etc/pacman.d/mirrorlist
echo 'Server = http://mirrors.163.com/archlinux/$repo/os/$arch' | sudo tee -a /etc/pacman.d/mirrorlist
```

### AUR

```
sudo pacman -S cmake
```

```
# Fix `==> ERROR: Cannot find the fakeroot binary.`
sudo pacman -S base-devel
```

### archlinuxcn repo

https://mirrors.bfsu.edu.cn/help/archlinuxcn/

https://mirrors.163.com/.help/archlinux-cn.html

```
sudo vim /etc/pacman.conf

[archlinuxcn]
SigLevel = Optional TrustedOnly
Server = https://mirrors.bfsu.edu.cn/archlinuxcn/$arch
Server = http://mirrors.163.com/archlinux-cn/$arch
```

```
sudo pacman -Sy archlinuxcn-keyring
```

```
# Require archlinuxcn repo
sudo pacman -S yay
```

```
yay -S downgrade
```

### arch4edu repo

https://mirrors.tuna.tsinghua.edu.cn/help/arch4edu/

```
sudo vim /etc/pacman.conf

[arch4edu]
SigLevel = Optional TrustAll
Server = http://mirrors.tuna.tsinghua.edu.cn/arch4edu/$arch
```

```
yay -Sy arch4edu-keyring
```

### Key

Ref https://wiki.archlinux.org/title/Pacman/Package_signing

```
pacman-key --recv-keys 152AC7B5F7608B26 --keyserver hkps://keyserver.ubuntu.com
```

```
sudo vim /etc/pacman.d/gnupg/gpg.conf

keyserver hkp://keyserver.ubuntu.com
```

### Tips

```
# Removing unused packages
sudo pacman -Rns $(sudo pacman -Qtdq)
```

```
# List install packages by size
sudo pacman -S expac 
expac "%n %m" -l'\n' -Q $(pacman -Qq) | sort -rhk 2 | less
```

#### Error 'could not fully load metadata for package'

```
pacman -Rs xxx
error: could not open file /var/lib/pacman/local/xxx-1.0.0-1/files: No such file or directory
warning: could not fully load metadata for package xxx-1.0.0-1
checking dependencies...
error: failed to prepare transaction (could not satisfy dependencies)
```

```
touch /var/lib/pacman/local/xxx-1.0.0-1/files
pacman -Rs xxx
```
