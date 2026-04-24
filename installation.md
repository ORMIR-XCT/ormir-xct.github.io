# Installation

**🚧 Page under construction 🚧**


::::{tab-set}

<!-- Tab 1: new environment -->
:::{tab-item} Install into a new Anaconda environment
:sync: tab1

***For Windows, Linux, and Intel-based Mac:***

1: Install the ormir_xct Anaconda environment from the YAML file:  
`conda env create -f environment.yml`

2: Activate and use the ormir_xct environment:  
`conda activate ormir_xct`  


***For Apple Silicon Mac (M-chips):***

1: Install the ormir_xct Anaconda environment, specifying macOS architecture:  
`CONDA_SUBDIR=osx-64 conda create -n ormir_xct python=3.11.11 pip`  

2: Activate the ormir_xct environment:  
`conda activate ormir_xct`

3: Tell conda to always use the macOS architecture:  
`conda env config vars set CONDA_SUBDIR=osx-64`

4: Deactivate and reactivate the environment:  
`conda deactivate`    
`conda activate ormir_xct`

5: Install the required dependencies using pip:  
`pip install -r requirements.txt` 

:::


<!-- Tab 2: existing environment -->
:::{tab-item} Install into an existing Anaconda environment
:sync: tab2

1: Activate your environment:  
`conda activate my_env`

2: Install ormir-xct from PyPi  
`pip install ormir-xct`

:::

::::


