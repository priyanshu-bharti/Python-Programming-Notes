# Python Programming (ITA6017) - Notes

## Module 4 - Strings and RegEx

- [x] ~~Strings and String Methods~~
- [x] ~~Slicing Strings~~
- [ ] Regular Expressions
- [ ] Patterns for matching Password, Emails, and URLs

## Strings and String Methods

- A string is a sequence of characters.
- A character is simply a symbol.
- Python uses unicode encoding.
- That means you can use 😎 emojis too!

```py
string = "This is a centered string"
# Following types of string literals are supported:
# "String"
# 'String'
# '''String'''
# """String"""
# f"{str}" # Allows us to directly use variable named 'str' in the string.

# Operators
string + string2 # Concatenate 2 strings together.
string * 2 # Repeat the string 2 times.

# Length
len(string) # Returns the length of the string

# Searching elements
string.find(sub) # Returns the first occurrence of the specified substring
string.count(sub) # Returns the number of occurrences of the specified substring

# Casing of characters
string.lower() # Returns all lower case characters
string.upper() # Returns all upper case characters
string.title() # Capitalizes each word in a string
string.capitalize() # Capitalizes first letter in the string.

# String Manipulation
string.replace(old, new) # Replaces all occurrences of the specified substring

# Check conditions
string.isalnum() # Contains only alphabetic and numeric characters (not even space).
string.isalpha() # Contains only alphabetic characters
string.isdigit() # Contains only numeric characters
string.islower() # Check if string is lower case
string.isupper() # Check if string is upper case
string.startswith(sub) # Check if string starts with a substring
string.endswith(sub) # Check if string starts with a substring
sub in string # Check if string contains a substring

# Splitting string
string.split(" ") # Returns each substring in a list as separate string

# Store multiple numbers separated by spaces in a list
string = "1 2 3 4 5"
list(map(int, string.split(" ")))

# Finding the ascii value of the character
ord(char)
```

## Slicing Strings

```py
string = "Milwaukee"

#   M   i   l   w   a   u   k   e   e
#   0   1   2   3   4   5   6   7   8
#  -9  -8  -7  -6  -5  -4  -3  -2  -1

string[1:]      # ilwaukee  : start at 1 till the end of string
string[1:5:2]   # iw        : start at 1 till 4 (excluding 5) and skip till the 2nd element
string[1:5:3]   # ia        : start at 1 till 4 (excluding 5) and skip till the 3rd element
string[:3]      # Mil       : start at 0 till 2 (excluding 3)
string[-6:-1:3] # wk        : Start at -6 till -2 (excluding -1) and skip till the 3rd element
string[-5:5]    # a         : Start at -5 till 4 (excluding 5)
string[5:-5]    # Empty     : There are no elements between 5 and 3 since 5 is greater.
string[1:-5]    # ilw       : start from 1 till -4 (excluding -5)
```

## Regular Expressions

```py

```

## Patterns for matching Password, Emails, and URLs

```py

```
