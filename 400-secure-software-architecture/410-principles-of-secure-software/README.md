---
description: >-
  Explore the foundational goals and principles that underpin the development of
  secure software.
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
---

# 410 Principles of secure software

This section introduces students to the conceptual building blocks of secure software systems. It focuses on the CIA triad and AAA model, which define the goals of security and the mechanisms for controlling user access. These frameworks are supported by industry-recognised design principles such as least privilege and defence in depth, which guide developers in making strategic security decisions throughout the software lifecycle.

### Targets

In this section, students learn to:

* Define the principles of confidentiality, integrity, and availability (CIA)
* Explain the concepts of authentication, authorisation, and accountability (AAA)
* Recognise how security goals shape software design
* Understand key principles used to reduce security risks and support safe software behaviour

### Key concepts in this section

#### Security goals: The CIA triad

**Confidentiality** ensures that only authorised users can access data. This is typically achieved through access controls, encryption, and careful user management.

**Integrity** refers to the accuracy and trustworthiness of data. Mechanisms such as hashing, checksums, input validation and audit logs help protect data from tampering or corruption.

**Availability** ensures that systems remain accessible and functional for legitimate users. Redundancy, load balancing, and protection against denial-of-service attacks all support this goal.

#### User access control: The AAA model

**Authentication** is the process of verifying a user’s identity. This might involve passwords, multi-factor authentication, or biometric verification.

**Authorisation** determines what resources a user can access once authenticated. Role-based access control (RBAC) is a standard model for managing permissions.

**Accountability** means that user actions are recorded and traceable. Audit logs and session tracking support this principle by making it possible to review activity and investigate incidents.

#### Security design principles

Security design principles provide strategic guidance to reduce the likelihood of vulnerabilities during software development and deployment.

* **Least privilege**: Each user or system component should have the minimum access necessary to perform its task.
* **Defence in depth**: Multiple layers of security should be used to protect systems, so that if one layer fails, others still provide protection.
* **Secure defaults**: Software should be configured to prioritise safety from the outset, requiring explicit action to enable access.
* **Fail securely**: When errors occur, the system should default to a safe state that avoids exposing sensitive data or creating new risks.
* **Keep it simple**: Simpler designs are easier to reason about and test, reducing the chance of mistakes or oversights.
* **Separation of duties**: Responsibilities should be distributed so that no single user or system has unchecked control over critical operations.
