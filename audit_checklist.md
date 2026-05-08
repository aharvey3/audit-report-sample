# Security Audit Walkthrough: Botium Toys Audit Checklist

This checklist was used to guide the audit process, simulating the review questions an auditor would ask.

**Asset Management**
- [x] *Is there a complete inventory of all company hardware (servers, laptops)?* **No.** The team relies on spreadsheets that are often out-of-date.
- [x] *Is there a complete inventory of all software (OS, applications)?* **No.** Unknown software is found on some workstations.

**Identity and Access Control**
- [x] *Is MFA enforced for all user accounts?* **No.**
- [x] *Is there a formal process for onboarding and offboarding employees?* **No.** An account for a former contractor was found to be active.
- [x] *Does the password policy meet NIST SP 800-63b guidelines?* **No.** Current policy is only 8 characters, no complexity rule.

**Data Protection and Disaster Recovery**
- [x] *Are backups performed daily and tested?* **No.** Backups exist but are not tested, and a disaster recovery plan is not documented.
- [x] *Is all sensitive data encrypted at rest?* **Partially.** Customer database is encrypted, but backups are not.

**Vulnerability Management**
- [x] *Are critical security patches applied within two weeks of release?* **No.** A server was found with a six-month-old critical patch missing.
- [x] *Are regular vulnerability scans performed on the internal network?* **No.**
