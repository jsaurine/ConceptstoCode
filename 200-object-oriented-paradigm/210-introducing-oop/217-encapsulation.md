---
description: >-
  Understand how encapsulation protects data and helps organise code in
  object-oriented programs.
---

# 217 Encapsulation

### Overview

In this topic, we explore **encapsulation**, a key principle of object-oriented programming (OOP). Encapsulation refers to the practice of keeping an object’s internal data private and exposing only carefully controlled methods for accessing or modifying it. This promotes code safety, simplifies maintenance, and reinforces logical boundaries between different parts of a program.

### Targets

In this topic, students learn to:

* Define encapsulation and explain its purpose in OOP
* Use access modifiers to hide and protect class attributes
* Understand how encapsulation relates to class structure and design
* Recognise the benefits of encapsulation for security and maintainability
* Interpret how encapsulation is represented in class diagrams

### Syllabus references

<details>

<summary><a href="https://curriculum.nsw.edu.au/learning-areas/tas/software-engineering-11-12-2022/content/year-11/f796d35e-3125-4824-ae92-427ee7048659"><strong>The object-oriented paradigm</strong></a></summary>

**Encapsulation**

* Explain the concept of encapsulation in object-oriented programming
* Demonstrate how encapsulation is used to protect the internal state of an object

</details>

### What is encapsulation?

Encapsulation means **bundling data (attributes) and methods into a class**, and **restricting direct access to that data** from outside the class.

This is usually done by:

* Making attributes **private** or **protected**
* Providing **public methods** to read or update the data

This ensures that internal data can only be changed in controlled ways, reducing bugs and protecting program logic.

#### Example: Python class using encapsulation

```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance  # private attribute

    def deposit(self, amount):
        if amount > 0:
            self.__balance += amount

    def get_balance(self):
        return self.__balance
```

Here, `__balance` is a **private variable**. It cannot be accessed directly (`account.__balance` will raise an error). Instead, all changes must go through methods like `deposit()` and `get_balance()`.

### Why use encapsulation?

* **Protects internal logic** – prevents external code from breaking class behaviour
* **Improves maintainability** – changes to internal structure don't affect the interface
* **Supports secure coding** – sensitive data is hidden from external access
* **Enforces rules** – all changes go through validation (e.g. deposits must be positive)

Encapsulation makes it easier to test, debug, and update code over time.

### Access modifiers and attribute access

In Python, access modifiers are by convention:

| Modifier  | Syntax      | Access level                                            |
| --------- | ----------- | ------------------------------------------------------- |
| Public    | `balance`   | Accessible from anywhere                                |
| Protected | `_balance`  | Accessible within the class or subclass (by convention) |
| Private   | `__balance` | Name-mangled to prevent external access                 |

Even private attributes can technically be accessed using name mangling (e.g. `_BankAccount__balance`), but this breaks encapsulation and is not recommended.

### Encapsulation in class diagrams

In **UML class diagrams**, encapsulated attributes are marked with visibility indicators:

* `+` public
* `-` private (accessible from inside the class and sub-classes)
* `#` protected (accessible from inside the class only)

**Example:**

```
--------------------------
|    BankAccount         |
--------------------------
| - balance: float       |
--------------------------
| + deposit(amount)      |
| + get_balance(): float |
--------------------------
```

Class diagrams show encapsulated attributes using `-` for private and `+` for public methods.\


### Summary

Encapsulation hides an object’s internal state and forces all access to go through controlled methods. This improves security, reduces bugs, and supports clean, modular design. By using private attributes and public interfaces, developers can create reliable, reusable components that are easy to maintain and understand.
