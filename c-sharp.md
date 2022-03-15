date = "2022-01-12T00:23:27Z"
title = "C# in WebAssembly"
description = "C# (C-sharp) is backed by the .NET (dotnet) ecosystem, whose Wasm support is rapidly maturing."
tags = ["c#", "csharp", "dotnet", ".net", "webassembly"]
template = "page_lang"
[extra]
author = "Fermyon Staff"
last_modified = "2022-03-10T21:50:50Z"
---
# C# and .NET in WebAssembly

The .NET (aka dotnet) ecosystem supports a variety of languages, including C# (C sharp) and ASP.NET. Programs that target .NET are compiled to an intermediary bytecode format that runs in the .NET Common Language Runtime (CLR). This makes .NET an example of a [virtual machine language](/blog/scripts-vs.compiled-wasm.md).

## Available Implementations

The .NET ecosystem has long had support for browser-side WebAssembly via the [Blazor toolkit](https://dotnet.microsoft.com/en-us/apps/aspnet/web-apps/blazor).

The team at Microsoft is rapidly building out a number of WebAssembly tools. In 2022, it seems reasonable to expect that Microsoft will have new tooling for WebAssembly. C# compiled using the .NET toolchain will have access to these WebAssembly features.

At the time of this writing, the closest we have seen to a full WASI runtime is Steve Sanderson's example [.NET WASI Runtime](https://github.com/SteveSandersonMS/dotnet-wasi-runtime).

In addition, browser-based support also seems to be available in the [Elements compiler](https://www.elementscompiler.com/elements/)

## Pros and Cons

Things we like:

- Blazor is enjoying a surge of popularity in the browser

For the most part, though, it is too early to speculate on the rest of the .NET tooling.

## Example

We do not yet have a demo.

## Learn More

Here are some great resources:

- [Blazor](https://dotnet.microsoft.com/en-us/apps/aspnet/web-apps/blazor)
- The .NET community call [previewed](https://www.youtube.com/watch?v=8gwSU3oaMV8&list=PLdo4fOcmZ0oX-DBuRG4u58ZTAJgBAeQ-t&t=3670s) `wasm32-wasi` with ASP.NET