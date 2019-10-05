## System Desktop

### Ref

https://wiki.archlinux.org/index.php/Xorg

https://wiki.archlinux.org/index.php/KDE

### Xorg

```
lspci | grep -e VGA -e 3D
```

```
sudo pacman -S xf86-video-vesa xf86-video-intel
```

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
