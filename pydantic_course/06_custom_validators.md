# Custom Validators

Use `@validator` to add custom validation logic.

## Example

```python
from pydantic import BaseModel, validator

class User(BaseModel):
    username: str

    @validator('username')
    def username_must_be_alphanumeric(cls, v):
        if not v.isalnum():
            raise ValueError('must be alphanumeric')
        return v
```
