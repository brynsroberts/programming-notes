The Factory pattern is a [[creational design pattern ]]that provides an interface for creating objects in a superclass, but allows subclasses to alter the type of objects that will be created.

Here's an example of implementing the Factory pattern in Python:

```python
class Shape:
    def draw(self):
        pass

class Circle(Shape):
    def draw(self):
        print("Drawing Circle")

class Square(Shape):
    def draw(self):
        print("Drawing Square")

class ShapeFactory:
    @staticmethod
    def create_shape(shape_type):
        if shape_type == "circle":
            return Circle()
        elif shape_type == "square":
            return Square()
        else:
            raise ValueError("Invalid shape type")

if __name__ == "__main__":
    shape_type = input("Enter shape type: ")
    shape = ShapeFactory.create_shape(shape_type)
    shape.draw()
```

In this example, we have a superclass `Shape` and two subclasses `Circle` and `Square`. We also have a `ShapeFactory` class that provides a static method `create_shape()` which takes a `shape_type` argument and returns an object of the appropriate subclass based on the value of `shape_type`.

When the main program runs, it prompts the user to enter a shape type, which is then passed to the `create_shape()` method of the `ShapeFactory` class. The appropriate subclass is then instantiated and its `draw()` method is called, which prints a message to indicate which shape is being drawn.