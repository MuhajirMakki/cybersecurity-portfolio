# Data Leak Worksheet

## Incident Summary

A sales manager shared access to a folder of internal-only documents with their team during a meeting. The folder contained files related to a new product that had not been publicly announced, along with customer analytics and promotional materials. After the meeting, the manager did not revoke access to the folder.

During a video call with a business partner, a sales representative intended to share only the promotional materials. However, they accidentally shared the link to the entire internal folder. The business partner later posted the link on their company's social media page, exposing the internal documents.

## Control

**Least privilege**

## Issue(s)

Access to the internal folder was not properly limited to the people who needed it. The sales representative also had access to information that was not necessary for sharing with the business partner, which increased the risk of accidental disclosure.

## Review

NIST SP 800-53: AC-6 addresses how organizations can protect information by implementing the principle of least privilege. It recommends giving users only the access and authorization required for their tasks and provides control enhancements to improve access management.

## Recommendation(s)

* Restrict access to sensitive resources based on user role.
* Regularly audit user privileges.

## Justification

Restricting access to sensitive files based on user roles would reduce the chance of confidential information being shared with external users. Regularly reviewing user privileges would also help identify and remove unnecessary access before it results in a data leak.

---

# Security Plan Snapshot

The NIST Cybersecurity Framework (CSF) organizes security information into functions, categories, subcategories, and references.

| Function | Category             | Subcategory                             | Reference            |
| -------- | -------------------- | --------------------------------------- | -------------------- |
| Protect  | PR.DS: Data security | PR.DS-5: Protections against data leaks | NIST SP 800-53: AC-6 |

NIST SP 800-53 provides security controls and control enhancements that organizations can use to protect information systems and data.

---

# NIST SP 800-53: AC-6

## AC-6 Least Privilege

**Control:**

Only the minimal access and authorization required to complete a task or function should be provided to users.

**Discussion:**

Processes, user accounts, and roles should be managed to achieve least privilege. The purpose is to prevent users from having more access than they need to complete their work.

**Control Enhancements:**

* Restrict access to sensitive resources based on user role.
* Automatically revoke access to information after a period of time.
* Keep activity logs of provisioned user accounts.
* Regularly audit user privileges.

**Note:** AC-6 is the sixth control in the access control family of NIST SP 800-53.
