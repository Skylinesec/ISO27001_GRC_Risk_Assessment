# 01 — Scope and Context

## 1. Organization

**Organization:** FinSecure Cloud GmbH

**Industry:** Financial Services

**Location:** Germany

**Technology Environment:** Microsoft Azure cloud environment


FinSecure Cloud GmbH is a **fictional** financial-services organization that provides a cloud-based financial management platform to business customers.

The platform processes business and personal information and relies heavily on cloud infrastructure and identity services.

---

## 2. ISMS Scope

The scope of the Information Security Management System (ISMS) for this assessment includes the people, processes, information, applications, and technology used to provide and support FinSecure's cloud-based financial platform.

The assessment specifically focuses on:

* Microsoft Azure infrastructure
* Cloud-hosted applications
* Customer and financial data
* Employee identities and access
* Authentication and authorization
* Security monitoring and logging
* Vulnerability and patch management
* Incident management
* Backup and recovery
* Information-security policies and procedures

The scope covers the security processes and controls required to protect the confidentiality, integrity, and availability of information within the defined environment.

---

## 3. Scope Boundaries

### Included

The following are included within the assessment:

| Area                 | Examples                                         |
| -------------------- | ------------------------------------------------ |
| Cloud infrastructure | Azure virtual machines, storage, networking      |
| Applications         | Customer-facing financial platform               |
| Data                 | Customer, financial, and personal information    |
| Identity             | Employee accounts, privileged accounts, MFA      |
| Monitoring           | Security logs, authentication logs, system logs  |
| Security processes   | Incident response, vulnerability management      |
| Personnel            | Employees and relevant contractors               |
| Policies             | Information security and access-control policies |

### ⛔️Excluded

The following are outside the scope of this simplified assessment:

* Physical security of Microsoft Azure data centers
* Detailed supplier audits
* Full financial-sector regulatory compliance
* Formal legal assessment of GDPR compliance
* Formal ISO 27001 certification or audit
* Detailed penetration testing

*These exclusions are made to keep the portfolio assessment focused on information-security risk management within the organization's cloud environment.*

---

## 4. Interested Parties

An interested party is a person or organization that can affect, be affected by, or have an interest in the organization's information security.

Relevant interested parties include:

| Interested Party  | Security Interest                                         |
| ----------------- | --------------------------------------------------------- |
| Customers         | Protection of their information and service availability  |
| Employees         | Secure access to systems and information                  |
| Management        | Effective management of security risks                    |
| Regulators        | Compliance with applicable requirements                   |
| Cloud providers   | Secure operation of cloud infrastructure                  |
| Business partners | Protection of shared information                          |
| Security team     | Detection, prevention, and response to security incidents |

---

## 5. Information Security Objectives

The organization should establish security objectives that support the protection of information and business operations.

For this assessment, the primary objectives are:

### Confidentiality **(C)**

Ensure that customer, financial, and personal information is only accessible to authorized individuals and systems.

### Integrity **(I)**

Ensure that information and systems are protected against unauthorized or accidental modification.

### Availability **(A)**

Ensure that critical applications and information remain available to authorized users when required.

### Risk Management

Identify, assess, and treat information-security risks in a consistent and documented manner.

### Security Monitoring

Maintain sufficient logging and monitoring to detect suspicious activity and support security investigations.

### Continual Improvement

Regularly review security controls, risks, incidents, and processes and improve them where necessary.

---

## 6. Security Context

FinSecure operates in a cloud-based environment where security risks can originate from both internal and external sources.

Relevant risks include:

* Compromised user credentials
* Unauthorized access
* Malware and ransomware
* Exploitation of vulnerable systems
* Misconfigured cloud resources
* Data leakage
* Insufficient logging or monitoring
* Loss of service availability
* Inadequate backup or recovery capabilities
* Third-party and supply-chain risks

The organization therefore requires a combination of preventive, detective, and corrective security controls.

---

## 7. Assumptions

This assessment makes the following assumptions:

1. FinSecure uses Microsoft Azure as its primary cloud platform.
2. Customer and employee information is stored or processed within the cloud environment.
3. Employees access corporate systems using individual user accounts.
4. Privileged accounts exist and require additional protection.
5. Security logging is enabled for important systems and services.
6. The organization has documented information-security policies.
7. The organization performs periodic risk assessments.
8. Microsoft remains responsible for security aspects of the underlying Azure infrastructure under the shared-responsibility model.

---

## 8. ISMS Perspective

The ISMS should be treated as a continuous management process rather than a one-time security project.

The basic cycle used in this assessment is:

**Identify → Assess → Treat → Monitor → Review → Improve**

This allows the organization to respond to changes in technology, threats, business requirements, and regulatory expectations.

---

## 9. Assessment Limitations

This project is an educational simulation and does not represent a complete implementation of an ISO/IEC 27001-compliant ISMS.

The assessment does not include:

* A complete organizational risk assessment
* A complete ISO/IEC 27001 Annex A control assessment
* Formal certification activities
* Legal advice
* Independent audit testing
* Detailed technical validation of Azure configurations

The purpose is to demonstrate practical understanding of the principles involved in information-security governance, risk management, and compliance.

