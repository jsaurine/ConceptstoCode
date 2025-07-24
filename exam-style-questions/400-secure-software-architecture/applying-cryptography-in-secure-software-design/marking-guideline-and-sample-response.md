---
description: >-
  Review a full-mark extended response, a completed SSDLC comparison table, and
  detailed marking criteria to strengthen your exam technique.
hidden: true
---

# Marking guideline and sample response

### Completed planning table (model answer)

<table data-header-hidden><thead><tr><th width="178.1484375">Design goal</th><th>How cryptography supports it</th></tr></thead><tbody><tr><td>Data protection</td><td>Encrypts data at rest (e.g. AES-encrypted databases) and in transit (e.g. HTTPS) to prevent unauthorised access.</td></tr><tr><td>Regulatory compliance</td><td>Satisfies requirements in privacy laws (e.g. GDPR, Australian Privacy Act) for data confidentiality and integrity.</td></tr><tr><td>Security by design</td><td>Embeds protection mechanisms like password hashing, digital signatures, and secure key handling into architecture from the start.</td></tr><tr><td>Privacy</td><td>Uses encryption to ensure personal data remains confidential, even if accessed by unauthorised users or third parties.</td></tr></tbody></table>

### Marking guideline (5 marks)

<table data-header-hidden><thead><tr><th width="102.06640625"></th><th></th></tr></thead><tbody><tr><td><strong>Mark</strong></td><td><strong>Criteria</strong></td></tr><tr><td>5</td><td>Demonstrates thorough understanding of how cryptographic techniques support software design. Accurately explains and applies at least two of the design goals listed. Uses clear examples.</td></tr><tr><td>4</td><td>Clearly explains cryptographic techniques in relation to at least one goal, and identifies a second with some accuracy.</td></tr><tr><td>3</td><td>Provides general explanation with some reference to cryptography or a relevant goal. Lacks clarity or detail.</td></tr><tr><td>2</td><td>Identifies a design goal or cryptographic technique with minimal explanation.</td></tr><tr><td>1</td><td>Minimal or unrelated response. Confused or inaccurate use of terms.</td></tr></tbody></table>

***

### Sample response (full marks)

Cryptographic techniques play a critical role in secure system design by ensuring confidentiality, integrity, and compliance with privacy standards.

One primary goal is data protection. For example, storing user passwords in plain text is a serious vulnerability. A secure design would apply hashing and salting (e.g. bcrypt) so that even if the database is breached, the passwords cannot be reversed. Similarly, data stored in files or backups should be encrypted using symmetric encryption (e.g. AES) to prevent unauthorised access.

Cryptography also supports regulatory compliance and privacy. Laws like the Australian Privacy Act and GDPR require that personal data be protected both in transit and at rest. Designing an application to use HTTPS for all web communications encrypts data in transit, ensuring compliance with these regulations and preventing data leaks.

By integrating these techniques into the architecture — not as an afterthought — developers apply a security-by-design approach, ensuring protection is embedded from the start of the software lifecycle.
