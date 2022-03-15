date = "2022-01-12T00:23:27Z"
title = "Erlang (BEAM languages) in WebAssembly"
description = "BEAM-based languages are getting support for a WebAssembly runtime and compiler."
tags = ["language", "webassembly", "beam", "erlang", "elixir"]
template = "page_lang"
[extra]
author = "Fermyon Staff"
---
# Erlang in WebAssembly

Erlang is the most prominent of the [BEAM languages](https://github.com/llaisdy/beam_languages). Elixir is another popular BEAM language.

The Lumen project is endeavoring to create a BEAM runtime and a compiler so that the BEAM applications can be run in a WebAssembly host environment. 

## Uses

The original goal of the Lumen project was to run Elixir in the web browser.

> The primary motivator for Lumen's development was the ability to compile Elixir applications that could target WebAssembly, enabling use of Elixir as a language for frontend development.

We are not clear on whether or not this is possible as of yet.

## Available Implementations

Lumen is the primary contender, and is interesting because if it is successful we will see support not just for Erlang, but for Elixir and other BEAM languages.

## Learn More

Here are some great resources:

- Lumen is a [compiler and runtime](https://github.com/lumen/lumen)
- Erlang fans may also appreciate [Lunatic](https://lunatic.solutions/), a WebAssembly platform built using an Erlang-style OTP. It will soon support WASI.
