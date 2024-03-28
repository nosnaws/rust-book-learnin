## Runtimes

Native
```bash
./target/release/fib.wasm
> The 50th fibonacci number is 12586269025
> ./target/release/fib  30.46s user 0.01s system 99% cpu 30.621 total
```

WebAssebly (with Wasmer) 
```bash
time wasmer run target/wasm32-wasi/release/fib.wasm
> The 50th fibonacci number is 12586269025
> wasmer target/wasm32-wasi/release/fib.wasm  34.28s user 0.04s system 99% cpu 34.341 total
```

WebAssembly (with Wasmtime)
```bash
time wastime target/wasm32-wasi/release/fib.wasm
> The 50th fibonacci number is 12586269025
> wasmtime target/wasm32-wasi/release/fib.wasm  32.86s user 0.04s system 99% cpu 33.152 total
```

