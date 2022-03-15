date = "2022-01-12T00:23:27Z"
title = "Zig in WebAssembly"
description = "Zig can be compiled to WebAssembly."
tags = ["zig", "webassembly"]
template = "page_lang"
[extra]
author = "Fermyon Staff"
---
# Zig in WebAssembly

Zig, a systems language, has official support for WebAssembly.
Zig's implementation uses LLVM to supply the compile target.

## Uses

LLVM has a `wasm32-wasi` target, so Zig should be usable to build Fermyon Platform applications.
It can also be used in the browser.

## Available Implementations

Zig officially supports WebAssembly via LLVM8.

## Learn More

Here are some great resources:

- The official [release notes](https://ziglang.org/download/0.4.0/release-notes.html#WebAssembly-Support) on WebAssembly support in Zig
- An example repo that shows how to [access the browser DOM](https://github.com/shritesh/zig-wasm-dom) in Zig
- A [short video](https://youtu.be/gJLIiF15wjQ) on Zig