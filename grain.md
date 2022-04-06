date = "2022-01-12T00:23:27Z"
title = "Grain in WebAssembly"
description = "Grain is a WebAssembly-first language. It supports both in-browser and WASI modes."
tags = ["grain", "webassembly"]
template = "page_lang"
[extra]
author = "Fermyon Staff"
---
# Grain in WebAssembly

Grain is a functional programming language that is designed specifically to compile to WebAssembly.
We have enjoyed using it because of its intuitive syntax and great tooling.

## Available Implementations

There is one official [implementation of Grain](https://grain-lang.org/)

## Usage

Grain can be used in the browser. It also supports WASI, so it can be used for the Fermyon Platform (Wagi and Spin) or with commandline runners like Wasmtime.

## Pros and Cons

Things we like:

- Easy to learn
- Good toolchain
- Good documentation

We're neutral about:

- Compiled object size.
- Execution speed.

Things we're not big fans of:

- Not a lot of third party libraries yet


## Example

>> All of our examples follow [a documented pattern using common tools](/wasm-languages/about-examples).

No examples yet

## Learn More

Here are some great resources:

- The official [Hello World example](https://grain-lang.org/docs/guide/hello_world)
- An InfoWorld article [on the basics of Grain](https://www.infoq.com/news/2021/05/grain-web-assembly-first/)
- An example [Wagi application in Grain](https://github.com/deislabs/hello-wagi-grain)
- A production-grade [Wagi file server in Grain](https://github.com/deislabs/wagi-fileserver)
- A French-language walk-thru video [of Grain, Wagi, and Wasmer](https://youtu.be/TDNxLGMDuVs)