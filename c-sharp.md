date = "2022-01-12T00:23:27Z"
title = "C# (and .NET) in WebAssembly"
description = "C# (C-sharp) is backed by the .NET (dotnet) ecosystem, whose Wasm support is rapidly maturing."
tags = ["c#", "csharp", "dotnet", ".net", "webassembly"]
template = "page_lang"
[extra]
author = "Fermyon Staff"
last_modified = "2023-10-26T00:50:50Z"
---
# C# and .NET in WebAssembly

The .NET (aka dotnet) ecosystem supports a variety of languages, including C# (C sharp) and ASP.NET. Programs that target .NET are compiled to an intermediary bytecode format that runs in the .NET Common Language Runtime (CLR). This makes .NET an example of a [virtual machine language](/blog/scripts-vs.compiled-wasm.md).

## Available Implementations

The .NET ecosystem has long had support for browser-side WebAssembly via the [Blazor toolkit](https://dotnet.microsoft.com/en-us/apps/aspnet/web-apps/blazor). As of .NET 7, it has support for WebAssembly as a compile target.

The team at Microsoft is rapidly building out a number of WebAssembly tools. .NET 7 includes support for compiling to WebAssembly. Read [Ivan Towlson's excellent tutorial](https://www.fermyon.com/blog/dotnet-wasi) on building a WebAssembly app with .NET.

In addition, browser-based support also seems to be available in the [Elements compiler](https://www.elementscompiler.com/elements/)

## Example

You will need to be running .NET 7 and also have the [WASI SDK](https://github.com/SteveSandersonMS/dotnet-wasi-sdk).

>> This example is derived from [Ivan's blog post](https://www.fermyon.com/blog/dotnet-wasi). Other examples of C# and F# can be found [here](https://github.com/fermyon/spin-kitchensink/)

Create a new project with `dotnet new console`. Then add the WASI SDK like this: `dotnet add package Wasi.Sdk --prerelease`

Now we can write a simple C# program. Here is the text of `Program.cs`:

```csharp
using System.Runtime.InteropServices;

Console.WriteLine($"Content-Type: text/html");
Console.WriteLine();
Console.WriteLine($"Hello, World");

```

To compile this, run the .NET 7 command line:

```console
dotnet build
```

This produces a `SpinPage` file in the `bin/Debug/net7.0` directory. 

To run this in Spin, create a `spin.toml` file like this:

```toml
spin_version = "1"
name = "spin-test"
trigger = { type = "http", base = "/" }
version = "1.0.0"

[[component]]
id = "spin-page"
source = "bin/Debug/net7.0/SpinPage.wasm"
[component.trigger]
route = "/"
executor = { type = "wagi" }
```

You can now start a server with `spin up`.

Using `curl`` or a web browser, we can hit `http://localhost:3000` and see the output:

```console
$ curl localhost:3000
Hello, World
```

To build more advanced applications, use the [Spin SDK for .NET](https://github.com/fermyon/spin-dotnet-sdk#fast-startup-using-wizer). This [blog post walks you through a new Spin .NET app](https://www.fermyon.com/blog/webassembly-for-dotnet-developers-spin-sdk-intro)

## Learn More

Here are some great resources:
- The best way to build Spin .NET apps is with the [Spin .NET SDK](https://github.com/fermyon/spin-dotnet-sdk#fast-startup-using-wizer)
- Read up on the SDK [in this detailed .NET Wasm blog post](https://www.fermyon.com/blog/webassembly-for-dotnet-developers-spin-sdk-intro)
- The [Running .NET in WebAssembly](https://www.fermyon.com/blog/dotnet-wasi) blog post on Fermyon.com walks you through the process of creating a new Wasm app with .NET.
- The [WASI SDK for .NET](https://github.com/SteveSandersonMS/dotnet-wasi-sdk) is available on GitHub
- Tobias Fenster wrote a tutorial on [Spin and .NET apps](https://tobiasfenster.io/net-in-webassembly-with-fermyon-spin-or-how-to-duplicate-your-planner-plans-with-adjustments)
- [Blazor](https://dotnet.microsoft.com/en-us/apps/aspnet/web-apps/blazor)
- The .NET community call [previewed](https://www.youtube.com/watch?v=8gwSU3oaMV8&list=PLdo4fOcmZ0oX-DBuRG4u58ZTAJgBAeQ-t&t=3670s) `wasm32-wasi` with ASP.NET
- JetBrains wrote a blog post in 2022 about [.NET's Wasm future](https://blog.jetbrains.com/dotnet/2022/12/15/the-future-of-net-with-wasm/)
- A possibly obsolete example from Steve Sanderson's [.NET WASI Runtime](https://github.com/SteveSandersonMS/dotnet-wasi-runtime).
