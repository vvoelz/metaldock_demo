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

## Install the MetalDock packacge

### Clone the `MetalDock` package into a *separate* Git repo

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

This now allows `metaldock` to run as a package installed in the MetalDock conda environment (yay!).

### Put `python2.7` in your PATH

But there's a new problem: The `metaldock` tries to find an installation of python2.7 and point an enviroment variable to it ..

<blockquote>
(MetalDock) vv@90-9c-4a-c0-7c-9e git % metaldock 
Error: The command 'python2.7' was not found in your system's PATH.
Pleae ensure that all paths are set correctly.
If paths keep failing, please try to set the absolute path manually in the file '/MetalDock/src/metal_dock/environment_variables.py'.
</blockquote>


To fix this problem, I had to install a conda enviroment with python2.7 (but not activate it), and point my $PATH to it:
```
(MetalDock) vv@90-9c-4a-c0-7c-9e git % conda create -y -n py27 python=2.7
....
(MetalDock) vv@90-9c-4a-c0-7c-9e git % which python2.7
/Users/vv/anaconda3/envs/py27/bin//python2.7


$ export PATH=$PATH:/Users/vv/anaconda3/envs/py27/bin/
```

Once this is achieved, it appears that metaldock is functional (!):
```

(MetalDock) vv@90-9c-4a-c0-7c-9e git % metaldock                                           
usage: metaldock [-h] -i INPUT_FILE
metaldock: error: the following arguments are required: -i/--input_file

```





# Problem in installation

please see the codes :
(MetalDock) saem@b0-be-83-3f-26-bb ~ % git clone https://github.com/MatthijsHak/MetalDock
fatal: destination path 'MetalDock' already exists and is not an empty directory.
(MetalDock) saem@b0-be-83-3f-26-bb ~ % 
