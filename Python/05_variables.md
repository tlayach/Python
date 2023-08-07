# Variables

As a developer, understanding variables in Python is crucial because variables allow us to store and manipulate data in our code. A variable in Python is simply a name that represents a value or object in memory.

In Python, we don't need to specify the data type of a variable explicitly, unlike many other programming languages. Python infers the data type of a variable from the value that is assigned to it. There are several built-in data types in Python, including strings, booleans, integers, floats, complex numbers, tuples, sets, lists, and dictionaries.

## Base Variables

Types	Example

| Types   | Example       |
| :-----: | :------------ |
| string  | "Hello World" |
| bool    | True          |
| int     | 1             |
| float   | 3.14159       |
| complex | 2 + 3j        |
| tuple   | (1, 2, 3, 4)  |
| set     | {1, 2, 3, 4}  |
| list    | [1, 2, 3, 4]  |
| dict    | {"a": 1, "b": 2, "c": 3, "d": 4} |

Here are examples of each:

String: A string is a sequence of characters enclosed in single or double quotes. Strings are immutable in Python, meaning that once a string is created, it cannot be changed.

```python
>>> name = "John"
```

Boolean: A boolean is a data type that has two possible values: True or False. Booleans are useful for making logical comparisons in code.

```python
>>> is_valid = True
```

Integer: An integer is a whole number (positive, negative, or zero) with no decimal point.

```python
>>> age = 28
```

Float: A float is a decimal number. Floats are used when we need to represent fractional numbers.

```python
>>> pi = 3.14
```

Complex: A complex number is a number with a real and imaginary part. In Python, we represent complex numbers using the "j" suffix.

```python
>>> z = 2 + 3j
```

Tuple: A tuple is an ordered collection of elements. Tuples are immutable, meaning that once created, the elements cannot be changed.

```python
>>> coordinates = (10, 20)
```

Set: A set is an unordered collection of unique elements. Sets are useful for performing set operations like union, intersection, and difference.

```python
>>> colors = {"red", "green", "blue"}
```

List: A list is an ordered collection of elements. Unlike tuples, lists are mutable, meaning that we can add, remove, or change elements.

```python
>>> fruits = ["apple", "banana", "orange"]
```

Dictionary: A dictionary is an unordered collection of key-value pairs. Each key must be unique within the dictionary.

```python
>>> person = {"name": "John", "age": 28, "city": "New York"}
```

## Type

The built-in function type() is used to get the type of an object. The type() function takes a single argument and returns the data type of that argument. The returned data type can be used to determine how to manipulate or use the object.

The syntax for using type() is simple, you just need to pass the object whose type you want to determine as an argument to the function, and it will return the type of the object. Here's an example:

```python
>>> x = 10
>>> type(x)
int
```

```python
>>> y = "Hello"
>>> type(y)
str
```

```python
>>> z = [1, 2, 3]
>>> type(z)
list
```

The type() function can be particularly useful when working with functions that accept arguments of different data types. It can also be useful when debugging code, helping you quickly identify the data type of a variable or object.

It's important to note that type() can only determine the data type of a single object at a time. If you want to determine the data type of multiple objects, you will need to call type() for each object individually.

## Cast

Casting is the process of converting one data type to another. Python provides built-in functions that allow us to cast variables from one data type to another. This is particularly useful when we need to perform operations or comparisons between variables of different data types.

Here are some of the built-in casting functions in Python:

int(): This function is used to cast a value to an integer data type.

```python
>>> x = 3.14159
>>> int(x)
3
```

float(): This function is used to cast a value to a floating-point data type.

```python
>>> x = 5
>>> float(x)
5.0
```

str(): This function is used to cast a value to a string data type.

```python
>>> x = 5
>>> str(x)
'5'
```

bool(): This function is used to cast a value to a boolean data type.

```python
>>> x = 5
>>> bool(x)
True
```

In addition to the built-in casting functions, Python also provides some implicit casting capabilities. For example, when performing operations between variables of different data types, Python will automatically cast the variables to a common data type. For example:

```python
>>> x = 5
>>> y = 5.5
>>> z = x + y
>>> z
10.5
```

In this example, x is an integer and y is a float, but Python automatically casts x to a float so that it can perform the addition operation with y. The result is a float.

Casting can be useful for making sure that variables have the correct data type before performing operations on them, or for converting data to a more suitable format for output. However, it's important to use casting with care, as it can sometimes result in data loss or unexpected behavior.
