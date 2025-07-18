---
description: >-
  The interactive command-line interface is completed in Sprint 2, connecting
  user input with core features through the TaskManager class.
---

# 225 Extending functionality (Sprint 2)

### Summary

In this sprint, the app transitions from passive object structures to an interactive user-facing interface. A command-line menu is implemented to allow the user to add new tasks, view all tasks, mark them as complete, and remove them by index. This marks the first sprint where control flow is shaped by user input, not by predefined test code. All functionality from Sprint 1 is preserved, and new logic is layered onto the `main.py` file.

The `TaskManager` class serves as the bridge between the user interface and the underlying task logic. Defensive programming is used to validate inputs and prevent runtime errors. While the app remains non-persistent and CLI-based, its usability improves significantly.

### Features implemented

* CLI menu with numbered options
* Task creation via user input (title, description, due date)
* Display of all tasks with indices and completion status
* Selection-based marking of tasks as complete
* Selection-based task deletion with input validation

### Testing and verification

The app was tested manually by running main.py in the terminal and interacting with each menu option. Edge cases such as invalid indices and non-numeric input were tested to ensure the CLI does not crash and provides useful feedback.

| Test case                      | Input                    | Expected outcome                             | Actual outcome | Notes                      |
| ------------------------------ | ------------------------ | -------------------------------------------- | -------------- | -------------------------- |
| Add task                       | Title: "Write doc"       | Task added and appears in list               | Success        | Input validated            |
| View all tasks                 | Select menu option 2     | List shows task with status ✗ (not complete) | Success        | Format clear and readable  |
| Mark task as complete          | Index: 0                 | Status changes to ✓                          | Success        | Handled valid input        |
| Mark task with invalid index   | Index: 10                | Error message shown                          | Error printed  | Index out of range handled |
| Remove task                    | Index: 0                 | Task removed from list                       | Success        | Confirmed by new list view |
| Remove task with invalid input | Index: "abc"             | Error message shown                          | Error printed  | Non-numeric handled        |
| Empty task list view           | After removing all tasks | "No tasks found" message shown               | Success        | Gracefully handled         |

### Reflections

This sprint demonstrates how object-oriented logic can be extended into an interactive user program. The CLI interface makes use of methods from `TaskManager` and `Task,` reinforcing the separation of concerns between user input, business logic, and data representation.

Students following this model can now see how the task classes support real-world interaction and control flow. A consistent commit history using Git documents each functional milestone, helping trace how new features were added incrementally. The current version includes user feedback, validation, and complete task lifecycle handling via a simple CLI.
