## Rust

### Install

```
sudo pacman -S rustup

rustup install stable

rustup default stable
```

```
sudo pacman -S rust-analyzer

# or

wget https://github.com/rust-analyzer/rust-analyzer/releases/download/2020-12-21/rust-analyzer-linux
sudo mv rust-analyzer-linux /usr/local/bin/rust-analyzer
sudo chmod +x /usr/local/bin/rust-analyzer
```

### Binaries

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
