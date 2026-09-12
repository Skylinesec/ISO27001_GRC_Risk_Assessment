# 02 — Asset Inventory

## 1. Purpose

The purpose of the asset inventory is to identify the information, systems, services, and identities that are important to FinSecure Cloud GmbH.

Identifying assets is an important first step in risk management because security risks cannot be properly assessed without understanding what the organization needs to protect.

The inventory focuses on assets within the defined ISMS scope.

---

## 2. Asset Classification

Assets are grouped into the following categories:

* Information
* Applications
* Infrastructure
* Identity and access
* Security monitoring
* Backup and recovery
* Supporting services

The inventory does not attempt to document every individual device or software component. Instead, it focuses on assets that could have a meaningful impact on information security or business operations.

---

## 3. Asset Inventory

| ID   | Asset                             | Category                  | Owner                | Importance | Information / Function                        | Confidentiality | Integrity | Availability |
| ---- | --------------------------------- | ------------------------- | -------------------- | ---------- | --------------------------------------------- | --------------- | --------- | ------------ |
| A-01 | Customer Database                 | Information / Data        | Data Owner           | Critical   | Customer and account information              | High            | High      | High         |
| A-02 | Financial Transaction Data        | Information / Data        | Finance / Data Owner | Critical   | Financial and transaction-related information | High            | Critical  | High         |
| A-03 | Azure Production Environment      | Infrastructure            | Cloud Operations     | Critical   | Hosts production workloads                    | High            | High      | Critical     |
| A-04 | Customer-Facing Application       | Application               | Application Owner    | Critical   | Provides financial platform services          | High            | High      | Critical     |
| A-05 | Employee Accounts                 | Identity & Access         | IT / Identity Team   | High       | Access to corporate resources                 | High            | High      | High         |
| A-06 | Privileged Administrator Accounts | Identity & Access         | IT / Security        | Critical   | Administrative access to systems              | Critical        | Critical  | Critical     |
| A-07 | Security and Authentication Logs  | Security Monitoring       | Security Team        | High       | Security events and investigation data        | High            | High      | High         |
| A-08 | Source Code Repository            | Application / Information | Development Team     | High       | Application source code                       | High            | High      | Medium       |
| A-09 | Backup Repository                 | Backup & Recovery         | IT Operations        | Critical   | Copies of critical systems and data           | High            | High      | Critical     |
| A-10 | Security Policies and Procedures  | Governance                | Security Management  | Medium     | Rules and requirements for security           | Medium          | High      | Medium       |

---

## 4. Asset Importance

Asset importance is based on the potential effect that compromise, loss, unauthorized modification, or unavailability could have on the organization.

### Critical

Loss or compromise could cause severe business, security, financial, legal, or regulatory consequences.

Examples:

* Customer database
* Financial transaction data
* Production environment
* Privileged administrator accounts

### High

Loss or compromise could significantly affect business operations or security.

Examples:

* Employee accounts
* Security logs
* Source code
* Backup systems

### Medium

Loss or compromise would have a limited but still relevant effect.

Example:

* Security policies and procedures

---

## 5. CIA Requirements

The CIA requirements describe which security properties are most important for each asset.

### Confidentiality

Confidentiality determines how important it is to prevent unauthorized access to the asset.

For example, financial transaction data requires a high level of confidentiality because unauthorized disclosure could harm customers and the organization.

### Integrity

Integrity determines how important it is to prevent unauthorized or accidental modification.

Financial transaction data has a critical integrity requirement because unauthorized changes could result in incorrect financial information or transactions.

### Availability

Availability determines how important it is for the asset to remain accessible when required.

The customer-facing application has a critical availability requirement because prolonged downtime could prevent customers from accessing essential services.

---

## 6. Asset Ownership

Each important asset should have an accountable owner.

The owner does not necessarily perform all technical security activities.

Instead, the owner is responsible for ensuring that the asset is appropriately managed and that relevant security requirements are understood and addressed.

For example:

* The **Data Owner** is responsible for determining appropriate requirements for customer data.
* **Cloud Operations** is responsible for the Azure production environment.
* The **Security Team** is responsible for security monitoring and security-related requirements.
* The **Application Owner** is responsible for the customer-facing application.

Clear ownership supports accountability and effective governance.

---

## 7. Key Observations

Several assets have particularly high security requirements.

### Customer and Financial Data

These assets require strong confidentiality and integrity protections because unauthorized disclosure or modification could have significant consequences.

### Privileged Accounts

Privileged accounts represent a high-value target because compromise could allow an attacker to make significant changes to systems and security configurations.

Additional controls should therefore be considered, including:

* Multi-factor authentication
* Least privilege
* Privileged access management
* Strong authentication
* Access reviews
* Administrative activity logging

### Security Logs

Security logs are important not only for monitoring but also for incident investigation.

If logs are deleted, modified, or unavailable, the security team may lose the ability to determine:

* What happened
* When it happened
* Which account or system was involved
* What actions were performed
* Whether the incident is still active

Logs therefore require protection for both confidentiality and integrity, as well as sufficient availability.

---

## 8. Relationship to Risk Assessment

The asset inventory provides the foundation for the next stage of the assessment.

The following process will be used:

**Asset**

↓

**Threat**

↓

**Vulnerability**

↓

**Risk Event**

↓

**Impact**

↓

**Likelihood**

↓

**Risk Rating**

↓

**Risk Treatment**

For example:

**Asset:** Privileged Administrator Account

**Threat:** Credential theft

**Vulnerability:** Insufficient authentication protection

**Risk Event:** Attacker gains privileged access

**Impact:** Unauthorized changes to critical systems

**Treatment:** Implement MFA, least privilege, privileged access management, and monitoring.

This relationship will be developed in the risk register.
