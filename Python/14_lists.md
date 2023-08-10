# Lists

In Python, variables of type list are used to store a collection of items in an ordered sequence. A list is a mutable data type that can contain elements of different data types, such as numbers, strings, and even other lists.

Lists can be created by enclosing a sequence of items in square brackets [], separated by commas.

Important methods: append(), copy(), count(), insert(), reverse(), remove(), sort(), pop(), extend(), index(), clear().

Creating an empty list.

```python
>>> my_list = []
>>> type(my_list)
<class 'list'>
```

Creating a list of numbers

```python
>>> my_list = [1, 2, 3, 4]
>>> type(my_list)
<class 'list'>
```

Generate automatically a list of numbers

```python
>>> list(range(1, 10))
[1, 2, 3, 4, 5, 6, 7, 8, 9]
```

Creating a list of numbers and words

```python
>>> demo = [1, 2, 3, "Mercury", "Venus", "Earth"]
>>> type(demo)
<class 'list'>
```

Creating an example list

```python
>>> planets = ["Mercury", "Venus", "Earth", "Mars", "Jupiter", "Saturn", "Uranus", "Neptune"]
>>> type(planets)
<class 'list'>
```

Sort list elements

```python
>>> sorted(planets)
['Earth', 'Jupiter', 'Mars', 'Mercury', 'Neptune', 'Saturn', 'Uranus', 'Venus']
```

Get element from the first position

If we want to access the individual elements of a list, we use something called an idex, An index is just the position of an individual element. In Python, we start counting indexes at zero.

```python
>>> planets[0]
'Mercury'
```

Get element from the third position

```python
>>> planets[2]
'Earth'
```

Obtaining the second and third elements of the list

```python
>>> planets[1:3]
['Venus', 'Earth']
```

```python
>>> planets[-3:-1]
['Saturn', 'Uranus']
```

Going backwards to get the last element of the list

```python
>>> planets[-1]
'Neptune'
```

Invert list

```python
>>> planets[-1::-1]
['Neptune', 'Uranus', 'Saturn', 'Jupiter', 'Mars', 'Earth', 'Venus', 'Mercury']
```

Even indexes

```python
>>> planets[0::2]
['Mercury', 'Earth', 'Jupiter', 'Uranus']
```

Get the number of elements on the list

```python
>>> len(planets)
8
```

Add a new element to the list

```python
>>> planets.append("Xena")
>>> planets
['Mercury', 'Venus', 'Earth', 'Mars', 'Jupiter', 'Saturn', 'Uranus', 'Neptune', 'Xena']
```

Add a new element to the second position of the list

```python
>>> planets.insert(1, "Pluto")
>>> planets
['Mercury', 'Pluto', 'Venus', 'Earth', 'Mars', 'Jupiter', 'Saturn', 'Uranus', 'Neptune', 'Xena']
```

The right way to copy a list

```python
>>> dummy = planets.copy()
>>> dummy
['Mercury', 'Pluto', 'Venus', 'Earth', 'Mars', 'Jupiter', 'Saturn', 'Uranus', 'Neptune', 'Xena']
```

Extend the list

```python
>>> dummy = ["Ceres", "Charon"]
>>> planets.extend(dummy)
>>> planets
['Mercury', 'Pluto', 'Venus', 'Earth', 'Mars', 'Jupiter', 'Saturn', 'Uranus', 'Neptune', 'Xena', 'Ceres', 'Charon']
```

Remove "pluto" from the list

```python
>>> planets.remove("Pluto")
>>> planets
['Mercury', 'Venus', 'Earth', 'Mars', 'Jupiter', 'Saturn', 'Uranus', 'Neptune', 'Xena', 'Ceres', 'Charon']
```

Remove the seventh and the eighth element from the list

```python
>>> del planets[8]
>>> del planets[8]
>>> planets
['Mercury', 'Venus', 'Earth', 'Mars', 'Jupiter', 'Saturn', 'Uranus', 'Neptune', 'Charon']
```

Removing the first element from the list

```python
>>> planets.pop(0)
>>> planets
['Venus', 'Earth', 'Mars', 'Jupiter', 'Saturn', 'Uranus', 'Neptune', 'Charon']
```

Removing the last element from the list

```python
>>> planets.pop()
>>> planets
['Venus', 'Earth', 'Mars', 'Jupiter', 'Saturn', 'Uranus', 'Neptune']
```

Checking the existence of the planet "Earth" in the list

```python
>>> 'Earth' in planets
True
```

Deleting the contents of a list

```python
>>> planets.clear()
>>> planets
[]
```

Eliminating the variable

```python
>>> del planets
```

Creating a nested list

```python
>>> my_matrix = [[1, 2, 3, 4], [5, 6, 7, 8]]
>>> my_matrix[1][1]
6
```

Sum elements from a list

```python
>>> my_list = [1, 2, 3, 4, 5]
>>> sum(my_list)
15
```

Convert set to list

```python
>>> list({1, 2, 3, 4})
[1, 2, 3, 4]
```

Max and min

```python
>>> my_list = [1, 2, 3, 4, 5]
>>> max(my_list)
5
>>> min(my_list)
1
```
