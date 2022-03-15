date = "2022-01-12T00:23:27Z"
title = "Ruby in WebAssembly"
description = "Ruby can be compiled to WebAssembly. While there are a number of projects to do so, none are complete."
tags = ["ruby", "webassembly"]
template = "page_lang"
[extra]
author = "Fermyon Staff"
---
# Ruby in WebAssembly

Ruby now has multiple WebAssembly-based projects.

A CRuby Wasm32-WASI implementation was merged into core in January 2022.
That would give Ruby an official Wasm32-WASI build of the Ruby runtime.
This does not compile Ruby scripts to Wasm, but runs the Ruby runtime itself in a Wasm interpreter.
(This is similar to how the existing [JavaScript](/wasm-languages/javascript) and [Python](/wasm-languages/python) implementations work.)

For the browser, the most promising Ruby technology for WebAssembly seems to be `Artichoke`, 
which would provide a Ruby runtime as a WebAssembly module.
In this case, one would be able to execute Ruby in the browser or on the commandline.

## Uses

We have tested the official Ruby patches and confirmed that they run in `wasm32-wasi`.
This means Ruby apps can be written for the Fermyon Platform.

There are also other Ruby implementations that we have not tested.

## Available Implementations

- CRuby (official Ruby) can be built to `wasm32-wasi`
- `rlang` (a subset of Ruby) can run Wasm32 code in a `wasm32-wasi` runtime like `wasmtime`.
 - `artichoke` is a new implementation of Ruby that will compile to Wasm.

## Learn More

Here are some great resources:

- The [pull request to merge wasm32-wasi in Ruby](https://bugs.ruby-lang.org/issues/18462)
- Instructions for [building Ruby with wasm32-wasi support](https://github.com/ruby/ruby/pull/5407)
- [Rlang](https://github.com/ljulliar/rlang) compiles a subset of the Ruby language to Wasm
- [Artichoke](https://www.artichokeruby.org/) is a Rust implementation of Ruby that can compile to WebAssembly (`wasm32-unknown`)
- The [mruby](https://github.com/mruby/mruby) runtime has been compiled to WebAssembly, which means you can interpret a Ruby script inside of a Wasm module
- [Prism](https://github.com/prism-rb/prism) uses `mruby` to run Ruby inside of WebAssembly
- While it doesn't seem to be active anymore, [run.rb](https://runrb.io/) is a project for running Ruby in the browser as Wasm.
- [wruby](https://github.com/pannous/wruby) also no longer looks active, but it was an `mruby`-based in-browser Ruby interpreter.