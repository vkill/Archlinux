## System Desktop

### Ref

https://wiki.archlinux.org/index.php/Xorg

https://wiki.archlinux.org/index.php/KDE

### Xorg

```
sudo lspci | grep -e VGA -e 3D
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
```

### PCManFM

```
sudo pacman -S pcmanfm
```

### Nvidia

```
sudo pacman -S nvidia bbswitch

sudo pacman -S opencl-nvidia

sudo pacman -S nvidia-settings

# Require archlinuxcn repo
sudo pacman -S optimus-manager-qt

sudo reboot
```

```
optimus-manager-qt

# change "startup mode" to "Nvidia"

sudo reboot
```

```
glxinfo | grep -i NVIDIA
```

### ARandR

```
sudo pacman -S arandr
```

Select 1600x900
