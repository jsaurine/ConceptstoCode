# 216 Calling methods

1. What is the generic syntax for calling a method on an object in Python?

<details>

<summary>Show solution</summary>

The syntax is `.()`. For example: `oLightSwitch.turnOn()`.

</details>

2. Why must the class definition appear before any code that creates objects from it?

<details>

<summary>Show solution</summary>

Because Python needs to know what the class is (its structure and methods) before it can create objects (instances) from it. If the class were undefined at the time of instantiation, Python would raise an error.

</details>

3. What happens to `oLightSwitch1.switchIsOn` and `oLightSwitch2.switchIsOn` in the following code?

```python
oLightSwitch1 = LightSwitch()
oLightSwitch2 = LightSwitch()
oLightSwitch1.turnOn()
oLightSwitch1.show()
oLightSwitch2.show()
```

<details>

<summary>Show solution</summary>

`oLightSwitch1.switchIsOn` becomes `True` after `turnOn()` is called, so `oLightSwitch1.show()` prints `True`. `oLightSwitch2.switchIsOn` remains `False`, so `oLightSwitch2.show()` prints `False`.

</details>

4. How does the use of instance variables in the `LightSwitch` class help when working with multiple objects?

<details>

<summary>Show solution</summary>

Each object (instance) has its own separate copy of the instance variables (like `switchIsOn`). This means the state of one object does not affect the state of another, making the program easier to manage and scale.

</details>

5. Write Python code to create two `LightSwitch` objects. Turn the first one on and leave the second one off. Print the state of both switches.

<details>

<summary>Show solution</summary>

```
oLightSwitch2 = LightSwitch()
oLightSwitch2 = LightSwitch()
oLightSwitch1.turnOn()
oLightSwitch1.show()
oLightSwitch2.show()
```

</details>

6. Why is it better to use objects with instance variables instead of using multiple global variables in larger projects?

<details>

<summary>Show solution</summary>

Objects with instance variables keep data and behaviour bundled together, reducing the risk of unintended interactions and making the code more modular, scalable, and easier to maintain. This is especially important in larger projects with many entities.

</details>
