## Rust

### Install

```
sudo pacman -S rustup

rustup install stable

rustup default stable
```

```
wget https://github.com/rust-analyzer/rust-analyzer/releases/download/2021-07-19/rust-analyzer-x86_64-unknown-linux-gnu.gz
gzip -d rust-analyzer-x86_64-unknown-linux-gnu.gz
sudo mv rust-analyzer-x86_64-unknown-linux-gnu /usr/local/bin/rust-analyzer
sudo chmod +x /usr/local/bin/rust-analyzer

# or

sudo pacman -S rust-analyzer
```

### Binaries

```
# https://github.com/dtolnay/cargo-expand
cargo install cargo-expand
```

```
# https://github.com/frewsxcv/cargo-all-features
cargo install cargo-all-features
```

```
# https://github.com/est31/cargo-udeps
cargo install cargo-udeps --locked
```

```
# https://github.com/launchbadge/sqlx
cargo install sqlx-cli --no-default-features --features postgres
```

```
# https://github.com/matthiaskrgr/cargo-cache
cargo install cargo-cache
```

```
# https://github.com/stepancheg/rust-protobuf/tree/master/protobuf-codegen
cargo install protobuf-codegen
```

```
# https://github.com/qarmin/czkawka
cargo install czkawka_gui
```

```
# https://github.com/kellpossible/cargo-i18n
# https://github.com/woboq/tr
cargo install cargo-i18n
cargo install xtr
```

```
# https://github.com/killercup/cargo-edit
cargo install cargo-edit
```
