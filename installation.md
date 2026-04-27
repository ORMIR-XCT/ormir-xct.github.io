# Installation

**🚧 Page under construction 🚧**


::::{tab-set}

<!-- Tab 1: new environment -->
:::{tab-item} Install into a new Anaconda environment
:sync: tab1

***For Windows, Linux, and Intel-based Mac:***

1: Install the ORMIR-XCT Anaconda environment from the YAML file:  
`conda env create -f environment.yml`

2: Activate and use the ORMIR-XCT environment:  
`conda activate ormir-xct`  


***For Apple Silicon Mac (M-chips):***

1: Install the ORMIR-XCT Anaconda environment, specifying macOS architecture:  
`CONDA_SUBDIR=osx-64 conda create -n ormir-xct python=3.11.11 pip`  

2: Activate the ORMIR-XCT environment:  
`conda activate ormir-xct`

3: Tell conda to always use the macOS architecture:  
`conda env config vars set CONDA_SUBDIR=osx-64`

4: Deactivate and reactivate the environment:  
`conda deactivate`    
`conda activate ormir-xct`

5: Install the required dependencies using pip:  
`pip install -r requirements.txt` 

:::


<!-- Tab 2: existing environment -->
:::{tab-item} Install into an existing Anaconda environment
:sync: tab2

1: Activate your environment:  
`conda activate my_env`

2: Install ORMIR-XCT from PyPi  
`pip install ormir-xct`

:::

::::


