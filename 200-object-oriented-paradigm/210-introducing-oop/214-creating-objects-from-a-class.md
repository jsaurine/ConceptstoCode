---
description: >-
  In Python, a class is code that defines what an object will remember (its data
  or state) and what it will be able to do (its functions or behaviour).
  Creating an object from a class is instantiation.
---

# 214 Creating objects from a class

> <mark style="color:green;">**ss**</mark>
>
> Code that defines what an object will remember (its data or state or attributes) and the things that it will be able to do (its functions or behaviour).

To get a feel for what a class looks like, here is the code of a light switch written as a class:

{% code title="lightSwitch.py" lineNumbers="true" %}
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
# oLightSwitch is used here to distinguish between the class name and the object name
oLightSwitch = LightSwitch()  # Create a LightSwitch object

#  Calls to methods
oLightSwitch.show() # Call the show method of oLightSwitch
oLightSwitch.turnOn() # Call the turnOn method of oLightSwitch
oLightSwitch.show()
oLightSwitch.turnOff() # Call the turnOff method of oLightSwitch
oLightSwitch.show()
oLightSwitch.turnOn() # Call the turnOn method of oLightSwitch
oLightSwitch.show()
```
{% endcode %}

We’ll go through the details in just a bit, but the things to notice are that this code defines a single variable, `self.switchIsOn`, which is initialised in one function and contains two other functions for the behaviours `turnOn()` and `turnoff()`.

If you write the code of a class and try to run it, nothing happens, like when you run a Python program that consists of only functions and no function calls. You have to tell Python to make an explicit object from the class.

To create a LightSwitch object from our LightSwitch class, we typically use a line like this:

```
oLightSwitch = LightSwitch()
```

This says: find the `LightSwitch` class, create a `LightSwitch` object from that class, and assign the resulting object to the variable `oLightSwitch`.

Another word you’ll encounter in OOP is instance. The words instance and object are essentially interchangeable; however, to be precise, we would say that a `LightSwitch` object is an instance of the `LightSwitch class`.

> <mark style="color:green;">**instantiation**</mark>
>
> The process of creating an object from a class

The previous assignment statement used the instantiation process to create a `LightSwitch` object from the `LightSwitch` class. We can also use this as a verb; we instantiate a `LightSwitch` object from the `LightSwitch` class.

### Creating multiple instances of the same class

One of the key features of OOP is that you can instantiate as many objects as you want from a single class. Creating more objects from the class is illustrated below.

```python
oLightSwitch1 = = LightSwitch() # Creates a light switch object
oLightSwitch2 = = LightSwitch() # Creates another light switch object
```

The important point here is that each object created from a class maintains _**its own version of the data**_. In this case, `oLightSwitch1` and `oLightSwitch2` each have their own instance `self.switchIsOn` instance variable, `self.SwitchIsOn`. Any changes made to the data of one object will not affect the data of other objects. Methods in the class can be called on specific objects.

Calling methods of different objects is illustrated at [216-calling-methods.md](216-calling-methods.md "mention").

### Review questions

***

1. What does the term instantiation mean in object-oriented programming?
2. In the LightSwitch example, what does `oLightSwitch = LightSwitch()` do?
3. Explain the difference between a class and an object using the LightSwitch example.
4. Write a Python line of code that creates a third LightSwitch object called `oLightSwitch3`.
5. If `oLightSwitch1` and `oLightSwitch2` are both instances of LightSwitch, what happens to `oLightSwitch2.switchIsOn` when you call `oLightSwitch1.turnOn()`?
6. Look at this code and predict what will be printed:

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

7. Write a short code snippet that creates two LightSwitch objects, turns one on, and prints the state of both.
