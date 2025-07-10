# Model Configuration

Pydantic models can be configured using the `Config` class.

## Example

```python
from pydantic import BaseModel

class User(BaseModel):
    id: int
    name: str

    class Config:
        anystr_lower = True
        allow_mutation = False
```

- `anystr_lower`: Converts all string fields to lowercase.
- `allow_mutation`: Makes model immutable.

## More Config Options

- `orm_mode`: For ORM integration
- `use_enum_values`: Use enum values instead of names
- `json_encoders`: Custom JSON encoding
