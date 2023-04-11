The Facade pattern is a design pattern in which a simplified interface is provided to a complex system or set of subsystems. It provides a unified interface to a set of interfaces in a subsystem, making it easier to use and reducing the complexity of the system. The Facade pattern is often used to provide a simple and user-friendly interface to a complex API or library, or to hide the internal details of a system from its users. The main idea behind the Facade pattern is to encapsulate the complexity of a system behind a simple interface, allowing users to interact with the system without having to understand its internal workings.

```python
class Burger:
    def __init__(self, patty, cheese=None, sauce=None):
        self.patty = patty
        self.cheese = cheese
        self.sauce = sauce

    def __str__(self):
        description = f"{self.patty} burger"
        if self.cheese:
            description += f" with {self.cheese} cheese"
        if self.sauce:
            description += f" and {self.sauce} sauce"
        return description


class BurgerFacade:
    def make_burger(self, patty_type, cheese_type=None, sauce_type=None):
        patty = f"{patty_type} patty"
        cheese = f"{cheese_type} cheese" if cheese_type else None
        sauce = f"{sauce_type} sauce" if sauce_type else None
        burger = Burger(patty, cheese, sauce)
        return burger


if __name__ == "__main__":
    burger_facade = BurgerFacade()

    # Ordering a basic burger
    basic_burger = burger_facade.make_burger("beef")
    print(basic_burger)

    # Ordering a cheeseburger with cheddar cheese
    cheddar_cheeseburger = burger_facade.make_burger("beef", "cheddar")
    print(cheddar_cheeseburger)

    # Ordering a bacon burger with bbq sauce
    bacon_bbq_burger = burger_facade.make_burger("beef", sauce_type="bbq", cheese_type="cheddar")
    print(bacon_bbq_burger)
```

In this example, we have a `Burger` class that represents a burger with a patty, cheese, and sauce. We also have a `BurgerFacade` class that provides a simplified interface for ordering burgers. The `BurgerFacade` class creates instances of the `Burger` class and initializes them with the requested ingredients.

In the main program, we create an instance of the `BurgerFacade` class and call its `make_burger` method to order different types of burgers. We can order a basic burger with just a patty, a cheeseburger with a specific type of cheese, or a bacon burger with a specific type of cheese and sauce. The `make_burger` method takes in the type of patty, cheese, and sauce as arguments and returns a `Burger` object initialized with the requested ingredients.

In this way, we have successfully used the Facade pattern to provide a simplified interface for ordering burgers with different combinations of ingredients. The `BurgerFacade` class hides the complexity of creating a `Burger` object with different ingredients and provides a single point of entry to order burgers.