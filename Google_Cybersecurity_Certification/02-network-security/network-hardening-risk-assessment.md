# Security Risk Assessment: Network Hardening

## Background / Scenario

The organization in this scenario is a fictional social media company that recently experienced a major data breach. The breach compromised customers' personal information, including names and addresses.

As part of the security investigation, a security analyst reviewed the organization's network and identified several weaknesses that could allow attackers to gain unauthorized access or move through the network.

The assessment identified four major vulnerabilities:

1. Employees share passwords with each other.
2. The database administrator account still uses the default password.
3. Firewalls do not have appropriate rules to filter incoming and outgoing network traffic.
4. Multifactor authentication (MFA) is not implemented.

These weaknesses increase the organization's risk of unauthorized access, brute-force attacks, malicious network traffic, and future data breaches.

The organization therefore needs to implement network hardening practices that can consistently reduce these risks and improve the overall security posture of the network.

---

# Risk Assessment

## Identified Vulnerabilities

| Vulnerability                           | Security Risk                                                   | Potential Impact                                           |
| --------------------------------------- | --------------------------------------------------------------- | ---------------------------------------------------------- |
| Employees share passwords               | Unauthorized users may gain access to accounts                  | Account compromise and loss of accountability              |
| Default database administrator password | Attackers may easily guess or obtain administrative access      | Database compromise and data breach                        |
| No effective firewall traffic rules     | Malicious or unnecessary traffic may enter or leave the network | Unauthorized access, malware, DoS/DDoS, and data exposure  |
| No MFA                                  | Compromised passwords may be enough to access systems           | Increased risk of account takeover and brute-force attacks |

The vulnerabilities are related to both **authentication security** and **network security**. The organization should prioritize controls that reduce unauthorized access and restrict potentially malicious network traffic.

---

# Part 1: Select Hardening Tools and Methods

The following three network hardening methods are recommended for the organization:

1. **Multifactor Authentication (MFA)**
2. **Strong Password Policies**
3. **Firewall Maintenance and Traffic Filtering**

---

## 1. Multifactor Authentication (MFA)

MFA requires users to verify their identity using two or more authentication factors before accessing a system or application.

Examples include:

* Password
* One-time password (OTP)
* Authentication application
* Security key
* Fingerprint
* Other approved authentication factors

MFA should be implemented for administrative accounts and other systems containing sensitive information.

### Vulnerabilities Addressed

MFA directly helps address:

* Lack of MFA
* Shared passwords
* Default or compromised passwords
* Brute-force and credential-based attacks

---

## 2. Strong Password Policies

The organization should establish and enforce password policies that require employees and administrators to use strong, unique passwords.

The policy should also prohibit password sharing and the use of default passwords.

Important password security practices include:

* Use strong and unique passwords.
* Never use default administrative passwords.
* Do not share passwords between employees.
* Prevent the reuse of compromised or previously used passwords.
* Implement protections against repeated unsuccessful login attempts.
* Store passwords securely using appropriate password hashing mechanisms.

Administrative accounts, especially database administrator accounts, should receive particular attention because compromise of these accounts could provide attackers with extensive access to sensitive information.

### Vulnerabilities Addressed

Password policies directly help address:

* Employee password sharing
* Default database administrator password
* Brute-force attacks
* Weak authentication

---

## 3. Firewall Maintenance and Traffic Filtering

The organization's firewalls should be configured with appropriate rules to control incoming and outgoing network traffic.

Firewall rules should follow the principle of allowing only traffic that is required for legitimate business operations and blocking unnecessary or suspicious traffic.

Security administrators should regularly:

* Review firewall rules.
* Remove unnecessary rules.
* Block unauthorized ports and services.
* Restrict suspicious traffic.
* Review inbound and outbound traffic.
* Update rules when new threats or security incidents are identified.

Firewall configuration should be based on the organization's security requirements and should be reviewed regularly.

### Vulnerabilities Addressed

Firewall maintenance directly helps address:

* Missing inbound traffic filtering
* Missing outbound traffic filtering
* Unauthorized network access
* Suspicious network traffic
* Some DoS/DDoS-related threats

---

# Part 2: Explain the Recommendations

## Recommendation 1: Implement Multifactor Authentication

MFA adds an additional layer of security beyond a username and password.

If an attacker obtains or guesses a user's password, the attacker would still need the second authentication factor to gain access.

This is particularly important for administrator and database accounts because these accounts can provide access to sensitive systems and customer information.

MFA can also reduce the usefulness of shared passwords because possession of the password alone would not be sufficient to access the protected system.

### Implementation Frequency

MFA is primarily **implemented once and then continuously maintained**.

The organization should:

* Enable MFA for appropriate accounts.
* Review MFA enrollment regularly.
* Remove MFA access for users who leave the organization.
* Review authentication methods when security requirements change.

---

## Recommendation 2: Implement and Enforce Strong Password Policies

Strong password policies can reduce the risk of attackers successfully guessing or using compromised credentials.

The organization should immediately replace the default database administrator password with a strong, unique password.

Employees should also be prohibited from sharing passwords.

The organization can additionally implement controls such as account lockout or rate limiting after repeated unsuccessful login attempts. These controls can make automated brute-force attacks more difficult.

### Implementation Frequency

Password policies should be **implemented as an organizational standard and reviewed regularly**.

The organization should also review administrator and user accounts whenever there is:

* A suspected account compromise
* A security incident
* An employee leaving the organization
* A change in security requirements

---

## Recommendation 3: Perform Regular Firewall Maintenance

Firewall maintenance is important because firewall rules determine what network traffic is allowed or blocked.

The organization should regularly review firewall configurations and ensure that only required traffic is permitted.

Suspicious or unauthorized traffic should be blocked according to the organization's security policies.

Firewall rules should also be reviewed after security incidents or significant changes to the network.

### Implementation Frequency

Firewall maintenance should be performed **regularly**, with additional reviews whenever:

* A security incident occurs.
* New services are added.
* Network architecture changes.
* Suspicious traffic is detected.
* New security requirements are introduced.

Regular firewall maintenance helps prevent outdated or overly permissive rules from creating unnecessary security risks.

---

# Security Hardening Priority

Based on the identified vulnerabilities, the organization should prioritize the controls in the following order:

### 1. Protect Administrative Accounts

The default database administrator password should be replaced immediately, and MFA should be enabled for administrative accounts.

### 2. Stop Password Sharing

A formal password policy should prohibit password sharing and require secure authentication practices.

### 3. Strengthen Network Traffic Controls

Firewall rules should be created and regularly maintained to control unauthorized inbound and outbound traffic.

These measures address both the authentication weaknesses and the network security weaknesses identified during the assessment.

---

# Key Findings

The security assessment identified several weaknesses that could contribute to another data breach:

* Employees are sharing passwords.
* The database administrator account uses a default password.
* MFA is not implemented.
* Firewall rules are insufficient for controlling network traffic.
* Sensitive customer information could be exposed if attackers compromise administrative accounts.
* Weak authentication controls increase the risk of brute-force and credential-based attacks.
* Poor firewall configuration can allow unauthorized or suspicious network traffic.

The three recommended hardening methods are:

1. **Multifactor authentication (MFA)**
2. **Strong password policies**
3. **Regular firewall maintenance and traffic filtering**

Together, these controls provide protection at both the **authentication layer** and the **network layer**.

---

# Security Concepts Demonstrated

* Network hardening
* Security risk assessment
* Multifactor authentication
* Password security
* Password policies
* Brute-force attacks
* Firewall configuration
* Traffic filtering
* Network access control
* Administrative account security
* Network security
* Data breach prevention
* Risk mitigation
* Security controls
* Security posture assessment

---

# Learning Outcome

This activity helped me understand how a security analyst can assess network vulnerabilities and select appropriate hardening techniques based on identified risks.

I learned that network hardening is not limited to a single security tool. Organizations need multiple layers of protection, including strong authentication, secure password practices, access controls, and properly configured firewalls.

The activity also demonstrated the importance of matching a security control to a specific vulnerability. For example, MFA helps protect compromised credentials, password policies reduce authentication-related risks, and firewall maintenance helps control unauthorized network traffic.

---

# Disclaimer

This activity uses a fictional social media organization scenario provided by the Google Cybersecurity Certificate for educational purposes.

The assessment and recommendations documented in this report represent my learning from the course activity and do not describe an assessment of a real organization.
