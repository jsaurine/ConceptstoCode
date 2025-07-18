---
description: Here, we will learn how to name and define a class in Python.
---

# 213 Creating classes

Let’s discuss the different parts of a class and the details of instantiating and using an object. The code below shows the general form of a class in Python.

<pre class="language-python"><code class="lang-python">class &#x3C;ClassName>():
    def __init__(self, &#x3C;optional param1>, ..., &#x3C;optional paramN>):
        # any initialisation code here
        
    # Any number of functions that access the data
    # Each has the form:
    
    def &#x3C;functionName1>(self, &#x3C;optional param1>, ..., &#x3C;optional paramN>):
        # body of function
        
        # ... more functions
    
    def &#x3C;functionNameN>(self, &#x3C;optional param1>, ..., &#x3C;optional paramN>):
<strong>        # body of function
</strong></code></pre>

A class definition begins with a class statement specifying the name you want to give the class. The convention for class names is to use camel case, with the first letter uppercase (for example, `LightSwitch`).&#x20;

Following the name you can optionally add a set of parentheses, but the statement must end with a colon to indicate that you’re about to begin the body of the class.&#x20;

Within the body of the class, you can define any number of functions. All the functions are considered part of the class, and the code that defines them must be indented. Each function represents some behaviour that an object created from the class can perform. All functions must have at least one parameter, which, by convention, is named `self`. OOP functions are referred to as **methods**.

> <mark style="color:green;">**method**</mark>
>
> A function defined inside a class. A method always has at least one parameter, which is usually named self.

The first method in every class should have the special name **init**. This method will run automatically whenever you create an object from a class. Therefore, this method is the logical place to put any initialisation code you want to run whenever you instantiate an object from a class. Python reserves the name init for this task, and it must be written exactly this way, with two underscores before and after the word init (which must be lowercase). In reality, the `init()` method is not strictly required. However, it’s generally considered good practice to include and use it for initialisation.

***

### Review Questions

1. What naming convention is typically used for class names in Python?
2. What does the colon at the end of a class statement indicate in Python?
3. Define a method in Python and describe its characteristics.
4. What is the purpose of the init method in a class?
5. Is the `init` method required in every Python class? Why might you include it anyway?
