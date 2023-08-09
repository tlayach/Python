# Strings

In Python, variables of type string are used to store text data. A string is a sequence of characters enclosed in either single quotes (') or double quotes (").

String configuration using (double) quotes.

```python
>>> "Hello World Again"
'Hello World Again'
```

String configuration using single quotes.

```python
>>> 'Hello World Again'
'Hello World Again'
```

Configuration of multiline strings.

```python
>>> """Hello 
             World"""
'Hello \n             World'
```

String concatenation.

```python
>>> "Hello " + "World"
'Hello World'
```

String multiplication.

```python
>>> "Hello " * 3
'Hello Hello Hello '
```

Conversion from string to uppercase.

```python
>>> "Hello World".upper()
'HELLO WORLD'
```

String conversion to lowercase.

```python
>>> "HELLO WORLD".lower()
'hello world'
```

String capitalization.

```python
>>> "hello world".capitalize()
'Hello world'
```

String to title conversion.

```python
>>> "hello world".title()
'Hello World'
```

Replacement of characters in a string.

```python
>>> "hello world".replace("o", "0")
'hell0 w0rld'
```

Split of the contents of a string.

```python
>>> planets = "Mercury,Venus,Earth,Mars,Jupiter,Saturn,Uranus,Neptune"
>>> planets.split()
['Mercury,Venus,Earth,Mars,Jupiter,Saturn,Uranus,Neptune']
>>> planets.split(sep=",")
['Mercury', 'Venus', 'Earth', 'Mars', 'Jupiter', 'Saturn', 'Uranus', 'Neptune']
```

Obtaining the email domain in a string.

```python
>>> "user@domain.com".split("@")[-1]
'domain.com'
```

Checking for the existence of the word "Earth" in a string.

```python
>>> "Earth" in "The planet Earth is amazing"
True
```

Obtaining the number of occurrences of a word in a string.

```python
>>> message = "The planet Earth is amazing!"
>>> message.count("planet")
1
```

## Dot format or string interpolation

```python
>>> "{} is a planet".format("Earth")
'Earth is a planet'
```

```python
>>> "{} and {} are planets".format("Earth", "Saturn")
'Earth and Saturn are planets'
```

```python
>>> "{1} and {0} are planets".format("Earth", "Saturn")
'Saturn and Earth are planets'
```

```python
>>> "{a} and {b} are planets".format(a="Earth", b="Saturn")
'Earth and Saturn are planets'
```

## f-Strings

```python
>>> missing = "World"
>>> f"Hello {missing}"
'Hello World'
```

Removal of prefix and suffix in a string.

```python
>>> "hello world".removeprefix("h")
'ello world
```

```python
>>> "hello world".removesuffix("d")
'hello worl'
```

Check if a string starts with a certain word.

```python
>>> "hello world".startswith("hello")
True
```

```python
>>> "hello world".startswith(("hello", "ola"))
True
```

Strip a string.

```python
>>> "mimimimi world".lstrip("mi")
' world'
```

```python
>>> "hello world".strip("world")
'hello '
```

Other tricks.

```python
>>> w = "hello world"
>>> f"{w = }"
"w = 'hello world'"
```

```python
>>> x = 7
>>> f"{x % 2 = }"
'x % 2 = 1'
```

## Conversions

Conversion of a string to ASCII.

```python
>>> w = "hello world é ó"
>>> f"{w!a}"
"'hello world \\xe9 \\xf3'"
```

Conversion of a string using the repr() function.

```python
>>> w = "hello world é ó"
>>> f"{w!r}"
"'hello world é ó'"
```

Converting a number to a string using the str() function.

```python
>>> x = 1234
>>> str(x)
'1234'
```

Formatting

```python
>>> import datetime
>>> now = datetime.datetime.now()
>>> f"{now = :%Y-%m-%d}"
'now = 2023-03-31'
```

```python
>>> x = 3.1416
>>> f"{x:.2f}"
'3.14'
```
