## VS Code

### Install

```
# https://aur.archlinux.org/packages/visual-studio-code-bin/

yaourt -S visual-studio-code-bin
```

### Configurate

File > Preferences > Settings editor.formatOnSave to true

### Extensions

#### Remote - SSH

https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh

* [issue] Connection error: Version mismatch, client refused.

https://github.com/microsoft/vscode-remote-release/issues/1056

#### rust-analyzer

Configurate "Rust-analyzer: Server Path" to /usr/bin/rust-analyzer
