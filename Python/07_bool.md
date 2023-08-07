# Boolean

In Python, variables of type boolean can only have two values: True or False. The boolean data type is often used in decision-making or conditional statements, such as if statements and loops.

```python
>>> type(True)
<class 'bool'>
```

```python
>>> type(False)
<class 'bool'>
```

## Truth Table

* AND: A.B
* OR: A+B,
* NOT: A'

| A    | B    | A.B  | A+B  | A'   |
| :--: | :--: | :--: | :--: | :--: |
| 0    | 0    | 0    | 0    | 1    |
| 0    | 1    | 0    | 1    |      |
| 1    | 0    | 0    | 1    | 0    |
| 1    | 1    | 1    | 1    |      |

```python
>>> (1 == 1) and ("a" == "a")
True
```

```python
>>> (1 == 1) or ("a" == "b")
True
```
