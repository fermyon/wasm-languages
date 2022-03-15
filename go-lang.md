date = "2022-01-12T00:23:27Z"
title = "Go in WebAssembly"
description = "Go can be compiled to WebAssembly. TinyGo, an alternative implementation of Go, is the most promising"
tags = ["go", "golang", "webassembly"]
template = "page_lang"
[extra]
author = "Fermyon Staff"
---
# Go in WebAssembly

Go was early to the WebAssembly game, with the Go compiler producing `wasm32` output alongside its regularly supported build targets.
But the core Go tools have fallen behind.
Instead, the alterative Go implementation called [TinyGo](https://tinygo.org/) seems to have taken the lead.

## Uses

TinyGo can compile to `wasm32-wasi`, and TinyGo apps can be run on the Fermyon Platform.

## Available Implementations

- Go supports browser-based WebAssembly
- TinyGo supports `wasm32-wasi` as a build target
- The [Elements compiler](https://www.elementscompiler.com/elements/) may also support compiling browser-oriented Wasm

## Learn More

Here are some great resources:

- TinyGo has [a step-by-step walkthrough](https://tinygo.org/docs/guides/webassembly/) for building and running Go WebAssembly modules
- Get started quickly with [Yo-Wasm](https://github.com/deislabs/yo-wasm), which has support for Go as well as several other languages.
- A [short article](https://golangbot.com/webassembly-using-go/) on compiling to Go's "JS/Wasm" target