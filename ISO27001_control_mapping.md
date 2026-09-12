# ISO/IEC 27001:2022 Control Mapping

## 1. Purpose

The purpose of this document is to map the risks identified in the risk register and the corresponding risk treatments to relevant ISO/IEC 27001:2022 Annex A controls.

This demonstrates how identified security risks can be addressed through appropriate organizational, people, physical, and technological controls.

This project uses a simplified control mapping approach for educational purposes. It is not intended to represent a complete ISO/IEC 27001 control assessment or certification audit.

---

## 2. What Is Control Mapping?

Control mapping is the process of connecting:

**Risk → Risk Treatment → Security Control → Evidence**

For example:

> Privileged account compromise
> ↓
> Implement stronger authentication and access restrictions
> ↓
> Apply access-control and identity-management controls
> ↓
> Evidence such as MFA configuration, access reviews, and administrator logs

The purpose is to demonstrate that security controls are not being selected randomly. They are connected to actual business risks.

---

## 3. Important ISO/IEC 27001 Principle

ISO/IEC 27001 uses a risk-based approach to information security.

Annex A provides a reference set of information-security controls that organizations compare against the results of their risk assessment and treatment process.

An organization does not simply implement every Annex A control because it appears in the standard.

Instead, the organization determines which controls are necessary based on its risks, business requirements, legal requirements, contractual requirements, and other relevant circumstances.

The selected controls are then documented in the Statement of Applicability (SoA).

For this project, only the controls relevant to the identified risks are mapped.

---

## 4. Risk-to-Control Mapping

| Risk ID | Risk                                     | Relevant ISO/IEC 27001:2022 Controls                                                                                                              | Purpose of Control                                                                  |
| ------- | ---------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| R-01    | Privileged account compromise            | A.5.15 Access control; A.5.16 Identity management; A.5.17 Authentication information; A.5.18 Access rights                                        | Restrict privileged access and strengthen identity and authentication controls      |
| R-02    | Unauthorized customer database access    | A.5.15 Access control; A.5.18 Access rights; A.8.15 Logging; A.8.16 Monitoring activities                                                         | Restrict database access and detect suspicious activity                             |
| R-03    | Exploitation of vulnerable Azure systems | A.5.23 Information security for use of cloud services; A.8.8 Management of technical vulnerabilities; A.8.9 Configuration management              | Manage cloud security, vulnerabilities, and secure configurations                   |
| R-04    | Employee account compromise              | A.5.16 Identity management; A.5.17 Authentication information; A.5.18 Access rights; A.6.3 Information security awareness, education and training | Protect identities and reduce the likelihood of successful credential-based attacks |
| R-05    | Security log manipulation                | A.8.15 Logging; A.8.16 Monitoring activities                                                                                                      | Maintain useful security logs and monitor security-relevant activity                |
| R-06    | Backup destruction by ransomware         | A.8.13 Information backup; A.5.30 ICT readiness for business continuity                                                                           | Protect backups and support recovery from disruptive incidents                      |
| R-07    | Customer-facing application outage       | A.5.30 ICT readiness for business continuity; A.8.14 Redundancy of information processing facilities; A.8.16 Monitoring activities                | Improve resilience, availability, and detection of service disruption               |
| R-08    | Source-code repository compromise        | A.8.4 Access to source code; A.8.25 Secure development life cycle; A.8.28 Secure coding                                                           | Restrict source-code access and integrate security into development                 |

The selected controls reflect the risks identified for the fictional FinSecure Cloud GmbH environment. The control numbers and titles are based on the ISO/IEC 27001:2022 Annex A control structure.

---

## 5. Detailed Control Mapping

### R-01 — Privileged Account Compromise

**Risk:**

An attacker steals administrator credentials and gains privileged access to critical systems.

**Treatment:**

* Multi-factor authentication (MFA)
* Least privilege
* Privileged Access Management (PAM)
* Periodic access reviews
* Administrator activity logging

**Relevant controls:**

**A.5.15 — Access control**

Access to systems and information should be restricted according to business and security requirements.

**A.5.16 — Identity management**

Identities should be managed throughout their lifecycle, including creation, modification, and removal.

**A.5.17 — Authentication information**

Authentication information should be appropriately managed and protected.

**A.5.18 — Access rights**

Access rights should be assigned, reviewed, modified, and removed according to organizational requirements.

**Example evidence:**

* MFA configuration
* Privileged-account inventory
* Access-review records
* PAM configuration
* Administrator activity logs

---

### R-02 — Unauthorized Customer Database Access

**Risk:**

An unauthorized user obtains access to customer information because permissions are too broad.

**Treatment:**

* Role-Based Access Control (RBAC)
* Least privilege
* Periodic access reviews
* Database monitoring

**Relevant controls:**

* A.5.15 — Access control
* A.5.18 — Access rights
* A.8.15 — Logging
* A.8.16 — Monitoring activities

**Example evidence:**

* Database access-control configuration
* User/role permission lists
* Access-review records
* Database audit logs
* Monitoring alerts

---

### R-03 — Exploitation of Vulnerable Azure Systems

**Risk:**

An attacker exploits a known vulnerability in the production environment.

**Treatment:**

* Vulnerability scanning
* Patch management
* Secure configuration
* Remediation tracking
* Cloud security monitoring

**Relevant controls:**

**A.5.23 — Information security for use of cloud services**

Security requirements should be addressed when using, managing, and changing cloud services.

**A.8.8 — Management of technical vulnerabilities**

Technical vulnerabilities should be identified, evaluated, and managed according to risk.

**A.8.9 — Configuration management**

Configurations should be established and managed to support secure operation.

**Example evidence:**

* Vulnerability scan reports
* Patch-management records
* Remediation tickets
* Azure configuration baselines
* Cloud security alerts

---

### R-04 — Employee Account Compromise

**Risk:**

An attacker compromises an employee account through phishing or credential theft.

**Treatment:**

* MFA
* Conditional access
* Security awareness training
* Identity monitoring
* Periodic access reviews

**Relevant controls:**

* A.5.16 — Identity management
* A.5.17 — Authentication information
* A.5.18 — Access rights
* A.6.3 — Information security awareness, education and training

**Example evidence:**

* MFA enrollment reports
* Conditional-access policies
* Security-awareness training records
* Phishing-awareness exercises
* Identity monitoring alerts

---

### R-05 — Security Log Manipulation

**Risk:**

An attacker alters or deletes security logs, reducing the organization's ability to investigate an incident.

**Treatment:**

* Centralized logging
* Restricted log access
* Log-integrity protection
* Log retention
* Security monitoring

**Relevant controls:**

* A.8.15 — Logging
* A.8.16 — Monitoring activities

**Example evidence:**

* SIEM configuration
* Log-retention settings
* Log-access permissions
* Security monitoring dashboards
* Alerting rules

This is particularly relevant to security operations because logs provide evidence for detecting and investigating security events.

---

### R-06 — Backup Destruction by Ransomware

**Risk:**

An attacker encrypts or destroys production systems and backup data.

**Treatment:**

* Isolated backups
* Restricted backup access
* Backup testing
* Recovery procedures
* Backup monitoring

**Relevant controls:**

* A.8.13 — Information backup
* A.5.30 — ICT readiness for business continuity

**Example evidence:**

* Backup schedules
* Backup-success reports
* Backup access-control configuration
* Recovery-test results
* Business continuity procedures

---

### R-07 — Customer-Facing Application Outage

**Risk:**

Customers cannot access the financial platform because of an outage or disruptive event.

**Treatment:**

* Availability monitoring
* Redundant infrastructure
* DDoS protection
* Incident response
* Business continuity planning

**Relevant controls:**

* A.5.30 — ICT readiness for business continuity
* A.8.14 — Redundancy of information processing facilities
* A.8.16 — Monitoring activities

**Example evidence:**

* Availability-monitoring reports
* Architecture documentation
* Redundancy configuration
* Incident records
* Business continuity tests

---

### R-08 — Source-Code Repository Compromise

**Risk:**

An attacker gains unauthorized access to proprietary source code or modifies it.

**Treatment:**

* Repository access controls
* MFA
* Branch protection
* Code review
* Repository monitoring

**Relevant controls:**

* A.8.4 — Access to source code
* A.8.25 — Secure development life cycle
* A.8.28 — Secure coding

**Example evidence:**

* Repository permission lists
* MFA configuration
* Branch-protection settings
* Pull-request/code-review records
* Repository audit logs

---

## 6. Control, Risk, and Evidence Relationship

The relationship between the project components can be represented as:

```text
BUSINESS ASSET
      ↓
IDENTIFIED RISK
      ↓
RISK ASSESSMENT
      ↓
RISK TREATMENT
      ↓
SECURITY CONTROL
      ↓
EVIDENCE
      ↓
REVIEW & MONITORING
```

For example:

```text
Privileged Administrator Account
            ↓
Credential Theft
            ↓
Critical Risk
            ↓
MFA + Least Privilege + PAM
            ↓
ISO 27001 Annex A Controls
            ↓
MFA Reports + Access Reviews + Logs
            ↓
Periodic Review
```

This demonstrates an important GRC principle:

**Controls should have a reason for existing.**

The organization should be able to explain what risk a control addresses and how it can demonstrate that the control is operating.

---

## 7. Preventive, Detective, and Corrective Controls

Controls can also be considered according to what they accomplish.

### Preventive controls

Designed to reduce the likelihood of an unwanted event.

Examples:

* MFA
* Least privilege
* RBAC
* Secure configuration
* Security awareness training

### Detective controls

Designed to identify suspicious activity or security events.

Examples:

* Security logging
* SIEM monitoring
* Identity monitoring
* Vulnerability scanning
* Security alerts

### Corrective / Recovery controls

Designed to help restore secure operations after an incident.

Examples:

* Backups
* Disaster recovery
* Incident response
* System recovery procedures
* Business continuity planning

A mature security program normally requires a combination of all three.

---

## 8. Why the Mapping Matters

The control mapping provides the connection between the risk-management process and ISO/IEC 27001.

Without this connection, an organization might have:

> A list of security controls

but no clear explanation of:

> Why those controls are necessary.

With risk-based mapping, the organization can demonstrate:

> "We identified this risk, determined that it required treatment, selected these controls, and can provide evidence that those controls are operating."

This is much closer to how GRC works in practice.

---

## 9. Relationship to the Statement of Applicability

The control mapping provides the foundation for the next stage of this project:

**Statement of Applicability (SoA).**

The SoA will document which relevant controls are:

* Applicable
* Not applicable
* Implemented
* Planned

and provide a justification for the organization's decisions.

The SoA therefore acts as a formal bridge between the organization's risk treatment process and its selected security controls.

---

## 10. Project Conclusion

The control-mapping exercise demonstrates how FinSecure Cloud GmbH can connect identified information-security risks with appropriate ISO/IEC 27001:2022 Annex A controls.

The process followed was:

**Asset → Risk → Treatment → Control → Evidence**

This demonstrates a practical understanding of risk-based information security management rather than simply memorizing ISO control numbers.

> **Note:** Control descriptions in this educational project are summarized for learning purposes. The authoritative ISO/IEC 27001:2022 standard should be consulted for the official control wording and requirements.
