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
list = []                                     # empty list
users = ['val', 'bob', 'mia', 'ron', 'ned']
```

### Accessing Elements
Individual elements in a list are accessed according to their position, called the index. The index of the first element is 0, the index of the second element is 1, and so forth. Negative indices refer to items at the end of the list. To get a particular element, write the name of the list and then the index of the element in square brackets.

```python
first_user = users[0]    # returns the first element
second_user = users[1]   # returns the second element
newest_user = users[-1]  # returns the last element
```

### Modifying Individual Elements
Once you've defined a list, you can change individual elements in the list. You do this by referring to the index of the item you want to modify.

```python
users[0] = 'valerie'
users[-2] = 'ronald'
```

### Adding Elements
You can add elements to the end of a list, or you can insert them into a specific index position.

```python
users.append('amy')
users.append('val')
users.append('bob')
users.append('mia')

users.insert(0, 'joe')  # inserts 'joe' at index 0
users.insert(3, 'bea')  # inserts 'bea' at index 3
```

### Removing Elements
You can remove elements by their position in a list, or by the value of the item. If you remove an item by its value, Python removes only the first item that has that value.

```python
del users[-1]

users.remove('mia')
```

### Popping Elements


## Dictionaries

## Functions

## Loops

## Clases

## Exceptions

## File Input & Output
