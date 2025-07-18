---
description: >-
  In this section, we introduce the general concepts behind object-oriented
  programming with a simple procedural example for comparison.
---

# 211 Procedural comparison

We often reference attributes to describe a physical object in our everyday world. When discussing a desk, you might describe its colour, dimensions, weight, material, etc. Some objects have attributes that apply only to them and not others. A car could be described by its number of doors, but a shirt could not. A box could be sealed or open, empty or full, but those characteristics would not apply to a wood block. Additionally, some objects are capable of performing actions. A car can go forward, back up, and turn left or right, but it wouldn’t be sensible to describe the actions of a wood block in the same way.

To model a real-world object in code, we must decide what data will represent that object’s attributes and what operations it can perform. These two concepts are often referred to as an object’s state and behaviour, respectively:

* the **state** is the data that the object remembers and
* the **behaviours** (or methods) are the actions that the object can do.

### State and Behaviour: Light Switch Example

The code illustrated below is a software model of a standard two-position light switch written in procedural Python. This is a trivial example, but it will demonstrate state and behaviour.

{% embed url="https://gist.github.com/jsaurine/1e02f28a314df61d584acdd27836024e" %}
A model of a light switch writeen in procedural code
{% endembed %}

The switch can only be in one of two positions: on or off. To model the state, we only need a single Boolean variable. We name this variable `switchIsOn` , and we say that `True` means on and False indicates off. When the switch comes from the factory, it is in the off position, so we initially set `switchIsOn` to `False`.&#x20;

Next, we look at the behaviour. This switch can only perform two actions: 'turn on' and 'turn off'. We, therefore, build two functions, `turnOn()` `and turnOff()`, which sets the value of the single Boolean variable to `True` and `False`, respectively. Some test code is added at the end to turn the switch on and off a few times. The output is exactly what we would expect:&#x20;

```
False
True
False
True
```

This is an extremely simple example, but starting with small functions like these makes the transition to an OOP approach easier. As explained previously, using a global variable to represent the state (in this case, the variable `switchIsOn`), makes this code only work for a single light switch.&#x20;

Next, we'll rebuild the light switch code using object-oriented programming, but we must first work through some of the underlying theory.

***

### Review Questions

1. In the light switch example, what variable represents the _state_ of the light switch?
2. What is meant by _behaviour_ in the context of the procedural light switch example?
3. Why is it necessary to use two separate functions (turnOn() and turnOff()) in the procedural version of the light switch?
4. What is the initial state of the light switch when it comes from the factory, according to the example? How is this represented in code?
5. What limitations would you encounter if you wanted to use this procedural code to model multiple light switches?
6. How does the use of a global variable affect the flexibility of the procedural code?
7. Imagine you want to add a new function to the procedural light switch code that toggles the switch (switching from on to off or off to on). How might you write that function?
8. How might combining the state and behaviour of the light switch into one structure (like a class) solve the limitations you identified?
