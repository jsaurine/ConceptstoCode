---
description: >-
  Learn how inheritance allows classes to share code and create powerful
  hierarchies in OOP.
---

# 219 Inheritance

### Objectives

* Define inheritance and explain how it creates relationships between classes
* Use Python to inherit attributes and methods from a parent class
* Understand when and why to use inheritance in your programs

### What is inheritance?

**Inheritance** allows one class (child or subclass) to reuse the attributes and methods of another class (parent or superclass). This avoids duplication and creates clear class relationships.

#### Example:

```python
class Vehicle:
    def __init__(self, brand):
        self.brand = brand

    def start_engine(self):
        return "Engine started"

class Car(Vehicle):  # Car inherits from Vehicle
    def play_radio(self):
        return "Playing music"
```

#### Using the subclass

```python
my_car = Car("Toyota")
print(my_car.start_engine())  # Inherited method
print(my_car.play_radio())    # Defined in subclass
```

#### **Output**

```
Engine started  
Playing music
```

### Why use inheritance?

* Reuse existing functionality
* Group similar classes into hierarchies
* Simplify large programs and reduce redundancy
