---
description: >-
  In this section, you will learn how to create objects from a class and call
  their methods, seeing how each object maintains its own independent data and
  behaviour.
---

# 216 Calling methods

We have seen that a class defines what an object will look like. To use a class, you have to tell Python to make an object from the class. The typical way to do this is to use an assignment statement like this:

```
<object> = <ClassName>(<optional arguments>)
```

This single line of code invokes a sequence of steps that ends with Python handing you back a new class instance, which you typically store into a variable. That variable then refers to the resulting object.

A class can be made available in two ways: the code of the class can be placed in the same file with the main program, or you can put the code of the class in an external file and use an import statement to bring in the contents of the file. This section will look at the first approach of keeping the class definition in the main code. **The only rule is that the class definition must precede any code that instantiates an object from the class.**

### **Calling Methods of An Object**

After creating an object from a class, to call a method of the object, you use the generic syntax:

```
<object>.<methodName>(<any arguments>)
```

The code below contains the `LightSwitch` class, code to instantiate an object from the class, and code to turn that `LightSwitch` object on and off by calling its `turnOn()` and `turnOff()` methods.

{% code title="lightSwitchWithTestCode.py" lineNumbers="true" %}
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
    
    def show(self): 
        # added for testing
        print(self.switchIsOn)
    
    # Main code
    
    oLightSwitch = LightSwitch() # create a LightSwitch object
    
    # Calls to methods
    oLightSwitch.show()
    oLightSwitch.turnOn()
    oLightSwitch.show()
    oLightSwitch.turnOff()
    oLightSwitch.show()
    oLightSwitch.turnOn()
    oLightSwitch.show()
```
{% endcode %}

First, we create a `LightSwitch` object and assign it to the `oLightSwitch` variable. We then use that variable to call other methods available in the `LightSwitch` class. We would read these lines as 'oLightSwitch dot show', 'oLightSwitch dot turnOn' and so on. If we run this code, it will output:

```
False
True
False
True
```

Recall that this class has a single instance variable named `self.switchIsOn`, but its value is remembered and easily accessed when different methods of the same object run.

### Creating Multiple Instances from the Same Class

One of the key features of OOP is that you can instantiate as many objects as you want from a single class, in the same way that you can make endless cakes from a cupcake pan. So, if you want two light switch objects, or three, or more, you can just create additional objects from the LightSwitch class like so:

```
oLightSwitch1 = LightSwitch() # create a light switch object
oLightSwitch2 = LightSwitch() # create another light switch object
```

The critical point is that each object you create from a class maintains its own version of the data. In this case, `oLightSwitch1` and `oLightSwitch2` each has its own instance variable, `self.switchIsOn`. Any changes you make to one object's data will not affect another object's data. You can call any of the methods in the class with either object.&#x20;

The example below creates two light switch objects and calls methods on the different objects.

{% code title="LightSwitchTwoInstances.py" lineNumbers="true" %}
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
oLightSwitch1 = LightSwitch()  # create a LightSwitch object
oLightSwitch2 = LightSwitch()  # create another LightSwitch object

#  Test code
oLightSwitch1.show()
oLightSwitch2.show()
oLightSwitch1.turnOn() # Turn switch 1 on
# Switch 2 is off at the start but to be clearer
oLightSwitch1.turnOff()
oLightSwitch1.show()
oLightSwitch2.show()
```
{% endcode %}

Here’s the output when this program is run:&#x20;

```
False
False
True
False
```

The code tells `oLightSwitch1` to turn itself on and `oLightSwitch2` to turn itself off. Notice that the code in the class has no global variables. Each `LightSwitch` object gets its own set of instance variables (just one in this case) defined in the class. While this may not seem like a huge improvement over having two simple global variables that could be used to do the same thing, the implications of this technique are enormous for coding larger projects.

### Review questions

***

1. What is the generic syntax for calling a method on an object in Python?
2. Why must the class definition appear before any code that creates objects from it?
3. What happens to `oLightSwitch1.switchIsOn` and `oLightSwitch2.switchIsOn` in the following code?

```python
oLightSwitch1 = LightSwitch()
oLightSwitch2 = LightSwitch()
oLightSwitch1.turnOn()
oLightSwitch1.show()
oLightSwitch2.show()
```

4. How does the use of instance variables in the `LightSwitch` class help when working with multiple objects?
5. Write Python code to create two `LightSwitch` objects. Turn the first one on and leave the second one off. Print the state of both switches.
6. Why is it better to use objects with instance variables instead of using multiple global variables in larger projects?
