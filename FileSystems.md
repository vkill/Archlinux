## File Systems

```
yaourt -S hfsprogs

# example
sudo modprobe hfsplus
dmg2img -v -i Install.macOS.Catalina.10.15.0.32.dmg -o Install.macOS.Catalina.10.15.0.32.img
sudo mkdir /mnt/img
sudo mount -o loop Install.macOS.Catalina.10.15.6.00.19G73.img /mnt/img
```

```
yaourt -S linux-apfs-dkms-git
```
