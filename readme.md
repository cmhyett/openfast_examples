OpenFAST is somehow very poorly documented for setup, this repository aims to help.

We install in virtual conda environment to enable deployment on HPC easily.

Run the commands individually (or I suppose you can just execute the whole bash script) from setup.sh

```
#!bin/bash

# first time conda setup (only do this once ever)
module load anaconda/2020
conda init bash
source ~/.bashrc
conda create -n openfast_env
conda activate openfast_env
conda install -c conda-forge openfast

# run basic example
openfast ./5MW_Land_DLL_WTurb/5MW_Land_DLL_WTurb.fst
```

Each subsequent login to the HPC will look like

```
module load anaconda/2020
conda activate openfast_env
openfast ./5MW_Land_DLL_WTurb/5MW_Land_DLL_WTurb.fst
```

The main interface to OpenFAST is via a LOT of input files. This is where we should begin digging next.
