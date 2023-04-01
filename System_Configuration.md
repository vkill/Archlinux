## System Configuration

### Ref

https://wiki.archlinux.org/index.php/Installation_guide

### WiFi

https://wiki.archlinux.org/index.php/Iwd

```
sudo systemctl enable iwd
sudo systemctl start iwd

sudo iwctl --passphrase WIFI_PASSWORD station wlan0 connect WIFI_SSID

sudo cat /var/lib/iwd/WIFI_SSID.psk
```

```
sudo vim /etc/systemd/network/wlan0.network
[Match]
Name=wlan0

[Network]
DHCP=yes

[DHCP]
UseDNS=false

sudo systemctl enable systemd-networkd
sudo systemctl start systemd-networkd

ping 8.8.8.8
```

```
sudo vim /etc/systemd/resolved.conf
[Resolve]
DNS=8.8.8.8

sudo systemctl enable systemd-resolved
sudo systemctl start systemd-resolved

sudo ln -sf /run/systemd/resolve/stub-resolv.conf /etc/resolv.conf

ping archlinux.org
```

### Base packages

```
sudo pacman -S net-tools dnsutils inetutils htop linux-headers
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
echo YOURUSERNAME-archlinux | sudo tee /etc/hostname
```

### font

```
sudo pacman -S wqy-zenhei wqy-microhei

sudo pacman -S ttf-dejavu adobe-source-code-pro-fonts
```

### USB Personal Hotspot

Ref https://wiki.archlinux.org/index.php/IPhone_tethering

```
sudo pacman -S dhcpcd

networkctl list
sudo dhcpcd enp0sxxxxxxxxxx
```

### Clear trash

```
sudo rm -rf ~/.local/share/Trash/*
```

