---
description: >-
  Security must be part of the design—not an afterthought. In this topic, you
  will identify and implement secure design strategies that protect user data
  and reduce vulnerabilities.
---

# 721 Designing secure architecture

### **What is secure architecture?**

Designing secure software means planning how your system will prevent, detect, and respond to potential threats. You should consider how users interact with the system, what data is being collected or stored, and how errors or malicious input will be handled.

**Key principles include:**

* **Confidentiality** – Protecting sensitive information from unauthorised access
* **Integrity** – Ensuring data is accurate and cannot be tampered with
* **Availability** – Keeping the system accessible to legitimate users
* **Authentication and authorisation** – Verifying user identity and permissions
* **Input validation** – Checking that all user inputs are safe before processing
* **Privacy by design** – Minimising data collection and embedding privacy in every part of the interface

### **What should I include in my SDS?**

When designing secure architecture for your project, be sure to include:

* A list of known risks (e.g. invalid inputs, unsafe file uploads)
* Your strategies to mitigate those risks (e.g. validation, rate limiting)
* UI annotations that show how users are guided to enter data safely
* Error messages that avoid revealing sensitive system information
* Notes on how your system protects privacy (e.g. no data collection unless necessary)

### **Worked example**

Let’s say your app allows users to submit a form. Consider the following design decisions:

* All fields are validated client-side (e.g. required fields, email format)
* Server-side sanitisation removes unwanted characters
* Inputs are rate-limited to prevent flooding
* The form avoids storing unnecessary data like location or browser fingerprinting
* If an error occurs, the user sees a generic message, not the internal server path

### Actions

{% hint style="success" %}
Use the following to draft the Secure Design section in the Software Design Specification (SDS):

* Identify at least three security risks relevant to your app
* Propose mitigation strategies for each risk
* Annotate your storyboard with design features that support secure input
* Write a brief privacy by design statement
* Draft error messages for at least one input or login process
* Record these in your SDS under “Secure Architecture”
* Include references to any tools or libraries used to support input validation or authentication
{% endhint %}

### Resources

<details>

<summary><strong>Secure design for the Bug Tracker App</strong></summary>

**Step 1 – Identify risks**

The Bug Tracker allows user-submitted bug reports. Risks include:

* Submitting malicious code via the description field (XSS)

- Overwriting or corrupting files via uploaded screenshots

* Accessing admin features without permission

**Step 2 – Plan mitigation**

* Use input sanitisation to clean text fields (e.g. html.escape() in Python)

- Restrict file types to .jpg or .png only and set a max file size

* Require login before access to admin functions

**Step 3 – Annotate the UI (storyboard)**

* Show placeholder text (e.g. “Describe the bug clearly, avoid pasting code”)

- Add tooltips explaining that screenshots must be JPG/PNG

* Indicate that admin buttons are hidden until login is verified

**Step 4 – Privacy by design**

The Bug Tracker collects minimal data:

* No personal accounts, only bug descriptions

- No tracking or analytics

* Uploaded files stored temporarily, deleted after 7 days

**Step 5 – Sample error messages**

* “Only .jpg and .png files up to 2MB are allowed.”

- “Login required to access this section.”

* “Oops! Something went wrong. Please try again later.”

Include these examples in your SDS template and adapt them to your own project.

</details>
