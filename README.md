lua\_nmake\_template
====================

Makefile for building Lua library using Microsoft Visual C++ and NMAKE.

Target environments
-------------------

Windows with Microsoft Visual Studio.

Tested Lua version is:
* [Lua 5.2.3 original source code](http://www.lua.org/ftp/lua-5.2.3.tar.gz "lua-5.2.3.tar.gz")

Tested Visual Studio version is:
* Visual Studio 2005 Professional SP1
* Visual Studio 2010 Professional SP1

Usage
-----

1. Put Makefile.nmake in a directory where Lua source files and Makefile exist.
    * If you build from lua-5.2.3.tar.gz, directory is: lua-5.2.3\src
2. Copy macro CORE\_O and LIB\_O from original Makefile.
3. Copy file dependencies list from original Makefile.
4. Start Visual Studio Command Prompt, and move to Lua source directory, and execute NMAKE.
    * If you want to build static library, execute `nmake /f Makefile.nmake lib`.
    * If you want to build DLL, execute `nmake /f Makefile.nmake dll`.
    * If you want to build both static library and DLL, execute `nmake /f Makefile.nmake all`.
