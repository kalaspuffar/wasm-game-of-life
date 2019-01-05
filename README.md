# wasm-game-of-life

Simple example from a guide.

```
curl https://sh.rustup.rs -sSf | sh
export PATH=$PATH:/c/Users/%USERNAME%/.cargo/bin/
curl https://rustwasm.github.io/wasm-pack/installer/init.sh -sSf | sh
cargo install cargo-generate
npm install npm@latest -g
```

```
cargo generate --git https://github.com/rustwasm/wasm-pack-template
```

```
wasm-pack build
```

```
npm init wasm-app www
```

```
cd www
npm install
cd ../pkg
npm link
cd ../www
npm link wasm-game-of-life
```