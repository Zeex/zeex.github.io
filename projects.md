---
title: Projects
---

# SA-MP Plugins & Tools

I made a bunch of open-source server-side plugins and libraries/tools for [San Andreas Multiplayer (SA-MP)](https://www.sa-mp.com) over the course of a few years. Among those projects are:

## [crashdetect](https://github.com/Zeex/samp-plugin-crashdetect)

This plugin detects when a SA-MP server crashes due to some unhandled exception and prints a stack trace along with other debugging information that can help locate and fix the issue. Additionally it detects runtime errors that occur in the Pawn virtual machine (AMX).

**Technologies/tools used:** C, C++, POSIX/Win32 API, CMake, CTest

## [jit](https://github.com/Zeex/samp-plugin-jit)

An implementation of a just-in-time (JIT) compiler for the [Pawn programming language](https://www.compuphase.com/pawn/pawn.htm), which is used for scripting in SA-MP. 

Basically this plugin replaces the default VM interpreter with its own function that compiles Pawn bytecode (P-code) into native machine code at runtime and executes it. This can speed up the script execution significantly.

**Technologies/tools used:** C++, x86 assembly, [asmjit](https://github.com/asmjit/asmjit), CMake, CTest

## [profiler](https://github.com/Zeex/samp-plugin-profiler)

Profiler allows a script developer to measure how much time is spent in each function of a script and helps analyze and optimize the code based on provided results. 

It's an instrumentation based profiler that records the start and end time of function calls by hooking into their code. Profiling statistics is saved as a table of all funcion calls groyped by function name. It can be configured to additionally  generate a graph of all function calls it was able to record where nodes are colored depending on their "hotness".

**Technologies/tools used:** C++, CMake, GraphViz

## [sampgdk](https://github.com/Zeex/sampgdk)

GDK is a library that provides a C/C++ API for writing scripts (gamemodes) for SA-MP via plugins. It's essentially a glue between the native plugin code and the Pawn language scripting APIs provided by the server.

**Technologies/tools used:** C, C++, CMake, Python, Python Lex-Yacc (PLY)

## [pawn](https://github.com/pawn-lang/compiler)

An effort to patch the Pawn compiler used in SA-MP and port it to other operating systesm besides Windows, e.g. Linux and macOS. 

**Technologies/tools used:** C, Pawn, CMake, CTest, Python, profiling

## [amx_assembly](https://github.com/Zeex/amx_assembly)

Some interesting low-level hacks that one can do with the AMX assembly language in SA-MP: reading/writing arbitrary memory outside of the VM, executing native assembly code and more.

**Technologies/tools used:** Pawn

## [rcon](https://github.com/Zeex/samp-rcon)

A re-implementation of the rcon.exe program (remote server console software) that comes with SA-MP. It's a CLI program that can be used to send RCON commands to a SA-MP server via UDP. Unlike rcon.exe it's cross-platform, so in addition to Windows it also works on Linux and macOS.

**Technologies/tools used:** C++, sockets, UDP, CMake, Boost

## [qawno](https://github.com/Zeex/qawno)

A simple code editor for the Pawn programming language. It's written in Qt (C++), has syntax highlighting and built-in compiler support.

**Technologies/tools used:** C++, Qt

# Misc

## [subhook](https://github.com/Zeex/subhook)

SubHook (subroutine hook) is a library for hooking functions at runtime. Given a function address it can redirect calls to that function to another function of choice by placing a special jump instruction in the original function.

**Technologies/tools used:** C, x86 assembly, yasm, CMake, CTest

# Contributions

I made some minor contributions to these projects (not anything ground-breaking):

* [CMake - a cross-platform build system for C and C++](https://github.com/Kitware/CMake)
* [asmjit - x86 assembler library](https://github.com/asmjit/asmjit)
