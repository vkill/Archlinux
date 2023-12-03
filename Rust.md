## Rust

### Install

```
sudo pacman -S rustup

rustup install stable
rustup install nightly

rustup default stable
```

```
wget https://github.com/rust-analyzer/rust-analyzer/releases/download/2023-07-24/rust-analyzer-x86_64-unknown-linux-gnu.gz
gzip -d rust-analyzer-x86_64-unknown-linux-gnu.gz
sudo mv rust-analyzer-x86_64-unknown-linux-gnu /usr/local/bin/rust-analyzer
sudo chmod +x /usr/local/bin/rust-analyzer

# or

sudo pacman -S rust-analyzer
```

```
# Tips
vim ~/.xrc
export PATH="$PATH:$HOME/.cargo/bin"

sudo mv ~/.rustup /media/data
ln -sf /media/data/.rustup ~/.rustup

sudo mv ~/.cargo /media/data
ln -sf /media/data/.cargo ~/.cargo
```

### Cross compiling

```
rustup target add x86_64-unknown-linux-gnu


# ldd
#   linux-vdso.so.1 (0x00007ffcb0790000)
#   libssl.so.3 => /usr/lib/libssl.so.3 (0x00007f4b6eb60000)
#   libcrypto.so.3 => /usr/lib/libcrypto.so.3 (0x00007f4b6e600000)
#   libz.so.1 => /usr/lib/libz.so.1 (0x00007f4b6f1f8000)
#   libgcc_s.so.1 => /usr/lib/libgcc_s.so.1 (0x00007f4b6f1d8000)
#   libm.so.6 => /usr/lib/libm.so.6 (0x00007f4b6ea78000)
#   libc.so.6 => /usr/lib/libc.so.6 (0x00007f4b6e419000)
#   /lib64/ld-linux-x86-64.so.2 => /usr/lib64/ld-linux-x86-64.so.2 (0x00007f4b6f236000)

cargo build --release --target x86_64-unknown-linux-gnu
```

```
sudo pacman -S musl openssl-1.1


rustup target add x86_64-unknown-linux-musl


# ldd
#   linux-vdso.so.1 (0x00007fffd35ab000)
#   libssl.so.1.1 => /usr/lib/libssl.so.1.1 (0x00007ff938149000)
#   libcrypto.so.1.1 => /usr/lib/libcrypto.so.1.1 (0x00007ff937e00000)
#   libc.so.6 => /usr/lib/libc.so.6 (0x00007ff937c19000)
#   /usr/lib64/ld-linux-x86-64.so.2 (0x00007ff9387f5000)
OPENSSL_INCLUDE_DIR=/usr/include/openssl-1.1 OPENSSL_LIB_DIR=/usr/lib/openssl-1.1 cargo build --release --target x86_64-unknown-linux-musl
```

Ref https://wiki.archlinux.org/title/rust#Cross_compiling

```
sudo pacman -S mingw-w64-gcc


rustup target add x86_64-pc-windows-gnu


vim ~/.cargo/config
[target.x86_64-pc-windows-gnu]
linker = "/usr/bin/x86_64-w64-mingw32-gcc"
ar = "/usr/bin/x86_64-w64-mingw32-ar"


cargo build --release --target "x86_64-pc-windows-gnu"
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
cargo install sqlx-cli --no-default-features --features postgres,mysql,native-tls
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

```
# https://github.com/crate-ci/typos
cargo install typos-cli
```

```
# https://github.com/davidcole1340/ext-php-rs
sudo pacman -S php
cargo install cargo-php
```

```
# https://github.com/nextest-rs/nextest
sudo pacman -S cargo-nextest
```

### Tips

```
find . -type d -mindepth 1 -maxdepth 1 | xargs -I{} cargo clean --manifest-path={}/Cargo.toml
```
