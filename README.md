# Conway's Game of Life [Rust 🦀 + WASM 🕸️]

Try it: https://conway-jordi.vercel.app/

## Requirements 

You need to have installed the Rust toolchain `rustup`. On a Unix system:
```sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

You need to have installed `wasm-pack`. On a Unix system:
```sh
curl https://rustwasm.github.io/wasm-pack/installer/init.sh -sSf | sh
```
Using cargo:
```sh
cargo install wasm-pack
```
Using npm:
```sh
npm install -g wasm-pack
```

## Generate web server code

Generate WASM:
```sh
wasm-pack build
```
This will generate a `pkg` directory.

Generate NodeJS app:
```sh
npm init wasm-app web
```
This will generate a `web` directory.

Move the `pkg` directory into `web` directory, remove the `pkg` directory and remove `.gitignore`:
```sh
cp -rf pkg web && rm -r pkg && rm web/pkg/.gitignore
```

## Run the web server

```sh
cd web
npm cache clean -f
rm -rf node_modules package-lock.json
npm i
npm run start
```