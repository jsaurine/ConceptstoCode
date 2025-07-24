---
description: >-
  Review a full-mark extended response, a completed security goal analysis
  table, and detailed marking criteria to strengthen your exam technique.
hidden: true
---

# Marking guideline and sample response

### Completed planning table (model answer)

<table data-header-hidden><thead><tr><th width="191.54296875">Security concept</th><th>How sandboxing helps</th></tr></thead><tbody><tr><td><strong>Security concept</strong></td><td><strong>How sandboxing helps</strong></td></tr><tr><td>Confidentiality</td><td>Isolates untrusted code or components so they cannot access or leak private data.</td></tr><tr><td>Integrity</td><td>Prevents external modules or scripts from modifying internal data or application logic.</td></tr><tr><td>Availability</td><td>Contains faults or failures within a sandbox, reducing the risk of full system crashes.</td></tr><tr><td>Authorisation</td><td>Enforces boundaries between user roles or components, limiting access to only permitted actions.</td></tr><tr><td>Accountability</td><td>Assigns responsibility to sandboxed processes or users, making misuse easier to trace.</td></tr></tbody></table>

### Marking guideline

<table><thead><tr><th width="123.38671875">Mark</th><th>Criteria</th></tr></thead><tbody><tr><td><strong>5</strong></td><td>Clearly explains how sandboxing supports the design stage. Demonstrates strong understanding of security by design. Accurately relates sandboxing to <strong>at least two named security concepts</strong> with relevant examples.</td></tr><tr><td><strong>4</strong></td><td>Explains sandboxing in the context of system design. Relates to at least one security concept with an example. May not fully develop all points.</td></tr><tr><td><strong>3</strong></td><td>Describes sandboxing with some link to security. Mentions a relevant security concept but lacks clear explanation or example.</td></tr><tr><td><strong>2</strong></td><td>Provides general or superficial comments on sandboxing or system design with limited relevance to security concepts.</td></tr><tr><td><strong>1</strong></td><td>Demonstrates minimal or confused understanding. May define sandboxing without linking to security or system design.</td></tr></tbody></table>

### Sample response

Sandboxing supports the system design stage of the SSDLC by enforcing **security by design** — isolating untrusted or potentially risky components to prevent them from compromising the wider system. In this stage, developers make architectural decisions that determine how software modules interact, what resources they can access, and how failures are contained.

For example, a system might be designed so that third-party plug-ins run in a restricted environment where they cannot access sensitive files or memory. This supports the security goals of confidentiality by preventing data leaks and integrity by stopping unauthorised modification of core system data.

Sandboxing also contributes to **authorisation**, because it limits what permissions or APIs an isolated module can access, and to **availability**, because faults in one sandboxed area are less likely to crash the entire application. By embedding these constraints at the design level, sandboxing helps ensure the system remains secure, resilient, and accountable.
