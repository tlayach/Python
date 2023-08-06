# Bytes

In Python, bytes are a data type that represents a sequence of bytes. A byte is a unit of data that is eight bits long and can represent a single character or binary data.

Bytes are represented using the bytes data type, which can be created in several ways. One way is to use a byte literal, which is a sequence of bytes enclosed in either single quotes (b'...') or double quotes (b"...").

```python
import base64
```

Encode using base64:

```python
>>> b64 = base64.b64encode(bytes("Planet Earth", "utf-8"))
>>> b64
b'UGxhbmV0IEVhcnRo'
```

Remove "b":

```python
>>> b64.decode("utf-8")
'UGxhbmV0IEVhcnRo'
```

Decode using base64
```python
>>> text = base64.b64decode(b64)
>>> text
b'Planet Earth'
```
