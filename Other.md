## Other

### Remote desktop client

```
sudo pacman -S rdesktop

sudo pacman -S remmina libvncserver
yaourt -S remmina-plugin-rdesktop
```

### UI and UX

```
yaourt -S akira
```

### ipa

```
sudo pacman -S libimobiledevice
yaourt -S ideviceinstaller

ideviceinstaller -i ~/Downloads/xxx.ipa
```

### Player

```
sudo pacman -S vlc
```

### BleachBit

```
sudo pacman -S bleachbit
```

### LabelImg

```
yaourt -S labelimg-git
```

### DingTalk

```
yaourt -S dingtalk-bin
```

```
find ~/.config/DingTalk -type f \( -name '*.log' -o -name '*.log.*' \) -ctime +1 | xargs -I{} rm -rf {}

find ~/.config/DingTalk/userdata -type f -ctime +90 | xargs -I{} rm -rf {}
```

### Tencent Meeting

```
yaourt -S wemeet-bin
```

### QQ

```
yaourt -S linuxqq-new
```

