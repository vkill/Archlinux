## Terminal

### Terminator

```
sudo pacman -S terminator
```

Preferences -> Profiles -> Command -> Enable "Run command as a login shell"

### Oh My Zsh

```
sudo pacman -S zsh zsh-completions
```

```
# Require archlinuxcn repo
pacman -S oh-my-zsh-git
```

```
cp /usr/share/oh-my-zsh/zshrc ~/.zshrc

vim ~/.zshrc

ZSH_THEME="gnzh"

DISABLE_AUTO_UPDATE="true"

[ -f ~/.bashrc ] && source ~/.bashrc
```

```
sudo usermod -s /bin/zsh YOURUSERNAME
```
