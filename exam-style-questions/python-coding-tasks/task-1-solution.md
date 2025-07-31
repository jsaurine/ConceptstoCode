# Task 1 Solution

```python
# Quiz Score Tracker
# This program asks a series of yes/no questions and tracks how many are answered correctly.

# ------------------------
# FUNCTION DEFINITIONS
# ------------------------

def ask_question(prompt, correct_answer):
    """
    Ask a yes/no question, validate the input, and return True if the answer is correct.

    Parameters:
    - prompt (str): The question to display to the user.
    - correct_answer (str): Either 'yes' or 'no', indicating the correct answer.

    Returns:
    - bool: True if the user's answer matches the correct answer, False otherwise.
    """
    while True:
        user_input = input(prompt + " (yes/no): ").strip().lower()
        if user_input in ["yes", "no"]:
            break  # Valid input
        else:
            print("Invalid input. Please enter 'yes' or 'no'.")
    
    if user_input == correct_answer:
        print("Correct!\n")
        return True
    else:
        print(f"Incorrect. The correct answer was '{correct_answer}'.\n")
        return False

# ------------------------
# MAIN PROGRAM LOGIC
# ------------------------

# Step 1: Define a list of quiz questions.
# Each item is a tuple: (question text, correct answer)
quiz_questions = [
    ("Is Python case-sensitive?", "yes"),
    ("Does 2 + 2 equal 5?", "no"),
    ("Can variables begin with a number in Python?", "no"),
    ("Is 'while' a loop structure in Python?", "yes"),
    ("Does Python use curly braces {} to define blocks?", "no")
]

# Step 2: Initialise a counter to keep track of correct answers.
score = 0

# Step 3: Loop through each question and ask it using the function.
print("Welcome to the Python quiz!\n")

for index, (question, correct_answer) in enumerate(quiz_questions, start=1):
    print(f"Question {index}:")
    if ask_question(question, correct_answer):
        score += 1  # Increment score if answer was correct

# Step 4: Print final result.
print(f"You scored {score} out of {len(quiz_questions)} correct.")

# Optional feedback
if score == len(quiz_questions):
    print("Excellent work! You got everything right.")
elif score >= 3:
    print("Good job! You have a solid understanding.")
else:
    print("Keep practising! Review the basic concepts.")

```
