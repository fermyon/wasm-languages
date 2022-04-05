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


## Available Implementations

When things land, they will be in the [GitHub CPython repo](https://github.com/python/cpython). The expected milestone is CPython 3.11.

More recently, we have been using [SingleStore's wasi-python project](https://github.com/singlestore-labs/python-wasi). As the name implies, it has full WASI support for filesystem, environment variables, random numbers, and clock access (and possibly others).

## Usage

Using Python, a scripting language, is a little different than using compiled languages like [Rust](/wasm-languages/rust) or [AssemblyScript](/wasm-languages/assemblyscript). Not only will the runtime need the Python interpreter compiled to Wasm, but it will also need a number of Python libraries available on the WASI filesystem. We [pre-built a version that you can use](https://github.com/fermyon/wagi-python).

Python scripts that are used this way do not need to be compiled to WebAssembly. They simply need to be loaded into the `python3.wasm` at startup time.

## Example

This section provides a basic example of running a Python 3 script. It is derived from a [Fermyon.com Python tutorial](https://www.fermyon.com/blog/python-wagi).

>> All of our examples follow [a documented pattern using common tools](/wasm-languages/about-examples).

Because we need both the Python 3 interpreter (compiled to Wasm) and the core Python 3 libraries, the first step in this example is to clone our pre-built demo repo: [https://github.com/fermyon/wagi-python](https://github.com/fermyon/wagi-python).

>> If you would prefer, you can build from source from either the [SingleStore Python repository](https://github.com/singlestore-labs/python-wasi) or from the [CPython repository](https://github.com/python/cpython).

A simple Python script for Wagi looks like this:

```python
import sys

print('Content-Type: text/plain; charset=UTF-8')
print()
print('Hello, World')
```

We'll put the script above in `code/hello.py`.

When creating a `modules.toml` for Wagi, you will need to use the `argv` directive to tell Wagi how to invoke `python3.wasm`:

```toml
[[module]]
route = "/"
module = "opt/wasi-python/bin/python3.wasm"
volumes = { "/code" = "code", "/opt" = "opt" }
argv = "python /code/hello.py"
```

Note that the `argv` line looks like the command you would normally invoke. However, it is not executed in a shell. Instead, this is provided so that the Python interpreter itself can see how it should act.

To run the example, start `wagi`:

```console
$ wagi -c modules.toml
No log_dir specified, using temporary directory /var/folders/rk/mkbs8vx12zs0gkm680h_gth00000gn/T/.tmpTxamNm for logs
Ready: serving on http://127.0.0.1:3000
```

(Note that the above may take several seconds.)

At this point you can use a web browser or curl to check the results:

```console
$ curl localhost:3000                                       
Hello, World
```

## Learn More

Here are some great resources:

- Fermyon.com published a slightly more [in-depth Python and Wasm tutorial](https://www.fermyon.com/blog/python-wagi)
- An in-browser [Python shell in Wasm](https://github.com/ethanhs/python-wasm)
- One version of [CPython + Wasm](https://github.com/ethanhs/python-wasm), where they are working on [WASI support](https://github.com/ethanhs/python-wasm/issues/18)
- Recent work on [WASI support in Python](https://bugs.python.org/issue46315)
- CPython has made progress on an [Emscripten-targeted Wasm target](https://bugs.python.org/issue40280). See also [this patch](https://github.com/python/cpython/pull/30495).
- There is currently a patch for [Python 3.11](https://bugs.python.org/issue46315).
- Much is happening on the WebAssembly Discord server. Check the `#python` channel.
