# Tutorial / Algorithms

## Question 1

State characteristics of a good algorithm.

### Question 2

What are the advantages of using pseudocode before implementing an algorithm in a programming language?

### Question 3

Explain how a flowchart could help identify logic errors in an algorithm before testing it in code.

### Question 4

How does the divide and conquer approach simplify the problem-solving process in software design? Provide a real-world example.

### Question 5

What are the key differences between desk checking and using a trace table, and when might you use each?

### Question 6

A Fibonacci series is a sequence of numbers where each is the sum of the two preceding numbers.

```
0, 1, 1, 2, 3, 5, 8, 13, 21, 34 and so on
```

Write an algorithm in which a user enters a number stored in the variable `num`. The algorithm prints all the numbers in the Fibonacci series less than or equal to the variable `num`.&#x20;

Prepare your algorithm in pseudocode and test it with a trace table.

### Question 7

Modify and test the algorithm you wrote in Question 6, in which a user is asked to enter the number of terms of the Fibonacci series to be printed.

### Question 8

Deduce the purpose of the Python program given by using a trace table.

```python
num1 = int(input("Enter the first number: "))
num2 = int(input("Enter the second number: "))

if num1 > num2:
    x = num1
else:
    x = num2

while True:  # Infinite loop until the break is hit
    if x % num1 == 0 and x % num2 == 0:
        print(x)
        break
    x = x + 1
```

### Question 9

Deduce the purpose of the Python program given by using a trace table.

```
BEGIN
  total = 0
  FOR i = 1 TO 5
    IF i MOD 2 = 0 THEN
      total = total + i * 2
    ELSE
      total = total + i
    ENDIF
  NEXT i
  OUTPUT total
END
```

### Question 10

Trace the algorithm below to identify why it does not work with the array `alpha_part`.

<pre><code>BEGIN
    alpha_part = [F, I, G, L, J, K, I, H]

    item = “J”
    lower_bound = 0
    upper_bound = LENGTH(alpha_part) - 1
    found = False

    WHILE found = False AND lower_bound &#x3C;= upper_bound
        midpoint = (lower_bound + upper_bound) DIV 2
        
        IF alpha_part[midpoint] = item THEN
            found = True
<strong>        ELSEIF
</strong><strong>            alpha_part[midpoint] &#x3C; item THEN
</strong>            lower_bound = midpoint + 1
        ELSE
            upper_bound = midpoint - 1
        ENDIF
<strong>    ENDWHILE
</strong>
<strong>    IF (found = True) THEN
</strong>        PRINT (“Item found at ”, midpoint)
<strong>    ELSE
</strong>        PRINT (“Item not present”)
    ENDIF
END
</code></pre>

