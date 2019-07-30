# CS100
Repository to demonstrate Jupyter notebook coversion of the Computer Science 1 course. 

## Example
Let's look at a sample file conversion. 

Try one of the notebooks by clicking one of the buttons below to open on Colab or via Binder:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/RPI-DATA/csci1100/blob/master/_build/jupyter/lecture_notes/lec02_calculator.ipynb)

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/RPI-DATA/csci1100/master?filepath=_build%2Fjupyter%2Flecture_notes%2Flec02_calculator.ipynb)


The Jupyter notebook is interactable with the code blocks ready to be executed. 

## Working
The conversion was done using [Sphinx-Jupyter](https://sphinxcontrib-jupyter.readthedocs.io/en/latest/). 

You can **install** using pip:

   `pip install sphinxcontrib-jupyter`

or get the **latest** version by getting a copy of the repository, and

   `python setup.py install`
   
## Configuration
   
Once installed, Update project ``conf.py`` file to include the jupyter extension.

``extensions = ["sphinxcontrib.jupyter"]``

Sample configuration can be seen [here](https://github.com/QuantEcon/sphinxcontrib-jupyter.minimal/blob/master/conf.py)

For a more comprehensive documentation refer [this](https://sphinxcontrib-jupyter.readthedocs.io/en/latest/).

## Running
Execute:
``make jupyter``

The output will be available in the ``_build`` folder.
