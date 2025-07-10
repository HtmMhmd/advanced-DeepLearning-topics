# Introduction to Pydantic

Pydantic is a Python library for data validation and settings management using Python type annotations. It enforces type hints at runtime and provides user-friendly errors.

## Why Use Pydantic?

- Automatic data parsing and validation
- Clear error messages
- Integration with FastAPI and other frameworks

## Installation

```bash
pip install pydantic
```

## Basic Example

```python
from pydantic import BaseModel

class User(BaseModel):
    id: int
    name: str

user = User(id=1, name="Alice")
print(user)
```
