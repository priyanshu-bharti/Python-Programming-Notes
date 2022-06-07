# Python Programming (ITA6017) - Notes

## Module 3 - Python List, Tuples, Dictionaries & Sets

- [x] ~~Sequenced Type Methods and Operations~~
- [x] ~~List~~
- [x] ~~List Methods~~
- [x] ~~Tuple~~
- [x] ~~Tuple Methods~~
- [x] ~~Dict~~
- [x] ~~Dict Methods~~
- [x] ~~Set~~
- [x] ~~Set Methods~~
- [x] ~~Comprehensions~~

## Sequenced Type Methods and Operations

- Indexing : `(sequence[index])`
- Slicing : `(sequence[start : end : step])`
- Concatenating : `+`
- Multiplying : `*`
- Checking Membership : `in` or `not in`
- Iterating : `for i in x:`
- Length of the sequence : `len(sequence)`
- Minimum Element : `min(sequence)`
- Maximum Element : `max(sequence)`
- Sum of elements : `sum(sequence)`
- Sorting the sequence : `sorted(sequence)`
- Count the occurence of an item : `sequence.count(item)`
- Return the index of an Item : `sequence.index(item)`

## List

- General Purpose Data Structure
- Most used data structure
- Dynamic Sizing
- Sequenced Type
- Sortable

## List Methods

```py
x = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
y = [11, 12, 13, 14, 15, 16, 17, 18, 19, 20]

# List methods

(x[1:4])  # Sublist from index 1 to 4
(x[1:6:2])  # Sublist from index 1 to 6 but with step = 2
(x[3:])  # Print all items from index 3 to the end
(x[:5])  # Print all items till the index 5
(x[-1])  # Return the last item
(x[-3:])  # Return last 3 items
(x[:-2])  # Return all items except the last 2
x + y  # Concatenate the Lists
a = [1, 2, 3] * 3  # Gives [1,2,3,1,2,3,1,2,3]
4 in a  # False
2 in a  # True
len(x)  # Number of items
min(x)  # Minimum item
max(x)  # Maximum item
sum(x)  # Sum of all items
sorted(x)  # Sorted list in ascending order
x.count(2)  # Number of occurences of 2 in the list
x.append(11)  # Add 11 to the end of the list
x.clear()  # Remove all the elements from the list
x.extend(y)  # add y to the end of the list x
x.index(4)  # Returns the 1st occurence of the value 4
x.insert(1, 2)  # Inserts 2 before the index 1
x.pop()  # removes the last element
x.remove(4)  # Removes the first occurence of the value 4
x.reverse()  # Reverses the list (Returns nothing)
x.sort()  # Sorts the list (Returns nothing)
del(x[2]) # Delete the 3rd item in the list
del(x) # Delete the entire list
p, q, r = a  # Unpack elements into variables (# of var = len(list))

for i in x:
    print(i)  # Gives access to all the items in a list

for i, item in enumerate(x):
    print(i, item)  # Gives access to index as well as the items
```

## Tuple

- Immutable
- Useful for fixed data
- Faster than lists
- Sequenced Type

## Tuple Methods

```py
x = (1, 2, 3, 4, 5, 6, 7, 8, 9, 10)
y = (11, 12, 13, 14, 15, 16, 17, 18, 19, 20)

# Tuple Methods

x = ()  # Empty Tuple
x = (1, 2, 3)  # A normal Tuple
x = 1, 2, 3  # Tuple without the parenthesis
x = 2, # Single Item Tuple
tuple(x) # Tuple from list or set
(x[1:4])  # Sublist from index 1 to 4
(x[1:6:2])  # Sublist from index 1 to 6 but with step = 2
(x[3:])  # Print all items from index 3 to the end
(x[:5])  # Print all items till the index 5
(x[-1])  # Return the last item
(x[-3:])  # Return last 3 items
(x[:-2])  # Return all items except the last 2
x + y  # Concatenate the tuples
a = (1, 2, 3) * 3  # Gives [1,2,3,1,2,3,1,2,3]
4 in a  # False
2 in a  # True
len(x)  # Number of items
min(x)  # Minimum item
max(x)  # Maximum item
sum(x)  # Sum of all items
sorted(x)  # Sorted list in ascending order
x.count(2)  # Number of occurences of 2 in the list
x.index(4)  # Returns the 1st occurence of the value 4

for i in x:
    print(i)  # Gives access to all the items in a list

for i, item in enumerate(x):
    print(i, item)  # Gives access to index as well as the items

```

## Dict

- Key Value Pairs
- Like Hashmaps (Associative Arrays)
- Unordered

## Dict Methods

```py
x = {}  # Empty dictionary
x = {
    'a': 1,
    'b': 2,
    'c': 3,
    'd': 4
}

# Dict Methods

x.clear()  # Clear the dictionary
x = dict.fromkeys([1, 2, 3], 0)  # Creates a dict {1: 0, 2: 0, 3: 0}
x.get(2)  # Get the value at the specified key else you get 'none'.
x.keys()  # Returns a list of keys in x
x.values  # Returns a list of values in x
x.items()  # Returns a list of key,value pairs in x

for key in x:
    print(key, x[key])

for key, value in x.items():
    print(key, value)

```

## Set

- Store unique items
- Very fast compared to lists
- Enables Mathematical Set Operations like union, intersection etc.
- Unordered

## Set Methods

```py
x = {3, 4, 5, 6}  # Create a set
y = {6, 4, 8, 9}  # Create a set

# Methods

x = set() # Empty Set
x = set(x) # Create set using list or a tuple
x.add(1) # Add 1 to the set
x.clear() # Clear the set
x.difference(y) # Set Difference x - y
x.difference_update(y) # Remove the difference between x and y from x
x.discard(item) # Remove the item from the set if it exists, else don't do anything
x.intersection(y) # Set Intersection x & y
x.intersection_update(y) # Perform the intersection and remove non common items
x.isdisjoint(y) # return True if the intersection is null
x.issubset(y) # return True if the set x exists inside y
x.issuperset(y) # return True if the set x contains y
print(x.symmetric_difference(y)) # Return the items that are unique to both sets
print(x.symmetric_difference_update(y)) # Remove the items that are not common to both sets.
x.union(y) # Return the union of the two sets

# Operations using Operators

x & y # Intersection
x | y # Union
x ^ y # Set Difference
x - y # In set x but not in set y
x >= y # x is a superset of y
x <= y # x is the subset of y
```

## Comprehensions

- Comprehensions allows us to create list in a concise manner.
- It makes assigning values easier and readable.
- Following are some examples where comment shows the tasks to be performed
- Following the comments are the comprehensions
- Note : in the examples, `zip()` methods performs 1:1 mapping between the elements of 2 lists.

```py
# List Comprehensions

# I want n for each n within a range of start to end.
mylist = [n for n in range(start, end)]

# I want n^2 for each n within a range of start to end.
mylist = [n**2 for n in range(start, end)]

# I want n for each n in another list Suppose anotherList = ['a', 'e', 'i', 'o', 'u']
mylist = [n for n in anotherList]

# I want n for each n within a range where n should also be even.
mylist = [n for n in range(start, end) if n%2 == 0]

# I want a [letter, num] pair for each letter in 'abcd' and for num in '1234'
mylist = [[letter, num] for letter in 'abcd' for num in '1234']


# Dictionary Comprehensions

# I want dict{num, letters} for each num, letters in zip(nums, letters).
# Assume nums = [1,2,3,4] and letters = ['a','b','c','d']
mydict = {num: letter for num, letter in zip(nums, letters)}


# Set Comprehensions

# I want n for each n*2 in list [1,1,2,2,3,3,4,4,5,5] in a set
myset = {n*2 for n in list}

```
