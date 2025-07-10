# Nested Models and Complex Types

Models can include other models as fields.

## Example

```python
from pydantic import BaseModel

class Address(BaseModel):
    city: str
    zip_code: str

class User(BaseModel):
    name: str
    address: Address

user = User(name="Alice", address={"city": "Paris", "zip_code": "75000"})
print(user.address.city)  # Paris
```

## Lists of Models

```python
class Group(BaseModel):
    users: list[User]
```
