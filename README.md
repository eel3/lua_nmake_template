lua\_nmake\_template
====================

Makefile for building Lua library using Microsoft Visual C++ and NMAKE.

License
-------

CC0 1.0 Universal, but attention!

In Makefile.nmake, part of Lua code (Makefile) is exist.
These codes are distributed under the terms of the MIT license.

    Copyright (c) 1994-2025 Lua.org, PUC-Rio.
    Released under the MIT license
    https://www.lua.org/license.html

Target environments
-------------------

Windows with Microsoft Visual Studio.

Tested Lua version is:
* [Lua 5.4.8 original source code](https://www.lua.org/ftp/lua-5.4.8.tar.gz "lua-5.4.8.tar.gz")

Tested Visual Studio version is:
* Visual Studio 2017 Professional

Usage
-----

1. Put Makefile.nmake in a directory where Lua source files and Makefile exist.
    * If you build from lua-5.4.8.tar.gz, directory is: lua-5.4.8\src
2. Copy macro CORE\_O LIB\_O LUA\_T LUA\_O LUAC\_T LUAC\_O from original Makefile.
3. Copy file dependencies list from original Makefile.
4. Start Visual Studio Command Prompt, and move to Lua source directory, and execute NMAKE.
    * If you want to build static library, execute `nmake /f Makefile.nmake lib`.
    * If you want to build DLL, execute `nmake /f Makefile.nmake dll`.
    * If you want to build lua.exe and luac.exe, execute `nmake /f Makefile.nmake exe`.
    * If you want to build both library and executable, execute `nmake /f Makefile.nmake all`.
