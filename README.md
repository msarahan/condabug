Steps to reproduce:

> conda build .\conda_recipe --py 35 --no-anaconda-upload

> conda build .\conda_recipe --py 34 --no-anaconda-upload

> conda build .\conda_recipe --py 27 --no-anaconda-upload

> conda create -n condabug --use-local python hw
