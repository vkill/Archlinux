## VS Code

### Install

```
# https://aur.archlinux.org/packages/visual-studio-code-bin/

sudo pacman -S visual-studio-code-bin
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
  "rust-analyzer.procMacro.attributes.enable": true
}
```

#### TabNine

```
{
  "tabnine.experimentalAutoImports": true
}
```

#### Markdown All in One

#### Even Better TOML

https://marketplace.visualstudio.com/items?itemName=tamasfe.even-better-toml

#### Playwright Test

https://marketplace.visualstudio.com/items?itemName=ms-playwright.playwright

#### vscode-proto3

```shell
yay -S clang-format-all-git
```

```
{
    "clang-format.style": "{ IndentWidth: 4, BasedOnStyle: google, AlignConsecutiveAssignments: true }",
    "[proto3]": {
        "editor.defaultFormatter": "xaver.clang-format"
    },
}
```

### Tips

[Install extension manually](https://stackoverflow.com/questions/42017617/how-to-install-vs-code-extension-manually)

[Troubleshooting keychain issues](https://code.visualstudio.com/docs/editor/settings-sync#_troubleshooting-keychain-issues)

