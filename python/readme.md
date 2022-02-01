
# Create a Workspace.
```
mkdir -p ~/workspace/mraj
```

please change `mraj` to the name you would want it to be

# Clone code from Git

```
git clone git@github.com:madhavanrtech/madhavanrtech.git
```
Following this command you should see a folder `madhavanrtech` in ~/workspace/mraj path

# Creation of Virtual Environment

A virtual environment in python is a container in which all your code and other python packages reside. It allows you to keep your python configuration separate from other versions on your system. It is a good idea to always use a virtual environment when developing python code.

You can choose a name for your virtual environment such as my_environment, but often you see a virtual environment called venv.

To create a virtual environment we will use the command:

```
cd madhavanrtech
python3 -m venv venvironment
```

Once the virtual environment has been created, you need to activate it. Once activated, your code runs inside the environment, including any packages you install. To activate the environment use one of the following commands:

## Activating 

```
source venvironment/bin/activate
```

## Deactivating

```
deactivate
```

# Table of Contents
1. [Variables](#variables)
2. [Data Types](#datatypes)
