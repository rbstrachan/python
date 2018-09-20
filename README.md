# Beginners Python Cheat Sheet

## Python Syntax [CC]

## Strings & Console Output [CC]

## Conditionals & Control Flow [CC]

## Functions [CC]

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
To access the value associated with an individual key, give the name of the dictionary and then place the key in a set of square brackets. If the key you're asking for is not in the dictionary, an error will occur.  You can also use the `get()` method, which returns `None` instead of an error if the key doesn't exist. You can also specify a default value to use if the key is not in the
dictionary.

```python
alien_0 = {'color': 'green', 'points': 5}

print(alien_0['color'])
print(alien_0['points'])
```
```python
alien_0 = {'color': 'green'}

alien_color = alien_0.get('color')
alien_points = alien_0.get('points', 0)

print(alien_color)
print(alien_points)
```

### Adding New Key-Pair Values
You can store as many key-pair values as you want in a dictionary, until the computer runs out of memory. To add a new key-value pair to an exisiting dictionary, give the name of the dictionary and the new key in square brackets and set it equal to the new value. This also allows you to start with an empty dictionary and add key-value pairs as they become relevant.

#### Adding key-value pairs
```python
alien_0 = {'color': 'green', 'points': 5}

alien_0['x'] = 0
alien_0['y'] = 25
alien_0['speed'] = 1.5
```
##### Adding key-value pairs to an empty dictionary
```python
alien_0 = {}

alien_0['color'] = 'green'
alien_0['points'] = 5
```

## Functions

## Loops

## Clases

## Exceptions

## File Input & Output

## Notes
### Styling Your Code
Styling your code helps with readability. This is especially important in Python. To keep your code neat and tidy, you should;
1. Use four spaces per indentation
1. Keep your lines below 80 characters
1. Use single blank lines to visually seperate individual groups of code
