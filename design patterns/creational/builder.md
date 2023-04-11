The Builder pattern is a [[creational design pattern]] that separates the construction of a complex object from its representation, allowing the same construction process to create different representations. It is useful when creating objects with many parts, where the parts can be created in different orders or with different configurations.

```python
class Burger:
    def __init__(self):
        self.burger_type = None
        self.patty_count = None
        self.cheese = False
        self.bacon = False
        self.lettuce = False
        self.tomato = False
        self.onion = False

    def __str__(self):
        cheese_str = "with cheese" if self.cheese else "without cheese"
        bacon_str = "with bacon" if self.bacon else "without bacon"
        lettuce_str = "with lettuce" if self.lettuce else "without lettuce"
        tomato_str = "with tomato" if self.tomato else "without tomato"
        onion_str = "with onion" if self.onion else "without onion"
        return f"{self.burger_type} burger with {self.patty_count} patties, {cheese_str}, {bacon_str}, {lettuce_str}, {tomato_str}, and {onion_str}"

class BurgerBuilder:
    def __init__(self):
        self.burger = Burger()

    def set_burger_type(self, burger_type):
        self.burger.burger_type = burger_type

    def set_patty_count(self, patty_count):
        self.burger.patty_count = patty_count

    def add_cheese(self):
        self.burger.cheese = True

    def add_bacon(self):
        self.burger.bacon = True

    def add_lettuce(self):
        self.burger.lettuce = True

    def add_tomato(self):
        self.burger.tomato = True

    def add_onion(self):
        self.burger.onion = True

    def get_burger(self):
        return self.burger

class BurgerDirector:
    def __init__(self, builder):
        self.builder = builder

    def build_standard_burger(self):
        self.builder.set_burger_type("Standard")
        self.builder.set_patty_count(1)
        self.builder.add_cheese()
        self.builder.add_bacon()
        self.builder.add_lettuce()
        self.builder.add_tomato()
        self.builder.add_onion()

    def build_double_burger(self):
        self.builder.set_burger_type("Double")
        self.builder.set_patty_count(2)
        self.builder.add_cheese()
        self.builder.add_bacon()
        self.builder.add_lettuce()
        self.builder.add_tomato()
        self.builder.add_onion()

if __name__ == "__main__":
    builder = BurgerBuilder()
    director = BurgerDirector(builder)

    director.build_standard_burger()
    standard_burger = builder.get_burger()
    print(standard_burger)

    director.build_double_burger()
    double_burger = builder.get_burger()
    print(double_burger)
    The Builder pattern is a creational design pattern that separates the construction of a complex object from its representation, allowing the same construction process to create different representations. It is useful when creating objects with many parts, where the parts can be created in different orders or with different configurations.
```

In this example, we have a `Burger` class that represents the burger being built, a `BurgerBuilder` class that defines the steps for building the burger, and a `BurgerDirector` class that takes a `BurgerBuilder` instance and uses it to construct the burger in a specific way.

When the main program runs, we create an instance of `BurgerBuilder` and `BurgerDirector`. We then call the `build_standard_burger` and `build_double_burger` methods on the `BurgerDirector` instance, which use the `BurgerBuilder` instance to construct the standard and double burgers respectively. Finally, we retrieve the finished burgers from the `BurgerBuilder` instance and print out their attributes.

This example demonstrates how the Builder pattern allows for flexible construction