---
title: Projects
---

# SA-MP

I coded a bunch of open-source server-side plugins and tools for [San Andreas Multiplayer (SA-MP)](https://www.sa-mp.com) some time ago. Among them are:

## [crashdetect](https://github.com/Zeex/samp-plugin-crashdetect)

Detects when the server crashes due to some unhandled error and spits out a stack trace along with other information such as register values at the moment of the crash, loaded DLLs/shared libraries, etc. It also shows runtime errors that occur in the virtual machine (AMX) which is  probably the most useful feature.

**Languages/tools used:** C, C++, CMake, CTest

## [jit](https://github.com/Zeex/samp-plugin-jit)

An implementation of a just-in-time compiler for the Pawn programming language (which is used for scripting in SA-MP). The plugin replaces the default VM interpreter with its own function that compiles bytecode to native machine code at runtime and executes it.

**Languages/tools used:** C++, x86 assembly, asmjit, CMake, CTest

## [profiler](https://github.com/Zeex/samp-plugin-profiler)

This plugin allows one to measure how much time is spent in each function and analyze and optimize the code based on the output. It's an instrumentation based profiler that records the start and end time of function calls by hooking into their code. Output data can be configured to be saved as a text, JSON or HTML file.

**Languages/tools used:** C++, CMake, GraphViz

## [sampgdk](https://github.com/Zeex/sampgdk)

A library that provides a C/C++ API for writing scripts (gamemodes) for SA-MP via plugins. Essentially a glue between the native plugin code and the Pawn language scripting APIs provided by the server. The implementation of those glue C/C++ functions is generated during build time based on a set of API definition files (I called them "IDL" files).

**Languages/tools used:** C, C++, CMake, Python, Python Lex-Yacc (PLY)

## [rcon](https://github.com/Zeex/samp-rcon)

A re-implementation of the rcon.exe program (remote server console software) that comes with SA-MP. It can be used to send RCON commands to a server via UDP. Unlike rcon.exe, it's cross-platform, so in addition to Windows it also works on Linux and macOS.

**Languages/tools used:** C++, UDP, sockets, Boost.Asio, CMake

## [qawno](https://github.com/Zeex/qawno)

My attempt to write a code editor for the Pawn programming language. It's written in Qt (C++), has syntax highlighting and built-in compiler support.

**Languages/tools used:** C++, Qt

# Misc

## [subhook](https://github.com/Zeex/subhook)

subhook is a library for hooking functions at runtime. Basically given a function address it redirects calls to that function to another function of choice by placing a jump instruction at the original function.

**Languages/tools used:** C, x86 assembly, CMake, yasm
