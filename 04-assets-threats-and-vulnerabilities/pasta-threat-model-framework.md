# PASTA Threat Modeling – Sneaker Shopping Application

## Introduction

In this activity, I practiced using the **PASTA (Process of Attack Simulation and Threat Analysis)** framework to identify security risks in a new mobile shopping application.

The application is being developed for a company that sells and allows customers to buy and sell sneakers. Since the app handles user accounts, messages, seller information, and financial transactions, security needs to be considered before the application is launched.

I worked through the seven stages of the PASTA framework to identify business objectives, technologies, threats, vulnerabilities, and security controls.

## Activity Scenario

I am part of the security team at a growing company for sneaker enthusiasts and collectors. The company is preparing to launch a mobile application that will allow customers to buy and sell shoes.

The application will allow users to:

* Create and manage accounts
* Buy and sell sneakers
* Communicate directly with sellers
* Rate sellers
* Make payments using different payment options

The company considers data privacy and secure payment processing important because the application will handle personal and financial information.

My task was to perform a threat model using the PASTA framework and identify security requirements before the application is launched.

---

## Part 1: Complete the PASTA Stages

### Stage I – Define Business and Security Objectives

First, I reviewed the business description to identify the main objectives and security requirements of the application.

I identified the following:

* Users should be able to create and manage member profiles.
* The application must process financial transactions securely.
* The application should follow **PCI-DSS** requirements for payment processing.

These requirements are important because the application will handle personal information and payment data.

---

### Stage II – Define the Technical Scope

The application uses the following technologies:

* Application Programming Interface (API)
* Public Key Infrastructure (PKI)
* SHA-256
* SQL

I would prioritize the **API** first because it connects different parts of the application and can exchange sensitive information between users and systems. APIs can have a larger attack surface, especially when they handle authentication, account information, and transaction data, so they should be reviewed carefully for security weaknesses.

---

### Stage III – Decompose the Application

For this stage, I reviewed the provided **PASTA data flow diagram** to understand how information moves through the application.

The diagram helped me understand that a user request can pass through different application components before reaching the database.

One security point I would review is how the application sends queries to the database. For example, SQL queries should use **prepared statements** so that user input cannot be used to manipulate database queries.

This stage helped connect the technologies from Stage II with the actual flow of information through the application.

---

### Stage IV – Threat Analysis

I identified two potential threats to the information handled by the application:

#### 1. SQL Injection

An attacker could attempt to insert malicious SQL commands through application input. If user input is not properly handled, this could allow unauthorized access to information stored in the database.

#### 2. Session Hijacking

An attacker could attempt to steal or misuse a user's session information. If session cookies or tokens are not properly protected, the attacker could potentially access the user's account.

---

### Stage V – Vulnerability Analysis

I identified two vulnerabilities that could be exploited:

#### 1. Lack of Prepared Statements

If the application directly places user input into SQL queries, attackers may be able to manipulate the queries and perform SQL injection attacks.

#### 2. Broken API Token

Poorly protected or improperly managed API tokens could allow an attacker to access application functions or data without proper authorization.

These vulnerabilities could make the threats identified in Stage IV more likely to succeed.

---

### Stage VI – Attack Modeling

For this stage, I reviewed the provided **PASTA attack tree**.

The attack tree connects possible threats and vulnerabilities to show how an attacker could potentially reach sensitive information.

For example, an attacker could exploit a vulnerability in the application or API and eventually gain unauthorized access to user or transaction information.

The attack tree helped me understand how different parts of the threat model are connected.

---

### Stage VII – Risk Analysis and Impact

Based on the previous stages, I identified four security controls that could reduce the risk:

1. **SHA-256** – can be used for securely storing appropriate sensitive values such as passwords.
2. **Incident response procedures** – provide a planned process for detecting, containing, and responding to security incidents.
3. **Password policy** – helps require stronger passwords and reduce account compromise.
4. **Principle of least privilege** – limits users and systems to only the access they need.

These controls can help reduce the likelihood and impact of security incidents before the application is launched.

---

## PASTA Stage Summary

| Stage                                      | My Analysis                                                             |
| ------------------------------------------ | ----------------------------------------------------------------------- |
| Stage I – Business and Security Objectives | User profiles, secure financial transactions, PCI-DSS compliance        |
| Stage II – Technical Scope                 | Prioritized APIs because they connect systems and handle sensitive data |
| Stage III – Decompose Application          | Reviewed the data flow and considered secure database queries           |
| Stage IV – Threat Analysis                 | SQL injection and session hijacking                                     |
| Stage V – Vulnerability Analysis           | Lack of prepared statements and broken API tokens                       |
| Stage VI – Attack Modeling                 | Reviewed how threats and vulnerabilities could lead to attacks          |
| Stage VII – Risk Analysis                  | SHA-256, incident response, password policy, least privilege            |

## What I Learned

This activity helped me understand how threat modeling can be performed before an application is launched. Instead of looking only for individual vulnerabilities, PASTA connects the business requirements, technologies, data flow, threats, vulnerabilities, and security controls.

I also learned that APIs and databases need careful security review because they can handle large amounts of sensitive information.

## Cybersecurity Connection

Threat modeling is useful because security teams can identify possible risks before attackers exploit them. In a real application, the process would involve security professionals, developers, system administrators, and other stakeholders.

For a shopping application, protecting account information, payment information, and user sessions is especially important.




## Conclusion

In this activity, I applied the seven stages of the PASTA threat modeling framework to a sneaker shopping application. I identified the main business objectives, prioritized the API as an important technology, identified SQL injection and session hijacking as threats, and identified lack of prepared statements and broken API tokens as vulnerabilities.

I also identified four security controls that could reduce the risk before the application is launched.

## Course Information

**Course:** Google Cybersecurity Certificate
**Course:** Assets, Threats, and Vulnerabilities
**Activity:** Apply the PASTA Threat Model Framework

## Disclaimer

This is a learning activity completed as part of the Google Cybersecurity Certificate. The analysis is based on the provided course scenario and materials.
