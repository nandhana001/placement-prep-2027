# Object-Oriented Programming (OOPs)

## What is OOP?

Object-Oriented Programming (OOP) is a programming paradigm that organizes code using objects and classes.

Benefits:
- Code Reusability
- Modularity
- Security
- Easy Maintenance

---

# Class and Object

## Class

A class is a blueprint for creating objects.

```python
class Student:
    pass
```

## Object

An object is an instance of a class.

```python
s1 = Student()
```

---

# Constructor

A constructor is automatically called when an object is created.

```python
class Student:
    def __init__(self, name):
        self.name = name

s1 = Student("Anandhu")
```

---

# self Keyword

- Refers to the current object.
- Used to access instance variables and methods.

```python
class Test:
    def display(self):
        print("Hello")
```

---

# Four Pillars of OOP

## 1. Encapsulation

Wrapping data and methods into a single unit.

```python
class Bank:
    def __init__(self):
        self.balance = 1000
```

Advantages:
- Data Security
- Data Hiding

---

## 2. Abstraction

Showing only essential details and hiding implementation.

```python
from abc import ABC, abstractmethod

class Vehicle(ABC):
    @abstractmethod
    def start(self):
        pass
```

Advantages:
- Reduces Complexity
- Improves Security

---

## 3. Inheritance

Acquiring properties from another class.

```python
class Parent:
    def show(self):
        print("Parent")

class Child(Parent):
    pass

c = Child()
c.show()
```

### Types of Inheritance

### Single Inheritance

```python
A → B
```

### Multilevel Inheritance

```python
A → B → C
```

### Hierarchical Inheritance

```python
    A
   / \
  B   C
```

### Multiple Inheritance

```python
A   B
 \ /
  C
```

Example:

```python
class A:
    pass

class B:
    pass

class C(A, B):
    pass
```

---

## 4. Polymorphism

One interface, many forms.

### Method Overriding

```python
class Animal:
    def sound(self):
        print("Animal Sound")

class Dog(Animal):
    def sound(self):
        print("Bark")

d = Dog()
d.sound()
```

### Operator Overloading

```python
print(5 + 3)
print("Hello" + "World")
```

---

# Access Specifiers

## Public

```python
self.name
```

Accessible everywhere.

---

## Protected

```python
self._name
```

Accessible within class and subclasses.

---

## Private

```python
self.__name
```

Accessible only inside the class.

Example:

```python
class Student:
    def __init__(self):
        self.__age = 20
```

---

# Instance Variable

Different for every object.

```python
class Student:
    def __init__(self, name):
        self.name = name
```

---

# Class Variable

Shared among all objects.

```python
class Student:
    college = "ABC College"
```

---

# Instance Method

```python
class Test:
    def display(self):
        print("Hello")
```

---

# Static Method

```python
class Test:
    @staticmethod
    def show():
        print("Static Method")
```

---

# Class Method

```python
class Test:
    count = 0

    @classmethod
    def display(cls):
        print(cls.count)
```

---

# Association

Relationship between two classes.

```python
class Engine:
    pass

class Car:
    def __init__(self):
        self.engine = Engine()
```

---

# Difference Between Class and Object

| Class | Object |
|---------|---------|
| Blueprint | Instance |
| Logical Entity | Physical Entity |
| No Memory Allocated | Memory Allocated |

---

# Difference Between Abstraction and Encapsulation

| Abstraction | Encapsulation |
|------------|---------------|
| Hides implementation | Hides data |
| Achieved using abstract classes | Achieved using access modifiers |

---

# Frequently Asked Interview Questions

1. What are the four pillars of OOP?
2. Difference between abstraction and encapsulation?
3. What is inheritance?
4. What is polymorphism?
5. What is method overriding?
6. What is constructor?
7. What is the use of self?
8. Difference between class variable and instance variable?
9. What is multiple inheritance?
10. What are access specifiers?
