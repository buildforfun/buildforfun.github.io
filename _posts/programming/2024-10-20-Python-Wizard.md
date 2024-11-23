---
layout: post
title:  "Python wizard"
categories: [ programming]
date:   2024-10-20 11:00:00
---

- [Python wizard 🧙🏽‍♂️](#python-wizard-️)
  - [Basics](#basics)
  - [Data Structures](#data-structures)
  - [Controlling flow of code](#controlling-flow-of-code)
  - [Functions](#functions)
  - [Object-Oriented Programming](#object-oriented-programming)
  - [Testing](#testing)
  - [Debugging](#debugging)
  - [Miscellaneous](#miscellaneous)

# Python wizard 🧙🏽‍♂️
## Basics
TODO:
- Variables
- Operators
- Boolean
- Strings
- Module

## Data Structures
Python offers several built-in data structures:

**Lists**
Ordered, mutable sequences:
```python
fruits = ["apple", "banana", "cherry"]
fruits.append("date")
print(fruits[1])  # Output: banana
```
**Dictionaries**
Key-value pairs:
```python
person = {"name": "John", "age": 30}
print(person["name"])  # Output: John
```

## Controlling flow of code
- Conditionals
- List comprehensions
- Loops
- Exceptions

```python
if x > 0:
    print("Positive")
elif x < 0:
    print("Negative")
else:
    print("Zero")

for i in range(5):
    print(i)

while x > 0:
    x -= 1
```

Error Handling
Python uses try-except blocks for error handling:

```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")
except ValueError:
    print("Value is wrong")
```
## Functions
TODO:
- writing proper functions
- keyword arguments
- variable number of arguments
- return values
- scope
- recursion

## Object-Oriented Programming
Python supports object-oriented programming through classes:

What is a class?

```python
class Dog:
    def __init__(self, name):
        self.name = name

    def bark(self):
        return f"{self.name}"
```
What is an object?
In Python, everything is an object. An object is a specific instance of a class that contains data and code.

```python
my_dog = Dog("Max")
print(my_dog.bark())
```

Object oriented programming is based on these main principles:
1. Encapsulation:
  - Putting funcs that affect a data into one class. This limits exposure of some of it's components.
  - Controlled access to internal state

2. Inheritance:
- Allows classes to inherit variables and funcs from another class. Usually the child class (new class) needs to initialise both it's own class and the parent class. 
- Method overriding: allows the child class to override existing functions in the parent class with it's own funcs.
- Eg. Dog and Cat would inherit from Animal class and you could override a function on how each speak fromt he base class. 

1. Polymorphism: 
- Allows objects of different classes to be treated as objects of a common base class.
- Think of a USB port - it can be used for different things but it's still one port - one interface. This one interface principle is polymorphism. 
- When multiple classes inherit from the base class and have the has a common function, this creates a common interface. 
- The child classes can also modify the function to do something different, but there is still a common interface as it has the same name. 
- The class that runs the common interface classes doesn't need to know what specific behaviour is happening - it just calls the function name that's common in all classes.

Benefits of OOP:
- modularity - objects are self contained
- resuability - inheritance and polymophism
- extensibility - easier to add new classes

## Testing
A unit tests allows us to test one specific part of a code repositry. We want to check if specific funcitons output expected values.

Unit testing in python
The most popular unittest module in python is the unittest module.

1. Import unittest
2. Write class of test in file: subclasses of the unittest.TestCase class
   ```python
   class Test_ClassName(unittest.TestCase):
   ```
3. Set up function
   ```python
   class Test_ClassName(unittest.TestCase):
      def test_name(self):
         class_ob = Class()
         self.assertEqual(class_ob.func_name(), expected value, "error")
   ```
4. Run command:
    - ```python3 -m unittest discover test/```


## Debugging
- Python has it's own terminal debugger called PDB. You need to import pdb and add pdb.set_trace() like you would a breakpoint.

## Miscellaneous
- Don't Repeat Yourself (DRY)
- You Ain’t Gonna Need It (YAGNI)
- Separation of concerns (SoC) - break a program into multiple functions
- Avoid unnecessary comments that explain what the code does. Comments are for explaining 'why' rather than 'what'
- Use good variable names
- Don't compare booleans to 'True/False'
- Write docstrings + follow conventions for docstrings
- Use single quotes for strings
- Use absolute imports instead of relative imports
- Use readme file to thoroughly document your code
- Python focusses on readability and simplicity.
- Use meaningful variable and function names.
- Write docstrings for functions and classes.
- Utilise virtual environments for project isolation.
- static analysis is sometimes useful - pylint, flake8, pycodestyle

