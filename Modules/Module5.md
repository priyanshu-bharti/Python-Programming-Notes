# Python Programming (ITA6017) - Notes

## Module 5 - Functions, Exceptions and Packages

- [x] ~~User Defined Functions~~
- [x] ~~Parameter Types~~
- [x] ~~Lambdas~~
- [x] ~~Exception Handling~~

## User Defined Functions

- Function is a group of related statements that performs a specific task.
- It breaks our program into smaller and modular chunks.
- It avoids repetition and makes the code reusable.

```py
def functionName (params) :
  # Statements
  return value
```

## Parameter Types

- **Parameters** are the variables in the definition of a function.
- They exist in the function signature and will be used as variables in the function body.
- **Arguments** are the actual values that were passed to the function when we call it.
- Argument could be an integer, a string, or any object passed during function call.

### Mandatory and Optional Parameters

- Mandatory parameters are always required since they're uninitialized.
- Optional parameters are well, optional as they're initialized.
- You must declare mandatory parameters first and then optional parameters.

```py
def my_func(man1, man2, opt1=0, opt2=''):
    print('man1:', man1) # Mandatory parameter
    print('man2:', man2) # Mandatory parameter
    print('opt1:', opt1) # Optional parameter
    print('opt2:', opt2) # Optional parameter
```

### Positional Arguments & Keyword Arguments

- Positional args assign the value to the parameters in the order specified.
- Keyword arguments takes the name of the parameter and can be specified in any order.
- Positional args must be in the front.

```py
my_func('a', 'b') # Positional arguments
my_func(man2='a', man1='b') # Keyword arguments
```

### Variable length parameters

- We can accept any number of parameters

```py
# Receive arguments as list. (useful when we're dealing with positional arguments)
def my_func(*args):
    print(args)

# Receive arguments as dictionary. (Used when we're dealing with Keyword arguments')
def my_func(**kwargs):
    print(kwargs)
```

## Lambdas

- They're anonymous functions which can be used inside another function call.
- They're generally used when we want to create an inline function.

```py
x = lambda a, b : a + b
print(x(5, 10)) # Outputs 15
```

## Exception Handling

- Python has many built-in exceptions that are raised when your program encounters an error.
- These are runtime errors that are not traced at compile time.
- If these errors aren't fixed, program may crash.
- In Python, problematic code can be placed in a try statement.
- The code that handles the exceptions is written in the except block.
- In some situations, you might want to run a certain block of code if the code block inside try ran without any errors.
- For these cases, you can use the optional else keyword with the try statement.
- There's also a finally statement which is executed whether the exception occurred or not.

```py
try:
    print(2/0)
except:
    print("Exception : You divided by Zero")
else:
    print("If this code executes, there were no exceptions.")
finally:
    print("This statement is always executed whether the exception occurred or not.")
```

## Built-in Errors and Exceptions

- `AttributeError` : 	Raised when attribute assignment or reference fails.
- `EOFError` : 	Raised when the input() function hits end-of-file condition.
- `ImportError` : 	Raised when the imported module is not found.
- `IndexError` : 	Raised when the index of a sequence is out of range.
- `KeyError` : 	Raised when a key is not found in a dictionary.
- `NameError` : 	Raised when a variable is not found in local or global scope.
- `RuntimeError` : 	Raised when an error does not fall under any other category.
- `SyntaxError` : 	Raised by parser when syntax error is encountered.
- `IndentationError` : 	Raised when there is incorrect indentation.
- `TypeError` : 	Raised when a function or operation is applied to an object of incorrect type.
- `ValueError` : 	Raised when a function gets an argument of correct type but improper value.
- `ZeroDivisionError` : 	Raised when the second operand of division or modulo operation is zero.
