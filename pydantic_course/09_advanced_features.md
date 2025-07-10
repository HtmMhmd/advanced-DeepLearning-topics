# Advanced Features

## Inheritance

```python
class Admin(User):
    admin_level: int
```

## Generic Models

```python
from pydantic.generics import GenericModel
from typing import TypeVar, Generic

T = TypeVar('T')

class Response(GenericModel, Generic[T]):
    data: T
```

## Settings Management

```python
from pydantic import BaseSettings

class Settings(BaseSettings):
    db_url: str

    class Config:
        env_file = ".env"
```
