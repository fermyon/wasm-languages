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
A few years ago, the Kotlin Native team introduced WebAssembly support for the browser.
However, in 2019 they began a rewrite of the feature.
In late 2020, they demoed the upcoming version, but as far as we know the implementation has not been released to the public (though the work is open source).
On top of this, Kotlin can be supported by some of the [Java-to-Webassembly tools](/wasm-languages/java).

## Uses

In-browser support for Kotlin has been available for a few years.
The new rewrite, though, is set to replace the older implementation.
At the time of this writing, it was unclear whether the new Kotlin implementation would support `wasm32-wasi`.
Therefore, we do not know whether Kotlin can be used to create Fermyon Platform applications.

## Available Implementations

- Kotlin-Native can be compiled to WebAssembly, but this method is going away.
- The new compiler is not yet readily available. See the links below.

## Learn More

Here are some great resources:

- A [great blog post](https://superkotlin.com/kotlin-and-webassembly/) on the older way of building Kotlin Wasm binaries.
- The official [preview video](https://www.youtube.com/watch?v=-pqz9sKXatw) of the next-gen Wasm compiler.
- For the latest feature plan, the [Kotlin Roadmap](https://kotlinlang.org/docs/roadmap.html#roadmap-details) is a good source of information.
    - The key issue is [KT-46773](https://youtrack.jetbrains.com/issue/KT-46773?_gl=1*srzlan*_ga*NzQzMDU1MDYwLjE2NDI1NTgwMDE.*_ga_J6T75801PF*MTY0MjU1ODAwMS4xLjEuMTY0MjU1ODAxNC4w&_ga=2.168897505.1369047405.1642558002-743055060.1642558001)
    - The compiler code is [in GitHub](https://github.com/JetBrains/kotlin/tree/master/compiler/ir/backend.wasm/src/org/jetbrains/kotlin/backend/wasm)