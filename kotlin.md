date = "2022-01-12T00:23:27Z"
title = "Kotlin in WebAssembly"
description = "Kotlin has experimental support for WebAssembly."
tags = ["kotlin", "jvm", "java", "webassembly"]
template = "page_lang"
[extra]
author = "Fermyon Staff"
---
# Kotlin in WebAssembly

Kotlin, like .NET, has an interesting history with WebAssembly.

### Kotlin Native (or Kotlin/Wasm)

A few years ago, the Kotlin Native team introduced WebAssembly support for the browser.
However, in 2019 they began a rewrite of the feature.
In late 2020, they demoed the upcoming version, called "Kotlin/Wasm".
In early 2023, the new version reached Beta, but requires the Wasm runtime support the experimental Wasm-GC proposal.

### Kotlin on JRE

Kotlin compiled to Java bytecode can be executed by the [Java-to-Webassembly tools](/wasm-languages/java).

## Uses

In-browser support for Kotlin has been available for a few years.
The new rewrite, though, is set to replace the older implementation.
At the time of this writing, KoWasm (see below) has WASI support. But because it still requires the Wasm-GC extension, Spin will not support it until [Wasmtime supports Wasm-GC](https://github.com/bytecodealliance/wasmtime/issues/5032).
Therefore, we do not know whether Kotlin can be used to create Fermyon Cloud applications.

## Available Implementations

- Kotlin-Native can be compiled to WebAssembly, but this method is going away.
- The new compiler is [in beta](https://kotlinlang.org/docs/whatsnew-eap.html#new-kotlin-wasm-target), but requires a version of the Wasm runtime that supports (experimental) Wasm Garbage Collection (Wasm-GC).
- Sebastian Deleuze is working on WASI Kotlin support as [KoWasm](https://github.com/sdeleuze/kowasm).

## Learn More

Here are some great resources:

- Sebastian Deleuze's [excellent article](https://seb.deleuze.fr/the-huge-potential-of-kotlin-wasm/) on the potential for Wasm GC and Kotlin (covering Kotlin 1.8.20 Beta)
- A Feb. 2023 Devclass blog post covering [the new Kotlin Wasm compiler](https://devclass.com/2023/02/14/kotlin-debuts-experimental-kotlin-wasm-target-in-new-beta-a-new-approach-to-frontend-development/)
- JetBrains' Kotlin and [WebAssembly announcement in Nov. 2021](https://blog.jetbrains.com/kotlin/2021/11/k2-compiler-kotlin-wasm-and-tooling-announcements-at-the-2021-kotlin-event/)
- A [great blog post](https://superkotlin.com/kotlin-and-webassembly/) on the older way of building Kotlin Wasm binaries.
- The official [preview video](https://www.youtube.com/watch?v=-pqz9sKXatw) of the next-gen Wasm compiler.
- For the latest feature plan, the [Kotlin Roadmap](https://kotlinlang.org/docs/roadmap.html#roadmap-details) is a good source of information.
    - The key issue is [KT-46773](https://youtrack.jetbrains.com/issue/KT-46773?_gl=1*srzlan*_ga*NzQzMDU1MDYwLjE2NDI1NTgwMDE.*_ga_J6T75801PF*MTY0MjU1ODAwMS4xLjEuMTY0MjU1ODAxNC4w&_ga=2.168897505.1369047405.1642558002-743055060.1642558001)
    - The compiler code is [in GitHub](https://github.com/JetBrains/kotlin/tree/master/compiler/ir/backend.wasm/src/org/jetbrains/kotlin/backend/wasm)
- Wasmtime [tracking issue](https://github.com/bytecodealliance/wasmtime/issues/5032) for Wasm GC
