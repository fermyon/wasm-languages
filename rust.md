date = "2022-01-12T00:23:27Z"
title = "Rust in WebAssembly"
description = "Rust supports a broad array of WebAssembly options."
tags = ["rust", "webassembly"]
template = "page_lang"
[extra]
author = "Fermyon Staff"
---
# Rust in WebAssembly

Rust is probably the best supporting language of the WebAssembly ecosystem.
Not only does Rust support several WebAssembly compile targets,
but the `wasmtime` reference runtime is written in Rust.
Rust can be used to create Fermyon Platform apps.

## Uses

- Compile Rust to browser-based Wasm
- Build a GUI that can run in the browser with egui
- Compile to `wasm32-wasi`
- Execute WebAssembly code with a Rust-native runtime

## Available Implementations

WebAssembly is supported in the official Rust distribution.

## Learn More

Here are some great resources:

- Rust has a [dedicated mini-site covering WebAssembly](https://www.rust-lang.org/what/wasm)
- The Rust Linz group did a [presentation on Rust and Wagi](https://www.youtube.com/watch?v=9NDwHBjLlhQ) and posted a GitHub [repo full of Wagi examples](https://github.com/rstropek/rust-samples)
- [Wasmtime](https://wasmtime.dev/) is the reference implementation of Wasm32-WASI.
- [egui](https://www.egui.rs/) provides a GUI toolkit that can be compiled into Wasm and run in the browser