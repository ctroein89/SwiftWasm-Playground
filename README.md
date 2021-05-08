# SwiftWasm-Playground
Experimenting with SwiftWasm


## Install
SwiftWasm: https://github.com/swiftwasm/swift
Wasmer: `curl https://get.wasmer.io -sSfL | sh; source /Users/christophertroein/.wasmer/wasmer.sh`
Tokamak: `brew install swiftwasm/tap/carton`

## Build and run Wasm app in command line
To compile hello.swift: `swiftc -target wasm32-unknown-wasi hello.swift -o hello.wasm`
To run: `wasmer hello.wasm`

## Initialixe and run Tokamak app in browser
```
mkdir TokamakApp && cd TokamakApp
carton init --template tokamak
carton dev
```
