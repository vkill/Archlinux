## System Configuration

### Ref

https://wiki.archlinux.org/index.php/Installation_guide

### Base packages

```
sudo pacman -S vim
```

### Time zone

```
sudo ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime

sudo hwclock --systohc
```

```
sudo timedatectl set-ntp true

timedatectl status
```

### Localization

```
sudo sed -i 's/^#en_US.UTF-8/en_US.UTF-8/' /etc/locale.gen

sudo locale-gen
```

```
echo 'LANG=en_US.UTF-8' | sudo tee /etc/locale.conf
```

### hostname

```
echo vkill-hostname | sudo tee /etc/hostname
```
