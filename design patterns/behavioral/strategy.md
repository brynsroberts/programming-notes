The Strategy pattern is a [[behavioral design pattern]] that allows you to define a family of algorithms, encapsulate each one as a separate class, and make them interchangeable at runtime. It enables the selection of an algorithm at runtime without tightly coupling the client code to the specific implementation of that algorithm.

Here's an example of implementing the Strategy pattern in Python:

```python
class SortStrategy:
    def sort(self, data):
        pass

class QuickSortStrategy(SortStrategy):
    def sort(self, data):
        print("Sorting using QuickSort")
        return sorted(data)

class MergeSortStrategy(SortStrategy):
    def sort(self, data):
        print("Sorting using MergeSort")
        return sorted(data, reverse=True)

class Sorter:
    def __init__(self, strategy):
        self.strategy = strategy

    def sort(self, data):
        return self.strategy.sort(data)

if __name__ == "__main__":
    data = [5, 1, 9, 3, 7]
    strategy_type = input("Enter sorting strategy (quick or merge): ")
    if strategy_type == "quick":
        strategy = QuickSortStrategy()
    elif strategy_type == "merge":
        strategy = MergeSortStrategy()
    else:
        raise ValueError("Invalid strategy type")

    sorter = Sorter(strategy)
    sorted_data = sorter.sort(data)
    print("Sorted data:", sorted_data)
```

In this example, we have a superclass `SortStrategy` and two subclasses `QuickSortStrategy` and `MergeSortStrategy` that implement different sorting algorithms. We also have a `Sorter` class that accepts a sorting strategy object and uses it to sort the input data.

When the main program runs, it prompts the user to enter a sorting strategy, which is then used to create an object of the appropriate subclass. This object is then passed to the `Sorter` constructor, which uses it to sort the input data by calling the `sort()` method of the strategy object. The sorted data is then printed to the console.

This example demonstrates how the Strategy pattern allows us to switch between different sorting algorithms at runtime by encapsulating each algorithm as a separate class and making them interchangeable. It also shows how the client code (in this case, the `Sorter` class) is decoupled from the specific implementation of the sorting algorithm.