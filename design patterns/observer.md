The Observer pattern is used when one or more objects need to be notified when a particular event occurs. In this pattern, there is a subject or observable object, which maintains a list of its dependents or observers. When an event occurs, the subject notifies all its observers, allowing them to update themselves accordingly.

Here is an example of implementing the Observer pattern in Python:

```python
class Subject:
    def __init__(self):
        self.observers = []

    def register_observer(self, observer):
        self.observers.append(observer)

    def remove_observer(self, observer):
        self.observers.remove(observer)

    def notify_observers(self, data=None):
        for observer in self.observers:
            observer.update(data)


class Observer:
    def update(self, data=None):
        pass


class StockTicker(Subject):
    def __init__(self):
        super().__init__()
        self.stock_price = None

    def set_stock_price(self, price):
        self.stock_price = price
        self.notify_observers(price)


class StockTracker(Observer):
    def __init__(self, name):
        self.name = name

    def update(self, price):
        print(f"{self.name} has been notified of a stock price change: {price}")


if __name__ == "__main__":
    ticker = StockTicker()

    john = StockTracker("John")
    ticker.register_observer(john)

    jane = StockTracker("Jane")
    ticker.register_observer(jane)

    ticker.set_stock_price(50.0)

    ticker.remove_observer(jane)

    ticker.set_stock_price(60.0)
```

In this example, we have a `Subject` class, which maintains a list of observers and notifies them when an event occurs. The `Observer` class defines the interface for objects that need to be notified of an event. We also have a `StockTicker` class, which is a concrete implementation of the `Subject` class. It maintains a stock price and notifies its observers when the price changes. Finally, we have a `StockTracker` class, which is a concrete implementation of the `Observer` class. It prints a message when it is notified of a stock price change.

In the main program, we create a `StockTicker` instance and two `StockTracker` instances named John and Jane. We register both John and Jane as observers of the `StockTicker` instance using the `register_observer` method. We then set the stock price to 50.0, which causes the `StockTicker` instance to notify both John and Jane of the price change. We then remove Jane as an observer using the `remove_observer` method, and set the stock price to 60.0, which causes only John to be notified of the price change.