---
hidden: true
---

# 164 Clearance / Solutions

<details>

<summary>1. What is a control structure?</summary>

A control structure is a programming construct that determines the flow of execution in a program. It allows the program to decide the order in which instructions are run, handle decisions, and repeat tasks.

</details>

<details>

<summary>2. Difference between sequence, selection, and repetition</summary>

\- Sequence: Instructions executed one after another.\
\- Selection: Conditional branching (e.g., if-else).\
\- Repetition: Looping until a condition is met (e.g., while, for).

</details>

<details>

<summary>3. Pseudocode: Check positive, negative, or zero</summary>

```
BEGIN
    INPUT number
    IF number > 0 THEN
        OUTPUT "Positive"
    ELSEIF number < 0 THEN
        OUTPUT "Negative"
    ELSE
        OUTPUT "Zero"
    ENDIF
END
```

</details>

<details>

<summary>4. Python: Check positive, negative, or zero</summary>

```python
number = int(input("Enter a number: "))
if number > 0:
    print("Positive")
elif number < 0:
    print("Negative")
else:
    print("Zero")
```

</details>

<details>

<summary>5. Binary vs multi-way selection</summary>

\- Binary: Two options (if-else).\
\- Multi-way: More than two options (if-elif-else or switch/case).

</details>

<details>

<summary>6. Python grade assignment</summary>

```python
score = int(input("Enter score: "))
if score >= 90:
    print("A")
elif score >= 80:
    print("B")
elif score >= 70:
    print("C")
elif score >= 60:
    print("D")
else:
    print("F")
```

</details>

<details>

<summary>7. When to use while vs for</summary>

\- Use `while` when you don’t know how many iterations (condition-controlled).\
\- Use `for` when you know how many iterations (count-controlled).

</details>

<details>

<summary>8. Pseudocode: Sum until -1</summary>

```
BEGIN
    SET sum = 0
    REPEAT
        INPUT number
            IF number != -1 THEN
                sum = sum + number
            ENDIF
    UNTIL number = -1
    OUTPUT sum
END
```

</details>

<details>

<summary>9. Python: Sum until -1</summary>

```python
sum = 0
while True:
    number = int(input("Enter number (-1 to stop): "))
    if number == -1:
        break
    sum += number
print("Total:", sum)
```

</details>

<details>

<summary>10. Post-test loop simulation in Python</summary>

Use `while True` with `break` to ensure the body runs at least once (post-test loop).

</details>

<details>

<summary>11. Break vs continue</summary>

\- `break`: Exits the loop entirely.\
\- `continue`: Skips to the next iteration.

</details>

<details>

<summary>12. Pseudocode: Menu-driven program</summary>

```
BEGIN
    REPEAT
    DISPLAY menu
    INPUT choice
    IF choice = 1 THEN
        PROCESS option 1
    ELSEIF choice = 2 THEN
        PROCESS option 2
    ELSEIF choice = 3 THEN
        PROCESS option 3
    UNTIL choice = exit
END
```

</details>

<details>

<summary>13. Python: Menu-driven program</summary>

```python
while True:
    print("1. Option 1\n2. Option 2\n3. Option 3\n4. Exit")
    choice = input("Select: ")
    if choice == "1":
        print("Option 1 selected")
    elif choice == "2":
        print("Option 2 selected")
    elif choice == "3":
        print("Option 3 selected")
    elif choice == "4":
        print("Exiting...")
        break
    else:
        print("Invalid choice")
```

</details>

<details>

<summary>14. Common testing errors</summary>

\- Off-by-one errors.\
\- Incorrect conditional logic.\
\- Infinite loops.

</details>

<details>

<summary>15. Benefits of pseudocode and flowcharts</summary>

They help clarify logic, identify edge cases, and simplify debugging by providing a clear plan before coding.

</details>
