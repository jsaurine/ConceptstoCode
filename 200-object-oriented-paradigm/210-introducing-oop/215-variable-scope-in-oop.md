---
description: >-
  Object-oriented programming and classes introduce a third level of scope,
  typically called object scope, though sometimes referred to as class scope.
---

# 215 Variable scope in OOP

In procedural programming, there are two principal levels of scope: variables created in the main code have a global scope and are available anywhere in a program, while variables created inside a function have a local scope and only live as long as the function runs. When the function exits, all local variables (variables with local scope) literally disappear.&#x20;

Object-oriented programming and classes introduce a third level of scope, typically called object scope, though sometimes referred to as class scope or more rarely as instance scope. They all mean the same thing: the scope consists of all the code inside the class definition. Methods can have both local variables and instance variables. In a method, any variable whose name does not start with self. is a local variable and will go away when that method exits, meaning other methods within the class can no longer use that variable. Instance variables have object scope, which means they are available to all methods defined in a class. Instance variables and object scope are the keys to understanding how objects remember data.

> <mark style="color:green;">**instance variable**</mark>
>
> In a method, any variable whose name begins, by convention, with the prefix self (for example, `self.x`). Instance variables have object scope.

Like local and global variables, instance variables are created when they are first given a value and do not need any special declaration. The `init()` method is the logical place to initialise instance variables. Here is an example of a class where the `init()` method initialises an instance variable `self.count` (read as “self dot count”) to zero and another method, `increment()`, which adds 1 to `self.count`:

```python
class MyClass():
    def __init__(self):
        self.count = 0 # create self.count and set it to 0
        
    def increment(self):
        self.count = self.count + 1 # increment the variable
```

When you instantiate an object from the `MyClass` class, the `init()` method runs and sets the value of the instance variable `self.count` to zero. If you then call the `increment()` method, the value of `self.count` goes from zero to one. If you call `increment()` again, the value goes from one to two, and on and on. Each object created from a class gets its own set of instance variables, independent of any other objects instantiated from that class.&#x20;

In the case of the `LightSwitch` class (reproduced below), there is only one instance variable, `self.switchIsOn`, so every LightSwitch object will have its own `self.switchIsOn`. Therefore, you can have multiple `LightSwitch` objects, each with its own independent value of `True` or `False` for its `self.switchIsOn` variable.

{% code title="lightSwitch.py" %}
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
oLightSwitch = LightSwitch()  # create a LightSwitch object

#  Calls to methods
oLightSwitch.show() # call the show method of oLightSwitch
oLightSwitch.turnOn() # call the turnOn method of oLightSwitch
oLightSwitch.show()
oLightSwitch.turnOff() # call the turnOff method of oLightSwitch
oLightSwitch.show()
oLightSwitch.turnOn() # call the turnOn method of oLightSwitch
oLightSwitch.show()
```
{% endcode %}

### Comparing Functions and Methods

To recap, there are three key differences between a function and a method:

1. All methods of a class must be indented under the class statement.
2. All methods have a special first parameter that (by convention) is named self.
3. Methods in a class can use instance variables, written in the form `self.`. Now that you know what methods are, we will see you how to create an object from a class and how to use the different methods that are available in a class.

***

### Review questions

1. In procedural programming, what are the two main types of variable scope?
2. What is object scope in OOP, and what type of variable has object scope?
3. In a method, how can you tell the difference between a local variable and an instance variable?
4. Compare what happens to local and instance variables after a method exits.
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

6. Write a class called `Counter` that starts with a count of 10 and has a method `addFive()` that adds 5 to the count.
7. Why can two different `LightSwitch` objects have different values for `switchIsOn` at the same time?
