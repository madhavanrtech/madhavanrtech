# Functions

A function is a named section of a program which performs a specific task. Functions add flexibility to code like variables because they are reusable, which reduces the amount of code we have to write.

In python we can declare a function using the syntax `def function_name():`

A function begins with def, has a name in lower case, with words separated by underscores to improve readability, a set of () which contain parameters (more on this later) and ends in :.

Here is a very simple function that when it is called will return hello world

```
# A function that prints hello world
def hello_world():
    print('hello world')

# This line calls (runs) the function
hello_world()

```