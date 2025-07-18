---
description: >-
  Principles, techniques and approaches that underpin safe and secure software
  design.
---

# 420 Secure software development principles

This section introduces the fundamental principles software engineers use to design secure systems. You’ll explore key techniques that protect data and reduce risk, learn how to apply “security by design” and “privacy by design,” and understand how the software development lifecycle structure contributes to your programs' safety and reliability.

{% tabs %}
{% tab title="Targets" %}
In this section, students learn to

* Describe the steps involved in the secure software development lifecycle
* Apply the CIA security model (confidentiality, integrity, availability) to design decisions
* Explain how cryptography, sandboxing and regulatory compliance support secure software
* Understand and apply the principles of “security by design” and “privacy by design”
* Identify how user capabilities and experience shape secure design features
* Evaluate how security features improve system resilience and reduce vulnerabilities
{% endtab %}

{% tab title="Syllabus" %}
New South Wales Education Standards Authority (2022). _Software Engineering 11–12 Syllabus_. NSW Curriculum. [https://curriculum.nsw.edu.au/learning-areas/tas/software-engineering-11-12-2022](https://curriculum.nsw.edu.au/learning-areas/tas/software-engineering-11-12-2022/overview)

**Outcomes**

* **SE-12-01**\
  Justifies methods used to plan, develop and engineer software solutions
* **SE-12-02**\
  Applies structural elements to develop programming code
* **SE-12-04**\
  Evaluates practices to safely and securely collect, use and store data
* **SE-12-05**\
  Explains the social, ethical and legal implications of software engineering on the individual, society and the environment
* **SE-12-07**\
  Designs, develops and implements safe and secure programming solutions
* **SE-12-08**\
  Tests and evaluates language structures to refine code

[**Secure software architecture / Designing software**](https://curriculum.nsw.edu.au/learning-areas/tas/software-engineering-11-12-2022/content/year-12/fa039e749d#cg-e8644600-1773-4d36-80cc-b5934b32690c)

* Describe the benefits of developing secure software, including data protection, minimising cyber attacks and vulnerabilities
* Interpret and apply fundamental software development steps to develop secure code
* Describe how the capabilities and experience of end users influence the secure design features of software

[**Secure software architecture / Developing secure code**](https://curriculum.nsw.edu.au/learning-areas/tas/software-engineering-11-12-2022/content/year-12/fa039e749d#cg-099b1e72-8fbe-4ed2-842d-787c5fb18bd7)

* Explore fundamental software design security concepts when developing programming code, including: confidentiality, integrity, availability, authentication, authorisation, accountability
* Apply security features incorporated into software, including: data protection, security, privacy, regulatory compliance
* Use and explain the contribution of cryptography and sandboxing to the 'security by design' approach
* Use and explain the 'privacy by design' approach, including: proactive not reactive approach, embed privacy into design, respect for user privacy
{% endtab %}

{% tab title="Glossary" %}
<table><thead><tr><th width="142.62890625" valign="top">Term</th><th valign="top">Definition</th></tr></thead><tbody><tr><td valign="top">CIA triad</td><td valign="top">A model describing the goals of secure software—confidentiality, integrity, and availability</td></tr><tr><td valign="top">security by design</td><td valign="top">An approach that integrates security features and checks into every stage of software development</td></tr><tr><td valign="top">privacy by desig</td><td valign="top">A proactive design philosophy that embeds data privacy principles into software architecture</td></tr><tr><td valign="top">authenticatin</td><td valign="top">A method of verifying a user’s identity before granting access</td></tr><tr><td valign="top">authorisation</td><td valign="top">Defining and enforcing what an authenticated user is allowed to do</td></tr><tr><td valign="top">sandboxing</td><td valign="top">Running code in an isolated environment to prevent it from affecting other parts of the system</td></tr></tbody></table>
{% endtab %}
{% endtabs %}

Building secure software begins well before the first line of code is written. In fact, many software vulnerabilities come not from coding errors but from flawed assumptions, missing design constraints, or a lack of consideration for how systems will be used and misused. This section explores how professional software engineers plan for security from the outset.

At the heart of this work are several guiding principles. The CIA triad—confidentiality, integrity, and availability—describes the goals that all secure systems aim to uphold. Security-conscious developers use these principles to evaluate trade-offs, reduce risk, and design resilient systems, even under attack. Other approaches, such as security by design and privacy by design, help teams embed best practices for protecting users and data throughout the software development lifecycle.

Modern secure development also draws from regulatory requirements and ethical responsibilities. Secure software must often meet compliance standards related to privacy and data protection. The experience and capabilities of users also influence how security is applied in interface design, error handling, and access control. In this section, you’ll learn how to implement these ideas in both theory and practice, starting with the structure of the development lifecycle itself.
