## System Desktop

### Ref

https://wiki.archlinux.org/index.php/Xorg

https://wiki.archlinux.org/index.php/KDE

### Plasma

```
sudo pacman -S plasma
```

### SDDM

```
sudo pacman -S sddm

sudo cp /usr/lib/sddm/sddm.conf.d/default.conf /etc/sddm.conf

sudo vim /etc/sddm.conf
Session=plasma.desktop

sudo systemctl enable sddm

sudo systemctl start sddm
```
