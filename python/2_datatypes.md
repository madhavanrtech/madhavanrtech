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

## Integers
An integer is a whole number such as 50. The data type integer is abbreviated to int.

## Floating point numbers
A floating point number is a number followed by a decimal point such as 50.5.