# Graphillion for Windows

[Graphillion](https://github.com/takemaru/graphillion) is a fast, lightweight library for a huge number of graphs, which is mainly developed by Takeru Inoue and JST ERATO MINATO project. This repository provides a windows installer of graphillion.

## Requirements

Graphillion for Windows requires "Python 2.7 for Windows," which is available at https://www.python.org/downloads/. We have confirmed that it worked well under the following environment:

* Windows 8.1
* Python 2.7.10

## Install

Just download and run the installer Graphillion-0.98-r0.win-amd64-py2.7.exe.

## Notes

This version is built based on the version 0.98 of graphillion.

## License

Graphillion for Windows obeys the license of graphillion, i.e., graphillion for Windows is distributed under the [MIT license](http://opensource.org/licenses/MIT).

## How to build graphillion for Windows

You need not read this section unless you are interested in the technical details. 

1. Download and install Anaconda version 2.1.0 from https://repo.continuum.io/archive/Anaconda-2.1.0-Windows-x86_64.exe (the latest version is not suitable for compiling graphillion).
2. Add the following paths to the %PATH% variable (Your Anaconda paths may be different):
```
set PATH=%PATH%;C:\Anaconda;C:\Anaconda\Scripts;C:\Anaconda\DLLs;C:\Anaconda\MinGW\bin;C:\Anaconda\MinGW\x86_64-w64-mingw32\lib
```
3. Download the source (tar.gz or zip file) from Github (Do not use the Pypi tarball):
   https://github.com/takemaru/graphillion
4. Run IPython
5. Change directory to the source directory
   (it should have the file setup.py)
6. Run ```run setup.py build``` to build
7. Run ```run setup.py bdist_wininst``` to make an installer for Windows

In this way, graphillion is compiled by gcc in MinGW. So, this binary might not work under cygwin or Visual C++ environment.
