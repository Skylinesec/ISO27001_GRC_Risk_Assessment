# Evidence Examples

## 1. Purpose

The purpose of this document is to identify examples of evidence that could demonstrate the implementation and operation of the security controls identified in the FinSecure Cloud GmbH GRC assessment.

In an actual Information Security Management System (ISMS), evidence helps demonstrate that security controls are not only documented but are implemented, maintained, and operating as intended.

This document provides examples only and does not represent evidence from a real organization.

---

## 2. What Is Security Evidence?

Security evidence is information that can demonstrate that a security requirement or control is being implemented and followed.

Examples include:

* Policies and procedures
* System configurations
* Access-control reports
* Security logs
* Vulnerability reports
* Training records
* Incident records
* Backup reports
* Risk assessments
* Access reviews
* Monitoring reports
* Meeting or management-review records

A useful GRC principle is:

> **If a control is claimed to exist, there should be appropriate evidence supporting that claim.**

---

## 3. Evidence Categories

Evidence can generally be divided into several categories.

### Policy and Documentation Evidence

Demonstrates that requirements and processes have been formally defined.

Examples:

* Information security policy
* Access-control policy
* Incident-response procedure
* Backup procedure
* Vulnerability-management procedure
* Business continuity plan

### Technical Evidence

Demonstrates that security controls are configured or operating within systems.

Examples:

* MFA configuration
* RBAC configuration
* Firewall rules
* Azure security configuration
* SIEM configuration
* Endpoint-security configuration
* Repository access settings

### Operational Evidence

Demonstrates that security processes are actually being performed.

Examples:

* Access-review records
* Vulnerability remediation tickets
* Backup test results
* Security-monitoring reports
* Incident tickets
* Patch-management reports

### Training Evidence

Demonstrates that personnel have received required security awareness or training.

Examples:

* Training completion records
* Security-awareness campaigns
* Phishing-awareness exercise results
* Training materials

---

## 4. Risk-to-Evidence Mapping

| Risk ID | Risk                                     | Relevant Controls              | Example Evidence                                                                                 |
| ------- | ---------------------------------------- | ------------------------------ | ------------------------------------------------------------------------------------------------ |
| R-01    | Privileged account compromise            | A.5.15, A.5.16, A.5.17, A.5.18 | MFA reports, privileged-account inventory, PAM configuration, access reviews, administrator logs |
| R-02    | Unauthorized customer database access    | A.5.15, A.5.18, A.8.15, A.8.16 | RBAC configuration, database permissions, access reviews, database logs, monitoring alerts       |
| R-03    | Exploitation of vulnerable Azure systems | A.5.23, A.8.8, A.8.9           | Vulnerability scans, patch reports, remediation tickets, Azure configuration records             |
| R-04    | Employee account compromise              | A.5.16, A.5.17, A.5.18, A.6.3  | MFA reports, conditional-access configuration, training records, phishing-awareness results      |
| R-05    | Security log manipulation                | A.8.15, A.8.16                 | SIEM configuration, log-retention settings, log-access permissions, monitoring alerts            |
| R-06    | Backup destruction by ransomware         | A.8.13, A.5.30                 | Backup reports, backup-access controls, recovery-test results, recovery procedures               |
| R-07    | Customer-facing application outage       | A.5.30, A.8.14, A.8.16         | Availability reports, redundancy configuration, incident records, continuity tests               |
| R-08    | Source-code repository compromise        | A.8.4, A.8.25, A.8.28          | Repository permissions, branch-protection settings, code-review records, repository audit logs   |

---

## 5. Example Evidence — Access Control

### Control Area

Access control and access rights.

### Relevant Risks

* R-01 — Privileged account compromise
* R-02 — Unauthorized customer database access
* R-04 — Employee account compromise
* R-08 — Source-code repository compromise

### Possible Evidence

**1. User access review**

A periodic report showing:

* User identity
* Role
* Systems accessible
* Privilege level
* Review date
* Reviewer
* Approval/removal decision

**2. Privileged-account inventory**

A list of administrator accounts showing:

* Account owner
* Privilege level
* Business justification
* MFA status
* Last review date

**3. MFA configuration**

Evidence showing that MFA is enforced for privileged accounts.

**4. RBAC configuration**

Evidence showing that users receive permissions according to their roles.

### What This Demonstrates

The organization can demonstrate that access is controlled rather than simply claiming:

> "We use least privilege."

---

## 6. Example Evidence — Vulnerability Management

### Control

A.8.8 — Management of technical vulnerabilities

### Relevant Risk

R-03 — Exploitation of vulnerable Azure systems

### Possible Evidence

A vulnerability-management report could contain:

| Finding                | Severity | Asset              | Status      | Owner            | Due Date   |
| ---------------------- | -------- | ------------------ | ----------- | ---------------- | ---------- |
| Critical vulnerability | Critical | Production VM      | Open        | Cloud Operations | 2026-09-15 |
| Outdated software      | High     | Application Server | Remediated  | IT Operations    | 2026-09-10 |
| Misconfiguration       | Medium   | Azure Resource     | In Progress | Cloud Operations | 2026-09-20 |

Additional evidence could include:

* Vulnerability scan results
* Patch-management reports
* Remediation tickets
* Risk acceptance records
* Exception approvals
* Retest results

### What This Demonstrates

The organization has a repeatable process for:

**Identify → Prioritize → Remediate → Verify**

rather than simply running a vulnerability scanner.

---

## 7. Example Evidence — Security Logging and Monitoring

### Controls

* A.8.15 — Logging
* A.8.16 — Monitoring activities

### Relevant Risks

* R-02 — Unauthorized database access
* R-05 — Security log manipulation
* R-07 — Application outage
* R-08 — Source-code repository compromise

### Possible Evidence

* SIEM configuration
* Log-source inventory
* Authentication logs
* Administrator activity logs
* Database audit logs
* Cloud security logs
* Monitoring dashboards
* Alerting rules
* Log-retention configuration
* Incident investigation records

### Example

A security monitoring report could show:

```text
Event:
Multiple failed administrator logins

Source:
Production environment

User:
admin-account

Time:
2026-09-10 14:32 UTC

Detection:
SIEM authentication alert

Investigation:
Security analyst reviewed authentication activity.

Result:
Activity determined to be suspicious and escalated for investigation.
```

### What This Demonstrates

Logging provides visibility, while monitoring turns that visibility into detection.

This is particularly relevant to Security Operations Center (SOC) work.

---

## 8. Example Evidence — Security Awareness

### Control

A.6.3 — Information security awareness, education and training

### Relevant Risk

R-04 — Employee account compromise

### Possible Evidence

* Security-awareness policy
* Training materials
* Training completion report
* Phishing-awareness campaign
* Phishing simulation results
* Follow-up training records

### Example

```text
Security Awareness Campaign

Topic:
Phishing and Credential Security

Target:
All employees

Completion:
95%

Follow-up:
Employees who did not complete training were notified.

Review:
Security team reviewed campaign results and identified
areas requiring additional awareness training.
```

### What This Demonstrates

Security awareness is not simply:

> "Employees were told to be careful."

There should be a defined process and evidence that the process was carried out.

---

## 9. Example Evidence — Backup and Recovery

### Controls

* A.8.13 — Information backup
* A.5.30 — ICT readiness for business continuity

### Relevant Risk

R-06 — Backup destruction by ransomware

### Possible Evidence

* Backup schedule
* Backup-success reports
* Backup-retention configuration
* Backup-access permissions
* Backup isolation configuration
* Recovery-test results
* Business continuity procedures

### Example Recovery Test

```text
Recovery Test

System:
Customer Application

Test Date:
2026-09-05

Objective:
Verify that critical application data can be restored.

Result:
Successful

Recovery Time:
Within defined recovery objective

Issues:
Minor documentation issue identified

Corrective Action:
Update recovery documentation
```

### What This Demonstrates

A backup that has never been tested provides less assurance than a backup that has been successfully restored and verified.

---

## 10. Example Evidence — Incident Management

### Relevant Controls

Incident-management controls can support several risks within this project.

### Possible Evidence

* Incident-response policy
* Incident tickets
* Security-alert records
* Investigation timelines
* Escalation records
* Communication records
* Post-incident reviews
* Corrective-action records

### Example Incident Record

```text
Incident ID:
INC-2026-0042

Date:
2026-09-09

Severity:
High

Description:
Suspicious authentication activity detected against
a privileged administrator account.

Initial Detection:
Security monitoring alert

Actions:
- Account activity reviewed
- Authentication logs investigated
- Access temporarily restricted
- Relevant stakeholders notified
- Additional investigation initiated

Status:
Contained / Under Investigation

Follow-up:
Review privileged-account controls and authentication policies.
```

### What This Demonstrates

The organization has a repeatable approach for responding to security events rather than handling each incident differently.

---

## 11. Evidence Quality

Not all evidence provides the same level of assurance.

Good evidence should generally be:

### Relevant

It directly supports the control being assessed.

### Reliable

It comes from a trustworthy source.

### Current

It reflects the organization's current environment and processes.

### Traceable

It can be connected to a specific system, process, user, control, or period.

### Complete

It provides enough information to understand what occurred.

For example:

> "MFA is enabled."

is a statement.

A current MFA configuration report showing privileged accounts and enforcement status is much stronger evidence.

---

## 12. Evidence Lifecycle

Evidence should also be managed over time.

A simplified lifecycle is:

```text
Control Requirement
       ↓
Evidence Generated
       ↓
Evidence Collected
       ↓
Evidence Reviewed
       ↓
Evidence Stored
       ↓
Periodic Reassessment
       ↓
Control Improvement
```

Evidence should not simply be collected once before an audit.

Security controls operate continuously, so evidence may need to be generated and reviewed periodically.

---

## 13. GRC Evidence vs SOC Evidence

There is an important connection between GRC and Security Operations.

A SOC analyst may look at:

> "What happened?"

GRC may ask:

> "Do we have a control designed to prevent or detect this?"

and:

> "Can we demonstrate that the control is operating?"

For example:

### SOC perspective

A suspicious administrator login is detected in the SIEM.

### GRC perspective

The organization should be able to demonstrate:

* Administrator accounts are identified
* Authentication requirements are defined
* MFA is enforced
* Privileged access is restricted
* Administrator activity is logged
* Access is periodically reviewed

The same technical data can therefore support both security operations and compliance activities.

---

## 14. Evidence and Continuous Improvement

Evidence can also identify weaknesses in the security program.

For example:

```text
Access Review
      ↓
Inactive privileged account discovered
      ↓
Account removed
      ↓
Process reviewed
      ↓
Offboarding procedure improved
```

This demonstrates the continual-improvement mindset associated with an effective ISMS.

The objective is not simply to "pass an audit."

The objective is to continually improve information security.

---

## 15. Project Conclusion

The evidence exercise completes the simplified GRC workflow developed throughout this project:

**Scope → Assets → Risks → Risk Treatment → Controls → Applicability → Evidence**

The project demonstrates how an organization can move from identifying what needs protection to determining how security controls should be implemented and how their operation could be demonstrated.

The key principle is:

> **A mature security program should be able to explain what it protects, what could go wrong, what controls address the risk, and what evidence demonstrates that those controls are working.**

---

## 16. Educational Disclaimer

This project is a fictional educational simulation created to demonstrate basic GRC and ISO/IEC 27001 concepts.

It is not:

* An ISO/IEC 27001 certification assessment
* A formal audit
* A real organization's risk assessment
* A legal GDPR assessment
* A C5 attestation
* Professional compliance advice

Evidence examples are illustrative and contain no real organizational information.
