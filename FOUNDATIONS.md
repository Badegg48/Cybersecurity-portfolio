# Security Foundations

This is my personal cybersecurity knowledge base, covering the concepts and
security practices I have developed through the NCFE Level 3 Certificate in
Cyber Security Practices, practical training and independent study.

I use this as a reference for things I have learned and want to retain, but
also as a way of documenting how my understanding has developed through
practical work.

My main career interest is incident response, cybersecurity investigation,
digital forensics and security monitoring, while continuing to build a broad
foundation across vulnerability management, networking, threat intelligence,
security testing and governance.

## Domains at a glance

| Domain | What I understand / can apply |
|---|---|
| Incident Response | Understand the incident lifecycle, investigation, containment, recovery and post-incident review |
| Security Monitoring | Use SIEM concepts, logs, Event IDs, baselines and anomaly analysis to investigate activity |
| Digital Forensics | Understand the role of digital evidence, artefacts, integrity and investigative documentation |
| Threat Intelligence & OSINT | Gather information, distinguish information from intelligence and use findings to understand threats |
| Vulnerability Management | Identify, assess, prioritise and investigate vulnerabilities and consider remediation |
| Active Directory & Identity | Understand authentication, authorisation, Active Directory, NTLM and Kerberos |
| Networking | Understand OSI/TCP-IP, protocols, ports and how network activity can be investigated |
| Web Security | Understand HTTP, web applications and common application security weaknesses |
| Security Testing | Understand reconnaissance, vulnerability assessment, penetration testing and the importance of scope |
| Governance & Risk | Understand the role of frameworks, standards, risk, legislation and security controls |
| Security Reporting | Produce structured security documentation and understand the importance of evidence, timelines and clear recommendations |

## 1. Incident Response

Incident response is the area I am currently most interested in developing. I have studied the incident lifecycle from preparation and detection through containment, eradication, recovery and lessons learned. One thing that stood out to me is that incident response is not simply about removing the immediate threat; the organisation also needs to understand what happened, how it was detected, how well the response worked and what needs to change afterwards.

I have also looked at the difference between **incident precursors** and **incident indicators**. A precursor is something that suggests an incident may happen, such as a newly disclosed vulnerability or exploit announcement, while an indicator provides evidence that an attack may already be underway.

My coursework has included a phishing incident exercise where I worked through the incident from initial reporting through investigation, response, recovery, timeline and lessons learned. I want to build on this with more practical investigation and digital forensics work.

## 2. Security Monitoring

My work with security monitoring has helped me understand that a security analyst is not simply looking for one "bad" log entry. The useful information often comes from putting several events together and understanding what normal activity looks like first.

I have worked with SIEM concepts and Splunk, including Windows security events, authentication activity, audit logging, baselines and anomaly identification. The process I use to think about SIEM is:

**Collect → Parse → Normalise → Correlate → Detect → Alert → Investigate**

The biggest lesson for me has been that an unusual event is not automatically an attack. It needs to be investigated in context, which is where baselines, correlation and knowledge of the environment become important.

## 3. Digital Forensics

Digital forensics is an area I am particularly interested in moving towards, although I am still building my practical experience.

The main principle I have taken from my studies is that an investigation needs to be **evidence-led**. Logs, files, metadata, authentication records, network traffic and other digital artefacts can help establish what happened, when it happened and which systems may have been affected.

I have also learned that finding an interesting artefact is only part of an investigation. Evidence needs to be considered in context, documented properly and distinguished from assumptions or conclusions. Maintaining evidence integrity and being able to explain how a finding was reached are just as important.

## 4. Threat Intelligence & OSINT

I have learned to distinguish between **open-source information** and **intelligence**. Open-source information is what can be collected from publicly available sources, while intelligence comes from analysing that information to answer a question or support a decision.

The threat intelligence process I have been taught is:

**Collect → Analyse → Understand the threat → Protect the organisation**

I have worked with OSINT and reconnaissance during my practical learning, using publicly available information to understand targets, technologies and potential security exposure. The main lesson I have taken from this is that collecting large amounts of information is not particularly useful on its own; the analysis and context are what turn information into intelligence.

## 5. Vulnerability Management

My practical vulnerability work has mainly involved Nessus, but I have found that vulnerability management is much broader than running a scan.

The process is better thought of as:

**Identify → Assess → Prioritise → Remediate → Verify → Monitor**

A scanner can identify a vulnerability, but somebody still needs to understand what it means, how serious it is in context, what the business impact could be and what needs to happen next. I have also used CVE resources when researching known vulnerabilities.

One thing I have found particularly useful is understanding that technical severity and business risk are not always the same thing. A finding needs to be considered in the context of the affected asset, potential impact, exploitability and the wider environment.

## 6. Active Directory & Identity

I have studied the difference between **authentication** and **authorisation**, along with Active Directory, NTLM and Kerberos.

What has made this particularly useful is connecting identity concepts with security monitoring. Authentication activity, account changes, group membership and Windows security events can provide useful information during an investigation.

I have used this knowledge alongside Splunk-based monitoring exercises, looking at authentication behaviour and Windows security events. It has helped me understand why identity is such an important part of investigating suspicious activity rather than treating a login as an isolated event.

## 7. Networking

Networking has become increasingly important to my cybersecurity learning because network activity can provide both an attack surface and evidence during an investigation.

I have studied the OSI and TCP/IP models, TCP and UDP, ports and common protocols including DNS, HTTP/HTTPS, SSH, FTP and SMTP. I have also completed Wireshark training, which helped connect the theory to actual network traffic.

One of the more useful things I have taken from this is being able to look at network communication as something that can be investigated. Understanding what a protocol normally does makes unusual traffic much easier to recognise.

## 8. Web Security

I have studied how web applications are structured across frontend components, backend application logic, databases and supporting infrastructure.

A lot of my understanding comes from learning how HTTP actually works. Requests contain things such as methods, headers, parameters, cookies and request bodies, while responses contain status codes, headers and returned content. Understanding that interaction makes it easier to understand where application security weaknesses can occur.

I have also studied SQL injection and its different forms in controlled learning environments. The main lesson I have taken from this is that application security is often about how trusted backend systems process input supplied by users.

## 9. Security Testing

My course has introduced me to several forms of security testing, including reconnaissance, vulnerability testing, penetration testing, red teaming and social engineering testing.

The common principle across all of them is **authorisation and scope**. Having the ability to run a scan or test a system does not mean I am entitled to do so. Testing needs to be conducted against agreed targets and within defined boundaries.

I have applied this through controlled practical learning, including Nessus vulnerability scanning, reconnaissance with Shodan and security exercises through TryHackMe. I have also studied web application security and SQL injection in controlled environments. The main thing I have learned is that tools provide information, but the analyst still needs to interpret what the results actually mean.

## 10. Governance & Risk

I have studied cybersecurity frameworks, standards, legislation and the role they play in managing security risk.

The main frameworks I have looked at are the **NIST Cybersecurity Framework, NCSC 10 Steps and CIS Controls**. I see them as different approaches rather than competing answers: NCSC provides broad UK-focused guidance, NIST provides a structured way of thinking about cybersecurity risk, and CIS provides more specific and prioritised safeguards.

I have also studied ISO/IEC standards including ISO/IEC 27001, along with UK legislation such as the Computer Misuse Act 1990, UK GDPR, the Data Protection Act 2018 and PECR.

One thing I have found important is understanding that a framework, a standard and a piece of legislation are not the same thing. They can work together, but they serve different purposes and the right approach depends on the organisation, its risks and what is being assessed.

## 11. Security Reporting

One of the areas I think is often overlooked when people talk about cybersecurity is **reporting and documentation**.

My coursework has covered vulnerability reporting, incident reporting and post-mortem reporting. In particular, I have worked through the structure of an incident post-mortem covering the incident summary, lead-up, fault, impact, detection, response, recovery, timeline, root cause, recurrence and lessons learned.

The part I find most useful is the distinction between describing what happened and identifying **why it happened**. Root cause analysis and techniques such as the 5 Why approach can help move an investigation beyond the immediate symptom.

I have also learned that a security report needs to make evidence, impact and recommendations understandable to its intended audience. Good technical work still needs to be communicated clearly if it is going to result in action.
