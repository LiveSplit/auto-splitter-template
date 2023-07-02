# Auto Splitter Template

This repository hosts a template for creating an auto splitter in Rust.

First you need to install the Rust compiler: [Install
Rust](https://www.rust-lang.org/tools/install)

Afterwards install the WebAssembly target. There are two targets that may be of
interest. By default we recommend the `wasm32-unknown-unknown` target.

```sh
rustup target add wasm32-unknown-unknown
```

There's also support for the WebAssembly System Interface (WASI), but WASI
itself is still in preview, so your auto splitter may need to be recompiled in
the future to keep working. WASI has the benefit that it gives you access to the
file system, randomness, clocks, and more. If your auto splitter only needs
access to processes, their memory and the timer, the WASI target is not needed.

```sh
rustup target add wasm32-wasi
```

After that you need to install the [`cargo
generate`](https://cargo-generate.github.io/cargo-generate/installation.html)
subcommand.

You are now ready to create your auto splitter from the template:

```sh
cargo generate LiveSplit/auto-splitter-template
```

Further instructions are available in the auto splitter's README.
