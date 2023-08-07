# Input

Standard input.

```python
>>> name = input("What is your name? ")
What is your name? Master Splinter
>>> name
'Master Splinter'
```

Password input.

```python
>>> from getpass import getpass
>>> password = getpass("Password: ")  # password hidden in the dialog
Password: 
>>> password
'1234'
```
