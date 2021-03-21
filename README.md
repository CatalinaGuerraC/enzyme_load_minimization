# Enzyme load minimization

## Install

In order to run this project you have to follow this steps:

1. Clone the project (and its `optstoic-python` submodule)

    ```bash
    git clone --recurse-submodules https://github.com/CatalinaGuerraC/enzyme_load_minimization
    ```

2. Open the folder
   
    ```bash
    cd enzyme_load_minimization
    ```

3. Create and activate a python environment
    ```bash
    python3 -m venv optstoic_env
    source optstoic_env/bin/activate
    ```

4. Setup `optstoic-python` module/library

    ```bash
    cd optstoic-python
    python setup.py install
    ```

Note that you have to have at least one solver installed in your machine. More info at [the optstoic-python documentation](https://github.com/CatalinaGuerraC/optstoic-python#solver-requirement). 


### `optstoic-python` submodule

The reason for the existance of an optstoic-python submodule is because the original project was designed in the form of a python library and for this project we needed to modify it in order to support Enzyme Load Minimization approach. Although we could have embedded the library in our source code we preferred to keep the library module and the project itself as two separate things.

## Usage

Open `optstoic_101.ipynb`. It contains all the utility functions for you to use optStoic in the original way (MinFlux) and the Enzyme Load Minimization approach with different case studies.

Main utility function:
- load reaction database (two load functions for every database: universal_db and ecolicore)
- create an optstoic problem 
- solve 
- draw result pathways
