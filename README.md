# Steps to reproduce

Using Miniconda based on Python 3.5, the following commands will succeed:

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