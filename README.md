# Beginners Python Cheat Sheet

## Contents
1. Python Syntax
1. Strings & Console Output
1. Conditionals & Control Flow
1. Functions
1. [Lists](#lists)
  1. [Defining A List](#defining-a-list)
  1. [Accessing Elements](#Accessing-Elements)
  1. [Modifying Individual Elements](#modifying-individual-elements)
  1. [Adding Elements](#adding-elements)
    1. [Using `.append()`](#adding-elements-to-the-end-of-a-list-using--.append()-)
    1. [Using `.insert()`](#inserting-elements-at-particular-positions-using--.insert()-)
  1. Removing Elements
    1. Using `del`
    1. Using `.remove()`
  1. Popping Elements
  1. List Length
  1. Sorting A List
    1. Using `.sort()`
    1. Using `sorted()`
    1. Using `.reverse()`
  1. Looping Through A List
  1. Slicing A List
  1. Copying A List
  1. List Comprehension
    1. Generating A List Of Square Numbers
      1. Using For Loop Method
      1. Using List Comprehension Method
    1. Converting A List to Uppercase
      1. Using For Loop Methos
      1. Using List Comprehension Method
1. Tuples
  1. Defining A Tuple
  1. Looping Through A Tuple
  1. Overwriting A Tuple
1. Dictionaries
  1. Defining A Dictionary
  1. Accessing Values
    1. Directly
    1. Using `.get()`
  1. Adding New Key-Pair Values
  1. Modifying Values
  1. Removing Key-Pair Values
  1. Looping Through A Dictionary
    1. Looping Through All Key-Value Pairs
    1. Looping Through All Keys
    1. Looping Through All Values
    1. Looping Through All Keys (In Order)
  1. Dictionary Length
  1. Nesting Dictionaries Inside Lists
    1. Using `.append()
    1. Directly`
  1. Nesting Lists Inside Dictionaries
  1. Nesting Dictionaries Inside Dictionaries
  1. Using OrderedDict
  1. Generating Dictionaries Using For Loops
1. If Statements
1. While Loops
1. Classes
1. Exceptions
1. File Import & Export

## Python Syntax [CC]

## Strings & Console Output [CC]

## Conditionals & Control Flow [CC]

## Functions

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
```
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

## While Loops

## Classes

## Exceptions

## File Import & Export

## Notes
### Styling Your Code
Styling your code helps with readability. This is especially important in Python. To keep your code neat and tidy, you should;
1. Use four spaces per indentation
1. Keep your lines below 80 characters
1. Use single blank lines to visually seperate individual groups of code
