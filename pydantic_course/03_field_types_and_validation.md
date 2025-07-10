# Field Types and Validation

Pydantic supports all standard Python types and more.

## Supported Types

- int, float, str, bool
- list, tuple, dict
- datetime, date, time
- UUID, Decimal, etc.

## Default Values

```python
from pydantic import BaseModel

class Item(BaseModel):
    name: str
    quantity: int = 1
```

## Field Validation

Use `Field` for constraints:

```python
from pydantic import BaseModel, Field

class User(BaseModel):
    username: str = Field(..., min_length=3, max_length=20)
    age: int = Field(..., ge=18, le=99)
```

## Example

```python
user = User(username="bob", age=25)  # Valid
user = User(username="a", age=17)    # Raises ValidationError
```
