# Parsing and Serialization

Pydantic models can parse data and export to JSON.

## Parsing

```python
data = {'id': '1', 'name': 'Alice'}
user = User.parse_obj(data)
```

## Serialization

```python
print(user.json())
print(user.dict())
```
