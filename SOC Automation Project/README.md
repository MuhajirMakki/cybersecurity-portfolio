# SOC Automation Project

## Intro

This project is a practical Security Operations Center (SOC) automation lab focused on building a small security monitoring and incident response environment.

The project combines **Wazuh**, **Shuffle**, **TheHive**, and a **Windows 10 client** to demonstrate how security events can be collected, analyzed, enriched, and handled through automated response workflows.

## Objective

The main objectives of this project are to:

* Build a small SOC lab environment.
* Monitor security events from a Windows 10 client.
* Use Wazuh for security monitoring, alerting, and response.
* Use Shuffle for security automation and IOC enrichment.
* Use TheHive for incident and case management.
* Understand how security events move through a SOC workflow.
* Practice basic alert investigation and automated response.

## Tools

* **Windows 10** — Endpoint used to generate and send security events.
* **Wazuh** — Security monitoring, SIEM, XDR, and alerting platform.
* **Shuffle** — Security Orchestration, Automation and Response (SOAR) platform.
* **TheHive** — Security incident response and case management platform.
* **VirtualBox** — Used for the local virtual machine environment.
* **draw.io** — Used to design and document the SOC architecture.

## Lab Workflow

The planned workflow is:

**Windows 10 → Wazuh → Shuffle → TheHive / SOC Analyst**

The general process is:

1. Windows 10 generates security events.
2. Wazuh receives and analyzes the events.
3. Wazuh generates alerts when suspicious activity is detected.
4. Shuffle receives alerts and performs automation tasks.
5. Shuffle can enrich Indicators of Compromise (IOCs).
6. Alerts can be sent to TheHive for case management.
7. The SOC analyst receives notifications and can provide a response.
8. The response can be passed back through Shuffle and Wazuh to the Windows endpoint.

## Demo

The SOC architecture is designed using **draw.io** to visualize the components and understand how data and response actions flow through the environment.

The architecture includes:

* Windows 10 endpoint with Wazuh Agent
* Wazuh Manager
* Shuffle
* TheHive
* SOC Analyst
* Internet/network connectivity

The diagram serves as the reference architecture for the SOC automation lab.

## Learning Focus

This project focuses on practical understanding of:

* SOC operations
* SIEM and security monitoring
* Security alerts and event analysis
* SOAR automation
* IOC enrichment
* Incident and case management
* Endpoint monitoring
* Automated response
* Security operations workflows
