---
description: >-
  Explore the key principles that guide secure software design decisions and
  prevent avoidable vulnerabilities.
---

# 412 Design principles

### Overview

Security design principles help developers make thoughtful, proactive choices that reduce risk and improve the long-term safety of software systems. These principles do not prescribe specific technologies or tools—instead, they provide a mindset for preventing vulnerabilities before they occur.

When consistently applied, these principles contribute to robust and predictable software, support regulatory compliance, and limit the damage caused by human error or malicious behaviour.

### Targets

In this topic, students learn to:

* Describe the role of design principles in secure software development
* Identify and apply common principles used to prevent vulnerabilities
* Explain how principles such as least privilege and fail securely support user safety

<details>

<summary><a href="https://curriculum.nsw.edu.au/learning-areas/tas/software-engineering-11-12-2022/content/year-12/fa039e749d">Secure software architecture</a></summary>

**Designing software**

*   Explore fundamental software design security concepts when developing programming code, including:

    – confidentiality

    – integrity

    – availability

    – authentication

    – authorisation

    – accountability

**Developing secure code**

* Use and explain the ‘privacy by design’ approach in the development of software solutions, including:\
  – proactive not reactive approach\
  – embed privacy into design\
  – respect for user privacy

</details>

### Least privilege

Each user, process, or system component should have only the access it needs—no more, no less. This limits the potential damage caused by compromised accounts or misused functionality.

**Example:**

A photo gallery app should not allow a basic user account to delete other users’ files or access the database directly.

### Defence in depth

Security should not rely on a single control or mechanism. Instead, multiple overlapping layers of protection should be used so that if one fails, others remain in place.

**Example:**&#x20;

Even if a firewall allows malicious traffic through, an internal validation check might still reject it.

### Fail securely

When an error or unexpected condition occurs, systems should default to a safe state. They should not disclose sensitive information or grant unintended access.

**Example:**&#x20;

If a login system encounters a timeout error, it should deny access, not log the user in automatically or crash with a detailed error message.

### Minimise attack surface

Software should expose the fewest possible points of entry for an attacker. This includes limiting unnecessary features, endpoints, or ports that increase complexity and risk.

**Example:**

Disabling admin interfaces on production environments reduces the number of exposed features that could be exploited.

### Secure defaults

Out-of-the-box configurations should prioritise security. Users or administrators should not have to "opt in" to protection; safety should be the default setting.

**Example:**&#x20;

A new user account should be created with strong password policies and no elevated privileges unless explicitly granted.

### Separation of duties

Responsibilities should be distributed across different roles or systems so that no single user has complete control over all parts of a sensitive process.

**Example:**&#x20;

In a deployment pipeline, one person might write code, another review and approve it, and a third deploy it to production.
