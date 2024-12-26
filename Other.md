## Other

### Remote desktop client

```
sudo pacman -S rdesktop
```

### VNC client

```
sudo pacman -S remmina libvncserver
```

### UI and UX

```
yay -S akira
```

### ipa

```
sudo pacman -S libimobiledevice
yay -S ideviceinstaller

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
yay -S labelimg-git
```

### DingTalk

```
yay -S dingtalk-bin
```

```
find ~/.config/DingTalk -type f \( -name '*.log' -o -name '*.log.*' \) -ctime +1 | xargs -I{} rm -rf {}

find ~/.config/DingTalk/userdata -type f -ctime +90 | xargs -I{} rm -rf {}
```

### Tencent Meeting

```
yay -S wemeet-bin
```

### QQ

```
yay -S linuxqq
```

### Telegram

```
sudo pacman -S telegram-desktop
```
