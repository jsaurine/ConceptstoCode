---
description: >-
  Use encryption, isolation, and safe communication methods to protect data and
  limit the effects of compromise.
---

# 423.3 Cryptography and isolation

### Overview

Security by design means applying not just abstract principles, but also **technical controls** that enforce protection. Two of the most essential strategies in secure systems are:

* **Cryptography**, which ensures data privacy, authenticity, and integrity
* **Isolation**, which limits what code or users can access, even if something goes wrong

This topic explores how developers use **cryptography**, secure **APIs**, and **sandboxing** to build systems that are hard to break, even when other defences fail.

### Targets

In this topic, students learn to:

* Explain the purpose of cryptography in secure software
* Use APIs that enforce encryption and data integrity
* Apply sandboxing techniques to contain potentially harmful processes
* Evaluate how isolation strategies reduce security risks

### Syllabus references

<details>

<summary><a href="https://curriculum.nsw.edu.au/learning-areas/tas/software-engineering-11-12-2022/content/year-12/fa039e749d">Secure software architecture</a></summary>

**Developing secure code**

* Use and explain the contribution of cryptography and sandboxing to the ‘security by design’ approach in the development of software solutions

</details>

### Cryptography in software

Cryptography is used to protect:

* **Data in transit** (e.g. HTTPS, secure messaging)
* **Data at rest** (e.g. encrypted files or databases)
* **Identity and access** (e.g. password hashing, digital signatures)

#### Common cryptographic goals

* **Confidentiality** – Keep data private
* **Integrity** – Detect if data has been tampered with
* **Authentication** – Prove identity
* **Non-repudiation** – Prove that something was done and can’t be denied

#### Secure practices

* Use strong, well-tested libraries (e.g. Python’s `cryptography`, Java’s `javax.crypto`)
* Never create your own algorithms
* Use proper **key management** – never hardcode keys or secrets

#### Example (Python password hashing):

```python
import bcrypt

password = b"secure123"
hashed = bcrypt.hashpw(password, bcrypt.gensalt())
```

### Secure APIs

APIs (Application Programming Interfaces) expose functionality to other software. If not secured, they can become entry points for attackers.

#### Common API vulnerabilities

* Missing authentication or authorisation
* Insecure or unencrypted connections
* Leaking sensitive data through error messages or overly verbose responses

#### Best practices

* Require authentication (e.g. API keys, OAuth2)
* Use HTTPS only
* Validate and sanitise all input
* Apply rate limiting to prevent abuse

### Sandboxing

Sandboxing is a technique used to **run code in a restricted environment**, where it cannot access system resources or harm other parts of the application.

It is used in:

* Web browsers (to isolate tabs)
* Mobile apps (through OS-level permission controls)
* Online compilers or code execution platforms
* Malware analysis tools

#### Benefits

* Prevents untrusted code from accessing sensitive files
* Reduces the impact of a vulnerability (e.g. a memory overflow stays confined)
* Supports defence in depth

#### Techniques

* Use virtual machines or containers (e.g. Docker)
* Apply file and system access controls
* Limit network or hardware access

### Summary

* Cryptography secures data, verifies identity, and ensures trust
* Secure APIs must enforce access control and validate data
* Sandboxing isolates processes to limit what an attacker can do
* These strategies enforce security at a technical level, even when other defences fail
