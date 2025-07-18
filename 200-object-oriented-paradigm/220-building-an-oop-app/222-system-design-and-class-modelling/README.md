---
description: >-
  This module develops the object-oriented system design for the Task Tracker
  app, including identification of core classes, attributes, and behaviours.
---

# 222 System design and class modelling

### **Outline**

This stage focuses on analysing the problem from a systems perspective and identifying the types of objects needed to model it. The design process begins with identifying responsibilities, selecting relevant data, and deciding on how objects will interact. Classes are defined by their attributes (what they remember) and methods (what they can do). A class diagram is used to represent the system's structure before coding begins.

### **Targets**

In this topic, students learn to:

* Recognise how object-oriented thinking is applied during software design
* Identify the responsibilities of each class based on user stories
* Define attributes and methods for core classes
* Use class diagrams to model the structure and relationships within a system

### **Glossary**

| Term               | Definition                                                                                                       |
| ------------------ | ---------------------------------------------------------------------------------------------------------------- |
| **Class**          | A blueprint that defines the data (attributes) and behaviour (methods) of an object.                             |
| **Attribute**      | A piece of data stored in an object that represents part of its state.                                           |
| **Method**         | A function defined inside a class that represents an action the object can perform.                              |
| **Class diagram**  | A visual representation showing the classes in a system, including their attributes, methods, and relationships. |
| **Responsibility** | A description of what a class is in charge of managing or doing within the system.                               |

### **Overview**

To structure the app effectively, two main classes are introduced:

* A `Task` class that models an individual task (title, description, due date, completion status)
* A `TaskManager` class that stores and manages a collection of tasks and provides user-facing behaviours (e.g. adding, listing, filtering tasks)

These classes are designed using the principle of separation of concerns. The `Task` class is responsible for remembering task details and updating its own status. The `TaskManager` class acts as a controller, coordinating the creation and retrieval of tasks and handling broader functionality.

A class diagram is produced to document the design before implementation begins. This diagram makes it easier to visualise how each object will behave and interact with others in the system.
