## Python Programming (ITA6017) - Notes

## Module 6 - Numpy and Pandas

- [x] ~~Pandas~~
- [x] ~~Numpy~~

## Pandas

```py
# Import Pandas
import pandas as pd

mylist = [1, 2, 3, 4, 5]

# Creating a data frame using only a list
df = pd.DataFrame(mylist)


# Creating a list and labeling the Rows
df = pd.DataFrame(mylist, index=["a", "b", "c", "d", "e"])


# Creating a dataframe and also adding column name
df = pd.DataFrame(mylist, index=["a", "b", "c", "d", "e"], columns=["Integers"])


# Using zip()
names = ["John", "Finn", "Cody", "Kenny"]
rating = [5, 4, 5, 4]

df = pd.DataFrame(list(zip(names, rating)), columns=['Wrestlers', 'Rating'])


# Using Multi-dimensional List
mylist = [
    ['Tom', 23],
    ['Jon', 43],
    ['Tim', 63],
    ['Vic', 33]
]

df = pd.DataFrame(mylist, columns=['Name', 'Age'])


# Using a dictionary
mydict = {
    'Name': ['UFC', 'WWE', 'NXT', 'AEW'],
    'Roster': ['89', '78', '32', '128'],
    'Year': ['2002', '1970', '2012', '2019']
}

df = pd.DataFrame(mydict)

```

## Numpy

```py
# Creating an array usi
import numpy as np
l1 = [1, 2, 3, 4, 5]
a = np.array(l1)
print(a)


# Creating numpy array using tuple
t1 = (5, 6, 7, 8, 9)
b = np.array(t1)
print(b)


# Create a 2 dimensional array
d = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
print(d)


# Multi-dimensional array using tuple
e = np.array(((11, 12), (13, 14)))
print(e)


# Shape of the array
print(a.shape)
print(b.shape)
print(d.shape)


# Getting the dimension of the multi-dimension
print(e.ndim)


# Fill the array with Zeroes and Ones
c1 = np.zeros((2, 3))  # 2 Rows, 3 Columns
d1 = np.ones((4, 5))  # 4 Rows, 5 Columns

print(c1)
print(d1)


# Fill the matrix with value of certain type
c2 = np.zeros((2, 3), dtype=int)
print(c2)


# Fill the matrix with value of certain type
c3 = np.full((3, 3), 6, dtype=float)
print(c3)


# scalar operations
a = np.array([1, 2, 3, 4, 5, 6, 7, 8])

print(a)
print(a+10)
print(a*2)
print(a-5)


# arithmetic operations
A = np.array([[1, 2], [3, 4]])
B = np.array([[5, 6], [7, 8]])

print(np.add(A, B))
print(np.subtract(A, B))
print(np.multiply(A, B))
print(np.dot(A, B))


# Reshape and Flatten
C = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15])
r = np.reshape(C, (3, 5))

print(r)
print(r.flatten())


# eigen values of a matrix
from numpy import linalg as linal

g = linal.eigvals([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
print(g)


# Transpose
c = a.transpose()
print(c)


# Determinant of matrix
n = np.array([[50, 29], [30, 44]])
det = linal.det(n)
print(det)
```