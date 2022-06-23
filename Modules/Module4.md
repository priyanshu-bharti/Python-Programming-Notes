# Python Programming (ITA6017) - Notes

## Module 4 - Strings and RegEx

- [x] ~~Strings and String Methods~~
- [x] ~~Slicing Strings~~
- [x] ~~Regular Expressions~~
- [x] ~~Patterns for matching Password, Emails, and URLs~~

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

string[1:]        # ilwaukee  : start at 1 till the end of string
string[1:5:2]     # iw        : start at 1 till 4 (excluding 5) and skip till the 2nd element
string[1:5:3]     # ia        : start at 1 till 4 (excluding 5) and skip till the 3rd element
string[:3]        # Mil       : start at 0 till 2 (excluding 3)
string[-6:-1:3]   # wk        : Start at -6 till -2 (excluding -1) and skip till the 3rd element
string[-5:5]      # a         : Start at -5 till 4 (excluding 5)
string[5:-5]      # Empty     : There are no elements between 5 and 3 since 5 is greater.
string[1:-5]      # ilw       : start from 1 till -4 (excluding -5)
```

## Regular Expressions

- Used for matching patterns in a string.
- Python has inbuilt `re` package for it.

### Regex Cheatsheet
- `"[abc]"` : Matches abc
- `"[^abc]"` : Matches anything except abc
- `"[a-z]"` : Matches lowercase alphabets
- `"[A-Z]"` : Matches uppercase alphabets
- `"[0-9]"` : Matches digits
- `"[]"` : Search for things mentioned inside the brackets.
- `"[]?"` : Occurs 0 or 1 time.
- `"[]+"` : Occurs at least once.
- `"[]*"` : May or may not occur even once.
- `"[]{start, end}"` : Occurs start to end times. (end might be empty).
- `"\d"` : digits
- `"\D"` : anything but digits
- `"\w"` : characters and digits
- `"\W"` : anything but characters and digits
- `"\s"` : Spaces
- `*` : Match 0+
- `+` : Match 1+
- `?` : Match exactly 0 or 1
- `^` : Beginning of line
- `$` : End of line
- `<` : Left word boundary
- `>` : Right word boundary
- `\B` : Not a word boundary

### Patterns for matching Password, Emails, and URLs

```py
import re

pattern = "[\w\d]+@[\w]+\.[\w]{2,3}" # Check for email
# Emails contains 1 or more characters which could be alphabets (\w) or numbers(\d).
# Then they have @ (at) symbol followed by the domain name which again contains alphabets
# Then there is the period symbol (.) followed by the domain name consisting of 2-3 characters max.

pattern = "^(?=.*\d)(?=.*[A-Z])(?=.*[a-z])(?=.*[^\w\d\s])([^\s]){8,}$" # Check for password
# This checks that the password is at least 8 characters long {8,}
# It has digits               : (?=.*\d)
# It has Lowercase characters : (?=.*[a-z])
# It has Uppercase Characters : (?=.*[A-Z])
# It has Special Characters   : (?=.*[^\w\d\s])
# Doesn't have spaces         : ([^\s])
# Has min length of 8         : {8,}
# Checks within boundary      : ^ ...  $

pattern = "((\w+:\/\/)[\w\D]+)" # Check for url
# protocol consisting of words and '://' part  : (\w+:\/\/)
# Then match any characters

print("valid" if re.search(pattern, input()) else "invalid")
```
