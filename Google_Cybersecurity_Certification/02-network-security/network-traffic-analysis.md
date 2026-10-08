# Cybersecurity Incident Report: Network Traffic Analysis

## Overview

This activity involved analyzing network traffic using `tcpdump` to investigate why users were unable to access the website `www.yummyrecipesforme.com`.

The analysis focused on DNS, UDP, and ICMP traffic to identify the network protocol and service affected by the incident.

---

# Part 1: Summary of the Problem Found in the tcpdump Log

The tcpdump log showed that the browser was sending DNS requests to a DNS server using the **UDP protocol**.

The DNS request was sent to the DNS server at `203.0.113.2` using **port 53**, which is commonly used for DNS traffic.

The DNS server responded with **ICMP error messages** stating:

`udp port 53 unreachable`

This indicates that the UDP traffic intended for DNS port 53 could not reach a service listening on that port.

The traffic sequence showed:

* UDP packets were sent from the user's computer to the DNS server.
* The DNS requests were attempting to resolve `www.yummyrecipesforme.com`.
* The DNS server returned ICMP error messages.
* The error specifically identified UDP port 53 as unreachable.
* The DNS request included an `A?` query, which indicates a request for an IPv4 address record.

Based on the captured traffic, the primary issue appears to be related to the **DNS service or access to DNS port 53**.

Because the DNS lookup could not be completed, the browser could not obtain the IP address required to connect to the website.

---

# Part 2: Analysis and Possible Cause of the Incident

## Incident Time

The first timestamp in the tcpdump log was:

`13:24:32.192571`

This indicates that the incident was first observed at approximately **1:24 p.m.**

## Reported Symptoms

Customers reported that they were unable to access:

`www.yummyrecipesforme.com`

After waiting for the website to load, they received the error:

`destination port unreachable`

I also reproduced the issue when attempting to access the website.

## Investigation Performed

To investigate the issue, network traffic was captured using `tcpdump`.

The analysis showed that:

1. The browser sent a DNS query using UDP.
2. The DNS traffic was directed to the DNS server.
3. DNS uses port 53 for this type of communication.
4. The DNS server returned ICMP error messages.
5. The ICMP messages indicated that UDP port 53 was unreachable.
6. The repeated errors showed that the DNS request could not be successfully delivered to the DNS service.

Since DNS resolution was unsuccessful, the browser could not determine the IP address of the requested website.

## Current Status

The issue has been reported to the appropriate security team and is being investigated by security engineers.

The immediate problem is that customers cannot successfully access the website because the DNS resolution process is failing.

## Next Troubleshooting Steps

The next steps should be:

1. Check whether the DNS server is operational.
2. Verify whether a DNS service is listening on UDP port 53.
3. Check firewall rules to determine whether port 53 traffic is being blocked.
4. Review recent firewall and DNS configuration changes.
5. Check DNS server logs for errors or unusual activity.
6. Investigate whether the DNS server is experiencing excessive traffic or a potential denial-of-service attack.
7. Restore or correct the DNS service if a configuration or availability problem is confirmed.

## Suspected Root Cause

The exact root cause cannot be confirmed from the tcpdump information alone.

Possible causes include:

* The DNS service may be down.
* A firewall may be blocking traffic to UDP port 53.
* A DNS configuration may have been changed incorrectly.
* The DNS server may be affected by a denial-of-service attack.

The most important finding from the network analysis is that **DNS communication over UDP port 53 is failing**, preventing successful domain-name resolution.

---

# Protocols Identified

| Protocol | Role in the Incident                                          |
| -------- | ------------------------------------------------------------- |
| DNS      | Used to resolve `www.yummyrecipesforme.com` to an IP address  |
| UDP      | Transport protocol used to send the DNS request               |
| ICMP     | Returned an error indicating that UDP port 53 was unreachable |

---

# Key Security Concepts Demonstrated

* Network traffic analysis
* `tcpdump`
* DNS
* UDP
* ICMP
* IP addresses
* Network ports
* Port 53
* Packet analysis
* Incident investigation
* Troubleshooting network connectivity
* Firewall analysis
* Denial-of-Service awareness

## Learning Outcome

This activity helped me understand how cybersecurity analysts can use network traffic captures to investigate connectivity and security incidents.

I learned how to identify DNS, UDP, and ICMP traffic in a packet capture and interpret an ICMP error message to determine that communication with DNS port 53 was failing.

The activity also demonstrated how network-level evidence can be used to identify possible causes of an incident and determine the next steps for investigation.

## Disclaimer

This activity uses the fictional `yummyrecipesforme.com` scenario provided by the Google Cybersecurity Certificate for educational purposes.
