# BO-SUM99
code available for [article title]
This repository is built for reproducing the Bayesion Optimization

## Install dependency packages
The code can currently only run on Linux systems; for Windows systems, you can install [WSL](https://learn.microsoft.com/en-us/windows/wsl/install).

It is recommended to use [conda](https://anaconda.org/) to run the environment.

Create a new environment in conda, install the [`hotpot`](https://github.com/Zhang-Zhiyuan-zzy/hotpot) package:

> conda create -n hp python==3.9 openbabel cclib lammps -c conda-forge
> conda activate hp
> pip install hotpot-zzy==0.5.0.1

Typing `hotpot` in your terminal to test completeness of the installation.

## Reproduce Bayesian Optimization
Running the following code for reproducing BO procedure:
```linux
(hp)mkdir result
(hp)hotpot optimize . result --examples COF
```

Then, the t-SNE map is shown in `result` dir.

## Data available
The source reaction parameters is shown in this github repository in `data` subdir.
you can download the source Excel sheet and perform BO step by step

```linux
(hp)mkdir result
(hp)hotpot optimize {/path/to/src/Excel_sheet.xlsx} result
```
Now, you can get the OB suggested next parameters in ./result/next_params.xlsx file.
