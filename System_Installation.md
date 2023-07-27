## System Installation

### Ref

https://wiki.archlinux.org/index.php/Installation_guide

https://itsfoss.com/install-arch-linux/

### Make live USB

```
wget https://mirrors.163.com/archlinux/iso/2023.07.01/archlinux-2023.07.01-x86_64.iso

wget https://mirrors.163.com/archlinux/iso/2023.07.01/sha256sums.txt
grep archlinux-2023.07.01-x86_64.iso sha256sums.txt | sha256sum -c -
rm -rf sha256sums.txt
```

```
sudo dd bs=4M if=archlinux-2023.07.01-x86_64.iso of=/dev/sdx status=progress oflag=sync

sync
```

### Boot from live USB

Disable "Secure Boot"

### Pre-Installation

```
fdisk /dev/nvme0n1

Disklabel type: gpt

nvme0n1p1 260M EFI System
nvme0n1p2 100G  Linux filesystem
nvme0n1p3 xxG  Linux filesystem
```

```
mkfs.fat -F32 /dev/nvme0n1p1
mkfs.ext4 /dev/nvme0n1p2
mkfs.ext4 /dev/nvme0n1p3
```

```
ip link

# LAN
# Insert network cable into LAN port on the network router
dhcpcd enp0s31f6

# WiFi
# https://wiki.archlinux.org/index.php/Iwd
iwctl --passphrase WIFI_PASSWORD station wlan0 connect WIFI_SSID

ping archlinux.org
```

```
cp /etc/pacman.d/mirrorlist /etc/pacman.d/mirrorlist.bak
cat /etc/pacman.d/mirrorlist.bak | grep 163 > /etc/pacman.d/mirrorlist
```

### Installation

```
mount /dev/nvme0n1p2 /mnt

mkdir -p /mnt/media/data
mount /dev/nvme0n1p3 /mnt/media/data
```

```
pacstrap /mnt base base-devel linux linux-firmware dhcpcd iwd vim
```

```
arch-chroot /mnt

pacman -S grub efibootmgr

mkdir /boot/efi
mount /dev/nvme0n1p1 /boot/efi
grub-install --target=x86_64-efi --efi-directory=/boot/efi --bootloader-id=GRUB
umount /boot/efi

grub-mkconfig -o /boot/grub/grub.cfg

passwd

useradd -m YOURUSERNAME

passwd YOURUSERNAME

echo '%YOURUSERNAME ALL=(ALL) NOPASSWD: ALL' >> /etc/sudoers

sync
exit
```

```
genfstab -U /mnt >> /mnt/etc/fstab
```

```
sync

umount /mnt/media/data
umount /mnt

sync

shutdown -r now
```

### Tips

If `ifconfig -a` can't find wlan0, please check if linux-firmware is uninstalled.

### Fix EFI

```
mount /dev/nvme0n1p2 /mnt
arch-chroot /mnt

mount /dev/nvme0n1p1 /boot/efi
grub-install --target=x86_64-efi --efi-directory=/boot/efi --bootloader-id=GRUB
umount /boot/efi

exit
umount /mnt
```
