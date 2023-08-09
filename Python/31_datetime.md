# Datetime

```python
>>> import datetime
```

Current date.

```python
>>> datetime.date.today()
datetime.date(2022, 6, 6)
```

Current datetime.

```python
>>> datetime.datetime.now()
datetime.datetime(2022, 6, 6, 10, 55, 7, 35045)
```

```python
>>> datetime.datetime.today()
datetime.datetime(2022, 6, 6, 10, 55, 8, 215002)
```

Current date UTC.

```python
>>> datetime.datetime.utcnow()
datetime.datetime(2022, 6, 6, 9, 55, 9, 832544)
```

Convert string to date.

```python
>>> datetime.datetime.strptime("31/12/2017", "%d/%m/%Y")
datetime.datetime(2017, 12, 31, 0, 0)
```

Convert datetime to string.

```python
>>> datetime.datetime.now().strftime("%Y-%m-%d")
'2022-06-06'
```

Current year.

```python
>>> datetime.date.today().year
2022
```

First day of the current month.

```python
>>> datetime.date.today().replace(day=1)
datetime.date(2022, 6, 1)
```

First day of the previous month.

```python
>>> (datetime.date.today().replace(day=1) - datetime.timedelta(days=1)).replace(day=1)
datetime.date(2022, 5, 1)
```

Last day of the previous month.

```python
>>> datetime.date.today().replace(day=1) - datetime.timedelta(days=1)
datetime.date(2022, 5, 31)
```

Current weekday.

```python
>>> datetime.date.today().weekday()
0
```

```python
>>> datetime.date.today().isocalendar().week
23
```

Current day.

```python
>>> datetime.date.today().day
6
```

Previous day.

```python
>>> datetime.date.today() - datetime.timedelta(days=1)
datetime.date(2022, 6, 5)
```

Sunday from the current week

```python
>>> datetime.date.today() + datetime.timedelta(days=-datetime.date.today().weekday() - 1, weeks=0)
datetime.date(2022, 6, 5)
```

Monday from the current week

```python
>>> datetime.date.today() + datetime.timedelta(days=-datetime.date.today().weekday(), weeks=0)
datetime.date(2022, 6, 6)
```

Monday from the previous week

```python
>>> datetime.date.today() + datetime.timedelta(days=-datetime.date.today().weekday(), weeks=-1)
datetime.date(2022, 5, 30)
```

Delta.

```python
>>> now = datetime.datetime.now()
>>> then = datetime.datetime(1978, 12, 10)
>>> delta = now - then
>>> delta.days, delta.seconds
(15884, 39317)
```

Execution time.

```python
>>> start = datetime.datetime.now()
>>> # process code here
>>> for i in range(100_000_000):
    pass
>>> end = datetime.datetime.now()
>>> # runtime in seconds
>>> runtime = (end - start).seconds
>>> # result in hours and the remaining seconds
>>> hours, remainder = divmod(runtime, 3600)
>>> minutes, seconds = divmod(remainder, 60)
>>> # output
>>> "{:02d}:{:02d}:{:02d}".format(hours, minutes, seconds)
'00:00:15'
```
