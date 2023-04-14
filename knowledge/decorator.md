A decorator in [[Python]] is a [[structural]] [[design pattern]] that allows a user to add functionality to an existing function or class without modifying its source code directly. Decorators are themselves functions that can take a function as an argument and return a new function that adds some kind of behavior to the original function.

Decorators are often used to add functionality such as logging, caching, or authentication to functions without changing their implementation. For example, you can define a decorator that logs the input and output of a function:

```python
def log(func):
    def wrapper(*args, **kwargs):
        result = func(*args, **kwargs)
        print(f"{func.__name__}({args}, {kwargs}) = {result}")
        return result
    return wrapper
```

You can then apply this decorator to a function using the `@` syntax:

```python
@log
def my_function(x, y):
    return x + y
```

Now, whenever `my_function` is called, the input and output will be logged to the console.

Decorators can also be used to add functionality to classes. For example, you can define a decorator that adds a `to_dict` method to a class:

```python
def to_dict(cls):
    def wrapper(*args, **kwargs):
        instance = cls(*args, **kwargs)
        return vars(instance)
    cls.to_dict = wrapper
    return cls
```

You can then apply this decorator to a class:

```python
@to_dict
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
```

Now, you can call `to_dict` on an instance of `Person` to get its attributes as a dictionary:

```python
person = Person("Alice", 25)
print(person.to_dict())  # {"name": "Alice", "age": 25}
```