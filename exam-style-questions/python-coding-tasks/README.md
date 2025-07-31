---
description: Try these Python coding tasks
---

# Python coding tasks

### **Task 1 – Quiz score tracker**

**Difficulty:** Easy\
**Duration:** \~20–25 minutes\
**Concepts:** Control structures, simple data types, functions

**Scenario:**\
Create a quiz score tracker that asks the user five yes/no questions and reports their total score.

**Requirements:**

* Use a `while` or `for` loop to cycle through five predefined questions.
* Accept `'yes'` or `'no'` answers only (with validation).
* Use a function `ask_question(prompt, correct_answer)` that returns `True` or `False`.
* At the end, print the number of correct answers.

**Sample input/output:**

```
Question 1: Is Python case-sensitive? (yes/no): yes  
Correct!

Question 2: Does 2+2 equal 5? (yes/no): no  
Correct!

You scored 2/2 correct.
```

***

### **Task 2 – Movie ratings menu system**

**Difficulty:** Moderate\
**Duration:** \~30–35 minutes\
**Concepts:** Control structures, structured data types (list of dictionaries), functions

**Scenario:**\
Design a menu-driven program that allows the user to:

1. Add a new movie and rating (1–5)
2. List all movies and ratings
3. Show the average rating
4. Exit

**Requirements:**

* Use a `while` loop to repeat the menu until the user chooses to exit.
* Store movies as a list of dictionaries: `{"title": "Movie", "rating": 4}`
* Include input validation for menu choices and ratings (must be an integer between 1 and 5).
* Use functions: `add_movie(movies)`, `list_movies(movies)`, `average_rating(movies)`

**Extension idea:**\
Save the list to a text file at exit.

***

### **Task 3 – Simple transaction ledger**

**Difficulty:** Advanced\
**Duration:** \~40–50 minutes\
**Concepts:** Control structures, file handling, functions, global/local variables, lists

**Scenario:**\
Build a simple transaction tracker for income and expenses.

**Requirements:**

* Allow the user to enter a transaction: description, amount (positive = income, negative = expense).
* Store all transactions in a list of tuples or dictionaries.
* Display current balance and recent transactions.
* Write all transactions to a file (`ledger.txt`) upon exiting the program.
* Read from `ledger.txt` at startup to load previous transactions.

**Key functions:**

* `load_ledger(filename)`
* `add_transaction(ledger)`
* `display_summary(ledger)`
* `save_ledger(ledger, filename)`

**Sample file content (ledger.txt):**

```
2025-07-31,Salary,+2500  
2025-07-31,Groceries,-120.50  
```

**Extension idea:**\
Implement a simple search by keyword in transaction descriptions.
