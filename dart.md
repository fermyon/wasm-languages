date = "2022-01-12T00:23:27Z"
title = "Dart in WebAssembly"
description = "Dart is experimenting with WebAssembly for the browser."
tags = ["dart", "webassembly"]
template = "page_lang"
[extra]
author = "Fermyon Staff"
last_modified = "2022-03-10T21:50:50Z"
---
# Dart in WebAssembly

Dart is largely a browser-oriented language. The Dart developers have experimented with compiling Dart to Wasm for running in the browser.

We are also excited to see Dart extend beyond the browser, but currently this seems to be embedding a Wasm runtime in Dart:

> We’re experimenting with support for Wasm interop in a new package, package:wasm. This prototype is built on the Wasmer runtime, and it supports WASI for OS interaction. Note that our current prototype is incomplete and supports only desktop platforms (Windows, Linux, and macOS).
[Source](https://medium.com/dartlang/experimenting-with-dart-and-wasm-ef7f1c065577)

## Available Implementations

The official Dart SDK now supports `dart2wasm` compilation, but it comes with some stipulations about using a WebAssembly runtime that supports the not-yet-complete Wasm GC extension:

Instructions can be found on the SDK's [Dart2Wasm page](https://github.com/dart-lang/sdk/blob/main/pkg/dart2wasm/dart2wasm.md)

We are not currently aware of any plan to support WASI from Dart. We also haven't found any good tutorials or examples. If you have information on either of these, please let us know!

## Usage

It appears that the only supported use case for Dart is for in-browser. However, we will update this once `dart2wasm` has been released.

## Pros and Cons

We will update this once `dart2wasm` has been released.

## Examples

We will update this once `dart2wasm` has been released.

## Learn More

Here are some great resources:

- The [Dart2Wasm](https://github.com/dart-lang/sdk/tree/main/pkg/dart2wasm) tool is in the official SDK
- This [blog post](https://medium.com/dartlang/experimenting-with-dart-and-wasm-ef7f1c065577) outlines the efforts to explore Dart and Wasm.
- There is a [tracking issue](https://github.com/dart-lang/sdk/issues/32894) for Dart-to-Wasm work