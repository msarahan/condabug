Steps to reproduce:

```batch
> conda build .\conda_recipe --py 35 --no-anaconda-upload
> conda build .\conda_recipe --py 34 --no-anaconda-upload
> conda build .\conda_recipe --py 27 --no-anaconda-upload
> conda create -n condabug --alt-hint --use-local python hw
Using Anaconda Cloud api site https://api.anaconda.org
Fetching package metadata: ........
Solving package specifications: ...
Error: Unsatisfiable package specifications.
Generating minimal hint:
[      COMPLETE      ]|##################################################| 100%

The following set of clauses is unsatisfiable:

not hw-1.0.0-py35_vc14_0
not hw-1.0.0-py27_vc9_0
not hw-1.0.0-py34_vc10_0
hw-1.0.0-py27_vc9_0 or hw-1.0.0-py35_vc14_0 or hw-1.0.0-py34_vc10_0
```