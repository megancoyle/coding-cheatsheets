# Python: Overview
Python is a high-level programming language created by Guido van Rossum in 1991. Whitespace matters in Python, and Python uses a syntax that allows programmers to use fewer lines of code. Everything in Python is an object (variables, functions, code).

## Bytes and Byte Arrays
Used for converting strings

## Conditionals
Uses if, elif, and else  statements

## Constructor Method
Constructor method is defined with `def __init__`

## Decorators
Decorators are special functions that return other functions and are used to modify the way that a function works - they're often used as accessor functions.

## Dictionaries
A dictionary is a set of key value pairs. All keys in a dictionary must be unique.

A dictionary can be created two different ways:

```python
  dictionary = { 'a':1, 'b':2, 'c':3, 'd':'phrase'}

  dictionary = dict(a = 1, b = 2, c 3)
```

## Generators
A generator object is an object that can be used in the context of an iterator. It uses the yield keyword, which means the first time the function is called, it will execute all the code, then the next time it's called, it will pick up where the yield is.

## Immutable and Mutable Objects
* Mutable objects may change value, immutable objects may not.
* Most fundamental types in Python are immutable (numbers, strings, tuples)
* Mutable objects include lists, dictionaries, and other objects depending on how they're implemented

## Lists
Lists are declared the following way:

```python
  x = [2,3,4,5]
```

## Loops
Only has two ways of doing loops - for loops and while loops

## Operators
Outside of the usual operators, Python also uses:

* // where the results is the quotient in which the digits after the decimal point are removed. If one of the operands is negative, the result is floored (rounded away from zero)
* ** performs exponential calculation

### Bitwise operators
* x << y returns x with the bits shifted to the left by y places
* x >> y returns x with the bits shifted to the right by y places
* x & y does a "bitwise and" - each bit of the output is 1 if the corresponding bit of x AND of y is 1, otherwise it's 0
* x|y does a "bitwise or" - each bit of the output is 0 if the corresponding bit of x AND y is 0, otherwise it's 1
* ~x returns the complement of x - the number you get by switching each 1 for a 0 and each 0 for a 1
* x ^ y does a "bitwise exclusive or" - each bit of the output is the same as the corresponding bit in x if that bit in y is 0, and it's the complement of the bit in x if that bit in y is 1

## Tuples
Consist of a number of values separated by commas. They are used for ordered pairs and returning several values form a function.

Tuples are created with the comma operator:

```python
  newTuple = 2,3,4,5
```
