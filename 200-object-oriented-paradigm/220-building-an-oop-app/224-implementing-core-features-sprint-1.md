---
description: >-
  Sprint 1 delivers a working foundation by implementing the core Task and
  TaskManager classes, supported by manual testing and internal documentation.
---

# 224 Implementing core features (Sprint 1)

Sprint 1 begins the development cycle by translating the class design into working Python code. The goal is to build and test the core object-oriented structure of the Task Tracker app, including class definitions, internal state handling, and basic user interaction via a test harness. This sprint models best practice in structured implementation and incremental testing.

### Sprint goal

To implement the core object-oriented structure of the Task Tracker app, including:

* Definition of the Task and TaskManager classes
* Methods for creating, storing, and displaying tasks
* Manual testing via main.py
* Internal documentation and preparation for future extension

### Tasks completed

* Created `task.py` containing the `Task` class with attributes: `title`, `description`, `due_date`, `is_complete`
* Implemented `Task` methods: `mark_complete()`, `mark_incomplete()`, `display_summary()`, `display_details()`
* Created `task_manager.py` containing the `TaskManager` class with an internal list of `Task` objects
* Implemented `TaskManager` methods: `add_task()`, `list_tasks()`, `find_task()`, `remove_task(),` `get_completed_tasks()`, `get_incomplete_tasks()`, `display_all_tasks()`
* Developed `main.py` to manually instantiate objects and verify behaviour through print-based testing
* Used controlled test data to verify functionality and validate core logic

### Testing log

Testing is conducted manually using `main.py`. Known tasks are added and manipulated in code to observe expected output and verify object behaviour. Outputs from method calls are printed and compared to expected results. Tasks are marked complete, filtered, and displayed in different formats to verify correctness.

#### Testing log example

| Test case                | Input                              | Expected outcome                    | Actual outcome                       | Notes                     |
| ------------------------ | ---------------------------------- | ----------------------------------- | ------------------------------------ | ------------------------- |
| Create new Task          | "Finish homework", "2025-07-01"    | Task object with correct attributes | Correct attributes shown in printout | Basic instantiation check |
| Toggle completion        | Call `toggle_complete()` on a Task | Task marked as complete/incomplete  | Correct status toggled each time     | State change confirmed    |
| Add task to TaskManager  | `add_task(task)`                   | Task appears in task list           | Found in list                        | Success                   |
| Display tasks (all)      | Call `display_tasks()`             | All tasks printed                   | Output matches                       |                           |
| Display incomplete tasks | Call `display_tasks(False)`        | Only incomplete tasks printed       | Output matches                       |                           |
| Mark task complete       | `mark_task_complete(index)`        | Task status updated                 | Worked as expected                   |                           |

### Version control

* Git repository initialised using SSH key authentication
* Commits follow a clear structure: initial class creation, method implementation, test driver setup, and documentation
* GitHub is used to store projects remotely with public visibility
* A `.gitignore` added to exclude Python cache files

### Reflections

This sprint establishes the core structure of the app and validates that the object-oriented model holds up under basic usage. Manual testing provides enough coverage for now, but automated testing will be introduced in future sprints. The method stubs prove helpful in guiding development, and Git has been used effectively to manage commits and push updates.

### Checklist

This checklist provides a structured method for verifying the completion of Sprint 1. It helps you confirm that all essential files, features, tests, and documentation are in place before moving on. Reviewing each item encourages careful reflection on what has been implemented, ensuring that your project aligns with professional development practices. The checklist also serves as a repeatable template for future sprints.

<details>

<summary>Sprint 1 checklist</summary>

#### **Project structure and files**

* `task.py` file created with a `Task` class and working attributes
* `task_manager.py` file created with a `TaskManager` class managing a list of tasks
* `main.py` contains manual test code for adding, marking, and displaying tasks
* `README.md` includes an overview of the project and how to run it
* `.gitignore` file prevents unnecessary files from being tracked

#### Implementation

* Task class includes `mark_complete()`, `mark_incomplete()`, `display_summary()`, and `display_details()`
* `TaskManager` includes methods for adding, removing, finding, and listing tasks
* Manual testing confirms that task creation and status changes work as expected

#### Git and version control

* Git is initialised and connected to GitHub via SSH
* At least three meaningful commits are made during the sprint
* The project is pushed to a GitHub repository with public visibility

#### Documentation

* A completed sprint log exists in `/docs/sprint_log_1.md`
* The sprint log includes a goal, completed tasks, testing log, and reflections
* Any TODOs or future ideas are noted in code comments or documentation

</details>
