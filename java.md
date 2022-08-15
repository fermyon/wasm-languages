date = "2022-01-12T00:23:27Z"
title = "Java in WebAssembly"
description = "Java can be compiled to WebAssembly by a number of projects. Most are currently focused on the browser."
tags = ["java", "webassembly"]
template = "page_lang"
[extra]
author = "Fermyon Staff"
---
# Java in WebAssembly

Many exciting WebAssembly things are happening in the Java ecosystem.
There are a few projects that are rapidly maturing, and that can generate browser-oriented JS.

The various projects handle memory management differently.
Their feature sets also differ.

## Uses

All of the existing Java implementations are browser oriented, and are designed to let developers write Java and link to it from JavaScript.

## Available Implementations


- The [Bytecoder project](https://mirkosertic.github.io/Bytecoder/) cross-compiles Java to WebAssembly that can be executed in the browser
- The [TeaVM project](https://teavm.org/) has experimental support for browser-based WebAssembly
- A dedicate WebAssembly compiler called [JWebAssembly](https://github.com/i-net-software/JWebAssembly) can translate any JVM bytecode to WebAssembly, including Groovy, Clojure, and Kotlin. It, too, is browser-centric.
- [CheerpJ](https://leaningtech.com/cheerpj/) is much more ambitious, handling the UI as well

## Learn More

Here are some great resources:

- An [in-depth blog](http://blog.dmitryalexandrov.net/webassembly-for-java-developers/) showing practical ways to run Java as Wasm
- Does Wasm remind you of Java Applets? Then read [this blog post](https://steveklabnik.com/writing/is-webassembly-the-return-of-java-applets-flash)
- [GraalVM](https://www.graalvm.org/reference-manual/wasm/) has gained a lot of momentum as a WebAssembly runtime, though it does not appear to support compiling from languages to WebAssembly.