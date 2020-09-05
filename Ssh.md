## Ssh

```
sudo pacman -S openssh keychain
```

```
mkdir ~/.ssh
chmod 700 ~/.ssh
```

```
mkdir ~/.ssh/sockets
chmod 700 ~/.ssh/sockets

vim ~/.ssh/config
Host *
  Compression yes
  ServerAliveInterval 60
  ServerAliveCountMax 5

  ControlPersist 4h
  ControlMaster auto
  ControlPath ~/.ssh/sockets/%r@%h-%p
```

```
vim ~/.xprofile

eval $(keychain --eval --quiet ~/.ssh/id_rsa ~/.ssh/id_rsa_foo)
```

```
ssh-add -l
```
