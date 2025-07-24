---
description: >-
  Learn how polymorphism lets different classes share behaviour while
  maintaining their own identity.
---

# 218 Polymorphism

### Objectives

* Define polymorphism and explain how it supports flexible code
* Demonstrate method overriding using a common interface
* Apply polymorphism in class hierarchies using Python examples

### What is polymorphism?

**Polymorphism** means "many forms". In OOP, it allows different classes to implement the same method in different ways.

This enables **objects to be used interchangeably**, even if they behave differently behind the scenes.

#### Example:

```python
class Animal:
    def speak(self):
        return "Some sound"

class Dog(Animal):
    def speak(self):
        return "Bark"

class Cat(Animal):
    def speak(self):
        return "Meow"
```

### Using polymorphism:

```python
animals = [Dog(), Cat()]
for animal in animals:
    print(animal.speak())
```

Output:

```
Bark  
Meow
```

* Each object uses the same `speak()` method
* Python automatically calls the correct version at runtime

### Why use polymorphism?

* Simplifies code
* Allows different classes to be treated the same way
* Encourages reusable and extendable designs
