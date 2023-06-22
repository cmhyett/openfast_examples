```
# first time setup
#   run this in bash
module load anaconda/2020
conda init bash
source ~/.bashrc
conda create -n openfast_env
conda activate openfast_env
conda install -c conda-forge openfast

# run basic example
git clone https://github.com/cmhyett/r-test.git
```