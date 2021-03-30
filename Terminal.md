## Terminal

### Terminator

```
sudo pacman -S terminator
```

Preferences -> Profiles -> Command -> Enable "Run command as a login shell"

Preferences -> Keybindings -> Update "switch_to_tab_x"

### Common

```
vim ~/.xrc

export VISUAL="vim"
export EDITOR="vim"

export LANG=en_US.UTF-8
```

### Oh My Zsh

```
sudo pacman -S zsh zsh-completions
```

```
# Require archlinuxcn repo
sudo pacman -S oh-my-zsh-git
```

```
cp /usr/share/oh-my-zsh/zshrc ~/.zshrc

vim ~/.zshrc

ZSH_THEME="gnzh"

[ -f ~/.xrc ] && source ~/.xrc
```

```
sudo usermod -s /bin/zsh YOURUSERNAME
```

### Bash

```
vim ~/.bashrc

[ -f ~/.xrc ] && source ~/.xrc
```
