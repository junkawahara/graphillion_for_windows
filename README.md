# Graphillion for Windows

[Graphillion](https://github.com/takemaru/graphillion) is a fast, lightweight library for a huge number of graphs, which is mainly developed by Takeru Inoue and JST ERATO MINATO project. This repository provides wheels of graphillion for windows.

## Requirements

Graphillion for Windows supports Python 3.6, 3.5, and 2.7.
We have confirmed that it worked well under the following environment:

* Windows 10, [Python 3.6.0 for Windows](https://www.python.org/downloads/),
* Windows 10, [Anaconda 4.3.0 for Windows, Python 3.6 version](https://www.continuum.io/downloads), Python 3.6.0
* Windows 10, [Anaconda 4.3.0 for Windows, Python 3.6 version](https://www.continuum.io/downloads), Python 3.5.3 (creating a virtual environment for python 3.5)
* Windows 10, [Python 2.7.13 for Windows](https://www.python.org/downloads/)
* Windows 10, [Anaconda 4.3.0 for Windows, Python 3.6 version](https://www.continuum.io/downloads), Python 2.7.13 (creating a virtual environment for python 2.7.13)
* Windows 10, Anaconda 2.1.0 for Windows, Python 2.7.8

Graphillion for Windows supports only 64 bit environment. We have no plan to support 32 bit version.

## Install

Just type
```
pip install graphillion
```
under a windows environment.

## License

Graphillion for Windows obeys the license of graphillion, i.e., graphillion for Windows is distributed under the [MIT license](http://opensource.org/licenses/MIT).

## Note

For Windows 10 and Python 2.7, reading or writing a file through graphillion causes a crash.

## How to build graphillion for Windows

You need not read this section unless you are interested in the technical details. 

### For Python 3.6

1. Install "Microsoft Visual C++ 2015 Build Tools": http://landinghub.visualstudio.com/visual-cpp-build-tools .
2. Install [Anaconda 4.3.0 for Windows, Python 3.6 version, 64 bit](https://www.continuum.io/downloads).
3. Clone graphillion from github: ```git clone https://github.com/takemaru/graphillion.git```
4. Set PATH environment variable: ```set PATH=C:\Anaconda3;C:\Anaconda3\Scripts;%PATH%```(your Anaconda paths may be different)
5. Change directory to the source directory
   (it should have the file setup.py)
6. Run ```python setup.py build```
7. Run ```python setup.py bdist_wheel```

### For Python 2.7

1. Download and install Anaconda version 2.1.0 from https://repo.continuum.io/archive/Anaconda-2.1.0-Windows-x86_64.exe (the latest version is not suitable for compiling graphillion on Python 2.7).
2. Add the following paths to the %PATH% variable: ```set PATH=%PATH%;C:\Anaconda;C:\Anaconda\Scripts;C:\Anaconda\DLLs;C:\Anaconda\MinGW\bin;C:\Anaconda\MinGW\x86_64-w64-mingw32\lib``` (your Anaconda paths may be different)
3. Install wheel: ```pip install wheel```
4. Clone graphillion from github: ```git clone https://github.com/takemaru/graphillion.git```
5. Change directory to the source directory
   (it should have the file setup.py)
6. Run ```python setup.py build```
7. Run ```python setup.py bdist_wheel```

In this way, graphillion is compiled by gcc in MinGW. So, this binary might not work under cygwin or Visual C++ environment.
