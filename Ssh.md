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

  HostKeyAlgorithms +ssh-dss
  PubkeyAcceptedAlgorithms +ssh-dss

  ControlPersist 1h
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

### Tips

#### sign_and_send_pubkey: no mutual signature supported

```
vim ~/.ssh/config
Host *
  PubkeyAcceptedKeyTypes +ssh-rsa
```

#### Gen

```
ssh-keygen -t rsa -C "username@xxx.com" -f ~/.ssh/id_rsa.xxx
```
