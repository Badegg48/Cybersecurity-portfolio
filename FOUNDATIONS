# Security Foundations

This document provides a consolidated overview of my understanding of core cybersecurity concepts developed through formal study, practical training and independent learning.

It focuses on the principles, technologies, processes and security practices that underpin my practical work and ongoing development.

## Domains at a Glance

| Domain | Areas Covered |
|---|---|
| Threats & Vulnerabilities | Threat actors, vulnerabilities, attack methods, risk |
| Access Control & Identity | Authentication, authorisation, Active Directory, NTLM, Kerberos |
| Defensive Security | Security controls, hardening, monitoring, malware defence |
| Offensive Security | Vulnerability assessment, penetration testing, reconnaissance, red teaming |
| Networking & Secure Protocols | OSI/TCP-IP, protocols, ports, network security |
| Security Monitoring | SIEM, logging, Windows Event IDs, baselines, anomaly detection |
| Vulnerability Management | Identification, assessment, prioritisation, remediation |
| Web Application Security | HTTP, application security, SQL injection, frontend/backend |
| Threat Intelligence & OSINT | Intelligence lifecycle, reconnaissance, information analysis |
| Cybersecurity Frameworks | NIST, NCSC, CIS, ISO |
| Legal, Ethical & Regulatory | UK legislation, GDPR, ethical conduct, authorisation |
| Incident Response | Incident lifecycle, investigation, containment and recovery |
| Cryptography | Encoding, hashing, encryption and data protection |

---

# Threats & Vulnerabilities

Cybersecurity threats are potential events or actions that could cause harm to systems, networks, data or organisations.

Threat actors can include individuals, organised criminal groups, insiders, hacktivists and other groups with different capabilities and motivations.

A vulnerability is a weakness that could be exploited by a threat actor. Vulnerabilities can exist in software, configurations, networks, human behaviour or physical environments.

Common vulnerability categories include:

- Software vulnerabilities
- Configuration vulnerabilities
- Network vulnerabilities
- Human vulnerabilities
- Physical vulnerabilities

Examples of vulnerabilities include insecure software, outdated systems, weak passwords, excessive permissions, exposed services, poor network segmentation and insecure configurations.

Vulnerability management involves identifying vulnerabilities, assessing their risk, prioritising them and taking appropriate action to reduce or remove the risk.

---

# Access Control & Identity

Access control is used to ensure that users and systems can only access the resources they are authorised to use.

Authentication is the process of establishing who or what an entity is.

Authorisation determines what an authenticated user or system is permitted to access or do.

These are separate processes. A user may successfully authenticate but still not have authorisation to access a particular resource.

## Active Directory

Active Directory provides identity and access management within Windows environments.

It can manage users, computers, groups and permissions and supports authentication across a domain environment.

Important areas include:

- User and computer accounts
- Security groups
- Group policies
- Authentication
- Authorisation
- Audit policies
- Windows security events

## NTLM & Kerberos

NTLM and Kerberos are authentication protocols used within Windows environments.

Kerberos is commonly used for authentication within Active Directory domain environments, while NTLM is an older authentication protocol that may still be present for compatibility or legacy systems.

Understanding authentication activity and the protocols involved can help identify unusual or potentially suspicious behaviour.

---

# Defensive Security

Defensive security focuses on protecting systems, networks, users and information against threats.

Defensive measures can include:

- Access controls
- Secure configuration
- Network segmentation
- Firewalls
- Antivirus and malware defences
- Security monitoring
- Logging and auditing
- Vulnerability management
- Data protection
- Backups and recovery
- Security awareness training

Effective defence involves multiple layers rather than relying on a single security control.

Security controls should also be reviewed and updated as threats, vulnerabilities and technology change.

---

# Offensive Security

Offensive security involves authorised security testing designed to identify weaknesses before malicious actors can exploit them.

## Reconnaissance

Reconnaissance is the process of gathering information about a target.

It can involve identifying:

- Infrastructure
- Technologies
- Services
- Domains
- Employees and organisational information
- Exposed systems
- Business processes

Reconnaissance can be passive or active.

Passive reconnaissance uses information obtained without directly interacting with the target, while active reconnaissance involves interacting with the target environment.

## Vulnerability Assessment

Vulnerability assessment involves identifying vulnerabilities within systems and assessing their potential risk.

Tools such as Nessus can be used to scan systems and identify known vulnerabilities and configuration issues.

The results then need to be reviewed and interpreted rather than simply accepted without analysis.

## Penetration Testing

Penetration testing is an authorised attempt to identify and exploit security weaknesses in order to determine their potential impact.

Unlike a basic vulnerability scan, penetration testing can involve manually validating vulnerabilities and demonstrating how weaknesses could be exploited.

## Red Teaming

Red teaming involves simulating realistic attacks against an organisation to test its people, processes and technology.

A red team exercise can assess not only whether vulnerabilities exist, but whether an organisation can detect and respond to an attack.

All offensive security activity must have appropriate authorisation and clearly defined boundaries.

---

# Networking & Secure Protocols

Understanding networking is important because many cybersecurity events involve communication between systems.

The OSI model provides a conceptual framework for understanding network communication, while the TCP/IP model is commonly used to describe practical network communications.

Important networking concepts include:

- IP addresses
- MAC addresses
- Ports
- Protocols
- TCP and UDP
- DNS
- HTTP and HTTPS
- SSH
- FTP
- SMTP
- Network segmentation
- Firewalls
- Secure communications

Insecure or outdated protocols can introduce security risks. Network security therefore includes protecting communications, limiting unnecessary exposure and controlling which systems can communicate with each other.

---

# Security Monitoring

Security monitoring involves collecting and analysing information from systems and networks to identify suspicious or abnormal activity.

## Logging

Logs provide records of activity within systems and applications.

Windows security logs can contain information relating to:

- Authentication
- Account activity
- Security policy changes
- Group membership
- System activity
- Other security-related events

Understanding relevant Windows Event IDs can help analysts investigate activity and identify potential security incidents.

## SIEM

A Security Information and Event Management (SIEM) system collects and correlates security information from multiple sources.

Splunk can be used to search, analyse and correlate security events.

Security monitoring can involve establishing a baseline of normal activity and looking for deviations from that baseline.

An unusual event does not automatically mean that an attack has occurred. It needs to be investigated within the wider context of the environment.

---

# Vulnerability Management

Vulnerability management is an ongoing process rather than a single scan.

A typical process includes:

1. Identify assets
2. Identify vulnerabilities
3. Assess risk
4. Prioritise vulnerabilities
5. Remediate or mitigate
6. Verify the remediation
7. Continue monitoring

Risk prioritisation helps organisations focus resources on vulnerabilities that present the greatest potential risk.

Vulnerability information can be researched using resources such as the Common Vulnerabilities and Exposures (CVE) database.

---

# Web Application Security

Web applications commonly consist of frontend components, backend application logic, databases and supporting infrastructure.

## HTTP

HTTP is used for communication between web clients and servers.

Requests can contain:

- Methods
- Headers
- Parameters
- Cookies
- Request bodies

Servers return HTTP responses containing status codes, headers and response content.

Understanding HTTP requests and responses is important when investigating web application security.

## SQL Injection

SQL injection occurs when untrusted input is incorporated into SQL queries in an unsafe way, potentially allowing an attacker to manipulate database queries.

Types of SQL injection can include:

- In-band injection
- Error-based injection
- Union-based injection
- Boolean-based blind injection
- Time-based blind injection
- Out-of-band injection
- Second-order injection

Web application security testing should be performed only within authorised or controlled environments.

---

# Threat Intelligence & OSINT

Threat intelligence involves collecting and analysing information about threats so that it can support security decisions.

A threat intelligence process can involve:

**Collect → Analyse → Understand the threat → Protect the organisation**

Open Source Intelligence (OSINT) involves gathering information from publicly available sources and analysing it to produce useful intelligence.

Open-source information can come from sources such as:

- Websites
- Newspapers
- Public databases
- Social media
- Satellite imagery
- Radio broadcasts
- Public technical information

The intelligence stage involves analysing the information to answer questions and identify useful findings rather than simply collecting information.

---

# Cyber Kill Chain

The Cyber Kill Chain describes stages that can occur during a cyber attack.

1. Reconnaissance
2. Weaponization
3. Delivery
4. Exploitation
5. Installation
6. Command & Control
7. Actions on Objectives

Understanding the stages of an attack can help defenders identify where security controls or monitoring could disrupt an attacker.

---

# Cybersecurity Frameworks

Cybersecurity frameworks provide organisations with structured approaches to managing cybersecurity risk and security activities.

## NIST Cybersecurity Framework

The NIST Cybersecurity Framework provides a risk-management structure based around:

- Identify
- Protect
- Detect
- Respond
- Recover

It can help organisations understand and manage cybersecurity risk.

## NCSC 10 Steps

The NCSC 10 Steps to Cyber Security provides broad cybersecurity guidance covering areas such as:

- Risk management
- User education and awareness
- Asset management
- Secure architecture and configuration
- Vulnerability management
- Identity and access management
- Data security
- Logging and monitoring
- Incident management
- Supply chain security

## CIS Controls

The CIS Controls provide prioritised security safeguards that organisations can implement to improve their security.

The framework contains 18 controls covering areas including:

- Asset management
- Software management
- Data protection
- Secure configuration
- Account management
- Access control
- Vulnerability management
- Logging
- Malware defence
- Data recovery
- Network security
- Security awareness
- Incident response
- Penetration testing

The CIS Controls also use Implementation Groups to help organisations prioritise safeguards according to their size, resources and risk profile.

## ISO Standards

ISO/IEC 27001 provides a framework for an Information Security Management System (ISMS).

Other ISO/IEC 27000-series standards provide guidance covering specific areas of information and application security.

Frameworks and standards can be used together where appropriate. The framework or standard selected should depend on the organisation's requirements, risks, regulatory obligations and the purpose of the assessment.

---

# Legal, Ethical & Regulatory

Cybersecurity activities must be carried out within legal and ethical boundaries.

Authorisation is particularly important when performing security testing. A person should not scan, access, exploit or interfere with systems without appropriate permission.

Relevant UK legislation and regulatory requirements can include:

- Computer Misuse Act 1990
- UK GDPR
- Data Protection Act 2018
- Privacy and Electronic Communications Regulations (PECR)

Ethical conduct includes acting responsibly, maintaining confidentiality, following agreed security procedures and avoiding conflicts of interest.

Security professionals should ensure that their activities remain within the agreed scope and that information discovered during security work is handled appropriately.

---

# Incident Response

Incident response is the process used by an organisation to identify, manage and recover from cybersecurity incidents.

An effective incident response process can include:

- Preparation
- Identification
- Containment
- Eradication
- Recovery
- Lessons learned

Incident response should consider both the technical response and the wider organisational impact.

## Incident Post-Mortem

Following an incident, a post-mortem can be used to document what happened, why it happened, the impact, how the incident was handled and what can be improved.

The aim should be to learn from the incident and reduce the likelihood or impact of similar incidents in the future.

---

# Cryptography & Data Analysis

Cryptography provides methods for protecting information and communications.

Important concepts include:

- Encoding
- Hashing
- Encryption
- Decryption
- Keys

Encoding is designed to represent data in another format and is not intended to provide confidentiality.

Hashing produces a fixed-length representation of data and is commonly used for integrity checking and other security purposes.

Encryption is used to protect confidentiality by transforming data so that it cannot be understood without the appropriate means of decryption.

## CyberChef

CyberChef can be used for a range of data analysis and transformation tasks, including:

- Base64 encoding and decoding
- URL encoding and decoding
- Hexadecimal conversion
- XOR operations
- Hashing
- Encryption and decryption

It is useful for analysing and transforming data encountered during security investigations and practical exercises.

---

# Security Principles

Across these areas, several principles are important to effective cybersecurity:

- Confidentiality
- Integrity
- Availability
- Least privilege
- Defence in depth
- Secure configuration
- Continuous monitoring
- Risk-based decision making
- Appropriate authorisation
- Regular review and improvement

Cybersecurity is an ongoing process. Systems, vulnerabilities, threats and technologies change continuously, meaning organisations need to continually assess and improve their security.

---

## Practical Application

The concepts documented here are supported by practical training and security assessments within this portfolio.

Relevant practical work will be linked as it is completed, including:

- Vulnerability assessment
- Security monitoring
- Active Directory investigation
- Network analysis
- Web application security
- Reconnaissance and OSINT
- Threat intelligence
- Vulnerability management
- Incident analysis
