---
description: >-
  The Waterfall approach is a sequential and structured approach to software
  development. Each phase must be completed before the next begins, ensuring
  thorough documentation and step-by-step execution.
cover: ../../../.gitbook/assets/101-hero.png
coverY: 0
---

# 112 Software development lifecycle

### TL:DR

The Waterfall model is a structured, sequential approach to software development where each phase must be completed before moving to the next. It ensures thorough documentation and well-defined processes but lacks flexibility for changes. This model is most effective for projects with stable requirements and strict compliance needs.

***

### Targets

By the end of this section, students will be able to:

* Describe the Waterfall model and its sequential approach to software development.
* Identify the key stages of the Waterfall development lifecycle, including requirements analysis, design, implementation, testing, deployment, and maintenance.
* Explain the advantages and limitations of the Waterfall model compared to iterative development approaches.
* Analyse how requirements gathering impacts later stages of development.
* Recognise the role of documentation and planning in the structured software development process.
* Evaluate real-world applications where the Waterfall model is most effective.

***

### Key phases in the Waterfall approach

The Waterfall model consists of six main phases. Each phase has specific deliverables and generates key documentation for future reference.

<figure><img src="../../../.gitbook/assets/Microsoft Edge 2025-03-06 17.38.19.png" alt=""><figcaption><p>The six key stages in the Waterfall methodology are used and sequenced differently in other Agile methodologies.</p></figcaption></figure>



{% stepper %}
{% step %}
### Requirements analysis

This phase aims to gather, document, and define all functional and non-functional requirements.

**Key activities** include conducting stakeholder meetings and interviews, defining the project's scope, identifying system constraints related to performance, security, and usability, and analyzing risks and feasibility.

**Documentation** includes the software requirements specification, which defines functional and non-functional requirements and acts as a contract between stakeholders and developers. Use case diagrams and user stories to illustrate how users interact with the system. A risk analysis report identifies potential risks and mitigation strategies.
{% endstep %}

{% step %}
### System design

This phase aims to translate requirements into a structured software architecture.

**Key activities** include designing the system structure, identifying software components and their interactions, and defining data models and database structures.

The **documentation** produced includes the high-level design document, which describes the system architecture, major modules, and their interactions. The low-level design document details how each module functions, including algorithms, data structures, and class diagrams. Data flow diagrams and entity-relationship diagrams illustrate how data moves through the system. A technology stack report lists the programming languages, frameworks, and tools used.
{% endstep %}

{% step %}
### Implementation

The purpose of this phase is to convert the system design into actual code.

**Key activities** include developing the software using the selected programming language, breaking down the project into modules and functions, and performing unit testing on individual components.

The **documentation** produced includes source code documentation, which provides well-commented code for future maintainability. Module-level design documentation defines each module's inputs, outputs, and functions. Version control logs track code changes and improvements. Code review reports document peer review findings and suggested improvements.
{% endstep %}

{% step %}
### Testing

This phase aims to ensure the entire system meets functional and non-functional requirements.

**Key activities** include conducting integration testing to ensure modules work together, performing system testing to validate functionality, and implementing user acceptance testing with real users.

The **documentation** produced includes a test plan that defines the testing scope, approach, and success criteria. Test case reports list individual test cases and expected outcomes. Defect logs and bug reports track identified bugs and resolutions. Performance test reports evaluate response time, load handling, and system performance.
{% endstep %}

{% step %}
### **Deployment**

This phase aims to release the software into a production environment.

Key activities include deploying software to live servers, providing user training and documentation, and monitoring initial feedback and bug reports.

Documentation includes release notes and a deployment guide outlining new features, version updates, and known issues. User manuals and help documentation guide end users on software usage. An installation and configuration guide details setup, configurations, and troubleshooting steps. A rollback plan defines steps to revert deployment in case of failure.
{% endstep %}

{% step %}
### **Maintenance**

The purpose of this phase is to ensure long-term functionality and updates.

**Key activities** include monitoring system performance, applying bug fixes and security patches, and enhancing the software with new features.

**Documentation** produced includes issue tracking reports that log bugs and performance issues. Patch management documentation tracks software updates and fixes. Performance logs and system health reports monitor server uptime and response times. A software version history maintains records of all updates and changes.
{% endstep %}
{% endstepper %}

### When the Waterfall approach works best (and when it doesn’t)

The Waterfall model is most effective for projects with well-defined requirements, such as banking software and military systems. It suits projects with stable technologies, such as embedded systems and hospital management software. It is also appropriate for projects that require extensive documentation, such as government contracts and healthcare applications.

Despite these advantages, the Waterfall model has limitations. It is inflexible to change, as revisiting previous phases is difficult and costly. Testing occurs late in the development process, which can result in expensive fixes. Client interaction is limited, as users do not see the software until completion. Long-term projects using the Waterfall model risk becoming outdated due to evolving technology.

### Case study: NASA space shuttle software project

The Waterfall methodology developed software for NASA’s space shuttle missions.

* **Requirements analysis** involved extensive documentation defining every function.
* The **system design** consisted of a complex architecture mapped for high reliability.
* **Implementation** involved highly structured modular code development.
* **Testing** required rigorous simulations and validation before launch.
* The **deployment** involved uploading software to shuttle systems.
* **Maintenance** ensured functionality through updates released over decades.

***

### Key Concepts

> * The Waterfall model is a linear and sequential approach to software development, where each phase must be completed before the next begins. This model is straightforward and has been traditionally used in various engineering disciplines.&#x20;
> * Key stages are
>   * **Requirements analysis**\
>     Gathering and documenting all system requirements.
>   * **System design**\
>     Creating system architecture based on requirements.
>   * **Implementation**\
>     Coding and converting design into a functional system.
>   * **Testing**\
>     Combining system components and verifying functionality.
>   * **Deployment**
>   * Releasing the system to users.
>   * **Maintenance**\
>     Addressing issues and performing updates post-deployment.
> * Advantages are
>   * **Structured approach**\
>     Clear, defined stages facilitate straightforward project management.
>   * **Documentation**\
>     Comprehensive documentation aids in understanding and future maintenance.
>   * **Predictability**\
>     Well-suited for projects with fixed requirements and schedules.
> * Disadvantages are
>   * **Inflexibility**\
>     Difficulty accommodating changes once the project is underway.
>   * **Late testing**\
>     Issues may not be identified until later stages, potentially leading to costly fixes.
>   * **Customer feedback**\
>     Limited opportunities for client input during development.**Concept**\
>     Content



