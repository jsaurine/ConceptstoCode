---
description: >-
  Define the purpose and boundaries of your software engineering project by
  identifying user needs, goals, constraints, and success criteria.
cover: ../../.gitbook/assets/711.png
coverY: 88
---

# 711 Project scoping requirements

Scoping your software engineering project means clearly defining what your software will do, who it is for, and what constraints apply. The goal is to outline a focused, achievable plan to guide your future design, implementation, and testing. A well-scoped project includes a concise description of its purpose, the people it serves, the functionality it provides, and the data it uses. It should also identify constraints, success criteria, and known risks or challenges.

The following example demonstrates how to complete the project scoping worksheet.

### Project scoping example

#### Project title

Secure Bug Tracker

#### Project summary

A full-stack web application tracking software bugs, issues, and development tasks with secure user authentication.

#### Intended users

* Developers (create, update, resolve bugs)
* Project Managers (view all issues, assign bugs)
* Admins (manage users and permissions)

#### Problem being solved / Purpose

It provides a structured system for logging, managing, and resolving software bugs, replacing ad hoc methods like email and spreadsheets.

#### Core functionality

* Create and edit bug reports (title, description, priority, status)
* Assign bugs to users and track progress
* Comment on bugs to document fixes and discussion

#### Data to be collected and stored

* Users (username, password, role)
* Bug reports (title, description, priority, status, timestamps)
* Comments (linked to bug reports)
* Optional: Attachments (screenshots)

#### Security considerations

* User authentication with hashed passwords
* Role-based access control (admin vs user)
* Input validation and sanitisation to prevent injection attacks

#### Stretch goals

* Email notifications when bugs are updated
* Upload files (screenshots/log files)
* Activity logs for auditing

#### Anticipated challenges

* Implementing secure role-based access control
* Managing file uploads safely
* Designing an intuitive UI for developers and admins

### Actions

{% hint style="success" %}
### Use these nine prompts to draft your project scope document. This becomes the first official entry in your process diary and sets the direction for your software engineering project. Your responses should be thoughtful, specific, and realistic — this document will shape the rest of your planning and development process.
{% endhint %}

### Resources

<details>

<summary>Project scope template</summary>

Project title:

(Write a clear, concise title for your project.)

Project summary (one sentence):

(Describe in one sentence what your app will do.)

Intended users:

(Who will use your app? Describe the main user types.)

Problem being solved / Purpose:

(Explain what problem your app addresses or what need it fulfils.)

Core functionality:

Feature 1:

Feature 2:

Feature 3:

(List at least three main things your app must do.)

Data to be collected and stored:

(What information will your app store in its database? List data types, e.g., tasks, events, users, comments.)

Security considerations:

(List at least 2–3 security features your app will need—e.g., user authentication, form validation, data protection.)

Stretch goals (optional):

(Are there any extra features you’d like to add if you have time?)

Anticipated challenges:

(What difficulties can you already foresee? E.g., login system, database design, tricky features.)

</details>

<details>

<summary>Project ideas</summary>

* **Mental health journal web app**\
  This secure, private journaling application allows users to log daily moods and reflections. It includes optional AI sentiment analysis and secure login with two-factor authentication.

- **Bug tracker for student coding projects**\
  A full-stack issue-tracking system for managing class coding tasks or projects. Features user roles, secure authentication, bug status workflow, and data visualisation of task progress.

* **Study planner and habit tracker PWA**\
  A progressive web app that supports students in planning study sessions and tracking habits. Incorporates responsive UI/UX, calendar APIs, notifications, and local or cloud-based storage.

- **Interactive learning dashboard for HSC revision**\
  A customisable front-end dashboard that pulls in quiz results, revision notes, and goal-setting tools. It uses back-end SQL to store user progress and analytics for adaptive study tips.

* **AI-based resume screener for mock job applicants**\
  Students upload CVs to a simulated job platform, using a machine learning model to score based on keywords. The backend stores uploads securely and tracks user feedback on accuracy.

- **Smart recipe and meal planning app**\
  A web-based app where users input dietary preferences and get automated weekly meal plans. Includes database storage, search filters, and optional automation to generate shopping lists.

* **Cybersecurity awareness game**\
  A gamified web application teaching users about common software vulnerabilities (e.g. SQL injection, XSS). Built with deliberate safe coding practices and tested for security flaws.

- **School event management system**\
  It manages registrations, attendance, and communications for school events. It features an admin portal, secure sign-in, automated reminder emails, and QR code ticketing.-&#x20;

* **IoT dashboard simulator for home automation**\
  A simulated web-based control panel for managing virtual smart devices (e.g. lights, thermostat). Incorporates asynchronous JavaScript, security features, and data visualisation tools.

- **Virtual classroom feedback system**\
  It allows students to give confidential feedback on lessons and is linked to a teacher dashboard for analytics. It uses database interfacing, sentiment analysis (optional), and role-based access control.

</details>
