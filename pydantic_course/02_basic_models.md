# Basic Models

Pydantic models are created by inheriting from `BaseModel`.

## Defining a Model

```python
from pydantic import BaseModel

class Product(BaseModel):
    name: str
    price: float
    in_stock: bool
```

## Creating and Accessing Instances

```python
product = Product(name="Laptop", price=999.99, in_stock=True)
print(product.name)  # Laptop
print(product.price) # 999.99
```

## Automatic Type Conversion

Pydantic will try to convert types:

```python
product = Product(name="Phone", price="499.99", in_stock="true")
print(product.price)    # 499.99 (float)
print(product.in_stock) # True (bool)
```
