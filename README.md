# Conway's Game of Life [Rust 🦀 + WASM 🕸️]

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

## Run the web server

```sh
cd web
npm cache clean -f
rm -rf node_modules package-lock.json
npm i
npm run start
```