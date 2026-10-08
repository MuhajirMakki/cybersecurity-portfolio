# Security Incident Report: OS Hardening and Brute-Force Attack

## Background / Scenario

`yummyrecipesforme.com` is a fictional website that provides free recipes to users.

A cybersecurity incident occurred after an attacker gained unauthorized access to the website's administrative account. The attacker used a **brute-force attack** against the web server's administrator account and successfully gained access because the account was protected by a known default password.

After gaining administrative access, the attacker changed the administrator password and modified the website's source code. The attacker inserted malicious JavaScript that prompted visitors to download and run an executable file.

Customers who downloaded and executed the file reported that their computers became slower and that their browsers were redirected to another website, `greatrecipesforme.com`.

The website owner also discovered that they could no longer log in to the administrative account.

A cybersecurity analyst investigated the incident in a sandbox environment and captured network traffic using `tcpdump`. The investigation showed DNS requests, HTTP traffic, and a redirection from `yummyrecipesforme.com` to `greatrecipesforme.com`.

The investigation determined that the root cause was a successful brute-force attack against an administrative account protected by a default password and insufficient authentication security controls.

---

# Section 1: Identify the Network Protocol Involved in the Incident

The primary network protocol involved in the incident was **Hypertext Transfer Protocol (HTTP)**.

The `tcpdump` traffic log shows HTTP communication between the user's computer and `yummyrecipesforme.com`. After the DNS server resolved the website's domain name to an IP address, the browser established a connection to the web server using HTTP.

The log contains:

`HTTP: GET / HTTP/1.1`

This indicates that the browser used HTTP to request content from the web server. The malicious executable was delivered to users through the compromised website over HTTP.

The logs also show that after the malicious file was executed, the browser performed another DNS lookup for `greatrecipesforme.com` and then established HTTP communication with that website.

DNS was therefore also involved in resolving the domain names, while TCP was used to establish the HTTP connections. However, **HTTP is the primary protocol associated with the web-based activity involved in the incident.**

---

# Section 2: Document the Incident

## Incident Description

Several customers contacted the `yummyrecipesforme.com` helpdesk after the website prompted them to download and run a file to access free recipes.

After running the file, customers reported that:

* Their computers became slower.
* Their browsers were redirected to another website.
* They were prompted to download an executable file.

The website owner also discovered that they could no longer log in to the administrative panel.

## Investigation

To investigate the incident safely, the cybersecurity analyst used a sandbox environment and captured network traffic using `tcpdump`.

When the analyst accessed `yummyrecipesforme.com`, the website prompted them to download an executable file presented as a browser update.

After the file was downloaded and executed, the browser was redirected to `greatrecipesforme.com`, which was identified as the malicious website.

## Network Traffic Analysis

The `tcpdump` log showed that the browser first performed a DNS request for `yummyrecipesforme.com`.

The DNS server returned the IP address:

`203.0.113.22`

The browser then established an HTTP connection with the website and sent an HTTP GET request:

`GET / HTTP/1.1`

After the suspicious file was executed, the browser performed another DNS request for:

`greatrecipesforme.com`

The DNS server returned another IP address, and the browser subsequently established an HTTP connection with the new website.

This network traffic provided evidence of the redirection from the compromised website to the malicious website.

## Website Investigation

The senior cybersecurity analyst inspected the website's source code and discovered that malicious JavaScript had been added.

The JavaScript was designed to prompt visitors to download the executable file.

Analysis of the downloaded file showed that it contained code that redirected users from:

`yummyrecipesforme.com`

to:

`greatrecipesforme.com`

## Root Cause

The investigation determined that the web server had been compromised through a **brute-force attack**.

The attacker repeatedly attempted known default passwords until successfully accessing the administrative account.

After gaining access, the attacker:

1. Changed the administrator password.
2. Modified the website's source code.
3. Added malicious JavaScript.
4. Prompted website visitors to download a malicious executable.
5. Redirected users to `greatrecipesforme.com`.

The use of a default administrative password and the absence of sufficient controls to prevent repeated login attempts made the web server vulnerable to the attack.

---

# Section 3: Recommend One Remediation for Brute-Force Attacks

One important security measure is to **implement two-factor authentication (2FA)** for administrative accounts.

With 2FA, logging in requires both a password and a second authentication factor, such as a one-time passcode or authentication-app approval.

Even if an attacker successfully guesses or obtains the password, they would still need the second authentication factor to access the administrative account.

The organization should also ensure that default passwords are immediately replaced with strong, unique passwords.

Implementing 2FA provides an additional layer of protection against unauthorized access and can significantly reduce the risk of a successful brute-force attack.

---

# Key Findings

* The primary application-layer protocol involved was **HTTP**.
* DNS was used to resolve the website domains.
* TCP was used to establish the HTTP connections.
* The website's source code had been modified with malicious JavaScript.
* Users were prompted to download a malicious executable.
* The executable redirected users to `greatrecipesforme.com`.
* The web server's administrative account was compromised through a brute-force attack.
* The administrative account was protected by a default password.
* Insufficient authentication controls allowed repeated login attempts.
* Two-factor authentication is recommended as a security control.

---

# Security Concepts Demonstrated

* Network traffic analysis
* `tcpdump`
* DNS
* HTTP
* TCP
* TCP/IP model
* Brute-force attacks
* Authentication security
* Two-factor authentication
* Web server security
* Malware analysis
* Incident investigation
* Incident documentation
* Security remediation
* OS hardening concepts

---

# Learning Outcome

This activity helped me understand how network traffic can be analyzed to identify the protocols involved in a security incident and how packet-level evidence can support an incident investigation.

It also demonstrated how weak authentication controls, such as default passwords and insufficient protection against repeated login attempts, can allow attackers to compromise administrative accounts.

The activity reinforced the importance of strong authentication controls and security hardening to reduce the risk of unauthorized access.

---

# Disclaimer

This activity uses the fictional `yummyrecipesforme.com` scenario provided by the Google Cybersecurity Certificate for educational purposes.

The analysis and recommendations documented in this report represent my learning from the activity and do not describe an assessment of a real organization.
