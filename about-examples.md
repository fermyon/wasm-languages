date = "2022-03-08T23:31:10Z"
title = "About WebAssembly Examples"
description = "The WebAssembly examples all follow some common patterns. This page explains them"
template = "page"

# Most important first. Try to get at least 3 for a blog post.
tags = ["webassembly", "examples"]

[extra]
author = "Fermyon Staff"  # Use "Fermyon Staff" for general content
# author_page = "/author/"
type = "page"
---

The [Fermyon WebAssembly Language Guide](/wasm-languages/webassembly-language-support) tracks languages that can be executed within a WebAssembly runtime. We do our best to keep things consistent across pages. This page explains how we create our examples.

## The Typical Example

Providing detailed language-specific examples is beyond the scope of the language guide. Instead, we try to provide the following pieces of relevant information:

- How to get the tools necessary to work with the language
- How to create a simple "Hello World" style program
- How to compile that program
- How to execute that program

Our canonical example is to build a simple web page that prints `Hello, World` in plain text. In order to serve it as a web page, we try to write the script using one of two tools:

- Spin, which supports fewer languages, but provides a great experience
- [Wagi](https://github.com/deislabs/wagi), which supports all languages that have [WASI support](https://wasi.dev/)

We also try to make sure that our example runs with [wasmtime](https://wasmtime.dev/), which is committed to implementing the WASI specification.

To that end, the simplest example, written in Swift, looks like this:

```swift
print("content-type: text/plain\n\n");
print("Hello, World\n");
```

When run on `wasmtime`, it should produce output like this:

```console
$ wasmtime hello.wasm
content-type: text/plain

Hello, World
```

When executed on Wagi and accessed via Curl, it should look like this:

```console
$ curl localhost:3000                                       
Hello, World
```

## Wagi Configuration

When we use WebAssembly on the cloud, we usually store our packages in a [Bindle server](https://github.com/deislabs/bindle). But for our examples here, we use Wagi's simple `modules.toml` format. A simple example looks like this:

```toml
[[module]]
module = "hello.wasm"
route = "/"
```

Then we start `wagi` with `wagi -c modules.toml`.