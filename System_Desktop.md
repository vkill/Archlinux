## System Desktop

### Ref

https://wiki.archlinux.org/index.php/Xorg

https://wiki.archlinux.org/index.php/KDE

### Xorg

```
sudo lspci -k | grep -A 2 -E "(VGA|3D)"
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

Ref https://wiki.archlinux.org/title/NVIDIA

```
sudo vim /etc/sddm.conf
#DisplayCommand=/usr/share/sddm/scripts/Xsetup
#DisplayStopCommand=/usr/share/sddm/scripts/Xstop
```

```
sudo pacman -S nvidia bbswitch

sudo pacman -S opencl-nvidia

sudo pacman -S nvidia-settings

yaourt -S optimus-manager-qt

sudo shutdown -r now
```

```
optimus-manager-qt

# change "startup mode" to "Nvidia"

sudo shutdown -r now
```

```
glxinfo | grep -i NVIDIA

__GL_SYNC_TO_VBLANK=0 glxgears
```

### Intel graphics

```
sudo pacman -Rs xf86-video-intel

sudo pacman -S mesa vulkan-intel
```

### ARandR

```
sudo pacman -S arandr
```

Select 1600x900

### Keyring

```
sudo pacman -S seahorse
```

```
seahorse
```

Ref https://wiki.archlinux.org/title/GNOME/Keyring#Manage_using_GUI



