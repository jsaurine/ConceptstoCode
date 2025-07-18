# 214 Creating objects from a class

1. What does the term instantiation mean in object-oriented programming?

<details>

<summary>Show solution</summary>

Instantiation is the process of creating an object (or instance) from a class. It involves using the class as a blueprint to create a working object that has its own data and can perform behaviours defined in the class.

</details>

2. In the LightSwitch example, what does `oLightSwitch = LightSwitch()` do?

<details>

<summary>Show solution</summary>

This statement creates a new `LightSwitch` object (an instance of the `LightSwitch` class) and assigns it to the variable `oLightSwitch`.

</details>

3. Explain the difference between a class and an object using the `LightSwitch` example.

<details>

<summary>Show solution</summary>

The `LightSwitch` class defines what data (state) and behaviours (methods) a light switch will have. An object, like `oLightSwitch`, is a specific instance of the class that contains its own data and can perform the behaviours defined by the class.

</details>

4. Write a Python line of code that creates a third LightSwitch object called `oLightSwitch3`.

<details>

<summary>Show solution</summary>

`oLightSwitch3 = LightSwitch()`

</details>

5. If `oLightSwitch1` and `oLightSwitch2` are both instances of LightSwitch, what happens to `oLightSwitch2.switchIsOn` when you call `oLightSwitch1.turnOn()`?

<details>

<summary>Show solution</summary>

Nothing happens to `oLightSwitch2.switchIsOn`. Each object has its own copy of `switchIsOn`, so calling `turnOn()` on `oLightSwitch1` only affects its own `switchIsOn` value.

</details>

5. Look at this code and predict what will be printed:

{% code lineNumbers="true" %}
```python
class LightSwitch():
    def __init__(self):
        self.switchIsOn = False

    def turnOn(self):
        # turn the switch on 
         self.switchIsOn = True

    def turnOff(self):
        # turn the switch off
         self.switchIsOn = False

    def show(self):  # added for testing
        print(self.switchIsOn)
    
# Main code
oLightSwitch1 = LightSwitch()
oLightSwitch2 = LightSwitch()
oLightSwitch1.turnOn()
oLightSwitch1.show()
oLightSwitch2.show()
```
{% endcode %}

<details>

<summary>Show solution</summary>

The output will be:

```
True
False
```

`oLightSwitch1` was turned on, so its `switchIsOn` is `True`. `oLightSwitch2` was not turned on, so its `switchIsOn` remains `False`.

</details>

7. Write a short code snippet that creates two `LightSwitch` objects, turns one on, and prints the state of both.

<details>

<summary>Show solution</summary>

```python
oLightSwitch1 = LightSwitch()
oLightSwitch2 = LightSwitch()
oLightSwitch1.turnOn()
oLightSwitch1.show()
oLightSwitch2.show()
```

</details>
