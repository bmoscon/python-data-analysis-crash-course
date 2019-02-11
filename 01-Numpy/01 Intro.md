# Package Management with Python

Python traditiionally installs it packages at the user level, or system level. This can lead to issues when incompatible packages are installed, with versioning, or other issues when working on different versions of Python. You can create separate python environments using various tools to manage a virtual environment. Popular ones include [pipenv](https://docs.python-guide.org/dev/virtualenvs/), [virtualenv](https://virtualenv.pypa.io/en/latest/) and [anaconda](https://docs.anaconda.com/anaconda/user-guide/getting-started/). I'm going to briefly walk you through using anaconda before we begin.

### Anaconda

You can install anaconda by downloading their installation script from [here](https://www.anaconda.com/distribution/). If you are using macOS you can install it via homebrew as well.

Once anaconda is installed you can create a virtual environment with the following command:

`conda create -n envname python=pythonx.x` where __envname__ is a name of your choice, and __pythonx.x__ is something like python3.7. Given that python 2 is very close to EOL and most major packages have announcemed their plans to imminently stop support for 2.7, I recommend 3.6 or 3.7. 

I'll create my env like so:

`$ conda create -n crashcourse python=3.7`

Once that has completed, anaconda will have created an environment with a few default packages installed and the python version of choice. You'll need to activate the env, which you can do so via the `activate` command.

`$ conda activate crashcourse`

You'll notice that now preceeding the command prompt, conda has inserted the name of the virtual env

`(crashcourse) $`

You can exit the environment with the `deactivate` command. Doing so will change the env to `base` which conda considers the root or base environment. 

### Installing packages

You can install packages in your virtual env with `pip`, `conda` or any of the other package tools python supports. I typically choose `pip` to install, but anaconda does support many packages in their mangagement system.

I've provided a `requirements.txt` file, you can install all the required packages with `pip install -r requirements.txt`

### Starting Jupyter

Once everything has been installed, you can start jupyter

`$ jupyter notebook`

It should open your browser. You can now navigate to the nodebook and begin!

