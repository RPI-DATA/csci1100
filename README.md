# CS100
Repository to demonstrate Jupyter notebook coversion of the Computer Science 1 course. 

## Example
Let's look at a sample file conversion. 

[This](https://github.com/Anuj-Chauhan/CS100/blob/master/_build/html/lecture_notes/lec02_calculator.html) html file after conversion to Jupyter notebook looks like [this](https://github.com/Anuj-Chauhan/CS100/blob/master/_build/jupyter/lecture_notes/lec02_calculator.ipynb).

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
