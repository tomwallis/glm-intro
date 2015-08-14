# The Generalised Linear Model

## A practical introduction using the Python environment

[Tom Wallis](http://www.tomwallis.info) and [Philipp Berens](http://philippberens.wordpress.com/)


This course provides an overview of an extremely flexible
statistical framework for describing and performing inference with a wide
variety of data types: the Generalised Linear Model (GLM). Many common statistical procedures are special cases of the GLM. In the course, we focus on the construction and understanding of design matrices (using S-style formula notation) and the interpretation of regression weights. We mostly concentrate on the linear Gaussian model, before discussing more general cases. We also touch on how this framework relates to ANOVA-style model comparison.

The course was designed and presented as a six week elective statistics course for graduate students in the neuroscience program at the University of Tübingen, in January 2015. Lectures were presented as a collection of IPython Notebooks. While the notebooks are (we hope) well documented, they *are* lecture materials rather than a textbook. As such, some content might not be self-explanatory. 

[You can find the notebooks on the nbviewer platform here](http://nbviewer.ipython.org/github/tomwallis/glm-intro/blob/master/index.ipynb)

We chose to do the course in Python because 

1. It is a general purpose programming language and thus more versatile than e.g. [R](http://cran.r-project.org/). Neuroscientists can use Python to not only analyse data but also to e.g. interface with hardware, [conduct behavioural experiments](http://www.psychopy.org/), etc. 
1. Its [popularity as a scientific computing environment is rapidly growing](http://www.nature.com/news/programming-pick-up-python-1.16833).
1. The scientific computing environment of Python has many similarities to MATLAB &trade;, which is the historically dominant environment in our field.
1. It is free and open source, and thus we feel will continue to benefit students who move out of a university environment. 

Nevertheless, the main statistical module we use here (`Statsmodels`) is well behind R in its maturity (no wonder, since R is a *lot* older). Thankfully, learning to create and interpret design matrices using `Patsy` formula notation is a skill that transfers easily to R's `glm` routines. 

Note two things:

1. *This is not a programming course*. If you do not have enough experience with programming (or Python) to follow the materials here, seek out an introduction to programming in Python. There are many available for free on the internet.
1. *This is not a basic statistics course*. You should be reasonably familiar with things like t-tests and ANOVA before proceeding.

Where content is erroneous, unclear or buggy, please tell us at our [GitHub repository](https://github.com/tomwallis/glm-intro) 

### Setting up the environment we used

I've exported an `environment.yml` file into this repo. According to [the conda docs](http://conda.pydata.org/docs/using/envs.html), you should be able to recreate our environment for the course using this file. 

> Make a new directory, change to the directory, and copy the environment.yml file into it.

    mkdir stats_course
    cd stats_course
    cp environment.yml

> In the same directory as the environment.yml file, create the new environment:

    conda env create

Too easy!
