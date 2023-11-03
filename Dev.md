## Dev

```
sudo pacman -S wget curl aria2
```

```
sudo pacman -S git tig
```

```
sudo pacman -S ansible
```

```
sudo pacman -S postgresql-libs
```

```
sudo pacman -S mariadb-clients
```

```
sudo pacman -S redis
```

```
sudo pacman -S imagemagick
```

```
sudo pacman -S protobuf
```

```
sudo pacman -S ruby ruby-rdoc
```

```
sudo pacman -S nodejs yarn npm typescript ts-node

yarn cache clean
```

```
yay -S mongodb-compass
```

```
sudo pacman -S dbeaver
```

```
sudo pacman -S rpm
```

```
sudo pacman -S ecapture
sudo pacman -S gnutls
sudo pacman -S nspr

sudo ecapture tls --libssl=/usr/lib/libssl.so --gnutls=/usr/lib/libgnutls.so --nspr=/usr/lib/libnspr4.so
```

### Git fetch all repos in a folder

```
find . -type d -mindepth 1 -maxdepth 1 | xargs -I{} -P4 git --git-dir={}/.git --work-tree=$PWD/{} fetch
find . -type d -mindepth 1 -maxdepth 1 | xargs -I{} git --git-dir={}/.git --work-tree=$PWD/{} rebase
```
