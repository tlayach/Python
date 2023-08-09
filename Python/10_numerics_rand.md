# Random Module

```python
>>> import random
```

Random between 1 and 99

```python
>>> random.randint(1, 100)
45
```

Choose randomly from list

```python
>>> planets = ["Mercury", "Venus", "Earth", "Mars", "Jupiter", "Saturn", "Uranus", "Neptune"]
>>> random.choice(planets)
'Saturn'
```

Shuffle

```python
>>> deck = ["Ace", "Two", "Three", "Four", "Five", "Six", "Seven", "Eight", "Nine", "Ten", "Jack", "Queen", "King"]
>>> random.shuffle(deck)
>>> deck
['Queen', 'Three', 'Two', 'Eight', 'Five', 'Nine', 'Jack', 'Four', 'Seven', 'Ten', 'Ace', 'King', 'Six']
```
