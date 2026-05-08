# IT Security Audit Report: Botium Toys

**Date:** May 2026
**Auditor:** Chase Harvey
**Organization:** Botium Toys (Fictional Small Business)
**Framework:** NIST Cybersecurity Framework (CSF) v1.1

---

## 1. Executive Summary

An internal security audit was conducted for Botium Toys, a small U.S. business that develops and sells toys online. The scope of this audit was to assess the company's current security posture, identify risks to its assets and data, and provide actionable recommendations for improvement.

The audit found that while Botium Toys has some basic security measures in place, there are **critical gaps** in access control, asset management, and disaster recovery planning. The highest-risk findings, if left unaddressed, could lead to significant financial loss and legal liability from data breaches.

---

## 2. Scope and Goals

*   **Scope:** The audit covered the company's entire digital environment, including its internal network, employee workstations, e-commerce web application, and customer data store.
*   **Primary Goal:** To identify and prioritize risks that threaten the confidentiality, integrity, and availability (CIA) of Botium Toys' information assets.
*   **Compliance Goals:** To align security controls with NIST CSF and begin working towards compliance with relevant standards like PCI DSS (for payment processing).

---

## 3. Risk Assessment

The following risks were identified and prioritized using a standard risk matrix (Likelihood x Impact = Risk Score, rated Critical, High, Medium, or Low).

### Critical Risk

| ID | Risk Description | Likelihood | Impact |
| :--- | :--- | :--- | :--- |
| **R-01** | **Lack of a Disaster Recovery (DR) and Business Continuity (BC) Plan.** A ransomware attack or natural disaster could destroy critical systems and data, leading to indefinite downtime and loss of business. | Medium | High |

### High Risks

| ID | Risk Description | Likelihood | Impact |
| :--- | :--- | :--- | :--- |
| **R-02** | **No centralized Identity and Access Management (IAM) with MFA.** Legacy accounts may be active, and user access is not reviewed. Administrative accounts lack multi-factor authentication (MFA), making them highly susceptible to takeover. | High | Medium |
| **R-03** | **Outdated or missing software patches on critical servers.** Unpatched vulnerabilities (e.g., Log4j, 'EternalBlue') could be exploited by known malware or attackers for remote code execution. | High | Medium |

### Medium Risks

| ID | Risk Description | Likelihood | Impact |
| :--- | :--- | :--- | :--- |
| **R-04** | **Lack of a centralized asset inventory.** The IT team cannot definitively account for all hardware and software, making it impossible to know what needs to be secured or patched. | Medium | Medium |
| **R-05** | **Limited employee security awareness training.** Employees are not trained to recognize sophisticated phishing or social engineering attacks, increasing the risk of credential theft. | Medium | Medium |

### Low Risks

| ID | Risk Description | Likelihood | Impact |
| :--- | :--- | :--- | :--- |
| **R-06** | **Weak password policy.** The current policy only requires 8 characters, with no complexity or annual change requirement, increasing the risk of brute-force attacks. | Medium | Low |

---

## 4. Findings and Recommendations

| Finding | Recommendation | Priority |
| :--- | :--- | :--- |
| **No DR/BC Plan (R-01)** | Immediately develop and document a DR/BC plan. Prioritize critical systems (e.g., e-commerce platform) and offline backups. | **Critical** |
| **No IAM/MFA (R-02)** | Implement a centralized IAM solution (e.g., Azure AD, Okta). Enforce MFA for all users, especially administrators. | High |
| **Outdated software patches (R-03)** | Establish a formal patch management policy. Automate patching for non-critical systems and schedule monthly maintenance windows. | High |
| **No asset inventory (R-04)** | Deploy a network scanning tool (e.g., Lansweeper, Spiceworks) to discover and catalog all connected assets. | Medium |
| **No security training (R-05)** | Purchase or develop an annual security awareness training for all employees. Conduct quarterly simulated phishing tests. | Medium |
| **Weak password policy (R-06)** | Update the password policy to require 12+ characters, complexity, and block common passwords. Consider a password manager. | Low |

---

## 5. Compliance Alignment

*   **NIST CSF (Current):** Partially mapped. **Gaps:** IR (Incident Response), PR (PR.AC for IAM), DE (Detective processes weak), RC (Recovery planning missing).
*   **PCI DSS:** **Non-compliant.** Critical failures for Requirement 8 (strong access control) and Requirement 12 (maintain a policy that addresses information security).
*   **GDPR (if handling EU customer data):** **Potentially Non-compliant.** The lack of data inventory and breach response plan would constitute a violation of Articles 30 and 33.

---

## 6. Conclusion

Immediate action is required to address the critical risk of lacking a disaster recovery plan and the high risks associated with access control. By following the recommendations in this report, Botium Toys can significantly improve its security posture, reduce its exposure to common cyber threats, and make demonstrable progress toward regulatory compliance.

**Next Steps for Management:**
1.  Authorize the immediate development of a DR/BC plan.
2.  Approve budget for an IAM/MFA solution.
3.  Schedule a follow-up audit in 90 days.
