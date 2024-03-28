# WebAssebly / Wasi (?) Hello World
While reading through the Rust book I wanted to explore using WebAssembly as a compilation target. My exploration so far is focusing on the [WebAssembly System Interface](https://github.com/WebAssembly/WASI) (WASI).

## Running the example
I'm going to assume you have the Rust toolchain installed on your computer.

Install the compilation target:
```bash
rustup target add wasm32-wasi
```

Install the runtime:
```bash
brew install wasmer
```

Another notable runtime is [`wasmtime`](https://github.com/BytecodeAlliance/wasmtime)

Build the example:
```bash
cargo build --release --target wasm32-wasi
```

Run the executable:
```bash
wasmer run target/wasm32-wasi/release/hello_cargo.wasm

> Hello, world!
```


