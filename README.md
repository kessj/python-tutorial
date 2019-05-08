# python-tutorial
This is a repository to give a quick intro to using python

## A Note on Terms
Working in python involves writing code (duh) however there different formats that code can be written in. For the purposes of this tutorial we will classify code as either scripts (files that end with .py) or notebooks (files that end with .ipynb). When working with scripts we will use the [visual studio text editor](https://code.visualstudio.com/) while we will use Jupyter Notebooks to work with notebooks. Often people will bundle scripts together into a python package which can then be reused in other code. For example there is a python package called pandas which performs some of the functions of microsoft excel. This package can be reused in your own code rather than you writing everything from scratch. Packages are stored in your developing environment which is like a toolbox for storing packages. You can have multiple environments with different configurations of packages for working on different kinds of projects. Code and packages can also be stored online in repositories on sites like GitHub. For example you are currently looking a the python-tutorial code repository which is stored at https://github.com/kessj/python-tutorial

## Getting Started

### Working with Anaconda
- Navigate to the [Anaconda website](https://www.anaconda.com/distribution/) and download the anaconda installer appropriate to your operating system.
- Install Anaconda, when it is finished find the "Anaconda Prompt" application.
- Open the Anaconda prompt, note that it should say (Base) to the far left of the terminal cursor line.
- Create a dummy environment using the command `conda create -n dummy_env`
- Now activate that environement with the command `conda activate dummy_env` your activated environment is where anaconda will look to install any packages you download as well as where it will look when you want to use a package
- Use the command `conda env list` to get a list of your environments.
- Use the command `conda list` to get a list of the packages present in your current activated environment.
- Use the command `conda install jupyter numpy pandas seaborn` to install the jupyter, numpy, pandas, and seaborn python packages to your environment.
- Use the command `conda remove pandas` to remove the pandas package from your environment
- Use the command `conda deactivate` to leave your current activated environment and return to the base environment.
- Use the command `conda env remove -n dummy_env` to delete your dummy environment
- Now use the command `conda install git` to install git to your base environment, it is a tool for saving and sharing code


### Using the command line
- The Anaconda prompt is a command line interface. Essentially this is just a different way of interacting with your filesystem that does not require the mouse. Using the command line is a fundamental skill for programming and should not be avoided.
- For now it suffices to note that the `cd` command allows you to change what directory/folder your are looking at in the Anaconda prompt e.g. C would move you to your desktop folder in Windows
- The other important command to know is `dir` (or `ls` if using a linux/mac operating system) which gives a list of the files in the current directory/folder you are looking at
- Now use the `cd` command to navigate to your "Downloads" folder in the Anaconda prompt
- Use the command `git clone https://github.com/kessj/python-tutorial.git` to download this repository (aka "repo")
- Once the repo has finished downloading use the command `cd python-tutorial` to change directories to python-tutorial

### Setting up environment
- At this point you should have the Anaconda prompt open and inside the python-tutorial folder
- Use the command `dir` to see a list of files in that folder, note the environment.yml file
- Open the environment.yml file with your visual studio code application, this will be the template for the creation of your own conda environment with all the packages you need to go through the exercises. Look at the list of packages
- Now back to the command line, use the command `conda env create -f environment.yml` to build an environment from this template.
- Activate this new environment named "tutorial" with `conda activate tutorial` you can now use all the packages inside when you write code

### Writing code
- There are a ton of ways to write code however for the purposes of this tutorial we will only use two:
- 1) With the tutorial environment activated, in the Anaconda prompt run `jupyter notebook` after a couple of seconds a window should pop up. It will show a list of your files and folders, hit the button that says create notebook. Now you are in a jupyter notebook which is a great way to explore using python. In one of the cells type `print("Hello World")` and then hit run cell. You should see the cell print "Hello World" in the output below. 
- 2) In visual studio open a new file, type `print("Hello World")` inside, then save it as "hello_world.py" in your Downloads folder. Next navigate to your Downloads folder using the `cd` command in the Anaconda prompt. Then use the command `python hello_world.py` to run your code in the prompt. You should see it print "Hello World" as the output.
- In the next section we will focus mainly on using Jupyter Notebooks to write and test code

## Example Notebooks
- In the Anaconda prompt activate your tutorial environment and navigate to the python-tutorial directory
- Open up Jupyter Notebooks with `jupyter notebook`
- In Jupyter Notebooks click the "notebooks" folder and then click the "0_intro.ipynb" notebook