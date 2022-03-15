date = "2022-01-12T00:23:27Z"
title = "Python in WebAssembly"
description = "Python can almost be compiled to WebAssembly. The implementations are coming along quickly in a few places."
tags = ["python", "webassembly"]
template = "page_lang"
[extra]
author = "Fermyon Staff"
---
# Python in WebAssembly

Python is one of the most popular programming languages in the world, and its WebAssembly implementation seems to be coming along quickly.
While it is not yet ready for use, we anticipate it will be functional in the first half of 2022.

The most momentum seems to be in the CPython community, which is rapidly approaching both Emscripten-based and WASI-based implementations.

# Uses

CPython is adding Wasm32 support in 3.11.
Once this is available, Python code can be compiled directly to wasm32-emscripten (browser) and wasm32-wasi (standalone).
Once WASI support lands in CPython, Python can be used to write Fermyon Platform apps with Wagi and Spin.
Once Emscripten support lands in CPython, Python code can be executed in the browser.

## Available Implementations

When things land, they will be in the [GitHub CPython repo](https://github.com/python/cpython). The expected milestone is CPython 3.11.

More recently, we have been using [SingleStore's wasi-python project](https://github.com/singlestore-labs/python-wasi). As the name implies, it has full WASI support for filesystem, environment variables, random numbers, and clock access (and possibly others).

## Learn More

Here are some great resources:

- An in-browser [Python shell in Wasm](https://github.com/ethanhs/python-wasm)
- One version of [CPython + Wasm](https://github.com/ethanhs/python-wasm), where they are working on [WASI support](https://github.com/ethanhs/python-wasm/issues/18)
- Recent work on [WASI support in Python](https://bugs.python.org/issue46315)
- CPython has made progress on an [Emscripten-targeted Wasm target](https://bugs.python.org/issue40280). See also [this patch](https://github.com/python/cpython/pull/30495).
- There is currently a patch for [Python 3.11](https://bugs.python.org/issue46315).
- Much is happening on the WebAssembly Discord server. Check the `#python` channel.
