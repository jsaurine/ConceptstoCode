---
description: >-
  Discover how secure software is planned, designed, and delivered using a
  structured lifecycle that incorporates risk, testing, and maintenance from the
  outset.
---

# 421 The secure development lifecycle

### Objectives

* Describe the phases of a secure development lifecycle
* Understand how security is embedded across planning, design, and testing
* Recognise how SDL reduces risk and supports sustainable software

### Syllabus references

<details>

<summary><a href="https://curriculum.nsw.edu.au/learning-areas/tas/software-engineering-11-12-2022/content/year-12/fa039e749d">Secure software architecture</a></summary>

**Designing software**

* Interpret and apply fundamental software development steps to develop secure code, including:\
  – requirements definition\
  – determining specifications\
  – design\
  – development\
  – integration\
  – testing and debugging\
  – installation\
  – maintenance

</details>

### What is a Secure Development Lifecycle?

A **Secure Development Lifecycle (SDL)** is a structured approach to building software that places security at the heart of each development phase. It ensures that design decisions, coding practices, and testing strategies anticipate and address potential vulnerabilities before software is deployed.

Unlike traditional development models that treat security as a final step, SDL integrates secure thinking throughout the process.

### Why SDL matters

Security added as an afterthought is often too late — or too expensive. Fixing vulnerabilities after a product is released is far more costly than addressing them during the planning and design stages.

Benefits of following SDL include:

* Fewer vulnerabilities in production
* Clear documentation and accountability
* Increased trust in system behaviour
* Compliance with industry security standards

### Typical SDL phases

Each organisation may have its version of SDL, but most follow a pattern similar to this:

<table><thead><tr><th width="250.0859375">Phase</th><th>Security focus</th></tr></thead><tbody><tr><td><strong>1. Requirements definition</strong></td><td>Identify security goals, constraints, and compliance obligations</td></tr><tr><td><strong>2. Design Specification</strong></td><td>Document how the system should behave, including authentication and authorisation needs, and apply design patterns that reduce risk (e.g. least privilege, sandboxing)</td></tr><tr><td><strong>3. Development</strong></td><td>Use secure coding practices, linters, and coding standards</td></tr><tr><td><strong>4. Testing</strong></td><td>Run static and dynamic tests to detect vulnerabilities</td></tr><tr><td><strong>5. Deployment</strong></td><td>Configure secure defaults and access controls</td></tr><tr><td><strong>6. Maintenance</strong></td><td>Monitor for issues, apply updates, and respond to new threats</td></tr></tbody></table>

<figure><img src="../../../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

### Using SDL as a thinking tool

In professional environments, SDL is more than a checklist — it's a mindset. Developers, project managers, and security analysts work together across phases to:

* Evaluate threats
* Document decisions
* Ensure that each step reduces risk, not just adds features

Good SDL practice supports both security and quality assurance.

### Summary

* SDL integrates security throughout the software development process
* Each phase has its own security focus — from requirements to maintenance
* Following SDL improves trust, reduces cost, and prevents vulnerabilities in production
