# Loops

## A Simple Loop
First we are going to create a simple example in the python interactive environment to show how looping over a list works. The steps are:

Create a list and assign it to a variable
Create a for loop
Print out the items in the list one by one.

```
>>> fruit = ['apples','oranges','bananas']

>>> for item in fruit:
...     print(f'The best fruit now is {item}')

```

If you want to want to use a loop as a counter, you could create a list of numbers and assign it to a variable like this.

numbers = [0,1,2,3,4,5,6,7,8,9,10]

and then run

```
>>> numbers = [0,1,2,3,4,5,6,7,8,9,10]
>>> for number in numbers:
...     print(f'The next number is {number}')
```

Which would print all the numbers from 0 to 10, but what if you wanted to count to 1000. It would be tedious to write all the numbers out in this way.

Instead we use the range() function:

```
>>> for number in range(10):
...     print(f'The next number is {number}')
```

You can see that computers start counting at 0 as the first number, If you want to start counting at 1, you can still use the range() method.

```
>>> for number in range(1,10):
...     print(f'The next number is {number}')
```

If you want to increment the counter by more than the default value of 1, perhaps if you wanted only odd numbers or even numbers for example. To do this you add a third parameter to the range() function as shown below.

```
>>> for number in range(1,10,2):
...     print(f'The next number is {number}')
```

## Looping over JSON

As we looked at in the Inputs section, JSON is a common format used to exchange information between computers, programs, functions and Application Programming Interfaces (APIs). JSON shares lots of similarities with a python dictionary. If you need a reminder of the differences review the Inputs section of the workshop.

In this section, we are going to look at a common use case where our input data is a sequence of dictionaries inside a list. In the first part of this section, you learned how to loop over a list. We can apply the same principle when the list comprises dictionaries.

```
{
    "Input":[
        {
        "Text":"What is cloud computing?",
        "SourceLanguageCode":"en",
        "TargetLanguageCode":"fr"
        },
        {
        "Text":"Cloud computing is the on-demand delivery of IT resources over the Internet with pay-as-you-go pricing.",
        "SourceLanguageCode":"en",
        "TargetLanguageCode":"fr"
        },
        {
        "Text":"Instead of buying, owning, and maintaining physical data centers and servers, you can access technology services, such as computing power, storage, and databases, on an as-needed basis from a cloud provider like Amazon Web Services (AWS)",
        "SourceLanguageCode":"en",
        "TargetLanguageCode":"fr"
        },
        {       
        "Text":"Who is using cloud computing?",
        "SourceLanguageCode":"en",
        "TargetLanguageCode":"fr"
        },
        {       
        "Text":"Organizations of every type, size, and industry are using the cloud for a wide variety of use cases, such as data backup, disaster recovery, email, virtual desktops, software development and testing, big data analytics, and customer-facing web applications.",
        "SourceLanguageCode":"en",
        "TargetLanguageCode":"fr"
        },
        {       
        "Text":"For example, healthcare companies are using the cloud to develop more personalized treatments for patients. Financial services companies are using the cloud to power real-time fraud detection and prevention.",
        "SourceLanguageCode":"en",
        "TargetLanguageCode":"fr"
        },        
        {       
        "Text":"And video game makers are using the cloud to deliver online games to millions of players around the world.",
        "SourceLanguageCode":"en",
        "TargetLanguageCode":"fr"
        }
    ] 
} 

```


```
# Standard Imports
import argparse
import json

# 3rd Party Imports
import boto3 

# Arguments
parser = argparse.ArgumentParser(description="Provides translation  between one source language and another of the same set of languages.")
parser.add_argument(
    '--file',
    dest='filename',
    help="The path to the input file. The file should be valid json",
    required=True)

args = parser.parse_args()

# Functions
def open_input():
    """This function returns a dictionary containing the contents of the Input section in the input file""" 
    with open(args.filename) as file_object:
        contents = json.load(file_object)
    return contents['Input']

# Boto3 function to use Amazon Translate to translate the text and only return the Translated Text
def translate_text(**kwargs): 
    client = boto3.client('translate')
    response = client.translate_text(**kwargs)
    print(response['TranslatedText']) 

# Add a Loop to iterate over the json file.
def translate_loop():
    input_text = open_input()
    for item in input_text: # Here we iterate over all dictionaries in the Input list
        translate_text(**item)

# Main Function - use to call other functions
def main():
    translate_loop()

if __name__ == "__main__":
    main()
```

## List Comprehensions

So far our examples have provided a list of items to iterate over. What if we want to create a new list out of the data provided. For example, maybe we want to generate a list of just the text we want to translate.

You could do this using a built-in python method .append() and a for loop.

```
# Create a list of the input text
def new_input_text_list():
    input_text = open_input()
    new_list = []
    for item in input_text:
        text = item['Text']
        new_list.append(text)
    print(new_list)
```