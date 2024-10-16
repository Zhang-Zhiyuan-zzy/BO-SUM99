# BO-SUM99
#### Author: Zhen-wu Shao, Zhiyuan Zhang, Chong Liu*
Code availability for **Bayesian Optimized Crystallization of a Hydroxamate-Functionalized Covalent Organic Framework for Enhanced Uranyl Uptake**: This repository is intended for reproducing Bayesian Optimization.

## Install dependency packages
The code can currently runs only on Linux; for Windows, you can install [WSL](https://learn.microsoft.com/en-us/windows/wsl/install).

Use [conda](https://anaconda.org/) to setup the environment.

Create a new conda environment and install the [`hotpot`](https://github.com/Zhang-Zhiyuan-zzy/hotpot) package:

> conda create -n hp python==3.9 openbabel cclib lammps -c conda-forge
> conda activate hp
> pip install hotpot-zzy==0.5.0.1

Type `hotpot` in your terminal to verify the installation completeness.

## Reproduce Bayesian Optimization
Run the following code to reproduce BO procedure:
```linux
(hp)mkdir result
(hp)hotpot optimize . result --examples COF
```

Then, the t-SNE map is displayed in `result` dir.

## Data available
The source reaction parameters are available in the `data` subdir of this GitHub repository.
you can download the Excel sheet and follow the BO steps:

```linux
(hp)mkdir result
(hp)hotpot optimize {/path/to/src/Excel_sheet.xlsx} result
```
Now, you can find the BO suggested next parameters in ./result/next_params.xlsx file.
