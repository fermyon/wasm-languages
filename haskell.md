date = "2022-01-12T00:23:27Z"
title = "Haskell in WebAssembly"
description = "Haskell can be compiled to WebAssembly with Asterius."
tags = ["haskell", "webassembly", "asterius"]
template = "page_lang"
[extra]
author = "Fermyon Staff"
---
# Haskell in WebAssembly

The Asterius project compiles Haskell to WebAssembly.

## Uses

Asterius targets Node.js and the browser.
It also appears to support `wasm32-wasi`, though we have not tested it.

## Available Implementations

- Asterius is the only known implementation of an Haskell-to-WebAssembly compiler.

## Learn More

Here are some great resources:

- The Asterius [main project page](https://github.com/tweag/asterius) discusses how Asterius works
- A blog post on using Asterius in [CloudFlare](https://www.tweag.io/blog/2020-10-09-asterius-cloudflare-worker/)
- The [roadmap](https://asterius.netlify.app/roadmap.html) provides a list of fixes, but it looks to not be updated recently