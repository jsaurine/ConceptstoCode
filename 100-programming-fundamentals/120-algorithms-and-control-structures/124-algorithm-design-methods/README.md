---
description: >-
  Learn how to translate a software specification into a clear and testable
  algorithm using structured design strategies.
---

# 124 Algorithm design methods

### Outline

This section introduces the process of designing algorithms within the software development lifecycle. You will learn how to interpret problem briefs, apply strategic thinking to problem decomposition, and use structured methods to outline algorithms using pseudocode and flowcharts. We will draw on industry-aligned models such as top-down and bottom-up design, and prepare you to test, refine, and document your solutions using best-practice approaches.

### Targets

In this topic, students learn to:

* Analyse software specifications to identify processes, inputs, and outputs
* Apply top-down and bottom-up approaches to break down complex problems
* Structure mainline logic and subprograms for clarity and modularity
* Design algorithms using strategy patterns, including divide and conquer and backtracking
* Use desk checking and trace tables to validate logic and test edge cases
* Link algorithm design to software development models such as Waterfall and Agile

### Glossary

<table data-view="cards"><thead><tr><th></th><th></th></tr></thead><tbody><tr><td><h4>mainline logic</h4></td><td>The top-level flow of an algorithm, typically calling subroutines to complete each part of the task.</td></tr><tr><td><h4>top-down design</h4></td><td>The top-level flow of an algorithm, typically calling subroutines to complete each part of the task.</td></tr><tr><td><h4>bottom-up design</h4></td><td>Building simple modules first, then integrating them into larger solutions.</td></tr><tr><td><h4>divide and conquer</h4></td><td>A problem-solving technique that divides the problem into parts and solves each recursively.</td></tr><tr><td><h4>backtracking</h4></td><td>An algorithm design technique that explores possible solutions and abandons invalid paths.</td></tr><tr><td><h4>refinement</h4></td><td>The process of expanding a high-level step into more detailed algorithmic steps.</td></tr><tr><td><h4>desk checking</h4></td><td>Manually walking through an algorithm with test inputs to check correctness.</td></tr><tr><td><h4>trace table</h4></td><td>A table used to track variable values and control flow during an algorithm's execution.</td></tr></tbody></table>

### Overview

Designing algorithms is one of the most critical stages in software engineering. It bridges the gap between understanding the problem and implementing a solution in code. This process begins with analysis: What are the inputs? What outputs are expected? What logical decisions and repetitions are needed?

Effective algorithm design often begins with **top-down decomposition**. This means breaking a complex task into manageable subroutines. Each subroutine can then be refined until its function is clear and easily implemented. This approach is supported by [**structure charts**](../../110-foundations-of-software-development/114-structure-charts/), which show the hierarchy and flow of data between modules.

Alternatively, a **bottom-up** strategy can be used where familiar, well-tested modules are developed independently and combined into a working system. This method is standard in Agile development, where reusable components and libraries may already exist.

Advanced design strategies like **divide and conquer** are essential for solving complex or recursive problems, such as searching or sorting. **Backtracking** is used in problems where multiple solution paths must be explored, such as puzzles or constrained optimisation problems.

Developers might use **desk checking** and **trace tables** to test algorithms' logic before coding. These help identify logic errors, unexpected outputs, or infinite loops before any syntax is introduced. Testing at this stage supports good design and avoids unnecessary rework later in development.

In a formal development process like **Waterfall**, algorithm design is front-loaded and documented thoroughly. In **Agile**, algorithms may be iteratively refined based on user feedback and testing during sprints.

This section builds directly on earlier learning in [**control structures**](../122-control-structures/) and [**algorithm representation**](../121-algorithm-fundamentals/). We are shifting the focus from _how to write_ algorithms to _how to design and validate_ them. Developing these skills will support later project work and the handling of exam-style questions requiring algorithmic thinking.
