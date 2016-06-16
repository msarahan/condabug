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