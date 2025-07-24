---
description: >-
  Review a full-mark extended response, a completed SSDLC comparison table, and
  detailed marking criteria to strengthen your exam technique.
hidden: true
---

# Marking guidelines and sample response

### Completed table: Privacy by Design vs Security by Design

| **Stage**             | **PbD issues to address**                                      | **PbD example(s)**                                                   | **SbyD issues to address**                                            | **SbyD example(s)**                                                |
| --------------------- | -------------------------------------------------------------- | -------------------------------------------------------------------- | --------------------------------------------------------------------- | ------------------------------------------------------------------ |
| **User Requirements** | What personal data is collected? Is consent required?          | Collect only email address; provide opt-out for usage analytics      | What access levels are needed? What is the threat model?              | Define role-based access control (RBAC); conduct STRIDE analysis   |
| **System Design**     | How will data be stored and shared? Will users retain control? | Use data minimisation; anonymise logs; inform users about sharing    | How will authentication, encryption, and input validation be applied? | Design multi-factor authentication (MFA); encrypt sensitive fields |
| **Development**       | Are privacy practices embedded in code?                        | Avoid hardcoded PII; disable tracking in dev environments            | Are secure coding practices followed?                                 | Use parameterised SQL; validate inputs using schemas               |
| **Testing**           | Is real user data protected in test environments?              | Use mock or anonymised datasets; test privacy settings               | Are known vulnerabilities being checked for?                          | Apply SAST and DAST tools; log access attempts and anomalies       |
| **Maintenance**       | Are data retention policies enforced?                          | Remove inactive accounts after 12 months; support user data deletion | Are systems patched and monitored?                                    | Run vulnerability scans; apply security updates promptly           |

### Marking guideline

<table data-header-hidden><thead><tr><th width="110.46875"></th><th></th></tr></thead><tbody><tr><td><strong>Mark</strong></td><td><strong>Criteria</strong></td></tr><tr><td><strong>6</strong></td><td>Demonstrates comprehensive understanding of both Privacy by Design and Security by Design across <strong>at least two distinct stages</strong> of the SSDLC. Explains relevant issues and provides specific, accurate examples. Clearly structured.</td></tr><tr><td><strong>5</strong></td><td>Demonstrates clear understanding of both concepts at two stages. Some examples may lack depth, but structure is logical.</td></tr><tr><td><strong>4</strong></td><td>Identifies both concepts with reasonable understanding but may explain only one well or show gaps in structure.</td></tr><tr><td><strong>3</strong></td><td>Provides basic explanation of one or both concepts, but lacks specific examples or stage-based detail.</td></tr><tr><td><strong>1–2</strong></td><td>Minimal or confused understanding. May generalise without linking to the SSDLC. Examples may be unrelated or vague.</td></tr></tbody></table>

### High-standard model response

Privacy by design (PbD) and security by design (SbD) work together to protect users throughout the software development lifecycle, but they focus on different types of risks. PbD is primarily concerned with minimising data collection, ensuring transparency, and giving users control over their personal information. SbD is focused on defending systems from misuse, vulnerabilities, and technical threats.

In the **requirements phase**, PbD requires that teams identify exactly what personal data is needed and why. A privacy-conscious system might ask only for an email and let users opt out of behavioural tracking. SbD during this phase would include identifying threat models (e.g. STRIDE) and specifying the access controls and authentication required. This lays the foundation for secure architecture.

In the **design phase**, privacy concerns include how data is stored and whether it can be linked to users unnecessarily. For example, anonymising logs or minimising what is written to analytics helps reduce risk. SbD at this stage involves designing encryption systems, structuring permission layers, and identifying entry points where attackers could exploit the system.

In **development**, PbD means avoiding unnecessary telemetry[^1], stripping out test accounts with elevated permissions, and writing clean, auditable code. Security concerns focus on the implementation of input validation, parameterised queries, and secure APIs.

At the **testing stage**, PbD means never using live personal data and validating whether privacy controls (like consent flags) work correctly. SbD includes running automated static and dynamic analysis tools and ensuring that system behaviour matches its intended access control structure.

Finally, in the **maintenance phase**, PbD addresses the duration for which personal data is retained and the processing of deletion requests. SbyD practices here include regular patching, incident response procedures, and continuous monitoring of system health and traffic anomalies.

Together, PbD and SbD produce systems that are **respectful of users and resilient against threats**. While they are conceptually distinct, both must be addressed at each stage of development to meet modern standards of trust and safety.

[^1]: **Telemetry** refers to the **automatic collection and transmission of data** from a system or application back to a central location — typically for monitoring, analytics, or debugging.
