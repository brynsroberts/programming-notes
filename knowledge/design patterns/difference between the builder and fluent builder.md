Using the [[Builder]] Pattern:

```python
class PersonBuilder:
    def __init__(self):
        self.person = Person()

    def set_name(self, name):
        self.person.name = name

    def set_age(self, age):
        self.person.age = age

    def set_address(self, address):
        self.person.address = address

    def build(self):
        return self.person

# Create a person using the Builder pattern
builder = PersonBuilder()
builder.set_name('John')
builder.set_age(30)
builder.set_address('123 Main St.')
person = builder.build()
print(person.name, person.age, person.address)
# Output: John 30 123 Main St.
```


Using the [[Fluent Builder]] Pattern:

```python
class PersonBuilder:
    def __init__(self):
        self.person = Person()

    def with_name(self, name):
        self.person.name = name
        return self

    def with_age(self, age):
        self.person.age = age
        return self

    def with_address(self, address):
        self.person.address = address
        return self

    def build(self):
        return self.person

# Create a person using the Fluent Builder pattern
person = PersonBuilder().with_name('John').with_age(30).with_address('123 Main St.').build()
print(person.name, person.age, person.address)
# Output: John 30 123 Main St.
```

As you can see, both implementations create the same `Person` object with the same properties. The difference is in the way the object is built: the Builder pattern uses separate `set_*` methods to configure the object, while the Fluent Builder pattern uses method chaining to configure the object directly.