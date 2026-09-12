# ISO 27001 GRC Risk Assessment
<img width="709" height="345" alt="Screenshot 2026-09-10 at 22 59 57" src="https://github.com/user-attachments/assets/9cf09fa9-60f0-400d-a89c-e4be6aa0f351" />

## Overview

This project demonstrates a practical, junior-level understanding of Governance, Risk and Compliance (GRC) principles within an information security environment.

The assessment is based on a **SIMULATED** German cloud-based financial services company, **FinSecure Cloud GmbH**.

The project applies concepts from:

* ISO/IEC 27001:2022
* ISO/IEC 27001:2022 Annex A
* GDPR
* BSI Cloud Computing Compliance Criteria Catalogue (C5)
* Risk assessment and risk treatment principles

The objective is not to perform a formal ISO 27001 audit or certification assessment. Instead, this project demonstrates:

**✨how a junior security professional can identify information-security risks, assess their potential impact, select appropriate treatments, and map security measures to relevant controls.✨**

---
  ## STRUCTURE


                    ORGANIZATION
                         │
                         ▼
                    ISMS SCOPE
                         │
                         ▼
                   ASSET INVENTORY
                         │
          ┌──────────────┼──────────────┐
          ▼              ▼              ▼
       DATA           SYSTEMS        IDENTITIES
          │              │              │
          └──────────────┼──────────────┘
                         ▼
                       RISKS
                         │
                         ▼
                   RISK ASSESSMENT
                         │
                         ▼
                   RISK TREATMENT
                         │
                         ▼
                  SECURITY CONTROLS
                         │
                         ▼
               ISO 27001 CONTROL MAPPING
                         │
                         ▼
                 EVIDENCE / REVIEW
---

## Scenario

**Organization:** FinSecure Cloud GmbH
**Industry:** Financial Services
**Environment:** Cloud-based application hosted in Microsoft Azure
**Location:** Germany

FinSecure Cloud GmbH provides a cloud-based financial management platform to business customers.

The environment contains:

* Customer account information
* Financial and transaction-related data
* Employee accounts
* Azure-hosted virtual machines
* Cloud databases
* Application services
* Security and system logs

**Because FinSecure processes sensitive business and personal information, the organization must consider:**
1) information security ✅
2) privacy ✅
3) regulatory requirements ✅
4) cloud-security risks ✅

---

## Project Objectives

The objectives of this assessment are to:

1. Define the scope and context of the information-security environment.
2. Identify important information assets.
3. Identify relevant threats and vulnerabilities.
4. Assess information-security risks.
5. Determine appropriate risk treatments.
6. Map selected security measures to ISO/IEC 27001:2022 Annex A controls.
7. Create a simplified Statement of Applicability (SoA).
8. Identify examples of evidence that could demonstrate control implementation.

---

## Project Workflow

The project follows a simplified risk-based GRC workflow:

```text
Scope & Context
       ↓
Asset Inventory
       ↓
Risk Assessment
       ↓
Risk Treatment
       ↓
ISO/IEC 27001 Control Mapping
       ↓
Statement of Applicability
       ↓
Evidence
```

Each stage builds on the previous stage to demonstrate how information-security risks can be identified, treated, mapped to security controls, and supported by evidence.

---

## Key Project Outputs

### 1. ISMS Scope & Context

Defined the boundaries of the simulated Information Security Management System (ISMS), including:

* Organizational context
* Interested parties
* Information-security objectives
* Cloud environment
* Scope boundaries
* Security assumptions

### 2. Asset Inventory

Identified critical information, systems, identities, and supporting services.

Assets were evaluated against:

* Confidentiality
* Integrity
* Availability
* Business importance
* Ownership

### 3. Risk Register

Created a simplified 5×5 risk assessment methodology using:

**Risk = Likelihood × Impact**

Eight example risks were identified and prioritized, including:

* Privileged account compromise
* Unauthorized customer-data access
* Vulnerable cloud systems
* Employee account compromise
* Log manipulation
* Ransomware-related backup destruction
* Application outage
* Source-code repository compromise

### 4. Risk Treatment Plan

Developed treatment strategies for identified risks using:

* Mitigation
* Avoidance
* Transfer
* Acceptance

Controls and actions were assigned to appropriate risk owners, with consideration given to residual risk.

### 5. ISO/IEC 27001:2022 Control Mapping

Mapped identified risks and treatment measures to relevant ISO/IEC 27001:2022 Annex A controls.

Example:

```text
Privileged Account Compromise
          ↓
MFA + Least Privilege + PAM
          ↓
A.5.15 / A.5.16 / A.5.17 / A.5.18
          ↓
Access Reviews + MFA Reports + Logs
```

### 6. Statement of Applicability

Created a simplified Statement of Applicability identifying:

* Applicable controls
* Implementation status
* Risk addressed
* Justification
* Potential supporting evidence

### 7. Security Evidence

Identified examples of evidence that could demonstrate that security controls are implemented and operating.

Examples include:

* Access reviews
* MFA reports
* Vulnerability-management reports
* SIEM configuration
* Security logs
* Backup and recovery tests
* Security-awareness records
* Incident records
* Repository access controls

---

## Skills Demonstrated

This project demonstrates practical familiarity with:

* Governance, Risk & Compliance (GRC)
* ISO/IEC 27001:2022 concepts
* Information Security Management Systems (ISMS)
* Risk identification and assessment
* Likelihood and impact analysis
* Risk treatment and residual risk
* Security-control selection
* ISO 27001 Annex A control mapping
* Statement of Applicability (SoA)
* Security evidence and audit readiness
* Access control and identity management
* Cloud security considerations
* Security logging and monitoring
* Vulnerability management
* Business continuity and recovery
* Security awareness

---

## Security Operations Connection

Although this project focuses on GRC, many of the controls have direct relevance to security operations.

For example:

**SOC activity:**

A SIEM detects suspicious administrator authentication activity.

**GRC perspective:**

The organization should be able to demonstrate that:

* Privileged accounts are identified
* Strong authentication is required
* Access is restricted
* Administrator activity is logged
* Security events are monitored
* Access rights are periodically reviewed

This demonstrates the relationship between technical security operations and governance/compliance processes.

---

## Project Outcome

The completed project demonstrates a simplified end-to-end approach to information-security risk management:

**Identify → Assess → Treat → Control → Evidence → Review**

The objective is not to simulate an ISO certification audit, but to demonstrate practical understanding of how GRC activities support an organization's broader information-security program.

---

## Disclaimer

This is an educational cybersecurity portfolio project using a fictional organization and simulated information.

It is intended to demonstrate practical familiarity with GRC, information-security risk management, and ISO/IEC 27001 concepts.

**⛔️It does not represent an official ISO 27001 audit, certification assessment, legal GDPR assessment, or C5 attestation.⛔️**
