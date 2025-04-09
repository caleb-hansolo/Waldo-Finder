# Waldo-Finder

## Initial Setup

This program runs using a python virtual environment running a local version of python 3.11.9 using pyenv.

### Setup Steps

1. Follow the steps to install and create environment variables for pyenv in the [pyenv Github repository](https://github.com/pyenv/pyenv) 
2. Run this command in a terminal window to install Python 3.11.9 with pyenv
```shell
pyenv install 3.11.9
``` 
3. Clone this repository to your machine
4. Navigate to the `Waldo-Finder` directory
5. Set Python 3.11.9 as the local version of Python in this repository using this command (must be executed within the `Waldo-Finder` directory)
```shell
pyenv local 3.11.9
```
Confirm that the local version of Python is 3.11.9 by running the command
```shell
python --version
```
6. Create a Virtual Environment manually using Python's built-in venv module
```shell
python -m venv waldo-finder-env
```
Then activate it
```shell
.\waldo-finder-env\Scripts\activate
```
7. Next, upgrade pip and install the necessary libraries (tensorflow)
```shell
pip install --upgrade pip
pip install tensorflow
```

### Troubleshooting

Some Windows users may experience trouble when installing tensorflow because of too-long nested directories. 

1. Press `Windows + R`
2. Type: `regedit` and press Enter
3. Navigate to:
```
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\FileSystem
```
4. Look for a key called `LongPathsEnabled`. If it is not there, right click on the right pane --> `New > DWORD (32-bit) Value`, and name it `LongPathsEnabled`. Double click it, and set the value to `1`. Click OK.
5. Restart your machine

After this, you should be able to rerun `pip install tensorflow` without any issues.

### Deactivation
To exit the virtual environment, use the command
```shell
deactivate
```

## Using the Model


