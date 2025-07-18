# 215 Variable scope in OOP

1. In procedural programming, what are the two main types of variable scope?

<details>

<summary>Show solution</summary>

The two main types are **global scope**, where variables are available throughout the program, and **local scope**, where variables exist only within a function and disappear when the function exits.

</details>

2. What is object scope in OOP, and what type of variable has object scope?

<details>

<summary>Show solution</summary>

Object scope refers to variables that are available to all methods of an object — these are called **instance variables**. They are prefixed with `self.#` (e.g. `self.count`) and belong to the object rather than just a single method.

</details>

3. In a method, how can you tell the difference between a local variable and an instance variable?

<details>

<summary>Show solution</summary>

A local variable **does not** begin with `self.#` and only exists while the method runs. An instance variable **does** begin with `self.#` and is available to all methods of the object.

</details>

4. Compare what happens to local and instance variables after a method exits.

<details>

<summary>Show solution</summary>

When a method exits:

* **Local variables** disappear. They are deleted from memory and can no longer be accessed by any method of the object.
* **Instance variables** (those prefixed with `self.#`) remain. They continue to exist as part of the object and can be accessed or modified by other methods of that object.

</details>

5. Given this code, what will `obj.count` print after both increment calls?

{% code lineNumbers="true" %}
```python
class MyClass():
    def init(self):
        self.count = 0
    
    def increment(self):
        self.count = self.count + 1

obj = MyClass()
obj.increment()
obj.increment()

print(obj.count)
```
{% endcode %}

<details>

<summary>Show solution</summary>

It will print `2`, because `self.count` starts at 0 and is increased by 1 each time `increment()` is called.

</details>

6. Write a class called `Counter` that starts with a count of 10 and has a method `addFive()` that adds 5 to the count.

<details>

<summary>Show solution</summary>

```python
class Counter:
    def __init__(self):
        self.count = 10
    def addFive(self):
        self.count += 5
```

</details>

7. Why can two different `LightSwitch` objects have different values for `switchIsOn` at the same time?

<details>

<summary>Show solution</summary>

Because each `LightSwitch` object has its own separate instance variable `self.switchIsOn`. The state of one switch does not affect the state of another.

</details>
