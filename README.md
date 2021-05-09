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

## Limitations
* Swift Foundation doesn't have the Dispatch library because WASM doesn't support threading, which is because Safari, Warmer, and Node.js don't support threading. It looks like Safari is working on it, meaning that support might be added soon.
