# 03 — Risk Register

## 1. Purpose

The purpose of the risk register is to identify, assess, and document information-security risks affecting assets within the defined ISMS scope.

Risk assessment allows the organization to prioritize security issues based on their potential likelihood and impact rather than treating every issue as equally important.

---

## 2. Risk Assessment Methodology

This project uses a simplified 5 × 5 risk-rating methodology.

### Likelihood

Likelihood represents how probable it is that the identified risk event could occur.

| Score | Rating         | Description                                   |
| ----: | -------------- | --------------------------------------------- |
|     1 | Rare           | Highly unlikely under normal circumstances    |
|     2 | Unlikely       | Could occur, but not expected frequently      |
|     3 | Possible       | Could reasonably occur                        |
|     4 | Likely         | Expected to occur under certain circumstances |
|     5 | Almost Certain | Very likely to occur                          |

### Impact

Impact represents the potential consequences if the risk event occurs.

| Score | Rating     | Description                                                   |
| ----: | ---------- | ------------------------------------------------------------- |
|     1 | Negligible | Minimal effect on the organization                            |
|     2 | Minor      | Limited operational or security impact                        |
|     3 | Moderate   | Noticeable business or security impact                        |
|     4 | Major      | Significant business, financial, legal, or security impact    |
|     5 | Severe     | Critical impact to the organization, customers, or operations |

### Risk Score

The risk score is calculated as:

**Risk = Likelihood × Impact**

The resulting score is used to prioritize risk treatment.

| Score | Risk Level | Treatment Priority             |
| ----: | ---------- | ------------------------------ |
|   1–4 | Low        | Monitor and review             |
|   5–9 | Medium     | Treatment should be considered |
| 10–14 | High       | Treatment required             |
| 15–25 | Critical   | Urgent treatment required      |

---

## 3. Risk Register

| ID   | Asset                             | Threat                       | Vulnerability                          | Risk Event                                                           | Likelihood | Impact | Score | Level    |
| ---- | --------------------------------- | ---------------------------- | -------------------------------------- | -------------------------------------------------------------------- | ---------: | -----: | ----: | -------- |
| R-01 | Privileged Administrator Accounts | Credential theft             | Insufficient authentication protection | Attacker gains privileged access to critical systems                 |          4 |      5 |    20 | Critical |
| R-02 | Customer Database                 | Unauthorized access          | Excessive permissions                  | Unauthorized user accesses customer information                      |          3 |      5 |    15 | Critical |
| R-03 | Azure Production Environment      | Exploitation                 | Unpatched systems                      | Attacker exploits a known vulnerability in production infrastructure |          3 |      5 |    15 | Critical |
| R-04 | Employee Accounts                 | Phishing / credential theft  | Insufficient MFA protection            | Attacker compromises an employee account                             |          4 |      4 |    16 | Critical |
| R-05 | Security and Authentication Logs  | Log deletion or manipulation | Insufficient protection and monitoring | Attacker alters or deletes logs, reducing investigation capability   |          3 |      4 |    12 | High     |
| R-06 | Backup Repository                 | Ransomware                   | Insufficient backup isolation          | Attacker encrypts or destroys production and backup data             |          3 |      5 |    15 | Critical |
| R-07 | Customer-Facing Application       | Denial of Service            | Insufficient resilience                | Customers cannot access the financial platform                       |          3 |      4 |    12 | High     |
| R-08 | Source Code Repository            | Unauthorized access          | Excessive permissions                  | Attacker obtains or modifies proprietary source code                 |          3 |      4 |    12 | High     |

---

## 4. Risk Analysis

### R-01 — Privileged Account Compromise

**Asset:** Privileged Administrator Accounts

**Threat:** Credential theft

**Vulnerability:** Insufficient authentication protection

An attacker who obtains privileged credentials could gain administrative access to critical systems.

Potential consequences include:

* Unauthorized configuration changes
* Creation of additional privileged accounts
* Disabling of security controls
* Access to sensitive information
* Deployment of malicious software
* Deletion or manipulation of security logs

**Likelihood:** 4 — Likely

Privileged credentials are valuable targets and can be exposed through phishing, credential theft, malware, or other attack techniques.

**Impact:** 5 — Severe

A compromised privileged account could affect multiple critical systems and potentially result in significant operational, financial, and security consequences.

**Risk Score:** 4 × 5 = **20 — Critical**

---

### R-02 — Unauthorized Customer Database Access

**Asset:** Customer Database

**Threat:** Unauthorized access

**Vulnerability:** Excessive permissions

Users with more access than required increase the potential impact of compromised accounts or insider misuse.

Potential consequences include:

* Exposure of customer information
* Privacy violations
* Regulatory consequences
* Reputational damage

**Likelihood:** 3 — Possible

**Impact:** 5 — Severe

**Risk Score:** 3 × 5 = **15 — Critical**

---

### R-03 — Exploitation of Vulnerable Azure Systems

**Asset:** Azure Production Environment

**Threat:** Exploitation

**Vulnerability:** Unpatched systems

An attacker could exploit a known vulnerability in an internet-facing or otherwise accessible production system.

Potential consequences include:

* Unauthorized system access
* Malware deployment
* Data exposure
* Service disruption
* Lateral movement

**Likelihood:** 3 — Possible

**Impact:** 5 — Severe

**Risk Score:** 3 × 5 = **15 — Critical**

---

### R-04 — Employee Account Compromise

**Asset:** Employee Accounts

**Threat:** Phishing / credential theft

**Vulnerability:** Insufficient MFA protection

An attacker could trick an employee into providing credentials through a phishing attack.

Potential consequences include:

* Unauthorized access to corporate systems
* Access to sensitive information
* Further credential theft
* Lateral movement
* Business email compromise

**Likelihood:** 4 — Likely

**Impact:** 4 — Major

**Risk Score:** 4 × 4 = **16 — Critical**

---

### R-05 — Security Log Manipulation

**Asset:** Security and Authentication Logs

**Threat:** Log deletion or manipulation

**Vulnerability:** Insufficient protection and monitoring

An attacker who gains access to systems may attempt to delete or modify logs to conceal malicious activity.

Potential consequences include:

* Reduced visibility
* Delayed incident detection
* Difficulty determining the attack timeline
* Loss of forensic evidence
* Reduced ability to identify affected systems

**Likelihood:** 3 — Possible

**Impact:** 4 — Major

**Risk Score:** 3 × 4 = **12 — High**

---

### R-06 — Destruction of Backup Data

**Asset:** Backup Repository

**Threat:** Ransomware

**Vulnerability:** Insufficient backup isolation

An attacker could compromise both production systems and accessible backups.

Potential consequences include:

* Loss of recovery capability
* Extended service outage
* Data loss
* Significant operational and financial impact

**Likelihood:** 3 — Possible

**Impact:** 5 — Severe

**Risk Score:** 3 × 5 = **15 — Critical**

---

### R-07 — Customer-Facing Application Outage

**Asset:** Customer-Facing Application

**Threat:** Denial of Service

**Vulnerability:** Insufficient resilience

A successful denial-of-service attack could make the financial platform unavailable to customers.

Potential consequences include:

* Service disruption
* Customer dissatisfaction
* Financial losses
* Reputational damage

**Likelihood:** 3 — Possible

**Impact:** 4 — Major

**Risk Score:** 3 × 4 = **12 — High**

---

### R-08 — Source Code Repository Compromise

**Asset:** Source Code Repository

**Threat:** Unauthorized access

**Vulnerability:** Excessive permissions

An attacker who compromises a developer account could access or modify proprietary source code.

Potential consequences include:

* Intellectual property loss
* Introduction of malicious code
* Supply-chain compromise
* Reputational damage

**Likelihood:** 3 — Possible

**Impact:** 4 — Major

**Risk Score:** 3 × 4 = **12 — High**

---

## 5. Risk Prioritization

The highest-priority risks are:

1. **R-01 — Privileged Account Compromise:** 20
2. **R-04 — Employee Account Compromise:** 16
3. **R-02 — Unauthorized Customer Database Access:** 15
4. **R-03 — Exploitation of Vulnerable Azure Systems:** 15
5. **R-06 — Destruction of Backup Data:** 15

These risks should receive priority because they combine relatively high likelihood with potentially severe consequences.

---

## 6. Risk Treatment Principle

Identified risks should not automatically be eliminated at any cost.

The organization should determine an appropriate treatment based on:

* Risk level
* Business impact
* Cost of mitigation
* Regulatory requirements
* Technical feasibility
* Business requirements
* Risk appetite

Common risk-treatment approaches include:

### Mitigate

Implement controls to reduce the likelihood or impact of the risk.

Example:

Implement MFA to reduce the likelihood of account compromise.

### Avoid

Stop the activity creating the risk.

Example:

Discontinue an insecure service that is not essential to the business.

### Transfer

Transfer some financial or operational consequences to another party.

Example:

Use appropriate cyber insurance or contractual arrangements.

### Accept

Consciously accept the remaining risk when it falls within the organization's risk appetite.

Risk acceptance should be documented and approved by an appropriate authority.

---

## 7. Risk Assessment Conclusion

The assessment identifies several risks requiring treatment, particularly those involving privileged access, identity security, customer information, cloud infrastructure, and backup protection.

The next stage of the project will define specific risk treatments and identify security controls that can reduce the likelihood or impact of these risks.

The risk register therefore provides the connection between:

**Business Assets**

→ **Security Risks**

→ **Risk Treatment**

→ **Security Controls**

→ **Compliance Evidence**
