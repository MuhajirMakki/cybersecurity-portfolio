
# Internal Security Audit — Botium Toys

## Background

Botium Toys is a fictional small U.S. company that develops and sells toys. The company operates from a single physical location that functions as its main office, storefront, and warehouse. Its online presence has expanded to customers in the United States and internationally, increasing the importance of protecting its IT infrastructure and customer information.

As the company grows, the IT department needs to ensure that security controls are effective, business operations can continue during security incidents, and applicable compliance requirements are addressed.

This activity involved conducting an internal security audit of Botium Toys by reviewing the organization's assets, risk assessment, security controls, and compliance requirements.

## Audit Objective

The objective of the audit was to:

* Identify existing security controls.
* Identify missing or insufficient controls.
* Evaluate risks to critical assets and sensitive information.
* Review relevant compliance requirements.
* Recommend improvements to strengthen the organization's security posture.

## Audit Approach

The assessment followed this general process:

1. Reviewed the organization's assets and risk assessment.
2. Reviewed the relevant control categories.
3. Assessed the security controls currently in place.
4. Assessed compliance-related best practices.
5. Identified security and compliance gaps.
6. Developed recommendations to reduce identified risks.

---

# Controls Assessment

| Control                                  | Status | Finding                                                                                                                  |
| ---------------------------------------- | ------ | ------------------------------------------------------------------------------------------------------------------------ |
| Least Privilege                          | ❌ No   | All employees have access to customer data. Access should be restricted according to job responsibilities.               |
| Disaster Recovery Plans                  | ❌ No   | No disaster recovery plans are currently in place.                                                                       |
| Password Policies                        | ❌ No   | Employee password requirements are minimal and should be strengthened.                                                   |
| Separation of Duties                     | ❌ No   | Separation of duties should be implemented to reduce the risk of fraud and unauthorized access.                          |
| Firewall                                 | ✅ Yes  | An existing firewall blocks traffic based on defined security rules.                                                     |
| Intrusion Detection System (IDS)         | ❌ No   | An IDS should be implemented to help identify potential intrusions.                                                      |
| Backups                                  | ❌ No   | Critical data should be backed up to support business continuity following a security incident.                          |
| Antivirus Software                       | ✅ Yes  | Antivirus software is installed and regularly monitored by the IT department.                                            |
| Legacy System Monitoring and Maintenance | ❌ No   | Legacy systems are monitored and maintained, but there is no regular schedule or clearly defined intervention procedure. |
| Encryption                               | ❌ No   | Encryption is not currently implemented to protect sensitive information.                                                |
| Password Management System               | ❌ No   | No password management system is currently in place.                                                                     |
| Physical Locks                           | ✅ Yes  | The company's physical locations have sufficient locks.                                                                  |
| CCTV Surveillance                        | ✅ Yes  | CCTV is installed and functioning at the physical location.                                                              |
| Fire Detection/Prevention                | ✅ Yes  | The physical location has a functioning fire detection and prevention system.                                            |

---

# Compliance Assessment

## PCI DSS

| Best Practice                                                         | Status | Finding                                                                                    |
| --------------------------------------------------------------------- | ------ | ------------------------------------------------------------------------------------------ |
| Only authorized users have access to customer credit card information | ❌ No   | All employees currently have access to internal data, including customer information.      |
| Credit card information is securely processed and stored              | ❌ No   | Credit card information is not encrypted and access is not sufficiently restricted.        |
| Data encryption procedures are implemented                            | ❌ No   | Encryption should be implemented to protect customers' financial information.              |
| Secure password management policies are adopted                       | ❌ No   | Password requirements are minimal and no password management system is currently in place. |

## GDPR

| Best Practice                                   | Status | Finding                                                                                 |
| ----------------------------------------------- | ------ | --------------------------------------------------------------------------------------- |
| E.U. customers' data is kept private and secure | ❌ No   | Sensitive financial information is not encrypted.                                       |
| A breach notification plan exists               | ✅ Yes  | A plan exists to notify E.U. customers within 72 hours of a data breach.                |
| Data is properly classified and inventoried     | ❌ No   | Assets have been inventoried but have not been properly classified.                     |
| Privacy policies and procedures are enforced    | ✅ Yes  | Privacy policies, procedures, and processes have been developed and enforced as needed. |

## SOC 1 / SOC 2

| Best Practice                               | Status | Finding                                                                           |
| ------------------------------------------- | ------ | --------------------------------------------------------------------------------- |
| User access policies are established        | ❌ No   | Least privilege and separation of duties are not currently implemented.           |
| Sensitive data is confidential/private      | ❌ No   | Encryption is not currently used to protect PII/SPII.                             |
| Data integrity is maintained                | ✅ Yes  | Data integrity is currently in place.                                             |
| Data is available to authorized individuals | ❌ No   | Data is available to all employees rather than only employees who require access. |

---

# Key Findings

The assessment identified several important weaknesses in Botium Toys' security posture.

### 1. Excessive User Access

Employees currently have broad access to internal and customer information.

**Risk:** Unauthorized access or accidental exposure of sensitive information.

**Recommendation:** Implement the principle of least privilege and role-based access controls.

### 2. Weak Password Security

Password requirements are minimal and there is no password management system.

**Risk:** Weak credentials could make unauthorized access easier.

**Recommendation:** Implement stronger password policies and a secure password management system.

### 3. Lack of Encryption

Sensitive information, including financial information, is not currently encrypted.

**Risk:** Exposed data could be read or misused if unauthorized access occurs.

**Recommendation:** Implement encryption for sensitive data at rest and in transit where appropriate.

### 4. Lack of Disaster Recovery and Backups

Critical data does not have sufficient backup and disaster recovery protections.

**Risk:** A security incident or system failure could significantly disrupt business operations.

**Recommendation:** Implement regular backups and develop a documented disaster recovery plan.

### 5. Lack of Intrusion Detection

The organization does not currently have an IDS.

**Risk:** Suspicious network activity or attempted intrusions may not be detected quickly.

**Recommendation:** Implement appropriate intrusion detection and monitoring capabilities.

### 6. Lack of Separation of Duties

Critical responsibilities are not sufficiently separated.

**Risk:** A single individual having excessive control over sensitive processes can increase the risk of fraud or unauthorized activity.

**Recommendation:** Separate critical responsibilities between appropriate personnel.

### 7. Legacy System Management

Legacy systems are being monitored but do not have a clearly defined maintenance and intervention schedule.

**Risk:** Unsupported or poorly maintained systems may introduce additional vulnerabilities.

**Recommendation:** Establish documented maintenance schedules and procedures for legacy systems.

### 8. Asset Classification

Assets have been inventoried but have not been properly classified.

**Risk:** Without classification, the organization may not apply appropriate protection to its most sensitive assets.

**Recommendation:** Classify assets and information according to sensitivity, business importance, and security requirements.

---

# Recommendations

The IT manager should prioritize the following improvements:

1. Implement least-privilege access.
2. Strengthen password policies.
3. Deploy a password management system.
4. Implement encryption for sensitive information.
5. Establish regular backups.
6. Develop a disaster recovery plan.
7. Implement an intrusion detection system.
8. Establish separation of duties.
9. Create formal procedures for legacy system monitoring and maintenance.
10. Classify organizational assets according to their sensitivity and importance.

These controls can help reduce security risks, improve protection of sensitive information, support business continuity, and strengthen the organization's overall security posture.

---

# Skills Demonstrated

* Internal security auditing
* Security controls assessment
* Risk identification
* Access control
* Least privilege
* Security compliance
* PCI DSS awareness
* GDPR awareness
* SOC 1/SOC 2 concepts
* Security recommendations
* Security posture assessment
* Risk mitigation

# Learning Outcome

This activity helped me understand how a cybersecurity professional can evaluate an organization's security controls, identify gaps, consider compliance requirements, and recommend improvements based on identified risks.

It also helped me understand that cybersecurity is not only about technical tools. Effective security requires appropriate controls, policies, access management, risk assessment, compliance awareness, and business continuity planning.

## Disclaimer

Botium Toys is a fictional organization used in the Google Cybersecurity Certificate for educational purposes. This audit was completed as part of the course learning activity and does not represent an assessment of a real organization.
