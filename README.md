# metaldock_demo
Demo code to get MetalDock working


# Installation

Following the instuctions on https://metaldock.readthedocs.io/ :

## Set up the conda environment

Create a conda environment for MetalDock 
```
conda create -n MetalDock python=3.8
```
Activate the conda environment
```
conda activate MetalDock
```

Install required packages
```
conda install -c conda-forge openbabel

pip install ase rdkit-pypi pdb2pqr networkx numpy plams ase pandas
```

## Clone the `MetalDock` package into a *separate* Git repo

```
cd ~/git
git clone https://github.com/MatthijsHak/MetalDock
cd ~/git/metaldock_demo
```

Then, following the steps found [here](https://www.reddit.com/r/learnpython/comments/oytst5/adding_local_directory_to_python_path_in_anaconda/), we will use pip to install python package:

```
python -m pip install ~/git/MetalDock
```

Get the 'metaldock' in your executable path
```
export PATH=$PATH:/Users/vv/git/MetalDock
```





# Problem in installation

please see the codes :
(MetalDock) saem@b0-be-83-3f-26-bb ~ % git clone https://github.com/MatthijsHak/MetalDock
fatal: destination path 'MetalDock' already exists and is not an empty directory.
(MetalDock) saem@b0-be-83-3f-26-bb ~ % 
