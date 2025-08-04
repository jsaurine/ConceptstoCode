---
description: >-
  Understand how polymorphism allows different object types to respond to the
  same message in different ways.
---

# 218 Polymorphism

### Overview

In this topic, we explore **polymorphism**, one of the core principles of object-oriented programming (OOP). Polymorphism allows multiple object types to respond to the same method call in a way that is specific to their own behaviour. This supports flexible code design, where functions and structures can work with a variety of related objects without knowing their exact type.

### Targets

In this topic, students learn to:

* Define polymorphism and explain its role in OOP
* Identify examples of polymorphism in Python
* Use method overriding to customise behaviour in subclasses
* Explain how polymorphism supports flexible and scalable code
* Recognise polymorphism in real-world programming contexts

### Syllabus references

<details>

<summary><a href="https://curriculum.nsw.edu.au/learning-areas/tas/software-engineering-11-12-2022/content/year-11/f796d35e-3125-4824-ae92-427ee7048659"><strong>The object-oriented paradigm</strong></a></summary>

**Polymorphism**

* Explain the concept of polymorphism in object-oriented programming
* Demonstrate how different objects can respond to the same message using their own methods

</details>

### What is polymorphism?

**Polymorphism** means “many forms.” In OOP, it allows different classes to define their own version of a method with the same name. This lets developers write more generic, reusable code that behaves differently depending on the object it interacts with.

#### In practice:

* A base class defines a method (e.g. `speak()`)
* Subclasses override that method with their own version
* A single function can call `speak()` without knowing the exact type of object

### Example: Animal polymorphism

```python
class Animal:
    def speak(self):
        return "Some sound"

class Dog(Animal):
    def speak(self):
        return "Woof!"

class Cat(Animal):
    def speak(self):
        return "Meow!"

def make_it_speak(animal):
    print(animal.speak())

dog = Dog()
cat = Cat()

make_it_speak(dog)  # Woof!
make_it_speak(cat)  # Meow!
```

Even though `make_it_speak()` doesn’t know whether it’s handling a Dog or a Cat, it works correctly with both. This is **runtime polymorphism**.

### Method overriding

**Overriding** is when a subclass provides a different implementation of a method inherited from a superclass.

* The method name stays the same
* The behaviour changes in the subclass
* The correct version is chosen at **runtime** based on the object’s actual type

This is the most common form of polymorphism in Python.

### Why use polymorphism?

* **Simplifies code** – write generic functions that work with many types
* **Improves flexibility** – easily add new object types without rewriting logic
* **Supports scalability** – extend systems with minimal disruption
* **Enhances readability** – lets code focus on _what_ to do, not _how_

### Real-world example: GUI components

In a graphical user interface:

* A `Button`, `Checkbox`, and `TextBox` might all inherit from a `Widget` class
* Each has a `draw()` method that is called in the UI loop
* The loop doesn’t care what kind of widget it’s drawing—just that each knows how to draw itself

```python
for widget in widget_list:
    widget.draw()  # Each widget handles this in its own way
```

<figure><img src="../../.gitbook/assets/ChatGPT 2025-08-04 13.02.32.png" alt=""><figcaption><p>Polymorphism allows objects to respond differently to the same message. This supports generic code that adapts to object types automatically.</p></figcaption></figure>

### Summary

Polymorphism allows different object types to respond to the same message with behaviour suited to their class. This simplifies code, improves flexibility, and supports the development of scalable systems. In Python, this is typically achieved through method overriding in subclass hierarchies.
