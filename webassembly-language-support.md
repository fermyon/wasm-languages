date = "2022-01-11T20:08:47Z"
title = "WebAssembly Language Support Matrix"
description = "Tracking the programming languages that compile to WebAssembly (Wasm). This page stays up to date with information about which languages can compile to Wasm, and what their language characteristics are."
template = "page"

# Most important first
tags = ["webassembly", "programming languages", "javascript", "python", "rust", "dotnet", "ruby"]

[extra]
author = "Fermyon Staff"
# author_page = "/author/"
---

This guide tracks support for compiling a language to WebAssembly. It is organized into three sections: Support for the top 20 languages, WebAssembly-specific languages, and other notable languages. We track whether the language can be compiled to run in the browser, in other non-browser environments, and in a [WASI](https://wasi.dev) environment. In the detail page for each language, we do our best to not only state the current level of support, but also point to an array of useful resources.

## WebAssembly Support in Top 20 Languages

This reports on the top 20 languages from [RedMonk's ranking](https://redmonk.com/sogrady/2022/03/28/language-rankings-1-22/).
Some languages, like CSS, PowerShell, and "Shell", don't really have a meaningful expression in Wasm. However, we have left them here for completeness.

| Language                  | Browser | Other | WASI | Notes |
| ------------------------- | ------- | --- | ---- | ----- |
| [JavaScript][JavaScript]  | ⏳  | ⏳ | ⏳ | |
| [Python][Python]          | ⏳ | ✅  | ✅  |  |
| [Java][Java]              |  ✅  | ✅  | ❌ ||
| [PHP][PHP]                | ✅ | ✅ | ✅ ||
| CSS                       | N/A | N/A | N/A |  |
| [C# and .NET][CSHARP]     | ✅ | ✅ | ✅ | Covers .NET as well |
| [C++][CPLUSPLUS]          | ✅  | ✅ | ✅ | |
| [TypeScript][TypeScript]  |  ❌  | ⏳ | ❌ | Consider [AssemblyScript](/wasm-languages/assemblyscript)|
| [Ruby][Ruby]              | ✅ | ✅ | ✅ |  |
| [C][C]                    | ✅  | ✅ | ✅ | |
| [Swift][Swift]            | ✅  | ✅ | ✅ | |
| [R][R]                    | ✅  | ❌ | ❌ | |
| [Objective-C][ObjectiveC] | ❌  | ? | ❌ | |
| [Shell][Shell]            | ✅ | ❌ | ❌ |  |
| [Scala (native)][Scala]   | ❌  | ⏳ | ❌ | See [Java](/wasm-languages/java) |
| [Go][Go]                  | ✅  | ✅ | ✅ | Via Go and TinyGo|
| [PowerShell][PowerShell]  | ❌  | ❌ | ❌ | This is unlikely to change. |
| [Kotlin][Kotlin]          | ✅ | ⏳ | ⏳ |  |
| [Rust][Rust]              | ✅  | ✅ | ✅ | |
| [Dart][Dart]              | ⏳ | ❌ | ❌ ||

## WebAssembly Specific Languages

| Language                  | Browser | CLI | WASI | Notes |
| ------------------------- | ------- | --- | ---- | ----- |
| [AssemblyScript][AssemblyScript] | ✅  | ✅ | ✅ | |
| [Grain][Grain]                   | ✅  | ✅ | ✅ | |
| [Motoko][Motoko]                 | ✅  | ✅ | ✅ | |

## Other Notable Languages

These languages enjoy broad use (though perhaps not in the top 20) and have at least some degree of WebAssembly Support

| Language                  | Browser | CLI | WASI | Notes |
| ------------------------- | ------- | --- | ---- | ----- |
| [COBOL][Cobol]            |⏳ | ✅ | ⏳ |  |
| [Erlang (BEAM)][Erlang]   | ⏳ | ⏳ | ⏳ |  |
| [Haskell][Haskell]        | ✅  | ✅ | ✅ | |
| [Lisp][Lisp]              | ⏳ | ⏳ | ⏳ |  |
| [Lua][Lua]                | ✅ | ❌ | ❌ |  |
| [Perl][Perl]              | ✅ | ❌ | ❌ |  |
| [Zig][Zig]                | ✅  | ✅ | ✅ | |

## How To Read These Charts

For each environment, we use the following icons to indicate a level of support:

- ✅  Usable
- ⏳ In progress
- ❌ Not implemented
- N/A Not applicable

The Fermyon Platform requires [WASI](https://wasi.dev) support. Any language that has a ✅ for WASI should be supported on the Fermyon Platform.

>> If you are interested in contributing to this guide, head on over to [the GitHub repo](https://github.com/fermyon/wasm-languages).

We are often asked which languages are best supported for production-grade WebAssembly. We suggest [C][C]/[C++][CPLUSPLUS], [Rust][Rust], and [AssemblyScript][AssemblyScript].

## Updates and Additions

The source for the WebAssembly Language Guide is located in a [public GitHub project](https://github.com/fermyon/wasm-languages). If you find errors, want to make additions, or have further corrections for us, the [issue queue](https://github.com/fermyon/wasm-languages/issues) is a great place to discuss.

If you're more interested in chatting about things, check out our [Discord server](https://discord.gg/AAFNfS7NGf) or hit us up a [@FermyonTech on Twitter](https://twitter.com/fermyontech)

## Relevant Standards

Throughout our pages, we talk about technologies like WASI, Wagi, and Spin. Many of these are backed by formal documents. See the [Standards] page for links to the relevant texts along with helpful resources.

[JavaScript]: /wasm-languages/javascript
[Python]: /wasm-languages/python
[Java]: /wasm-languages/java
[PHP]: /wasm-languages/php
[CPLUSPLUS]: /wasm-languages/cpp
[CSHARP]: /wasm-languages/c-sharp
[TypeScript]: /wasm-languages/typescript
[Ruby]: /wasm-languages/ruby
[C]: /wasm-languages/c-lang
[Swift]: /wasm-languages/swift
[R]: /wasm-languages/r-lang
[ObjectiveC]: /wasm-languages/objective-c
[Shell]: /wasm-languages/shell
[Scala]: /wasm-languages/scala
[Go]: /wasm-languages/go-lang
[PowerShell]: /wasm-languages/powershell
[Kotlin]: /wasm-languages/kotlin
[Rust]: /wasm-languages/rust
[Dart]: /wasm-languages/dart

[AssemblyScript]: /wasm-languages/assemblyscript
[Grain]: /wasm-languages/grain
[Motoko]: /wasm-languages/motoko

[Cobol]: /wasm-languages/cobol
[Erlang]: /wasm-languages/erlang-beam
[Haskell]: /wasm-languages/haskell
[Lisp]: /wasm-languages/lisp
[Lua]: /wasm-languages/lua
[perl]: /wasm-languages/perl
[Zig]: /wasm-languages/zig

[Standards]: /wasm-languages/standards
