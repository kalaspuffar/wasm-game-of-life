# wasm-game-of-life

Simple example from a guide.

To setup your tooling you can run the commands below. Changing the path to your cargo bin directory. For instance in windows you might have another %USERNAME% folder when running in msys2.
```
curl https://sh.rustup.rs -sSf | sh
export PATH=$PATH:/c/Users/%USERNAME%/.cargo/bin/
curl https://rustwasm.github.io/wasm-pack/installer/init.sh -sSf | sh
npm install npm@latest -g
```

To generate your own project starting from scratch you may use the below command.
```
cargo install cargo-generate
cargo generate --git https://github.com/rustwasm/wasm-pack-template
```

To setup a web application to use with wasm project. This will create a webpack project in www.
```
npm init wasm-app www
```

To update all the dependencies in your web directory you run the install command in your www directory.
```
npm install
```


Building the wasm rust library you run the command below in your project directory.
```
wasm-pack build
```

In order to link your web directory with your rust package.
```
cd pkg
npm link
cd ../www
npm link wasm-game-of-life
```