---
description: >-
  Translate the needs of your stakeholders into clear and testable requirements
  using structured documentation and visual modelling tools.
---

# 712 User requirements

### User stories

User requirements describe what the system must do to meet the needs of different users. These are expressed as **user stories**, written from the user's perspective. A user story captures a goal and its reason, and helps ensure the system is grounded in real needs.

Each user story follows the format:

**As a \[user type], I want to \[action], so that \[goal].**

These are not technical specifications. They are plain-language descriptions of what users expect to be able to do. Later in the project, they will be refined into functional and non-functional requirements during system design.

**Bug Tracker – sample user stories**

* As a **developer**, I want to update a bug’s status so my team knows what I’m working on.
* As a **project manager**, I want to assign bugs to developers to distribute work effectively.
* As a **tester**, I want to report new bugs with screenshots so developers have the necessary information.
* As an **admin**, I want to control user access levels to protect sensitive project data.
* As a **team member**, I want to comment on bugs so that I can contribute suggestions or context.

These stories help define what the system should support. Once gathered, they become the basis for creating user flows.

### From user stories to user flows

A **user flow** describes the steps a user takes to achieve the goal described in a user story. Depending on how the user interacts with the system, multiple user stories may lead to multiple distinct flows, or the same story might give rise to several alternative flows.

**Bug Tracker – flow for the developer updating a bug**

1. Log in
2. View assigned bugs
3. Open bug detail
4. Change status to “In Progress”
5. Add a comment
6. Submit changes
7. Return to dashboard

Another flow might begin with a notification email or a bug search. These are different starting points, but they share the same underlying story.

### Storyboarding the user experience

A **storyboard** is a sequence of panels that visualise what the user sees and does during the interaction. It focuses on the interface and user experience, rather than logic.

Each frame shows a key screen or moment in the flow, usually accompanied by a short caption.

**Bug Tracker – storyboard for reporting a new bug**

1. **Login screen** – User enters credentials
2. **Dashboard** – User clicks “New Bug”
3. **Bug form** – User enters title, description, and uploads a screenshot
4. **Submit screen** – A message confirms the bug was created
5. **Bug list** – New bug appears at the top

Storyboards help test your assumptions. Before any code is written, you can spot missing screens, unclear steps, or awkward transitions. You can spot missing screens, unclear steps, or awkward transitions before any code is written.

<figure><img src="../../.gitbook/assets/image (34).png" alt=""><figcaption><p>The storyboard above shows the relationship between three pages of information aimed at promoting a school canteen on a website.</p></figcaption></figure>

### Synthesising user flows into diagrams

A **user flow diagram** brings together the logic behind user flows. It visualises common paths and variations, using boxes for steps and arrows for transitions.

**Bug Tracker – user flow diagram (developer flow)**

```plaintext
[Login]
   ↓
[View Dashboard]
   ↓
[Select Bug]
   ↓
[Edit Bug: Change Status + Add Comment]
   ↓
[Submit Changes]
   ↓
[Confirmation Message]
   ↓
[Return to Dashboard]
```

A single diagram may represent the synthesis of multiple user flows (below) derived from different stories. This helps identify shared pathways and structural requirements for the system.

<figure><img src="https://cdn.prod.website-files.com/649ae86ac1a4be707b656519/65b3b74f6fbc86dbe15398a1_FlowMapp%20User%20Flow%20Diagrams%20(FlowCharts)-CnO6d7lLv6o-1080p-1654225304596%202.webp" alt=""><figcaption><p>A well-thought-out user flow is like a pleasant walk in a large park. Here, by following well-equipped paths and signs, you will spend your time much more productively than in a park without even a hint of a route.</p></figcaption></figure>

Working through user stories, flows, and diagrams ensures your project starts with a solid foundation. These artefacts guide the system design phase and provide the structure for testing, validation, and user feedback.

### Actions

{% hint style="success" %}
**Use the examples below to create the following drafts for your software engineering project:**

* **User stories**
* **User flows**
* **Storyboards**
* **User flow diagram**
{% endhint %}

### Resources

The examples below show a possible approach for establishing user requirements for a Bug Tracker, a structured system for logging, managing, and resolving software bugs, replacing ad hoc methods like email and spreadsheets.

<details>

<summary>User stories</summary>

These user stories are grouped by user role to support design planning and future refinement into functional/non-functional requirements.

#### **User role: Developer**

* As a developer, I want to log in securely, so that I can access my assigned tasks.
*
* As a developer, I want to view a list of bugs assigned to me, so that I can see what needs to be fixed.
* As a developer, I want to open a bug to view its details, so that I can understand the issue.
* As a developer, I want to change the status of a bug (e.g. “In Progress”, “Resolved”), so that others know its current state.
* As a developer, I want to add comments to a bug, so that I can document progress or ask for clarification.
* As a developer, I want to upload files (e.g. screenshots, logs), so that I can provide evidence or supporting material.
* As a developer, I want to search for bugs by ID, keyword, or status, so that I can find issues quickly.
* As a developer, I want to filter bugs by priority or date, so that I can focus on urgent tasks first.
* As a developer, I want to mark a bug as resolved, so that I can indicate it is ready for testing.
* As a developer, I want to reassign a bug to another developer, so that the most suitable person can address it.
* As a developer, I want to receive notifications when I’m assigned a new bug, so that I don’t miss any tasks.

#### **User role: Project Manager**

* As a project manager, I want to create a new bug report, so that issues can be formally tracked.
* As a project manager, I want to assign bugs to specific developers, so that work is distributed appropriately.
* As a project manager, I want to edit or update bug reports, so that descriptions stay accurate.
* As a project manager, I want to prioritise bugs (e.g. “Low”, “Medium”, “Critical”), so that the team can focus their efforts.
* As a project manager, I want to view all bugs across the project, so that I can track overall progress.
* sdf
* As a project manager, I want to filter bugs by status, priority, or developer, so that I can analyse workload and bottlenecks.
* As a project manager, I want to generate reports or summaries, so that I can communicate progress to stakeholders.
* As a project manager, I want to see a history of changes made to each bug, so that I can track accountability.
* As a project manager, I want to reopen a resolved bug if it was not fixed correctly, so that it can be reassigned.
* As a project manager, I want to archive or delete obsolete bugs, so that the system remains tidy.

#### **User role: Tester**

* As a tester, I want to create bug reports based on test results, so that issues found during testing are tracked.
* As a tester, I want to describe the steps to reproduce a bug, so that developers can replicate it easily.
* As a tester, I want to attach screenshots or videos, so that I can demonstrate the issue clearly.
* As a tester, I want to view the status of submitted bugs, so that I know if issues are being addressed.
* As a tester, I want to comment on bugs after retesting, so that I can confirm if they’ve been fixed.
* As a tester, I want to filter bugs by test cycle or date reported, so that I can review recent results.

#### **User role: Admin**

* As an admin, I want to manage user accounts (add/remove), so that access is controlled.
* As an admin, I want to assign roles to users (e.g. Developer, Tester, Manager), so that they have the correct permissions.
* As an admin, I want to view activity logs for all users, so that I can audit system usage.
* As an admin, I want to change or reset user passwords, so that account access can be recovered.
* As an admin, I want to configure system-wide settings (e.g. email notifications), so that the tool works for the team.
* As an admin, I want to back up the database regularly, so that data is not lost.
* As an admin, I want to delete or archive inactive users, so that the system remains secure and clean.

#### **User role: All users**

* As a user, I want to change my password, so that I can maintain account security.
* As a user, I want to view my own profile, so that I can see my activity and assigned bugs.
* As a user, I want to receive email or in-app notifications about bug status changes, so that I stay updated.
* As a user, I want to use the bug tracker on a mobile device, so that I can work on the go.
* As a user, I want to customise my dashboard (e.g. sort or hide widgets), so that I can focus on relevant information.
* As a user, I want to log out securely, so that others cannot access my account.

</details>

<details>

<summary>User flows</summary>

Translating the user stories above into user flows would make for a long list. To illustrate, six user stories are transcribed into user flows, which are later synthesised into a user flow diagram.

**1. As a user, I want to create an account so that I can access the bug tracking system.**\
Registration form → Password validation → Account creation → Verification email

**2. As a user, I want to log in securely so that I can access my dashboard.**\
Login form → Credential validation → Dashboard

**3. As a tester, I want to create a new bug report so that developers are aware of software issues.**\
Click "New Bug" → Complete bug form → Submit → Bug added to list

**4. As a developer, I want to view assigned bugs so that I can begin working on them.**\
Dashboard → Filter bugs → Select bug → View details

**5. As a developer, I want to update a bug’s status so that my team knows what I’m working on.**\
Bug detail → Change status → Add comment → Save changes

**6. As a project manager, I want to assign bugs to developers so that work is distributed effectively.**\
Bug list → Select bug → Assign user → Confirm assignment

</details>

<details>

<summary>Storyboards</summary>

The storyboard below shows that for the user role of developer.

<figure><img src="../../.gitbook/assets/image (29).png" alt=""><figcaption><p>A five-panel low-fidelity storyboard for the Bug Tracker web application showing the typical developer flow.</p></figcaption></figure>

</details>

<details>

<summary>User flow diagram</summary>

This user flow diagram integrates the developer user flows shown above.

<figure><img src="../../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

</details>
