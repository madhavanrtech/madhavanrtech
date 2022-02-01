
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
1. [Variables](1_variables.md)
2. [Data Types](2_datatypes.md)
3. [Functions](3_functions.md) - To Do
4. [Arguments & Parameters](4_arguments_parameters.md) - To Do
5. [Inputs](5_Inputs.md) - To Do
6. [Loops](6_Loops.md) - To Do
7. [Conditions](7_Conditions.md) - To Do
8. [Logging](8_Logging.md) - To Do
9. [Errors & Exceptions](9_Errors.md) - To Do
