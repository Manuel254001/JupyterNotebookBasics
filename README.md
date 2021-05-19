# An introduction to Jupyter Notebooks

## Basic Python configuration
First, ensure that python3 is installed by running
```
python3 --version
```
If installed correctly, it should display the version number, and look similar
to this.
```
Python 3.6.4
```

### Creating a Virtual Environment
The next thing is to create a python virtual environment. This is an important
step because different projects may require libraries with different versions,
and it can be a nightmare to manage this you install all of your libraries
globally. To remedy this, we create python virtual environments. This is
essentially a local installation of all library packages that you may need to
use, and you create one for each project. I usually name all of my virtual
environments venv and store them in the top most folder of the project.

To create a virtual environment use the command
```
python3 -m venv <path/to/environment>
```

This command creates a virtual environment named venv in the current directory.
```
python3 -m venv venv
```

### Activating and Deactivating a virtual Enviroment
Once you create your virtual environment, you need to let the bash interpreter
know that you want to use that environment instead of the global one. You can
do this with the source command.
```
source venv/bin/activate
```
Notice that after activating your venv, it will show up on your command prompt.
```
(venv) zekes-mbp:jupyterIntro zeke$
```

You can exit the virtual env at any time using the command `deactivate` on its own.

### Installing Library Packages
In order to install packages, you must have your venv activated. pip is the
most common python package manager and makes life pretty easy. To install a new
library package, simply use the command `pip install <package name>`. Example
for pandas:
```
pip install pandas
```

for juptyer:
```
pip install jupyterlab
```

You can also install multiple libraries at once using a txt file with the
libraries listed. These are often called requirements.txt.
```
pip install -r requirements.txt
```

## Running a Jupyter Notebook
Now that you have activated your venv and installed jupyter, simply run the
command `jupyter notebook` and your jupyter server will start running and
automatically open a browser!
