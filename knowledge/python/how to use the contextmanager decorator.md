In [[Python]], the `contextmanager` [[decorator]] from the `contextlib` module can be used to create a [[context manager]] without having to define a class with the `__enter__` and `__exit__` methods. Instead, you define a [[generator function]] that yields the value to be used inside the `with` statement, and the `contextmanager` decorator takes care of the rest.

Here is an example of using the `contextmanager` decorator:

```python
from contextlib import contextmanager

@contextmanager
def file_context_manager(filename, mode):
    file = open(filename, mode)
    try:
        yield file
    finally:
        file.close()
```

In this example, the `file_context_manager` generator function takes a filename and a mode as input and opens the file using the `open` function. The `yield` statement returns the file object to be used inside the `with` statement. The `finally` block ensures that the file is closed even if an exception is raised inside the `with` statement.

You can use this context manager in a `with` statement like this:

```python
with file_context_manager('example.txt', 'w') as file:
    file.write('Hello, world!')
```

In this example, the `file_context_manager` context manager is used to open the file `example.txt` in write mode, and the `write` method is called on the file object to write the string `'Hello, world!'` to the file. When the block of code inside the `with` statement exits, the `finally` block is executed and the file is closed.