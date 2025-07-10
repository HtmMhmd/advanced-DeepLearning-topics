# Error Handling

Pydantic raises `ValidationError` on invalid data.

## Example

```python
from pydantic import ValidationError

try:
    user = User(id='abc', name=123)
except ValidationError as e:
    print(e)
```
