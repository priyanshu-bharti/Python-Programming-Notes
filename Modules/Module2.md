# Python Programming (ITA6017) - Notes

## Module 2 - Python Operators, Expressions, Flow control

- [x] ~~Operators~~
- [x] ~~if else and elif~~
- [x] ~~Loops~~
- [x] continue and pass

## Operators

- **Arithmetic** : `+`, `-`, `*`, `/`, `%`, `//`, `**`.
- **Comparison** : `<`, `>`, `==`, `!=`, `>=`, `<=`.
- **Logical** : `and`, `or`, `not`.
- **Bitwise** : `&`, `|`, `~`, `>>`, `<<`.
- **Assignment** : `=`, `+=`, `-=`, `*=`, `/=`, `%=`, `//=`, `**=`, `&=`, `|=`, `^=`, `>>=`, `<<=`.
- **Identity** : `is`, `is not`.
- **Membership** : `in`, `not in`.

## if else and elif

```py
if condition :
  # Statement
elif condition : 
  # Statement
else :
  # Statement
```

## Loops

```py
# For Loop

for i in range(count) : 
  # Statement


# For Each Loop

for i in collection :
  # Statement


# For Else Loop

for i in range(count) :
  # Statement
else :
  # Executed if the loop completes successfully, 
  # not when if break is encountered.


# While Loops

while condition :
  # Statement


# While else loop

while condition :
  # Statement
else : 
  # Executed if the loop completes successfully, 
  # not when if break is encountered.
```

## continue and pass

- `continue` : Skips the current iteration of the loop
- `pass` : Executes nothing (used to declare empty block)

```py
for i in range(count):
  if i == k :
    continue # Skip the iteration when i equals k
  print(i)

while condition :
  pass # Doesn't do anything
```
