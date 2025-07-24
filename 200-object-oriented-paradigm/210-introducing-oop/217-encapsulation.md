---
description: >-
  Understand how encapsulation protects data and helps organise code in
  object-oriented programs.
---

# 217 Encapsulation

### Objectives

* Define encapsulation and explain its purpose in OOP
* Use access modifiers to hide data and control object behaviour
* Identify how encapsulation improves maintainability and security

### What is encapsulation?

**Encapsulation** means bundling data (attributes) and the methods that operate on them into a single unit — the class — and restricting direct access to that data from outside the class.

This helps protect the internal state of objects and controls how data is changed.

#### Example:

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

* `__balance` is a **private** variable
* It cannot be accessed directly (`account.__balance` fails)
* Changes must go through methods like `deposit()` or `get_balance()`

### Why use encapsulation?

* Prevents external code from breaking internal logic
* Makes programs easier to understand and maintain
* Supports secure coding practices by hiding sensitive data
