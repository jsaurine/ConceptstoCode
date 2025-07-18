# 211 Procedural comparison

1. In the light switch example, what variable represents the state of the light switch?

<details>

<summary>Show solution</summary>

The variable `switchIsOn` represents the state of the light switch. It is a Boolean variable that is `True` when the switch is on and False when it is off.

</details>

2. What is meant by behaviour in the context of the procedural light switch example?

<details>

<summary>Show solution</summary>

Behaviour refers to the actions the light switch can perform — turning on and turning off. These are represented in the code as the functions `turnOn()` and `turnOff()`.

</details>

3. Why is it necessary to use two separate functions , `(turnOn()` and `turnOff()`, in the procedural version of the light switch?

<details>

<summary>Show solution</summary>

Each function performs a distinct operation on the global variable \`switchIsOn\`. \`turnOn()\` sets it to \`True\`, and \`turnOff()\` sets it to \`False\`. Since state and behaviour are separate, separate functions are needed to change the state.

</details>

4. What is the initial state of the light switch when it comes from the factory, according to the example? How is this represented in code?

<details>

<summary>Show solution</summary>

The initial state is off, represented by setting \`switchIsOn = False\` at the start of the program.

</details>

5. What limitations would you encounter if you wanted to use this procedural code to model multiple light switches?

<details>

<summary>Show solution</summary>

The code utilises a single global variable to store the state. To model multiple switches, you would need multiple global variables or more complex data structures, which would make the code harder to manage and extend.

</details>

6. How does the use of a global variable affect the flexibility of the procedural code?

<details>

<summary>Show solution</summary>

It limits flexibility because all functions depend on and modify the same shared variable. This makes it difficult to extend the code to handle multiple switches or more complex behaviour.

</details>

7. Imagine you wanted to add a new function to the procedural light switch code to toggle the switch (switch from on to off or off to on). How might you write that function?

<details>

<summary>Show solution</summary>

```python
def toggle():
    global switchIsOn
    switchIsOn = not switchIsOn
```

This function reverses the current state of the switch.

</details>

8. How might combining the state and behaviour of the light switch into one structure (like a class) solve the limitations you identified?

<details>

<summary>Show solution</summary>

Combining state and behaviour into a class allows each light switch to have its own state and associated behaviours. This makes it easy to create multiple independent switches, improving scalability and maintainability.

</details>
