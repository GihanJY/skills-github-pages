---
title: "Object-Oriented-Programming"
date: 2024-12-26
---

# Object-Oriented Programming (OOP)

Object Oriented Programming (OOP) is a programming paradigm that organizes software design around data, or objects, rather than functions and logic. It emphasizes the use of objects, which can contain both data (attributes) and functions (methods).

---

## OOP Concepts

The four main principles of OOP are:

1. **Encapsulation**
2. **Inheritance**
3. **Abstraction**
4. **Polymorphism**

---

## Class

A class is a blueprint for creating objects. It defines a set of attributes (properties) and methods (functions) that the created objects will have.

### Example (Python):
```python
class Car:
    def __init__(self, brand, model):
        self.brand = brand
        self.model = model

    def drive(self):
        print(f"{self.brand} {self.model} is driving!")
```

---

## Object

An object is an instance of a class. When a class is defined, no memory is allocated until an object of that class is created.

### Example (Python):
```python
my_car = Car("Toyota", "Corolla")
my_car.drive()  # Output: Toyota Corolla is driving!
```

---

## Encapsulation

Encapsulation is the process of bundling data (attributes) and methods (functions) that operate on the data into a single unit (class). It also restricts direct access to some of the object's components, which is called data hiding.

### Example (Python):
```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance  # Private attribute

    def deposit(self, amount):
        self.__balance += amount

    def get_balance(self):
        return self.__balance

account = BankAccount(1000)
account.deposit(500)
print(account.get_balance())  # Output: 1500
```

---

## Inheritance

Inheritance allows a class (child class) to inherit attributes and methods from another class (parent class). This promotes code reuse.

### Example (Python):
```python
class Animal:
    def speak(self):
        print("Animal speaks")

class Dog(Animal):
    def speak(self):
        print("Dog barks")

dog = Dog()
dog.speak()  # Output: Dog barks
```

---

## Abstraction

Abstraction is the process of hiding complex implementation details and showing only the necessary features of an object. It is often achieved using abstract classes or interfaces.

### Example (Python):
```python
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius * self.radius

circle = Circle(5)
print(circle.area())  # Output: 78.5
```

---

## Polymorphism

Polymorphism means "many forms." It allows objects of different classes to be treated as objects of a common superclass. The most common use is method overriding.

### Example (Python):
```python
class Bird:
    def fly(self):
        print("Bird is flying")

class Penguin(Bird):
    def fly(self):
        print("Penguins can't fly")

def make_fly(bird):
    bird.fly()

sparrow = Bird()
penguin = Penguin()

make_fly(sparrow)  # Output: Bird is flying
make_fly(penguin)  # Output: Penguins can't fly
```

---

## Summary

| Concept        | Description                                                   |
|----------------|---------------------------------------------------------------|
| Class          | Blueprint for creating objects                                |
| Object         | Instance of a class                                           |
| Encapsulation  | Bundling data and methods, restricting access to certain parts|
| Inheritance    | Deriving new classes from existing classes                    |
| Abstraction    | Hiding implementation details, showing essential features     |
| Polymorphism   | Allowing methods to perform differently based on the object   |

By mastering these concepts, you can design efficient and modular software systems!
