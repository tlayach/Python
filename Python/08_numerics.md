# Numerics

In Python, numeric variables are variables that store numeric data types, such as integers, floating-point numbers, and complex numbers.

Integers are whole numbers without a fractional component. They can be positive or negative.

Floating-point numbers are numbers with a decimal point or an exponent. They can also be positive or negative.

Complex numbers are numbers with both a real and imaginary component. They are expressed in the form a + bj, where a is the real part, b is the imaginary part, and j represents the square root of -1.

## Types

| Types   | Example       |
| :-----: | :------------ |
| int     | 1             |
| float   | 3.14159       |
| complex | 2 + 3j        |

Integer type variable.

```python
>>> type(13)
<class 'int'>
```

Variable of type float.

```python
>>> type(3.14159)
<class 'float'>
```

## Math Operations

Numeric variables support a wide range of arithmetic operations, such as addition, subtraction, multiplication, and division.

Sum operation.

```python
>>> 1 + 1
2
```

Subtraction operation.

```python
>>> 3 - 2
1
```

Division operation.

```python
>>> 2 / 3
0.6666666666666666
```

Multiply operation.

```python
>>> 3.14 * 3
9.42
```

Power operation.

```python
>>> pow(2, 3)
8
>>> 2**3
8
```

Mod - remainder after division.

```python
>>> 4 % 2
0
>>> 5 % 2
1
```

Sum operation of complex numbers.

```python
>>> (1 + 2j) + (2 + 4j)
(3+6j)
```

## Underscore placeholders

```python
>>> 1_000_000 * 2
2000000
>>> f"{1_000_000 * 2:,}"
'2,000,000'
>>> "{:,.2f}".format(1_000_000 * 2)
'2,000,000.00'
```

## Range of numbers

```python
>>> list(range(0, 9))
[0, 1, 2, 3, 4, 5, 6, 7, 8]
```
