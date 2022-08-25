# Python tutorial - Data types

After learning how to execute Python files and use the command line, let's move on to real development. We'll start with data types.

Our main goal when developing software, is to manipulate data, for this to happen, we should store it in our program to access it. Python offers multiple data types. 

## Numbers
There are multiple alternatives to store numbers, each of them address a certain need.
* Integer `int()`: positive or negative number, no decimal
* Float `float()`: positive or negative number with decimal
* Complex `complex()`: number with its imaginary part, represented as `a + bj`, `j` being the imaginary part

Lets use them in our Python Command Line Interface (CLI):
```python
# sets the number 2 as integer
>>> int(2)
# 2

# sets the number 2 as float, in this case, adding the decimal number
>>> float(2)
# 2.0

# sets the number 2 as complex, in this case, adding the imaginary part as 0
>>> complex(2)
# 2+0j
```
Python is capable enough off detecting the data type when it's declared. As we mentioned on the first part of the tutorial, the language offers multiple [built-in functions](https://docs.python.org/3/library/functions.html#built-in-functions), we'll use [`type()`](https://docs.python.org/3/library/functions.html#type), this one receives data, and returns it's type.
```python
>>> type(2)
# <class 'int'>

>>> type(2.0)
# <class 'float'>

>>> type(2+0j)
# <class 'complex'>
```

### Operators
We got numbers, are they useful without operations? no. Operators are symbols  (`+`, `-`, `*`, etc.) that carry out computations.
```python
# to add, we use the '+' operator
>>> 2 + 3
# 5
# same for complex numbers
>>> (2 + 3j) + (3 + 5j)
# (5 + 8j)

# to substract, we use the '-' operator
>>> 3 - 2
# 1
# same for negative operations
>>> 2 - 3
# -1

# to multiply, we use the '*' operator
>>> 2 * 3
# 6

# to divide, we use the '/' operator
>>> 8 / 3
# 2.6666666666666666
# in this case it returns a float, but what if we want it as an integer?
>>> 8 // 3
# 2

# to divide and get the remainder, we use the '%' (modulus) operator
>>> 8 % 3
# 2

# to get an exponent, we use the '**' operator
>>> 2 ** 3
# 8
```
There are more operators, but we'll cover them later. These are the basics for numbers.

## Strings
Strings are text, they are represented with _single_ (`''`) or _double_ (`""`) quotes. It needs to start and finish with the same quote that started.
```python
# using single quotes
>>> print('hello')
# hello

# using double quotes
>>> print("hello")
# hello

>>> type('hello')
# <class 'str'>
```

What if we want to use quotes in our text?
```python
# if we type: 'hello, it's my tutorial'
# it raises an error
>>> print('hello, it's my tutorial')
SyntaxError: invalid syntax
```

To address this error, we should be using double and single quotes depending on the needs
```python
# we should be using double quotes if are single quotes in the string
>>> print("hello, it's my tutorial")
# hello, it's my tutorial

# and viceversa
>>> print('hello "stranger"')
# hello "stranger"
```

If we want to use both of them, we got two ways of doing it, using the _escape character_ (`\`) or _triple quotes_ (`'''`)
```python
# the escape caracter ignores the following character, and interprets it as a string
print("we\'d rather use \"triple quotes\" than \"escape character\"")
# we'd rather use "triple quotes" than "escape character"

# the triple quotes are expecting another triple quotes to finish the string
print('''we'd rather use "triple quotes" than "escape character"''')
# we'd rather use "triple quotes" than "escape character"
```

To print a new line use the special character `\n`
```python
>>> print('hello\nhello again')
# hello
# hello again

# the escape character has multiple uses
# \t adds a tab
print('hello\n\thello again')
# hello
# 	hello again

# \\ adds a \
print('printing special character \\')
# printing special character \

# \' adds a '
print('printing special character \'')
# printing special character '

# \" adds a "
print("printing special character \"")
# printing special character "
```

We can also use the triple quotes to manipulate a multiline string
```python
# using triple quotes in a multiline string automatically adds a new line
>>> '''hello,
i'm a multiline
string'''
# "hello,\ni'm a multiline\nstring"
>>> print('''hello,
i'm a multiline
string''')
# hello,
# i'm a multiline
# string
```

### Operators
Same with numbers, we can use operators to manipulate our strings
```python
# to concatenate two strings
print('hello' + ' ' + 'my' + ' ' + 'friend')
# hello my friend
```

Strings are saved as arrays of data, we can access indicating the `index` of the character. If we got a string with the value `'hello'`, it will populate an array as `['h', 'e', 'l', 'l', 'o']`, the index of `h` is `0` and the index of `o` is `4`, with this example, the number of characters is `n = 5`, so the first index is `0` and the last index is `n - 1`.
```python
# to access the index, we should specify it within brackets [index]
>>> 'hello'[0]
# h
>>> 'hello'[2]
# l
>>> 'hello'[4]
# o
```

With the function [`len()`](https://docs.python.org/3/library/functions.html#len) we can pass a string and it'll return an integer with the length of the given string
```python
>>> len('hi, lets print a range of characters')
# 5
```

To access a range of characters in the string we use slicing: `[start_index:stop_index]`, `start_index` indicate in which character we'll start and `stop_index` in which we are going to stop
```python
>>> print('hi, lets print a range of characters'[17:23])
# range

# what if we try negative numbers?
>>> print('hi, lets print a range of characters'[-19:23])
# range
# it will start counting the index from end to beginning

# we can use both as negative indexes
>>> print('hi, lets print a range of characters'[-19:-14])
# range

# if we don't specify a start or stop index, it'll use the first and last index respectively
>>> print('hi, lets print a range of characters'[:2])
# hi
>>> print('hi, lets print a range of characters'[-10:])
# characters
```

The `*` operand is helpful when we want to print multiple times the same string
```python
>>> print(20 * '-')
# --------------------
```

## Boolean
In programming, boolean data is expressed as `True` or `False`. They are based on electricity concepts, if there is electricity we define it as `True`, if there is no electricity we define it as `False`. 
```python
>>> type(True)
# <class 'bool'>
>>> type(False)
# <class 'bool'>
```

They are mostly used to evaluate an `expression`.
```python
# to compare if a value is greater that another one
>>> 10 > 5
# True
>>> 10 < 5
# False
```
If there is _data_, it's defined as `True`, if not, is defined as `False`. Lets use the function [`bool()`](https://docs.python.org/3/library/functions.html#bool) to see its behaivor.
```python
>>> bool(1)
# True
>>> bool(0)
# False
>>> bool('a')
# True
>>> bool('')
# False
```

## Arrays
An array is a collection of multiple values that can store **any** type of data. Before moving forward, we need to define what are `mutable` and `immutable` objects.
* Mutable: values can change
* Immutable: values cannot change

Python has multiple array types:
* List `list()`: mutable, allow duplicates and allows access
* Tuple `tuple()`: immutable, allow duplicates and allows access
* Set `set()`: sorted, doesn't allow duplicates neither access

### List
Lists are arrays that we can modify, set duplicates and access by providing an index, same as strings, starts at `0`. They are defined as `[]`. 
```python
>>> type([])
# <class 'list'>
>>> type([1, 2, 3, 4, 5])
# <class 'list'>

# to access a value we set the index within brackets
>>> [1, 2, 3, 4, 5][2]
# 3

# we can set duplicate values
>>> [1, 2, 3, 4, 5, 5, 6]
# [1, 2, 3, 4, 5, 5, 6]

# same as strings, we can use the ':' operator
>>> [1, 2, 3, 4, 5][:3]
# [1, 2, 3]

# we can also use len()
>>> len([1, 2, 3, 4, 5])
# 5
```

Let's try to store different data types within lists.
```python
>>> type(['hello', 'my', 'friend'])
# <class 'list'>

>>> type(['hello', 'my', 2, 'friends'])
# <class 'list'>

>>> type([int(), float(), complex(), str(), list(), tuple(), set()])
# <class 'list'>

>>> [int(), float(), complex(), str(), list(), tuple(), set()]
# [0, 0.0, 0j, '', [], (), set()]
```
