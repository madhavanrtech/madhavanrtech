# Conditions

if statements add decision making logic to your code. The if statement is used to match a defined condition to a True or False boolean outcome. So with an if statement we can start to introduce different paths through our code and provide different outcomes depending on our inputs.

In this chapter we look at how we can define if, elif and else statements in our code.

we introduce:

- If statements.
- Else statements.
- Elif statements.

In this section we add some conditional tests, using the if statement. For example, imagine we want to perform some input validation to make sure that the parameters provided are valid values that Amazon Translate will accept.

Equivalence
Sometimes we want to check if two values are equal. We cannot use the = as this is reserved for declaring a variable. To check if two values are equivalent you need to use the == sign.

Where two values are equal this will return a True and where they are not equal it will return False

We can combine this with an if statement. You can test this using the following code in the python interactive environment:

1
2
3
4
>>> SourceLanguageCode = "en"
>>> TargetLanguageCode = "fr"
>>> SourceLanguageCode == TargetLanguageCode
False

Complete the exercise again, but change the SourceLanguageCode to "fr".

Remember to use ctrl + d or exit() to exit from the interactive python session.

Using equivalence could be useful to prevent an error where you try to translate from "en" to "en". We will now use an if statement to demonstrate this.

```
import json

# This uses a json string as an input 
json_string = """
{
    "Input":[
        {
        "Text":"I am learning to code in AWS",
        "SourceLanguageCode":"en",
        "TargetLanguageCode":"fr"
        }
    ]
}
```

json_input = json.loads(json_string) # We use loads as we are loading from a string.

# Defines two variables to store the language code from the input.
SourceLanguageCode = json_input['Input'][0]['SourceLanguageCode']
TargetLanguageCode = json_input['Input'][0]['TargetLanguageCode']

# The if statement checks to see if the language code is the same as the source code
if SourceLanguageCode == TargetLanguageCode:
    print("The SourceLanguageCode is the same as the TargetLanguageCode - stopping")
else:
    print("The Source Language and Target Language codes are different - proceeding")

To run the program, enter the following command in the terminal:

python lab_7_step_1_equivalence.py

This should return:

The Source Language and Target Language codes are different - proceeding

Change the SourceLanguageCode to fr and run the code again.
What python did
The if statement is checking to see if the SourceLanguageCode and TargetLanguageCodes are equivalent or not and returning a True or False value. If the answer is True it will print the message and then exit. If the answer is False then it move onto the else statement.

Operators
When using if statements you will often be using different operators to determine equivalence. Here are some of the operators that python supports

Operator	Meaning
==	is equivalent to
!=	is not equivalent to
>	is greater than
<	is less than
>=	is equal to or greater than
<=	is equal to or less than
