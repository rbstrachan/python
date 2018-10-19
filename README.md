# [Beginners Python Crash Course - Cheat Sheet](https://ehmatthes.github.io/pcc/cheatsheets/README.html)

## Contents
- [Python Syntax](#)
- [Strings & Console Output](#)
- [Conditional Tests](#conditional-tests)
  - [Checking For Equality](#checking-for-equality)
    - [String Comparisons](#string-comparisons)
    - [Numerical Comparison](#numerical-comparison)
  - [Checking For Inequality](#checking-for-inequality)
    - [String Comparison](#string-comparison)
    - [Numerical Comparison](#numerical-comparison-1)
  - [Comparison Operators](#comparison-operators)
  - [Checking Multiple Conditions](#checking-multiple-conditions)
    - [Using `and`](#using-and-to-check-multiple-conditions)
    - [Using `or`](#using-or-to-check-multiple-conditions)
  - [Boolean Values](#boolean-values)
  - [Ignoring Case](#ignoring-case)
- [Functions](#functions)
  - [Defining A Function](#defining-a-function)
  - [Passing Information To A Function](#passing-information-to-a-function)
  - [Positional & Keyword Arguments](#positional--keyword-arguments)
    - [Using Positional Arguments](#using-positional-arguments)
    - [Using Keyword Arguments](#using-keyword-arguments)
  - [Default Values](#default-values)
    - [Using A Default Value](#using-a-default-value)
    - [Using `None`](#using-none-to-make-an-argument-optional)
  - [Return Values](#return-values)
    - [Returning A Single Value](#returning-a-single-value)
    - [Returning A Dictionary](#returning-a-dictionary)
    - [Returning A Dictionary (With Optional Values)](#returning-a-dictionary-with-optional-values)
  - [Passing A List To A Function](#passing-a-list-to-a-function)
    - [Passing A List As An Argument](#passing-a-list-as-an-argument)
    - [Allowing A Function To Modify A List](#allowing-a-function-to-modify-a-list)
    - [Preventing A Function From Modifying A List](#preventing-a-function-from-modifying-a-list)
  - [Passing An Arbitrary Number Of Arguments](#passing-an-arbitrary-number-of-arguments)
    - [Collecting An Arbitrary Number Of Arguments](#collecting-an-arbitrary-number-of-arguments)
    - [Collecting An Arbitrary Number Of Keyword Arguments](#collecting-an-arbitrary-number-of-keyword-arguments)
  - [Modules](#modules)
    - [Storing A Function In A Module](#storing-a-function-in-a-module)
    - [Importing An Entire Module](#importing-an-entire-module)
    - [Importing A Specific Function](#importing-a-specific-function)
    - [Giving A Module An Alias](#giving-a-module-an-alias)
    - [Giving A Function An Alias](#giving-a-function-an-alias)
    - [Importing All Functions From A Module](#importing-all-functions-from-a-module)
- [Lists](#lists)
  - [Defining A List](#defining-a-list)
  - [Accessing Elements](#Accessing-Elements)
  - [Modifying Individual Elements](#modifying-individual-elements)
  - [Adding Elements](#adding-elements)
    - [Using `.append()`](#adding-elements-to-the-end-of-a-list-using-append)
    - [Using `.insert()`](#inserting-elements-at-particular-positions-using-insert)
  - [Removing Elements](#removing-elements)
    - [Using `del`](#deleting-elements-by-index-position-using-del)
    - [Using `.remove()`](#removing-elements-by-value-using-remove)
  - [Popping Elements](#popping-elements)
  - [List Length](#list-length)
  - [Sorting A List](#sorting-a-list)
    - [Using `.sort()`](#permanently-sorting-a-list-using-sort)
    - [Using `sorted()`](#temporarily-sorting-a-list-using-sorted)
    - [Using `.reverse()`](#reversing-the-order-of-a-list-using-reverse)
  - [Looping Through A List](#looping-through-a-list)
  - [Slicing A List](#slicing-a-list)
  - [Copying A List](#copying-a-list)
  - [List Comprehension](#list-comprehensions)
    - [Generating A List Of Square Numbers](#generating-a-list-of-square-numbers)
      - [Using For Loop Method](#using-for-loop-method)
      - [Using List Comprehension Method](#using-list-comprehension-method)
    - [Converting A List to Uppercase](#converting-a-list-to-uppercase)
      - [Using For Loop Method](#using-for-loop-method-1)
      - [Using List Comprehension Method](#using-list-comprehension-method-1)
- [Tuples](#tuples)
  - [Defining A Tuple](#defining-a-tuple)
  - [Looping Through A Tuple](#looping-through-a-tuple)
  - [Overwriting A Tuple](#overwriting-a-tuple)
- [Dictionaries](#dictionaries)
  - [Defining A Dictionary](#defining-a-dictionary)
  - [Accessing Values](#accessing-values)
    - [Directly](#accessing-key-values-directly)
    - [Using `.get()`](#accessing-key-values-using-get)
  - [Adding New Key-Pair Values](#adding-new-key-pair-values)
  - [Modifying Values](#modifying-values)
  - [Removing Key-Pair Values](#removing-key-value-pairs)
  - [Looping Through A Dictionary](#looping-through-a-dictionary)
    - [Looping Through All Key-Value Pairs](#looping-through-all-key-value-pairs)
    - [Looping Through All Keys](#looping-through-all-keys)
    - [Looping Through All Values](#looping-through-all-values)
    - [Looping Through All Keys (In Order)](#looping-through-all-the-keys-in-order)
  - [Dictionary Length](#dictionary-length)
  - [Nesting Dictionaries Inside Lists](#nesting-dictionaries-inside-lists)
    - [Using `.append()`](#nesting-dictionaries-using-append)
    - [Directly](#nesting-dictionaries-directly)
  - [Nesting Lists Inside Dictionaries](#nesting-lists-inside-dictionaries)
  - [Nesting Dictionaries Inside Dictionaries](#nesting-dictionaries-inside-dictionaries)
  - [Using OrderedDict](#using-ordereddict)
  - [Generating Dictionaries Using For Loops](#generating-dictionaries-using-for-loops)
- [If Statements](#if-statements)
  - [If Statement](#if-statement)
  - [If-Else Statement](#if-else-statement)
  - [If-Elif-Else Chain](#if-elif-else-chain)
- [While Loops](#while-loops)
  - [Using A While Loop To Count](#using-a-while-loop-to-count)
  - [Letting The User Choose When To Quit](#letting-the-user-choose-when-to-quit)
  - [Using A Flag](#using-a-flag)
  - [Using `break` To Exit A Loop](#using-break-to-exit-a-loop)
  - [Using `continue` In A Loop](#using-continue-in-a-loop)
  - [Avoiding Infinite Loops](#avoiding-infinite-loops)
    - [Example Of An Infinite Loop](#example-of-an-infinite-loop)
  - [Removing All Instances Of A Value From A List](#removing-all-instances-of-a-value-from-a-list)
- [Classes](#classes)
  - [Creating Classes](#creating-classes)
    - [Creating The `Car()` Class](#creating-the-car-class)
    - [Creating An Object From A Class](#creating-an-object-from-a-class)
    - [Accessing Attribute Values](#accessing-attribute-values)
    - [Calling Methods](#calling-methods)
    - [Creating Multiple Objects](#creating-multiple-objects)
  - [Modifying Attributes](#modifying-attributes)
    - [Modifying An Attribute Directly](#modifying-an-attribute-directly)
    - [Writing A Method To Update An Attributes Value](#writing-a-method-to-update-an-attributes-value)
    - [Writing A Method To Increment An Attributes Value](#writing-a-method-to-increment-an-attributes-value)
  - [Class Inheritance](#class-inheritance)
    - [Using The `__init()__` Method](#using-the-init-method)
    - [Adding New Methods To The Child Class](#adding-new-methods-to-the-child-class)
    - [Using Child And Parent Methods](#using-child-and-parent-methods)
    - [Overriding Parent Methods](#overriding-parent-methods)
  - [Instances As Attributes](#instances-as-attributes)
    - [Creating The `Battery()` Class](#creating-the-battery-class)
    - [Using An Instance As An Attribute](#using-an-instance-as-an-attribute)
    - [Using The Instance](#using-the-instance)
  - [Importing Classes](#importing-classes)
    - [Storing Classes In A File](#storing-classes-in-a-file)
    - [Importing Individual Classes From A Module](#importing-individual-classes-from-a-module)
    - [Importing An Entire Module](#importing-an-entire-module-1)
    - [Importing All Classes From A Module](#importing-all-classes-from-a-module)
  - [Storing Objects In A List](#storing-objects-in-a-list)
- [Exceptions](#exceptions)
- [File Import & Export](#file-import--export)

## Python Syntax

## Strings & Console Output [CC]

## Conditional Tests
A conditional test is an expression that can be evaluated as `True` or `False`. Python uses the values `True` and `False` to decide whether the code in an `if` statement or `while` loop should be executed.

### Checking For Equality
##### String comparisons
```python
>>> car = "bmw"
>>> car == "bmw"
True
```
```python
>>> car = "audi"
>>> car == "bmw"
False
```

##### Numerical comparison
```python
>>> age = 18
>>> age == 18
True
```

### Checking For Inequality
##### String comparison
```python
>>> topping = "chicken"
>>> topping != "sweetcorn"
True
```

##### Numerical comparison
```python
>>> age = 18
>>> age != 18
False
```

### Comparison Operators
```python
>>> age = 19
>>> age < 21
True
>>> age <= 21
True
>>> age > 21
False
>>> age >= 21
False
```

### Checking Multiple Conditions
You can check multiple conditions at the same time. The `and` operator returns `True` if all the conditions listed are `True`. The `or` operator returns `True` if any condition is `True`.

##### Using `and` to check multiple conditions
```python
>>> age_0 = 22
>>> age_1 = 18
>>> age_0 >= 21 and age_1 >= 21
False
>>> age_1 = 23
>>> age_0 >= 21 and age_1 >= 21
True
```

##### Using `or` to check multiple conditions
```python
>>> age_0 = 22
>>> age_1 = 18
>>> age_0 >= 21 or age_1 >= 21
True
>>> age_0 = 18
>>> age_0 >= 21 or age_1 >= 21
False
```

### Boolean Values
A boolean value is either `True` or `False`. Variables with boolean values are often used to keep track of certain conditions within a program.

```python
game_active = True
can_edit = False
```

### Ignoring Case
```python
>>> car = "Audi"
>>> car.lower() == "audi"
True
```

## Functions
Functions are named blocks of code designed to do one specific job. Functions allow you to write code once that can then be run whenever you need to accomplish the same task. Functions can take in the information they need, and return the information they
generate. Using functions effectively makes your programs easier to write, read, test, and fix.

### Defining A Function
The first line of a function is its definition, marked with the keyword `def`. The name of the function is followed by a set of parentheses and a colon. A docstring, in triple quotes, describes what the function does. The body of a function is indented one level. To call a function, give the name of the function followed by a set of parentheses.

```python
def greet_user():    # defines the function greet_user()
  print("Hello!")
  
greet_user()         # calls the function greet_user()
```

### Passing Information To A Function
Information that's passed to a function is called an argument; information that's received by a function is called a parameter. Arguments are included in parentheses after the function's name, and parameters are listed in
parentheses in the function's definition.

```python
def greet_user(username):
  print("Hello, " + username + "!")
  
greet_user('jesse')
greet_user('diana')
greet_user('brandon')
```

### Positional & Keyword Arguments
The two main kinds of arguments are positional and keyword arguments. When you use positional arguments Python matches the first argument in the function call with the first parameter in the function definition, and so forth. With keyword arguments, you specify which parameter each argument should be assigned to in the function call. When you use keyword arguments, the order of the
arguments doesn't matter.

##### Using positional arguments
```python
def describe_pet(animal, name):
  print("\nI have a " + animal + ".")
  print("Its name is " + name + ".")
  
describe_pet('hamster', 'harry')
describe_pet('dog', 'willie')
```

##### Using keyword arguments
```python
def describe_pet(animal, name):
  print("\nI have a " + animal + ".")
  print("Its name is " + name + ".")
  
describe_pet(animal='hamster', name='harry')
describe_pet(name='willie', animal='dog')
```

### Default Values
You can provide a default value for a parameter. When function calls omit this argument the default value will be used. Parameters with default values must be listed after parameters without default values in the function's definition so positional arguments can still work correctly.

##### Using a default value
```python
def describe_pet(name, animal='dog'):
  print("\nI have a " + animal + ".")
  print("Its name is " + name + ".")
  
describe_pet('harry', 'hamster')
describe_pet('willie')
```

##### Using `None` to make an argument optional
```python
def describe_pet(animal, name=None):
  print("\nI have a " + animal + ".")
  if name:
    print("Its name is " + name + ".")
    
describe_pet('hamster', 'harry')
describe_pet('snake')
```

### Return Values
A function can return a value or a set of values. When a function returns a value, the calling line must privide a variable in which to store the return value. A function stops running when it reaches a return statement.

##### Returning a single value
```python
def get_full_name(first, last):
  full_name = first + ' ' + last
  return full_name.title()
 
musician = get_full_name('jimi', 'hendrix')
print(musician)
```

##### Returning a dictionary
```python
def build_person(first, last):
  person = {'first': first, 'last': last}
  return person
 
musician = build_person('jimi', 'hendrix')
print(musician)
```

##### Returning a dictionary with optional values
```python
def build_person(first, last, age=None):
  person = {'first': first, 'last': last}
  if age:
    person['age'] = age
  return person
  
musician = build_person('jimi', 'hendrix', 27)
print(musician)

musician = build_person('janis', 'joplin')
print(musician)
```

### Passing A List To A Function
You can pass a list as an argument to a function, and the function can work with the values in the list. Any changes the function makes to the list will affect the original list. You can prevent a function from modifying a list by passing a copy of the list as an argument.

##### Passing a list as an argument
```python
def greet_users(names):
  for name in names:
    msg = "Hello, " + name + "!"
    print(msg)

usernames = ['hannah', 'ty', 'margot']
greet_users(usernames)
```

##### Allowing a function to modify a list
###### The following example sends a list of models to a function forprinting. The original list is emptied, and the second list is filled.
```python
def print_models(unprinted, printed):
  while unprinted:
    current_model = unprinted.pop()
    print("Printing " + current_model)
    printed.append(current_model)

# Store some unprinted designs, and print each of them.
unprinted = ['phone case', 'pendant', 'ring']
printed = []
print_models(unprinted, printed)

print("\nUnprinted:", unprinted)
print("Printed:", printed)
```

##### Preventing a function from modifying a list
###### The following example is the same as the previous one, except the original list is unchanged after calling `print_models()`.
```python
def print_models(unprinted, printed):
  while unprinted:
    current_model = unprinted.pop()
    print("Printing " + current_model)
    printed.append(current_model)

# Store some unprinted designs, and print each of them.
original = ['phone case', 'pendant', 'ring']
printed = []
print_models(original[:], printed)

print("\nOriginal:", original)
print("Printed:", printed)
```

### Passing An Arbitrary Number Of Arguments
Sometimes you won't know how many arguments a function will need to accept. Python allows you to collect an arbitrary number of arguments into one parameter using the * operator. A parameter that accepts an arbitrary number of arguments must come last in the function definition. The ** operator allows a parameter to collect an arbitrary
number of keyword arguments.

##### Collecting an arbitrary number of arguments
```python
def make_pizza(size, *toppings):
  print("\nMaking a " + size + " pizza.")
  print("Toppings:")
  for topping in toppings:
    print("- " + topping)

# Make three pizzas with different toppings.
make_pizza('small', 'pepperoni')
make_pizza('large', 'bacon bits', 'pineapple')
make_pizza('medium', 'mushrooms', 'peppers', 'onions', 'extra cheese')
```

##### Collecting an arbitrary number of keyword arguments
```python
def build_profile(first, last, **user_info):
  # Build a dict with the required keys.
  profile = {'first': first, 'last': last}
  
  # Add any other keys and values.
  for key, value in user_info.items():
    profile[key] = value
 
  return profile
  
# Create two users with different kinds of information.
user_0 = build_profile('albert', 'einstein', location='princeton')
user_1 = build_profile('marie', 'curie', location='paris', field='chemistry')

print(user_0)
print(user_1)
```

### Modules
You can store your functions in a separate file called a module, and then import the functions you need into the file containing your main program. This allows for cleaner program files. (Make sure your module is stored in the same directory as your main program.)

##### Storing a function in a module
```python
def make_pizza(size, *toppings):
  print("\nMaking a " + size + " pizza.")
  print("Toppings:")
  for topping in toppings:
    print("- " + topping)
```

##### Importing an entire module
```python
import pizza

pizza.make_pizza('medium', 'pepperoni')
pizza.make_pizza('small', 'bacon', 'pineapple')
```

##### Importing a specific function
```python
from pizza import make_pizza

make_pizza('medium', 'pepperoni')
make_pizza('small', 'bacon', 'pineapple')
```

##### Giving a module an alias
```python
import pizza as p

p.make_pizza('medium', 'pepperoni')
p.make_pizza('small', 'bacon', 'pineapple')
```

##### Giving a function an alias
```python
from pizza import make_pizza as mp

mp('medium', 'pepperoni')
mp('small', 'bacon', 'pineapple')
```

##### Importing all functions from a module
```python
from pizza import *

make_pizza('medium', 'pepperoni')
make_pizza('small', 'bacon', 'pineapple')
```

## Lists
A list stores a series of items in a particular order. Lists allow you to store sets of information in one place, whether you have just a few items or millions of items. Lists are one of Python's most powerful features readily accessible to new programmers, and
they tie together many important concepts in programming.

### Defining A List
Use square brackets to define a list, and use commas to separate individual items in the list. Use plural names for lists, to make your code easier to read. 

```python
things = []
users = ['val', 'bob', 'mia', 'ron', 'ned']
```

### Accessing Elements
Individual elements in a list are accessed according to their position, called the index. The index of the first element is 0, the index of the second element is 1, and so forth. Negative indices refer to items at the end of the list. To get a particular element, write the name of the list and then the index of the element in square brackets.

```python
users = ['val', 'bob', 'mia', 'ron', 'ned']

first_user = users[0]             # returns the first element
second_user = users[1]            # returns the second element
newest_user = users[-1]           # returns the last element
second_newest_user = users[-2]    # returns the penultimate element
```

### Modifying Individual Elements
Once you've defined a list, you can change individual elements in the list. You do this by referring to the index of the item you want to modify.

```python
users = ['val', 'bob', 'mia', 'ron', 'ned']

users[0] = 'valerie'
users[-2] = 'ronald'
```

### Adding Elements
You can add elements to the end of a list, or you can insert them into a specific index position.

##### Adding elements to the end of a list using `.append()`
```python
users = ['ron']

users.append('amy')
users.append('val')
users.append('bob')
users.append('mia')
```

##### Inserting elements at particular positions using `.insert()`
```python
users = ['val', 'bob', 'mia', 'ron', 'ned']

users.insert(0, 'joe')  
users.insert(3, 'bea')
```

### Removing Elements
You can remove elements by their position in a list, or by the value of the item. If you remove an item by its value, Python removes only the first item that has that value.

##### Deleting elements by index position using `del`
```python
users = ['val', 'bob', 'mia', 'ron', 'ned']

del users[0]    # deletes first element
del users[3]    # deletes element at index position 3
del users[-1]   # deletes last element
```

##### Removing elements by value using `.remove()`
```python
users = ['val', 'bob', 'mia', 'ron', 'ned']

users.remove('mia')   # removes lowest index list item with value 'mia'
```

### Popping Elements
If you want to work with an element that you're removing from the list, you can "pop" the element. If you think of the list as a stack of items, `pop()` takes an item off the top of the stack. By default `pop()` returns the last element in the list, but you can also pop elements from any position in the list.

```python
users = ['val', 'bob', 'mia', 'ron', 'ned']

most_recent_user = users.pop()    # returns last element of list
print(most_recent_user)

first_user = users.pop(0)         # returns first list element
print(first_user)
```

### List Length
The `len()` function returns the number of items in a list.

```python
num_users = len(users)
print("We have " + str(num_users) + " users.")
```

### Sorting A List
The `sort()` method changes the order of a list permanently. The `sorted()` function returns a copy of the list, leaving the
original list unchanged. You can sort the items in a list in alphabetical order, or reverse alphabetical order. You can
also reverse the original order of the list. Keep in mind that lowercase and uppercase letters may affect the sort order.

##### Permanently sorting a list using `.sort()`
```python
users.sort()                # permanently sorts list in alphabetical order
users.sort(reverse=True)    # permanently sorts list in reverse alphabetical order
```

##### Temporarily sorting a list using `sorted()`
```python
user_sort = sorted(users)                          # temporarily sorts list in alphabetical order
user_sort_reverse = sorted(users, reverse=True)    # temporarily sorts list in reverse alphabetial order
```

##### Reversing the order of a list using `.reverse()`
```python
users.reverse()    # reverses order of list
```

### Looping Through A List
Lists can contain millions of items, so Python provides an efficient way to loop through all the items in a list. When
you set up a loop, Python pulls each item from the list one at a time and stores it in a temporary variable, which you
provide a name for. This name should be the singular version of the list name. The indented block of code makes up the body of the
loop, where you can work with each individual item. Any lines that are not indented run after the loop is completed.

```python
for user in users:
  print(user)   # prints each item of list
```
```python
for user in users:
  print("Welcome, " + user + "!")               # prints message after each item in list

print("Welcome, we're glad to see you all.")    # prints message after all items of list are printed
```

### Slicing A List
You can work with any set of elements from a list. A portion of a list is called a slice. To slice a list, start with the index of the first item you want, then add a colon and the index of the last item you want, plus one. If an initial index value is not specified, the slice will be started at the beginning of the list. If a final index value is not specified, slice will end at the end of the list.

```python
finishers = ['kai', 'abe', 'ada', 'gus', 'zoe']

first_three = finishers[:3]      # returns first three list items
middle_three = finishers[1:4]    # returns list items in index positions 1, 2 and 3
last_three = finishers[-3:]      # returns last three list items
```

### Copying A List
To copy a list, you must make a slice that starts with the first item and ends with the last. Failure to do this will result in unintended changes to the original list.

```python
finishers = ['kai', 'abe', 'ada', 'gus', 'zoe']

finishers_copy = finishers[:]    # creates a seperate copy of the list
```

### List Comprehensions
You can use a loop to generate a list based on a range of numbers or on another list. This is a common operation, so Python offers a more efficient way to do it. List comprehensions may look complicated at first; if so, use the for loop approach until you're ready to start using comprehensions. To write a comprehension, define an expression for the values you want to store in the list. Then write a for loop to generate input values needed to make the list.

##### Generating a list of square numbers
###### Using `for` loop method
```python
squares = []

for x in range(1,11):       # iterates from 1 to 10
  square = x**2
  squares.append(square)    # appends the value of 'square' onto list each iteration
```

###### Using list comprehension method
```
squares = [x**2 for x in range(1,11)]    # generates a list of the first ten square numbers
```

##### Converting a list to uppercase
###### Using `for` loop method
```python
names = ['kai', 'abe', 'ada', 'gus', 'zoe']

upper_names = []
for name in names:
  upper_names.append(name.upper())    # appends items converted to upper case from list 'names'
```

###### Using list comprehension method
```python
upper_names = [name.upper() for name in names]    # generates list of items converted to uppercase from list 'names'
```

## Tuples
A tuple is like a list, except you can't change the values in a tuple once it's defined. Tuples are good for storing information that doesn't change for the entirety of the program. Tuples are designated by parenthesis instead of square brackets. Information in tuples can be overridden completely, however, individual elements cannot be changed.

### Defining A Tuple
```python
dimensions = (800,600)
```

### Looping Through A Tuple
```python
for dimension in dimensions:
  print(dimension)
```

### Overwriting A Tuple
```python
dimensions = (800,600)
print(dimensions)

dimensions = (1200,900)
```

## Dictionaries
Python's dictionaries allow you to connect pieces of related information. Each piece of information in a dictionary is stored as a key-value pair. When you provide a key, Python returns the value associated with that key. You can loop through all the key-value
pairs, all the keys, or all the values.

### Defining A Dictionary
Use curly braces to define a dictionary. Use colons to connect keys and values, and use commas to separate individual key-value pairs.

```python
alien_0 = {'color': 'green', 'points': 5}
alien_1 = {'color': 'purple', 'points': 3}
alien_X = {'color': 'invisible', 'points': 'unknown'}
```

### Accessing Values
To access the value associated with an individual key, give the name of the dictionary and then place the key in a set of square brackets. If the key you're asking for is not in the dictionary, an error will occur.  You can also use the `.get()` method, which returns `None` instead of an error if the key doesn't exist. You can also specify a default value to use if the key is not in the
dictionary.

##### Accessing key values directly
```python
alien_0 = {'color': 'green', 'points': 5}

print(alien_0['color'])
print(alien_0['points'])
```

##### Accessing key values using `.get()`
```python
alien_0 = {'color': 'green'}

alien_color = alien_0.get('color')
alien_points = alien_0.get('points', 0)    # The second argument of the `.get()` function is the default value.

print(alien_color)
print(alien_points)
```

### Adding New Key-Pair Values
You can store as many key-pair values as you want in a dictionary, until the computer runs out of memory. To add a new key-value pair to an exisiting dictionary, give the name of the dictionary and the new key in square brackets and set it equal to the new value. This also allows you to start with an empty dictionary and add key-value pairs as they become relevant.

```python
alien_0 = {'color': 'green', 'points': 5}

alien_0['x'] = 0
alien_0['y'] = 25
alien_0['speed'] = 1.5
```
```python
alien_0 = {}

alien_0['color'] = 'green'
alien_0['points'] = 5
```

### Modifying Values
You can modify the value associated with any key in a dictionary. To do so, give the name of the dictionary and anclose the key in square brackets, then preovide the new value for that key.

```python
alien_0 = {'color': 'green', 'points': 5}

alien_0['color'] = 'yellow'
alien_0['points'] = 10
```

### Removing Key-Value Pairs
You can remove any key-value pair you want from a dictionary. To do so, use the `del` keyword and the dictionary name, followed by the key in square brackets. This will delete the key and its associated value.

```python
alien_0 = {'color': 'green', 'points': 5}

del alien_0['color']
del alien_0['points']
```

### Looping Through A Dictionary
You can loop through a dictionary in three ways, you can loop through all the key-value pairs, all the keys, or all the values. A dictionary only tracks the connections between keys and values; it doesn't track the order of items in the dictionary. If you want to process the information in order, you can sort the keys in your loop.

##### Looping through all key-value pairs
```python
# Store people's favorite languages.
fav_languages = {
  'jen': 'python',
  'sarah': 'c',
  'edward': 'ruby',
  'phil': 'python',
}

# Show each person's favorite language.
for name, language in fav_languages.items():
  print(name + ": " + language)
```

##### Looping through all keys
```python
# Store people's favorite languages.
fav_languages = {
  'jen': 'python',
  'sarah': 'c',
  'edward': 'ruby',
  'phil': 'python',
}

# Show everyone who's taken the survey.
for name in fav_languages.keys():
  print(name)
```

##### Looping through all values
```python
# Store people's favorite languages.
fav_languages = {
  'jen': 'python',
  'sarah': 'c',
  'edward': 'ruby',
  'phil': 'python',
}

# Show all the languages that have been chosen.
for language in fav_languages.values():
  print(language)
```

##### Looping through all the keys in order
```python
# Store people's favorite languages.
fav_languages = {
  'jen': 'python',
  'sarah': 'c',
  'edward': 'ruby',
  'phil': 'python',
}

# Show each person's favorite language, in order by the person's name.
for name in sorted(fav_languages.keys()):
  print(name + ": " + language)
```

### Dictionary Length
You can find the number of key-value pairs in a dictionary using the `len()` function.

```python
# Store people's favorite languages.
fav_languages = {
  'jen': 'python',
  'sarah': 'c',
  'edward': 'ruby',
  'phil': 'python',
}

num_responses = len(fav_languages)
```

### Nesting Dictionaries Inside Lists
It's sometimes useful to store a set of dictionaries in a list; this is called nesting.

##### Nesting dictionaries using `.append()`
```python
# Start with an empty list.
users = []

# Make a new user, and add them to the list.
new_user = {
  'last': 'fermi',
  'first': 'enrico',
  'username': 'efermi',
}
users.append(new_user)

# Make another new user, and add them as well.
new_user = {
  'last': 'curie',
  'first': 'marie',
  'username': 'mcurie',
}
users.append(new_user)

# Show all information about each user.
for user_dict in users:
  for k, v in user_dict.items():
  print(k + ": " + v)
  print("\n")
```

##### Nesting dictionaries directly
```python
# Define a list of users, where each user is represented by a dictionary.
users = [
  {
    'last': 'fermi',
    'first': 'enrico',
    'username': 'efermi',
  },
  {
    'last': 'curie',
    'first': 'marie',
    'username': 'mcurie',
  },
]

# Show all information about each user.
for user_dict in users:
 for k, v in user_dict.items():
 print(k + ": " + v)
 print("\n")
```

### Nesting Lists Inside Dictionaries
Storing a list inside a dictionary allowys you to associate more than one value with each key.

```python
# Store multiple languages for each person.
fav_languages = {
  'jen': ['python', 'ruby'],
  'sarah': ['c'],
  'edward': ['ruby', 'go'],
  'phil': ['python', 'haskell'],
}
# Show all responses for each person.
for name, langs in fav_languages.items():
  print(name + ": ")
  for lang in langs:
  print("- " + lang)
```

### Nesting Dictionaries Inside Dictionaries
You can store a dictionary inside another dictionary. In this case each value associates with a ket is itself a dictionary.

```python
users = {
    'aeinstein': {
    'first': 'albert',
    'last': 'einstein',
    'location': 'princeton',
  },
    'mcurie': {
    'first': 'marie',
    'last': 'curie',
    'location': 'paris',
  },
}

for username, user_dict in users.items():
  print("\nUsername: " + username)
  full_name = user_dict['first'] + " "
  full_name += user_dict['last']
  location = user_dict['location']
 
  print("\tFull name: " + full_name.title())
  print("\tLocation: " + location.title())
```

### Using OrderedDict
Standard Python dictionaries don't keep track of the order in which keys and values are added; they only preserve the
association between each key and its value. If you want to preserve the order in which keys and values are added, use
an OrderedDict.

```python
from collections import OrderedDict

# Store each person's languages, keeping track of who respoded first.
fav_languages = OrderedDict()

fav_languages['jen'] = ['python', 'ruby']
fav_languages['sarah'] = ['c']
fav_languages['edward'] = ['ruby', 'go']
fav_languages['phil'] = ['python', 'haskell']

# Display the results, in the same order they were entered.
for name, langs in fav_languages.items():
  print(name + ":")
  for lang in langs:
    print("- " + lang)
```

### Generating Dictionaries Using For Loops
You can use a loop to generate a large number of dictionaries efficiently, if all the dictionaries start out with similar data.

```python
aliens = []

# Make a million green aliens, worth 5 points each. Have them all start in one row.
for alien_num in range(1000000):
  new_alien = {}
  new_alien['color'] = 'green'
  new_alien['points'] = 5
  new_alien['x'] = 20 * alien_num
  new_alien['y'] = 0
  aliens.append(new_alien)

# Prove the list contains a million aliens.
num_aliens = len(aliens)

print("Number of aliens created: " + num_aliens)
```

## If Statements
`If` statements allow you to examine the current state of a program and respond apporopriately to that state. You can write a simple `if` statement that checks one condition, or you can create a complex series of if statements that identify the exact conditions you are looking for. Several kinds of if statements exist. Your choice of which to use depends on the number of conditions you need to test. You can have as many elif blocks as you need, and the else block is always optional.

### If Statement
```python
age = 19

if age >= 18:
  print("You are old enough to vote.")
```

### If-Else Statement
```python
age = 19

if age >= 18:
  print("You are old enough to vote.")
else:
  print("You can't vote yet.")
```

### If-Elif-Else Chain
```python
age = 19

if age < 5:
  price = 0
elif age < 18:
  price = 5
else:
  price = 10
  
print("Your cost is £" + str(price) + ".")
```

## While Loops
A while loop repeats a block of code as long as a condition is `True`.

### Using A While Loop To Count
```python
current_number = 1

while current_number <= 5:
  print(current_number)
  current_number += 1
```

### Letting The User Choose when To Quit
```python
prompt = "\nTell me something, and I'll "
prompt += "repeat it back to you."
prompt += "\nEnter 'quit' to end the program. "

message = ""
while message != "quit":
  message = input(prompt)
  if message != "quit":
    print(message)
```

### Using A Flag
```python
prompt = "\nTell me something, and I'll "
prompt += "repeat it back to you."
prompt += "\nEnter 'quit' to end the program. "

active = True
while active:
  message = input(prompt)
  if message == "quit":
    active = False
  else:
    print(message)
```

### Using `break` To Exit A Loop
```python
prompt = "\nWhat cities have you visited?"
prompt += "\nEnter 'quit' when you're done. "

while True:
  city = imput(prompt)
  if city == "quit":
    break
  else:
    print("I've been to " + city + "!")
```

### Using `continue` In A Loop
```python
banned_users = ['eve', 'fred', 'gary', 'helen']

prompt = "\nAdd a player to your team."
prompt += "\nEnter 'quit' when you're done. "

players = []
while True:
  player = input(prompt)
  if player == 'quit':
    break
  elif player in banned_users:
    print(player + " is banned!")
    continue
  else:
    players.append(player)
```

### Avoiding Infinite Loops
Every `while` loop needs a way to stop running so it doesn't continue to run forever. If there is now way for the condition to become `False`, the loop with never stop running.

##### Example Of An Infinite Loop 
```python
while True:
  name = input("\nWho are you? ")
  print("Nice to meet you, " + name + "!")
```

### Removing All Instances of A Value From A List
The `.remove()` method removes a specific value from a list, however it only removes the first instance of the value provided. You can use a while loop to remove all instances of a particular value.

```python
pets = ['dog', 'cat', 'dog', 'fish', 'cat', 'rabbit', 'cat']

print(pets)

while 'cat' in pets:
  pets.remove('cat')

print(pets)
```

## Classes
Classes are the foundation of object-oriented programming. Classes represent real-world things you want to model in your programs: for example dogs, cars, and robots. You use a class to make objects, which are specific instances of dogs, cars, and robots. A class defines the general behavior that a whole category of objects can have, and the information that can be associated with those objects. Classes can inherit from each other – you can write a class that extends the functionality of an
existing class. This allows you to code efficiently for a wide variety of situations.

### Creating Classes
Consider how we might model a car. What information would we associate with a car, and what behavior would it have? The information is stored in variables called attributes, and the behavior is represented by functions. Functions that are part of a class are called methods.

##### Creating the `Car()` class
```python
class Car():
  def __init__(self, make, model, year):
    self.make = make
    self.model = model
    self.year = year

    # Fuel capacity and level in gallons.
    self.fuel_capacity = 15
    self.fuel_level = 0

  def fill_tank(self):
    self.fuel_level = self.fuel_capacity
    print("Fuel tank is full.")

  def drive(self):
    print("The car is moving.")
```

##### Creating an object from a class
```python
my_car = Car('audi', 'a4', 2016)
```

##### Accessing attribute values
```python
print(my_car.make)
print(my_car.model)
print(my_car.year)
```

##### Calling methods
```python
my_car.fill_tank()
my_car.drive()
```

##### Creating multiple objects
```python
my_car = Car('audi', 'a4', 2016)
my_old_car = Car('subaru', 'outback', 2013)
my_truck = Car('toyota', 'tacoma', 2010)
```

### Modifying Attributes
You can modify an attribute's value directly, or you can write methods that manage updating values more carefully.

##### Modifying an attribute directly
```python
my_new_car = Car('audi', 'a4', 2016)
my_new_car.fuel_level = 5
```

##### Writing a method to update an attribute's value
```python
def update_fuel_level(self, new_level):
  if new_level <= self.fuel_capacity:
    self.fuel_level = new_level
  else:
    print("The tank can't hold that much!")
```

##### Writing a method to increment an attribute's value
```python
def add_fuel(self, amount):
  if (self.fuel_level + amount <= self.fuel_capacity):
    self.fuel_level += amount
    print("Added fuel.")
  else:
    print("The tank won't hold that much.")
```

### Class Inheritance
If the class you're writing is a specialized version of another class, you can use inheritance. When one class inherits from another, it automatically takes on all the attributes and methods of the parent class. The child class is free to introduce new attributes and methods, and override attributes and methods of the parent class. To inherit from another class, include the name of the parent class in parentheses when defining the new class.

##### Using the `__init__()` method
```python
class ElectricCar(Car):
  def __init__(self, make, model, year):
    super().__init__(make, model, year)
    
    # Attributes specific to electric cars. Battery capacity in kWh.
    self.battery_size = 70
    
    # Charge level in %.
    self.charge_level = 0
```

##### Adding new methods to the child class
```python
class ElectricCar(Car):
  --snip--
  def charge(self):
    self.charge_level = 100
    print("The vehicle is fully charged.")
```

##### Using child and parent methods
```python
my_ecar = ElectricCar('tesla', 'model s', 2016)

my_ecar.charge()
my_ecar.drive()
```

##### Overriding parent methods
```python
class ElectricCar(Car):
  --snip--
  def fill_tank(self):
    print("This car has no fuel tank!")
```

### Instances As Attributes
A class can have objects as attributes. This allows classes to work together to model complex situations.

##### Creating the `Battery()` class
```python
class Battery():
  def __init__(self, size=70):
    # Capacity in kWh, charge level in %.
    self.size = size
    self.charge_level = 0
 
  def get_range(self):
    if self.size == 70:
      return 240
    elif self.size == 85:
      return 270
```

##### Using an instance as an attribute
```python
class ElectricCar(Car):
  --snip--
  def __init__(self, make, model, year):
    super().__init__(make, model, year)
 
    # Attribute specific to electric cars.
    self.battery = Battery()
 
  def charge(self):
    self.battery.charge_level = 100
    print("The vehicle is fully charged.")
```

##### Using the instance
```python
my_ecar =  ElectricCar('tesla', 'model x', 2016)

my_ecar.charge()
print(my_ecar.battery.get_range())
my_ecar.drive()
```

### Importing Classes
Class files can get long as you add detailed information and functionality. To help keep your program files unclutttered, you can store your classes in modules and import the classes you need into your main program.

##### Storing classes in a file
```python
class Car():
  --snip--

class Battery():
  --snip--

class ElectricCar(Car):
  --snip--
```

##### Importing individual classes from a module
```python
from car import Car, ElectricCar

my_beetle = Car('volkswagen', 'beetle', 2016)
my_beetle.fill_tank()
my_beetle.drive()

my_tesla = ElectricCar('tesla', 'model s', 2016)
my_tesla.charge()
my_tesla.drive()
```

##### Importing an entire module
```python
import car

my_beetle = car.Car('volkswagen', 'beetle', 2016)
my_beetle.fill_tank()
my_beetle.drive()

my_tesla = car.ElectricCar('tesla', 'model s', 2016)
my_tesla.charge()
my_tesla.drive()
```

##### Importing all classes from a module
```python
from car import *

my_beetle = Car('volkswagen', 'beetle', 2016)
```

### Storing Objects In A List
A list can hold as many items as you want, so you can make a large number of objects from a class and store them in a list. Here's an example showing how to make a fleet of rental cars, and make sure all the cars are ready to drive.

```python
from car import Car, ElectricCar

# Make lists to hold a fleet of cars.
gas_fleet = []
electric_fleet = []

# Make 500 gas cars and 250 electric cars.
for _ in range(500):
  car = Car('ford', 'focus', 2016)
  gas_fleet.append(car)
for _ in range(250):
  ecar = ElectricCar('nissan', 'leaf', 2016)
  electric_fleet.append(ecar)

# Fill the gas cars, and charge electric cars.
for car in gas_fleet:
  car.fill_tank()
for ecar in electric_fleet:
  ecar.charge()

print("Gas cars:", len(gas_fleet))
print("Electric cars:", len(electric_fleet))
```

## Exceptions

## File Import & Export

## Notes
### Styling Your Code
Styling your code helps with readability. This is especially important in Python. To keep your code neat and tidy, you should;
1. Use four spaces per indentation
1. Keep your lines below 80 characters
1. Use single blank lines to visually seperate individual groups of code

### Naming Conventions
In Python, class names are written in CamelCase and object names are written in lowercase with underscores. Modules that contain classes should still be named in lowercase with underscores.
