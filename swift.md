date = "2022-01-12T00:23:27Z"
title = "Swift in WebAssembly"
description = "Swift can be compiled to WebAssembly and run in-browser, at the CLI, and with WASI enabled."
tags = ["swift", "webassembly"]
template = "page_lang"
[extra]
author = "Fermyon Staff"
---
# Swift in WebAssembly

Swift is no longer just for iOS apps.
Thanks to a recent community-led project, it is possible to [compile Swift into WebAssembly](https://swiftwasm.org/)
destined either for the browser or for a WASI environment.

## Uses

Because Swift supports WASI, it is a great language choice for writing Fermyon Platform apps in Spin or Wagi.

It can also be used for browser apps.

## Available Implementations

The [SwiftWasm](https://swiftwasm.org/) project handles pretty much everything.

It appears that the [RemObjects Elements](https://www.elementscompiler.com/elements/) compiler (commercial license required) may support compiling Swift to WebAssembly, too.

## Learn More

Here are some great resources:

- The [SwiftWasm Book](https://book.swiftwasm.org/) has examples and info about compiling to Wasm32+WASI
- [yo-wasm](https://github.com/deislabs/yo-wasm) supports Swift
- Here is a [very quick quickstart](https://betterprogramming.pub/get-started-with-swift-for-webassembly-on-macos-with-swiftwasm-5d588a086120) if the docs look too verbose