# Disassembler

```python
>>> import dis
>>> dis.dis("print('hello world')")
  1           0 LOAD_NAME                0 (print)
              2 LOAD_CONST               0 ('hello world')
              4 CALL_FUNCTION            1
              6 RETURN_VALUE
```
