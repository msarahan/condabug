# Steps to reproduce

The following commands will succeed:

```batch
> conda build .\conda_recipe --py 35
> conda build .\conda_recipe
> set CONDA_PY=35
> conda build .\conda_recipe
```

These commands will fail:

```batch
> conda build .\conda_recipe --py 27
> set CONDA_PY=27
> conda build .\conda_recipe
```

# conda info

```
> conda info
Using Anaconda Cloud api site https://api.anaconda.org
Current conda install:

             platform : win-64
        conda version : 4.1.0
  conda-build version : 1.21.0
       python version : 3.5.1.final.0
     requests version : 2.9.1
     root environment : C:\Users\korij\Miniconda3  (writable)
  default environment : C:\Users\korij\Miniconda3
     envs directories : C:\Users\korij\Miniconda3\envs
        package cache : C:\Users\korij\Miniconda3\pkgs
         channel URLs : https://repo.continuum.io/pkgs/free/win-64/
                        https://repo.continuum.io/pkgs/free/noarch/
                        https://repo.continuum.io/pkgs/pro/win-64/
                        https://repo.continuum.io/pkgs/pro/noarch/
          config file : C:\Users\korij\.condarc
    is foreign system : False
```

# output of failing command

```
korij@KORIJN-LAPTOP C:\Users\korij\dev\condabug
> conda build conda_recipe --py 27
Removing old build environment
BUILD START: hw-1.0.0-py_0
Using Anaconda Cloud api site https://api.anaconda.org
Fetching package metadata ...........
Solving package specifications .............

The following NEW packages will be INSTALLED:

    jpeg:           8d-vc14_0       [vc14]
    libpng:         1.6.22-vc14_0   [vc14]
    libtiff:        4.0.6-vc14_2    [vc14]
    openssl:        1.0.2h-vc14_0   [vc14]
    pip:            8.1.2-py35_0
    pyqt:           4.11.4-py35_6
    python:         3.5.1-4
    qt:             4.8.7-vc14_8    [vc14]
    setuptools:     23.0.0-py35_0
    sip:            4.16.9-py35_2
    vs2015_runtime: 14.00.23026.0-0
    wheel:          0.29.0-py35_0
    zlib:           1.2.8-vc14_3    [vc14]

Linking packages ...
        1 file(s) copied.########################################        |  84%
[      COMPLETE      ]|##################################################| 100%
Copying C:\Users\korij\dev\condabug to C:\Users\korij\Miniconda3\conda-bld\work
Package: hw-1.0.0-py_0
source tree in: C:\Users\korij\Miniconda3\conda-bld\work

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "GIT_FULL_HASH=6d29ca396abd79491e657374e2c3739d4600abcb"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "CPU_COUNT=4"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "GIT_DESCRIBE_HASH=g6d29ca3"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "PSModulePath=C:\WINDOWS\system32\WindowsPowerShell\v1.0\Modules\;C:\Program Files (x86)\Microsoft SQL Server\120\Tools\PowerShell\Modules\;C:\Program Files\WindowsPowerShell\Modules\;C:\Program Files (x86)\Microsoft SDKs\Azure\PowerShell\ResourceManager\AzureResourceManager\;C:\Program Files (x86)\Microsoft SDKs\Azure\PowerShell\ServiceManagement\;C:\Program Files (x86)\Microsoft SDKs\Azure\PowerShell\Storage\"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ProgramFiles=C:\Program Files"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ConEmuDrive=C:"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "CONDA_OLD_PS1=$E[32m$E]9;8;"USERNAME"$E\@$E]9;8;"COMPUTERNAME"$E\$S$E[92m$P$E[90m$_$E[90m$G$E[m$S"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ConEmuDir=C:\Program Files\ConEmu"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "windir=C:\WINDOWS"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "GIT_BUILD_STR=1_g6d29ca3"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "LUA=C:\Users\korij\Miniconda3\envs\_build\lua.exe"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ConEmuBuild=151210"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "CONDA_PATH_BACKUP=C:\Users\korij\Miniconda3\Library\bin;C:\Users\korij\Miniconda3\Library\bin;C:\Program Files\ConEmu;C:\Program Files\ConEmu\ConEmu;C:\ProgramData\Oracle\Java\javapath;C:\Program Files\PHP\v7.0;C:\Program Files\PHP\v5.3;C:\Program Files\iis express\PHP\v7.0;C:\Program Files\Dell\DW WLAN Card;C:\Program Files (x86)\Intel\iCLS Client\;C:\Program Files\Intel\iCLS Client\;C:\WINDOWS\system32;C:\WINDOWS;C:\WINDOWS\System32\Wbem;C:\WINDOWS\System32\WindowsPowerShell\v1.0\;C:\Program Files (x86)\Intel\Intel(R) Management Engine Components\DAL;C:\Program Files\Intel\Intel(R) Management Engine Components\DAL;C:\Program Files (x86)\Intel\Intel(R) Management Engine Components\IPT;C:\Program Files\Intel\Intel(R) Management Engine Components\IPT;c:\Program Files\WIDCOMM\Bluetooth Software\;c:\Program Files\WIDCOMM\Bluetooth Software\syswow64;C:\Program Files\Git\cmd;C:\Program Files\Microsoft\Web Platform Installer\;C:\Program Files\Microsoft SQL Server\120\Tools\Binn\;C:\Program Files\Microsoft SQL Server\Client SDK\ODBC\110\Tools\Binn\;C:\Program Files (x86)\Microsoft SQL Server\120\Tools\Binn\;C:\Program Files\Microsoft SQL Server\120\DTS\Binn\;C:\Program Files (x86)\Microsoft SQL Se;C:\Program Files\TortoiseHg;C:\Program Files\Git\bin;C:\Program Files (x86)\Skype\Phone\;C:\Users\korij\Miniconda3;C:\Users\korij\Miniconda3\Scripts;C:\Users\korij\Miniconda3\Library\bin;C:\Program Files\Docker Toolbox"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "PY3K=0"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "PYTHON=C:\Users\korij\Miniconda3\envs\_build\python.exe"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "SUBDIR=win-64"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ConEmuPrompt3=$E[m$S"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ConEmuBackHWND=0x000303A6"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ConEmuPrompt1=$E[32m$E]9;8;"USERNAME"$E\@$E]9;8;"COMPUTERNAME"$E\$S$E[92m$P$E[90m"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "PKG_NAME=hw"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ConEmuWorkDir=C:\Users\korij"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "SystemDrive=C:"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "SCRIPTS=C:\Users\korij\Miniconda3\envs\_build\Scripts"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "SRC_DIR=C:\Users\korij\Miniconda3\conda-bld\work"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ConEmuArgs="

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "SYS_PYTHON=C:\Users\korij\Miniconda3\python.exe"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "CONDA_BUILD=1"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "PROMPT=((_build)) $E[32m$E]9;8;"USERNAME"$E\@$E]9;8;"COMPUTERNAME"$E\$S$E[92m$P$E[90m$_$E[90m$G$E[m$S"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "PATH=C:\Users\korij\Miniconda3\envs\_build;C:\Users\korij\Miniconda3\envs\_build\Library\mingw-w64\bin;C:\Users\korij\Miniconda3\envs\_build\Library\usr\bin;;C:\Users\korij\Miniconda3\envs\_build\Library\bin;C:\Users\korij\Miniconda3\envs\_build\Scripts;C:\Users\korij\Miniconda3\envs\_build;C:\Users\korij\Miniconda3\envs\_build\Library\mingw-w64\bin;C:\Users\korij\Miniconda3\envs\_build\Library\usr\bin;C:\Users\korij\Miniconda3\envs\_build\Library\bin;C:\Users\korij\Miniconda3\envs\_build\Scripts;C:\Users\korij\Miniconda3\Library\bin;C:\Users\korij\Miniconda3\Library\bin;C:\Users\korij\Miniconda3\Library\bin;C:\Program Files\ConEmu;C:\Program Files\ConEmu\ConEmu;C:\ProgramData\Oracle\Java\javapath;C:\Program Files\PHP\v7.0;C:\Program Files\PHP\v5.3;C:\Program Files\iis express\PHP\v7.0;C:\Program Files\Dell\DW WLAN Card;C:\Program Files (x86)\Intel\iCLS Client\;C:\Program Files\Intel\iCLS Client\;C:\WINDOWS\system32;C:\WINDOWS;C:\WINDOWS\System32\Wbem;C:\WINDOWS\System32\WindowsPowerShell\v1.0\;C:\Program Files (x86)\Intel\Intel(R) Management Engine Components\DAL;C:\Program Files\Intel\Intel(R) Management Engine Components\DAL;C:\Program Files (x86)\Intel\Intel(R) Management Engine Components\IPT;C:\Program Files\Intel\Intel(R) Management Engine Components\IPT;c:\Program Files\WIDCOMM\Bluetooth Software\;c:\Program Files\WIDCOMM\Bluetooth Software\syswow64;C:\Program Files\Git\cmd;C:\Program Files\Microsoft\Web Platform Installer\;C:\Program Files\Microsoft SQL Server\120\Tools\Binn\;C:\Program Files\Microsoft SQL Server\Client SDK\ODBC\110\Tools\Binn\;C:\Program Files (x86)\Microsoft SQL Server\120\Tools\Binn\;C:\Program Files\Microsoft SQL Server\120\DTS\Binn\;C:\Program Files (x86)\Microsoft SQL Se;C:\Program Files\TortoiseHg;C:\Program Files\Git\bin;C:\Program Files (x86)\Skype\Phone\;C:\Users\korij\Miniconda3;C:\Users\korij\Miniconda3\Scripts;C:\Users\korij\Miniconda3\Library\bin;C:\Program Files\Docker Toolbox"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ConEmuHWND=0x00040396"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ConEmuPrompt2=$_$E[90m$G"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "CommonProgramFiles(x86)=C:\Program Files (x86)\Common Files"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ConEmuServerPID=2128"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "SYS_PREFIX=C:\Users\korij\Miniconda3"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ConEmuPID=13172"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ARCH=64"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "PY_VER=2.7"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "LIBRARY_LIB=C:\Users\korij\Miniconda3\envs\_build\Library\lib"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "LIBRARY_BIN=C:\Users\korij\Miniconda3\envs\_build\Library\bin"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "GIT_DESCRIBE_NUMBER=1"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "LUA_INCLUDE_DIR=C:\Users\korij\Miniconda3\envs\_build\include"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ConEmuPrompt0=$E[32m$E]9;8;"USERNAME"$E\@$E]9;8;"COMPUTERNAME"$E\$S"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "SystemRoot=C:\WINDOWS"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "DIRTY="

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "HTTPS_PROXY="

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "R=C:\Users\korij\Miniconda3\envs\_build\Scripts\R.exe"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "PREFIX=C:\Users\korij\Miniconda3\envs\_build"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "RECIPE_DIR=C:\Users\korij\dev\condabug\conda_recipe"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "CGML_STORAGE_KEY=mnV0IjEClUvobhkYhlS2FhzrfdeYx+71oni9m1kmcZpB3TbRAk4XeWk9nQOSeIcnaY+7tCrYASdJzIKuRZ+PPQ"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "PKG_VERSION=1.0.0"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "LUA_VER=5.2"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "Path=C:\Users\korij\Miniconda3\envs\_build;C:\Users\korij\Miniconda3\envs\_build\Library\mingw-w64\bin;C:\Users\korij\Miniconda3\envs\_build\Library\usr\bin;C:\Users\korij\Miniconda3\envs\_build\Library\bin;C:\Users\korij\Miniconda3\envs\_build\Scripts;C:\Users\korij\Miniconda3\Library\bin;C:\Users\korij\Miniconda3\Library\bin;C:\Users\korij\Miniconda3\Library\bin;C:\Program Files\ConEmu;C:\Program Files\ConEmu\ConEmu;C:\ProgramData\Oracle\Java\javapath;C:\Program Files\PHP\v7.0;C:\Program Files\PHP\v5.3;C:\Program Files\iis express\PHP\v7.0;C:\Program Files\Dell\DW WLAN Card;C:\Program Files (x86)\Intel\iCLS Client\;C:\Program Files\Intel\iCLS Client\;C:\WINDOWS\system32;C:\WINDOWS;C:\WINDOWS\System32\Wbem;C:\WINDOWS\System32\WindowsPowerShell\v1.0\;C:\Program Files (x86)\Intel\Intel(R) Management Engine Components\DAL;C:\Program Files\Intel\Intel(R) Management Engine Components\DAL;C:\Program Files (x86)\Intel\Intel(R) Management Engine Components\IPT;C:\Program Files\Intel\Intel(R) Management Engine Components\IPT;c:\Program Files\WIDCOMM\Bluetooth Software\;c:\Program Files\WIDCOMM\Bluetooth Software\syswow64;C:\Program Files\Git\cmd;C:\Program Files\Microsoft\Web Platform Installer\;C:\Program Files\Microsoft SQL Server\120\Tools\Binn\;C:\Program Files\Microsoft SQL Server\Client SDK\ODBC\110\Tools\Binn\;C:\Program Files (x86)\Microsoft SQL Server\120\Tools\Binn\;C:\Program Files\Microsoft SQL Server\120\DTS\Binn\;C:\Program Files (x86)\Microsoft SQL Se;C:\Program Files\TortoiseHg;C:\Program Files\Git\bin;C:\Program Files (x86)\Skype\Phone\;C:\Users\korij\Miniconda3;C:\Users\korij\Miniconda3\Scripts;C:\Users\korij\Miniconda3\Library\bin;C:\Program Files\Docker Toolbox"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "CommonProgramW6432=C:\Program Files\Common Files"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "HTTP_PROXY="

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "CommonProgramFiles=C:\Program Files\Common Files"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "CYGWIN_PREFIX=/cygdrive/c/Users/korij/Miniconda3/envs/_build"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "PYTHONNOUSERSITE=1"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "SP_DIR=C:\Users\korij\Miniconda3\envs\_build\Lib\site-packages"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "CONDA_DEFAULT_ENV=C:\Users\korij\Miniconda3\envs\_build"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ComSpec=C:\WINDOWS\system32\cmd.exe"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ProgramW6432=C:\Program Files"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ConEmuDrawHWND=0x0004034C"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ConEmuWorkDrive=C:"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "CONDA_PY=27"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "GIT_DESCRIBE_TAG=unsatisfiable-package-specifications"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "STDLIB_DIR=C:\Users\korij\Miniconda3\envs\_build\Lib"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "PERL_VER=5.18.2"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ConEmuHooks=Enabled"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ConEmuANSI=ON"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ConEmuAnsiLog="

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ProgramFiles(x86)=C:\Program Files (x86)"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "PKG_BUILDNUM=0"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "PKG_BUILD_STRING=py_0"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "LIBRARY_INC=C:\Users\korij\Miniconda3\envs\_build\Library\include"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ProgramData=C:\ProgramData"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "LIBRARY_PREFIX=C:\Users\korij\Miniconda3\envs\_build\Library"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ConEmuConfig="

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "ConEmuBaseDir=C:\Program Files\ConEmu\ConEmu"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set INCLUDE=C:\Users\korij\Miniconda3\envs\_build\Library\include;

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set LIB=C:\Users\korij\Miniconda3\envs\_build\Library\lib;

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "VS_VERSION=9.0"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "VS_MAJOR=9"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "VS_YEAR=2008"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "CMAKE_GENERATOR=Visual Studio 9 2008 Win64"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "MSYS2_ARG_CONV_EXCL=/AI;/AL;/OUT;/out;"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> set "MSYS2_ENV_CONV_EXCL=CL"

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> call "C:\Users\korij\AppData\Local\Programs\Common\Microsoft\Visual C++ for Python\9.0\vcvarsall.bat" amd64
The system cannot find the path specified.

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> if errorlevel 1 call "C:\Program Files (x86)\Common Files\Microsoft\Visual C++ for Python\9.0\vcvarsall.bat" amd64
The system cannot find the path specified.

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> if errorlevel 1 call "C:\Program Files (x86)\Microsoft Visual Studio 9.0\VC\bin\vcvars64.bat" amd64
The system cannot find the path specified.

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> if errorlevel 1 call "C:\Program Files (x86)\Microsoft Visual Studio 9.0\VC\vcvarsall.bat" amd64
The system cannot find the path specified.

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> REM ===== end generated header =====

((_build)) korij@KORIJN-LAPTOP C:\Users\korij\Miniconda3\conda-bld\work
> C:\Users\korij\Miniconda3\envs\_build\python.exe setup.py install
running install
running bdist_egg
running egg_info
creating hw.egg-info
writing hw.egg-info\PKG-INFO
writing top-level names to hw.egg-info\top_level.txt
writing dependency_links to hw.egg-info\dependency_links.txt
writing manifest file 'hw.egg-info\SOURCES.txt'
reading manifest file 'hw.egg-info\SOURCES.txt'
writing manifest file 'hw.egg-info\SOURCES.txt'
installing library code to build\bdist.win-amd64\egg
running install_lib
running build_py
creating build
creating build\lib
creating build\lib\hw
copying hw\__init__.py -> build\lib\hw
creating build\bdist.win-amd64
creating build\bdist.win-amd64\egg
creating build\bdist.win-amd64\egg\hw
copying build\lib\hw\__init__.py -> build\bdist.win-amd64\egg\hw
byte-compiling build\bdist.win-amd64\egg\hw\__init__.py to __init__.cpython-35.pyc
creating build\bdist.win-amd64\egg\EGG-INFO
copying hw.egg-info\PKG-INFO -> build\bdist.win-amd64\egg\EGG-INFO
copying hw.egg-info\SOURCES.txt -> build\bdist.win-amd64\egg\EGG-INFO
copying hw.egg-info\dependency_links.txt -> build\bdist.win-amd64\egg\EGG-INFO
copying hw.egg-info\top_level.txt -> build\bdist.win-amd64\egg\EGG-INFO
zip_safe flag not set; analyzing archive contents...
creating dist
creating 'dist\hw-1.0.0-py3.5.egg' and adding 'build\bdist.win-amd64\egg' to it
removing 'build\bdist.win-amd64\egg' (and everything under it)
Processing hw-1.0.0-py3.5.egg
Copying hw-1.0.0-py3.5.egg to c:\users\korij\miniconda3\envs\_build\lib\site-packages
Adding hw 1.0.0 to easy-install.pth file

Installed c:\users\korij\miniconda3\envs\_build\lib\site-packages\hw-1.0.0-py3.5.egg
Processing dependencies for hw==1.0.0
Finished processing dependencies for hw==1.0.0
found egg: C:\Users\korij\Miniconda3\envs\_build\Lib\site-packages\hw-1.0.0-py3.5.egg
compiling .pyc files...
*** Error compiling 'C:\\Users\\korij\\Miniconda3\\envs\\_build\\Lib\\site-packages\\PyQt4\\uic\\port_v2\\invoke.py'...
  File "C:\Users\korij\Miniconda3\envs\_build\Lib\site-packages\PyQt4\uic\port_v2\invoke.py", line 36
    except IOError, e:
                  ^
SyntaxError: invalid syntax

*** Error compiling 'C:\\Users\\korij\\Miniconda3\\envs\\_build\\Lib\\site-packages\\PyQt4\\uic\\port_v2\\load_plugin.py'...
  File "C:\Users\korij\Miniconda3\envs\_build\Lib\site-packages\PyQt4\uic\port_v2\load_plugin.py", line 38
    except Exception, e:
                    ^
SyntaxError: invalid syntax

Command failed: C:\Users\korij\Miniconda3\envs\_build\python.exe -Wi C:\Users\korij\Miniconda3\envs\_build\Lib\compileall.py -q -x port_v3 C:\Users\korij\Miniconda3\envs\_build\Lib\site-packages
```