## keychain

```
sudo pacman -S openssh keychain
```

```
mkdir ~/.ssh
```

```
vim ~/.xprofile

eval $(keychain --eval --quiet ~/.ssh/id_rsa ~/.ssh/id_rsa_foo)
```

```
ssh-add -l
```
