## IBus

### Install

```
sudo pacman -S ibus ibus-sunpinyin ibus-libpinyin
```

```
sudo vim /etc/xprofile

export GTK_IM_MODULE=ibus
export XMODIFIERS=@im=ibus
export QT_IM_MODULE=ibus
ibus-daemon -rvx -d &
```
