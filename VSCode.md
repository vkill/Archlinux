## VS Code

### Install

```
# https://aur.archlinux.org/packages/visual-studio-code-bin/

yaourt -S visual-studio-code-bin
```

### Configurate

File > Preferences > Settings editor.formatOnSave to true

```
{
  "editor.formatOnSave": true
}
```

### Extensions

#### CodeLLDB

#### Remote - SSH

https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh

* [issue] Connection error: Version mismatch, client refused.

https://github.com/microsoft/vscode-remote-release/issues/1056

#### rust-analyzer

Configurate "Rust-analyzer: Server Path" to `/usr/bin/rust-analyzer` or `/usr/local/bin/rust-analyzer`

```
{
  "rust-analyzer.server.path": "/usr/local/bin/rust-analyzer",
  "rust-analyzer.procMacro.enable": true,
  "rust-analyzer.cargo.loadOutDirsFromCheck": true,
  "rust-analyzer.experimental.procAttrMacros": false
}
```

#### TabNine

```
{
  "tabnine.experimentalAutoImports": true
}
```

#### Markdown All in One

### Tips

[Install extension manually](https://stackoverflow.com/questions/42017617/how-to-install-vs-code-extension-manually)

[Troubleshooting keychain issues](https://code.visualstudio.com/docs/editor/settings-sync#_troubleshooting-keychain-issues)

