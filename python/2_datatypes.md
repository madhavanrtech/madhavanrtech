# Data Types

In this section we look at data types. The computer needs to know whether a variable is a string or a number or another type of data. This to prevent mistakes like attempting to add a string "Alice" to a number 5.

## Strings

In python a string, is shortened to str and refers to anything inside quotes. The quotes can be double or single. The examples below are identical to python.

```
"The quick brown fox jumped over the lazy dog"
'The quick brown fox jumped over the lazy dog'
```

Using Variables in Strings
Imagine we want to use the value of a variable in the middle of a string. This can be done a few ways in python.

### .format()
In this method you can use the {} in your string to indicate where the variable should go. Then use .format(variable_name) after the quotation marks. If you have multiple variables, for each variable you use a {}. In the .format() separate each variable with a comma. For example .format(variable_1, variable_2).

Try this in the interactive python. Type or paste each line after the >>>.

```
>>>first_name = "John"
>>>surname = "Doe"
>>>print("My first name is {}. My family name is {}".format(first_name, surname))
```

### f strings

Since python version 3.6 it has been possible to use a format called f-strings to include variables in your strings. Some people find this format easier to read. please try to stick with 3.6 version of formatting as 2.7 is EOL soon.

```
firstname = "Jane"
surname = "Doe"

print(f"My first name is {firstname}. My family name is {surname}")

```

## Numbers

### Integers
An integer is a whole number such as 50. The data type integer is abbreviated to int.

### Floating point numbers
A floating point number is a number followed by a decimal point such as 50.5.

## Dictionaries

A dictionary is a way of storing related information in key-value pairs. It uses a key as an identifier and a value to store the information. For example, the key could be first_name and the value could be Ada.

A dictionary when written in python would look like {"first_name":"Ada"}. A dictionary in python is abbreviated to dict and has the following syntax {"key":"value"}. The key is a string providing an identifier and the value can be the same kind of values you would store in a variable.

Dictionaries are very common in AWS, so you will see them frequently.

They are used to exchange information between different services and functions
They are returned by Application Programming Interfaces (API)
They are used as Tag values


## Lists

A list is an ordered sequence of values separated by spaces. For example:

[0,1,2,3,4]

or

["apples","oranges","bananas"]

A list can contain other objects, for example dictionaries, which we learned about in the last lesson. For example:

[{"fruit_type":"apples"},{"number":50}]

# Determining Type

Sometimes your code will raise a TypeError. These can be frustrating to fix. The first step is often to find out what type of data python thinks the object is.

The way to find out what type of data python has stored in a variable is to use the type() method.

```
>>>my_variable = "A string"
>>>print(type(my_variable))
```

This should return:

```
<class 'str'>

```
