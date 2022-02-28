# Errors and Exceptions

Errors are an inevitable part of programming. As Amazon's CTO, Werner Vogels says "Everything fails, all the time". We need a way to manage errors using Exceptions to help us identify and fix errors as well as to make our code more stable and resilient.

```
import logging

integer = 50
string = "The number is"

try:
    print(string + integer)
except TypeError as err:
    logging.warning("Error - {}. You cannot add a string to an integer, without converting the integer to a string first".format(err))

```