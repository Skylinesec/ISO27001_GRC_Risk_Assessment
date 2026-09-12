# Statement of Applicability (SoA)

## 1. Purpose

The Statement of Applicability (SoA) documents the information-security controls considered relevant to the FinSecure Cloud GmbH Information Security Management System (ISMS).

The SoA provides a structured overview of:

* Which controls are applicable
* Why the controls are applicable
* The implementation status of each control
* The risks or security requirements addressed
* The evidence that could demonstrate implementation

This is a simplified educational example and does not represent an actual ISO/IEC 27001 certification Statement of Applicability.

---

## 2. What Is a Statement of Applicability?

The Statement of Applicability is a key document within an ISO/IEC 27001-aligned ISMS.

It connects the organization's:

**Risk Assessment → Risk Treatment → Security Controls**

The organization reviews the relevant Annex A controls and determines whether they are applicable to its information-security risks and requirements.

A control may be:

* **Applicable** — the control is relevant to the organization's security requirements.
* **Not applicable** — the organization determines that the control is not necessary, with justification.
* **Implemented** — the applicable control has been put into operation.
* **Planned** — the organization considers the control applicable but implementation is not yet complete.

The SoA should provide a clear justification for these decisions.

---

## 3. Applicability Method

For this project, controls were selected based primarily on:

1. Identified information-security risks
2. Risk-treatment decisions
3. Business requirements
4. Cloud environment considerations
5. Protection of customer and financial information
6. Identity and access requirements
7. Security monitoring requirements
8. Availability and business-continuity requirements
9. Secure software-development requirements

The project does not assume that every Annex A control is automatically applicable.

---

## 4. Statement of Applicability

| Control | Control Area                                           | Applicable? | Status  | Risk / Requirement Addressed | Justification                                                                                        |
| ------- | ------------------------------------------------------ | ----------: | ------- | ---------------------------- | ---------------------------------------------------------------------------------------------------- |
| A.5.15  | Access control                                         |         Yes | Planned | R-01, R-02, R-04, R-08       | Access to systems and information must be restricted according to business and security requirements |
| A.5.16  | Identity management                                    |         Yes | Planned | R-01, R-04                   | Employee and privileged identities require controlled lifecycle management                           |
| A.5.17  | Authentication information                             |         Yes | Planned | R-01, R-04                   | Authentication information must be appropriately protected                                           |
| A.5.18  | Access rights                                          |         Yes | Planned | R-01, R-02, R-04             | Excessive or inappropriate permissions could result in unauthorized access                           |
| A.5.23  | Information security for use of cloud services         |         Yes | Planned | R-03                         | FinSecure relies on Microsoft Azure for production infrastructure                                    |
| A.5.30  | ICT readiness for business continuity                  |         Yes | Planned | R-06, R-07                   | Critical financial services require recovery and continuity capabilities                             |
| A.6.3   | Information security awareness, education and training |         Yes | Planned | R-04                         | Employees need awareness of phishing and credential-security risks                                   |
| A.8.4   | Access to source code                                  |         Yes | Planned | R-08                         | Source code is a valuable business asset requiring controlled access                                 |
| A.8.8   | Management of technical vulnerabilities                |         Yes | Planned | R-03                         | Vulnerabilities in production systems can be exploited by attackers                                  |
| A.8.9   | Configuration management                               |         Yes | Planned | R-03                         | Secure and controlled configurations reduce cloud and infrastructure risks                           |
| A.8.13  | Information backup                                     |         Yes | Planned | R-06                         | Critical data and systems require recoverable backups                                                |
| A.8.14  | Redundancy of information processing facilities        |         Yes | Planned | R-07                         | Redundancy can reduce the impact of infrastructure failures                                          |
| A.8.15  | Logging                                                |         Yes | Planned | R-02, R-05, R-08             | Logs provide security evidence and support investigation                                             |
| A.8.16  | Monitoring activities                                  |         Yes | Planned | R-02, R-05, R-07             | Security and availability monitoring supports detection and response                                 |
| A.8.25  | Secure development life cycle                          |         Yes | Planned | R-08                         | Security should be integrated into application development                                           |
| A.8.28  | Secure coding                                          |         Yes | Planned | R-08                         | Secure coding practices reduce software-related vulnerabilities                                      |

---

## 5. Example of a Non-Applicable Control

A control should not be marked "Not Applicable" simply because it is inconvenient to implement.

There must be a reasonable business or security justification.

For example, a physical-security control relating to areas that FinSecure does not operate directly could potentially be considered outside the organization's defined ISMS scope.

FinSecure's production infrastructure is hosted in Microsoft Azure. Therefore, the physical security of Azure's underlying data centers is not directly operated by FinSecure.

For this educational project:

> **Physical security of Azure data centers is outside the defined operational scope of FinSecure's own controls.**

This does not mean physical security is irrelevant.

Instead, responsibility is considered in the context of the cloud provider relationship and the organization's cloud-security requirements.

This illustrates an important cloud GRC concept:

**Shared responsibility does not mean "the cloud provider handles everything."**

The organization must still understand which security responsibilities remain with it.

---

## 6. Implementation Status

The implementation status in this project is intentionally set primarily to **Planned**.

This is because the project is a simulated GRC exercise rather than a real organization's operational ISMS.

A real organization could use statuses such as:

### Implemented

The control is operating and supporting evidence exists.

Example:

> MFA is enforced for privileged administrator accounts and configuration evidence is available.

### Planned

The control has been determined to be necessary but implementation is incomplete.

Example:

> PAM has been approved but deployment is still in progress.

### Not Applicable

The control has been reviewed and determined not to apply to the organization's circumstances, with a documented justification.

### Partially Implemented

The control exists but does not yet fully meet the organization's requirements.

Example:

> MFA is enabled for administrators but has not yet been enforced for all employee accounts.

---

## 7. Example Control Assessment

### A.5.18 — Access Rights

**Applicability:** Yes

**Status:** Planned

**Risks addressed:**

* R-01 — Privileged account compromise
* R-02 — Unauthorized customer database access
* R-04 — Employee account compromise

**Reason for applicability:**

FinSecure processes sensitive customer and financial information and operates critical cloud infrastructure.

Excessive permissions could allow compromised or unauthorized accounts to access or modify critical resources.

**Planned implementation:**

* Least-privilege access
* Role-Based Access Control (RBAC)
* Periodic access reviews
* Joiner/mover/leaver processes
* Removal of unnecessary privileges
* Separate privileged administrator accounts

**Potential evidence:**

* Access-control policy
* RBAC configuration
* User access reviews
* Privileged-account inventory
* Access approval records

---

## 8. Example Control Assessment

### A.8.8 — Management of Technical Vulnerabilities

**Applicability:** Yes

**Status:** Planned

**Risk addressed:**

* R-03 — Exploitation of vulnerable Azure systems

**Reason for applicability:**

FinSecure operates cloud infrastructure and applications that may contain technical vulnerabilities.

Unmanaged vulnerabilities could be exploited to compromise systems or data.

**Planned implementation:**

* Vulnerability scanning
* Vulnerability severity classification
* Patch management
* Remediation deadlines based on risk
* Exception management
* Periodic vulnerability reporting

**Potential evidence:**

* Vulnerability scan reports
* Patch reports
* Remediation tickets
* Vulnerability-management procedures
* Risk exceptions

---

## 9. Example Control Assessment

### A.8.15 — Logging

**Applicability:** Yes

**Status:** Planned

**Risks addressed:**

* R-02 — Unauthorized customer database access
* R-05 — Security log manipulation
* R-08 — Source-code repository compromise

**Reason for applicability:**

Security logs provide visibility into authentication, administrative activity, access to important systems, and potential security incidents.

**Planned implementation:**

* Centralized security logging
* Defined log sources
* Log-retention requirements
* Restricted access to logs
* Protection against unauthorized modification
* Integration with security monitoring

**Potential evidence:**

* SIEM configuration
* Log-source inventory
* Retention configuration
* Monitoring dashboards
* Access-control configuration
* Security alerts

---

## 10. SoA and Evidence

The SoA should not exist in isolation.

For each applicable control, an organization should be able to identify evidence demonstrating how the control is implemented and maintained.

The relationship is:

```text
Risk
  ↓
Risk Treatment
  ↓
ISO 27001 Control
  ↓
Implementation
  ↓
Evidence
  ↓
Review
```

For example:

```text
Credential Theft Risk
        ↓
Implement MFA
        ↓
A.5.17 Authentication Information
        ↓
MFA enforced
        ↓
MFA configuration/report
        ↓
Periodic review
```

This distinction is important:

**A policy saying that MFA is required is not necessarily evidence that MFA is actually enforced.**

A mature GRC process looks for evidence that the control is both **defined and operating**.

---

## 11. Relationship Between the Project Documents

The project now forms a connected GRC workflow:

```text
01 — Scope & Context
          ↓
02 — Asset Inventory
          ↓
03 — Risk Assessment
          ↓
04 — Risk Treatment
          ↓
05 — ISO 27001 Control Mapping
          ↓
06 — Statement of Applicability
          ↓
07 — Evidence
```

Each stage builds on the previous one.

For example:

**Asset:** Privileged administrator account

→ **Risk:** Credential theft

→ **Risk score:** Critical

→ **Treatment:** MFA, least privilege, PAM

→ **ISO controls:** A.5.15, A.5.16, A.5.17, A.5.18

→ **SoA:** Controls are applicable and planned

→ **Evidence:** MFA reports, access reviews, PAM configuration, administrator logs

This is the core logic behind the project.

---

## 12. Key GRC Takeaways

The project demonstrates several fundamental GRC concepts:

### Governance

Establishing policies, responsibilities, decision-making processes, and security requirements.

### Risk

Understanding what could go wrong, how likely it is, and what impact it could have.

### Compliance

Demonstrating that organizational, legal, regulatory, contractual, and security requirements are being addressed.

### Control

A measure designed to reduce risk or support security objectives.

### Evidence

Information demonstrating that a control has been implemented and/or is operating.

### Statement of Applicability

A documented explanation of which relevant security controls apply to the organization and why.

---

## 13. Project Limitation

This Statement of Applicability is intentionally simplified.

A real ISO/IEC 27001 implementation would involve significantly more organizational context, risk criteria, controls, policies, evidence, control owners, implementation details, and management review.

This project demonstrates the methodology and reasoning rather than claiming certification readiness.

---

## 14. Conclusion

The Statement of Applicability provides the connection between FinSecure Cloud GmbH's identified risks and its selected information-security controls.

The project has now progressed from:

**"What do we need to protect?"**

to:

**"What could go wrong?"**

to:

**"What should we do about it?"**

to:

**"Which security controls address those risks?"**

to:

**"Which controls are applicable, and how would we demonstrate implementation?"**

The final stage of the project is therefore to identify the **evidence** that could demonstrate that these controls are actually operating.
