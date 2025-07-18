---
description: Use this template to prepare your System Design Specification (SDS) document.
---

# SDS template

#### 1. Project overview

**Summarise the project in 2–3 sentences.**\
State the system’s intended purpose, target users, and the problem it aims to solve.

_Example:_\
&#xNAN;_&#x41; secure bug tracking system for small development teams to report, assign, and resolve issues efficiently._

***

#### 2. User requirements (synthesised summary)

List key user stories from earlier work, grouped by user type.\
Use the format:\
&#xNAN;_&#x41;s a \[user], I want to \[action], so that \[outcome]._

***

#### 3. User flow diagram

Embed or link to the diagram developed in Module 721.\
This should show the key tasks users will complete, from login through to task completion.

***

#### 4. System modelling tools

**4.1 Level 0 Data Flow Diagram**

Include a clear Level 0 DFD with external entities, high-level processes, and data flows.\
Label each element clearly.

**4.2 Level 1 Data Flow Diagram (at least one)**

Choose a key process (e.g. “Manage Bugs”) and expand it using a Level 1 DFD.\
Identify inputs, outputs, and data stores.

**4.3 Structure chart**

Show the top-down design of your subroutines.\
Indicate parameters (empty/filled circles), decision points (diamonds), and loops (curved arrows) using standard notation.

***

#### 5. Data dictionary

Provide a table outlining the key data used in your system.

| **Field**    | **Type**                          | **Validation**         | **Example**   | **Purpose**              |
| ------------ | --------------------------------- | ---------------------- | ------------- | ------------------------ |
| `username`   | String                            | Required, alphanumeric | `jdoe23`      | Identifies unique user   |
| `bug_status` | Enum (New, In Progress, Resolved) | Must match enum        | `In Progress` | Tracks progress of a bug |
| ...          | ...                               | ...                    | ...           | ...                      |

***

#### 6. Tool selection and justification

Summarise your stack (HTML, CSS, JS, Flask, SQLite) and explain why each tool is appropriate.\
Include 1–2 sentences per tool.

_Example:_\
**Flask** is a lightweight Python framework that supports routing and templating, making it ideal for small web applications with dynamic pages.

***

#### 7. Interface mock-ups and prototypes

Insert annotated screenshots from your Figma designs (or another prototyping tool).\
Use callouts to explain interface elements and design choices related to usability and accessibility.

***

#### 8. Security and data handling considerations

Briefly describe how user data will be collected, stored, and protected.\
Mention any relevant techniques such as input validation, sanitisation, authentication, or error handling.

***

#### 9. Development plan

Include a brief Gantt chart or timeline of major tasks.\
Indicate when front-end and back-end development will take place, testing phases, and buffer periods.

***

#### 10. Testing and evaluation strategy

Outline how the system will be tested:

* What types of test data will be used?
* How will you handle edge cases?
* Will you use black-box or white-box testing?
* What will success look like?

***

#### 11. Version control and project management

Describe how you will use Git and GitHub.\
Mention features such as commits, branches, issues, and README documentation.

***

#### 12. Appendix

Attach any other design artefacts or research material not already included above.\
This may include extended user flows, storyboard frames, pseudocode samples, or early paper sketches.

