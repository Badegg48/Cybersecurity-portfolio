# Security Foundations

This is my personal cybersecurity knowledge base, covering the concepts and security practices I have developed through the NCFE Level 3 Certificate in Cyber Security Practices, practical training, independent study and wider professional development.

I use this as a reference for things I have learned and want to retain, but also as a way of documenting how my understanding has developed through practical work.

My main career interest is incident response, cybersecurity investigation, digital forensics and security monitoring, while continuing to build a broad foundation across vulnerability management, networking, threat intelligence, security testing, detection engineering and governance.

## Domains at a glance

| Domain | What I understand / can apply |
|---|---|
| Incident Response | Understand the incident lifecycle, investigation, containment, recovery and post-incident review |
| Security Monitoring | Use SIEM concepts, logs, Event IDs, alert triage, baselines and anomaly analysis to investigate activity |
| Digital Forensics | Understand the role of digital evidence, artefacts, integrity and investigative documentation |
| Threat Intelligence & OSINT | Gather information, distinguish information from intelligence and use findings to understand threats |
| Vulnerability Management | Identify, assess, prioritise and investigate vulnerabilities and consider remediation |
| Active Directory & Identity | Understand authentication, authorisation, Active Directory, NTLM, Kerberos and Windows identity events |
| Networking | Understand OSI/TCP-IP, protocols, ports and how network activity can be investigated |
| Web Security | Understand HTTP, web applications and common application security weaknesses |
| Security Testing | Understand reconnaissance, vulnerability assessment, penetration testing, Metasploit and the importance of scope |
| Governance & Risk | Understand frameworks, standards, risk, legislation, security controls and organisational governance |
| Security Reporting | Produce structured security documentation and understand the importance of evidence, timelines, root cause and recommendations |
| Detection Engineering | Understand how detections are designed, tested, tuned, deployed and maintained within a SOC |
| Project & Change Management | Understand project lifecycle, planning, stakeholder communication, change management, governance and project methodologies |

## 1. Incident Response

Incident response is the area I am currently most interested in developing. I have studied the incident lifecycle from preparation and detection through containment, eradication, recovery and lessons learned. One thing that stood out to me is that incident response is not simply about removing the immediate threat; the organisation also needs to understand what happened, how it was detected, how well the response worked and what needs to change afterwards.

I have also looked at the difference between **incident precursors** and **incident indicators**. A precursor is something that suggests an incident may happen, such as a newly disclosed vulnerability or exploit announcement, while an indicator provides evidence that an attack may already be underway.

My coursework has included a phishing incident exercise where I worked through the incident from initial reporting through investigation, response, recovery, timeline and lessons learned. I have also studied incident response through wider case studies, including WannaCry, to understand how a vulnerability can be exploited, how malware can propagate and how defensive measures can affect the course of an incident.

The WannaCry case study was particularly useful because the malware behaved like a worm, automatically spreading by exploiting the Windows SMB vulnerability associated with EternalBlue rather than relying entirely on user interaction. The case also demonstrated the importance of patch management, legacy systems, network exposure and rapid containment. A kill switch discovered during the outbreak significantly slowed the spread of the original malware. 

I want to build on this with more practical investigation and digital forensics work.

## 2. Security Monitoring

My work with security monitoring has helped me understand that a security analyst is not simply looking for one "bad" log entry. The useful information often comes from putting several events together and understanding what normal activity looks like first.

I have worked with SIEM concepts and Splunk, including Windows security events, authentication activity, audit logging, baselines and anomaly identification. The process I use to think about SIEM is:

**Collect → Parse → Normalise → Correlate → Detect → Alert → Investigate**

A major part of my newer training has been understanding the relationship between events, logs, security detections and SOC alerts:

**Event → Log → SIEM/EDR → Alert → SOC Investigation**

An alert is generated when activity matches a detection rule or other detection logic. SOC L1 analysts then triage alerts to determine whether activity is legitimate or potentially malicious, escalating genuine threats when deeper investigation is required.

### SOC L1 Alert Triage

I have studied and practised the process of reviewing and triaging security alerts.

The main information I consider includes:

- Alert time and event time
- Alert name and description
- Severity
- Status
- Verdict
- Assignee / ownership
- Affected host, IP and user
- Detection logic and triggering fields

My basic prioritisation process is:

**Filter → Severity → Time**

New, unseen and unresolved alerts are considered first, followed by severity from critical to low and then the age of the alert within the same severity level.

The investigation process can include identifying the affected user or host, understanding the activity that triggered the alert, reviewing surrounding events, checking threat intelligence and determining whether the activity is malicious or legitimate.

The final stage is to document what was investigated, the evidence found, the analysis performed and the reason for the final verdict before closing or escalating the alert.

This has helped me understand the importance of **ownership, prioritisation, investigation, escalation and accurate documentation** within a SOC.

### Windows Security Monitoring

My newer Windows monitoring training has given me more detailed experience with Windows event logs and host-based investigation.

Two particularly important Windows Security events I have studied are:

- **4624 – Successful Logon**
- **4625 – Failed Logon**

Event 4625 can be useful when investigating brute-force attacks, password spraying and other suspicious authentication activity. Event 4624 can then be used to investigate successful access, including suspicious RDP logins.

Important fields include:

- Logon ID
- Logon Type
- Username
- Source IP
- Hostname / Workstation Name

For RDP investigation, **Logon Type 10** indicates an RDP login, while **Logon Type 3** represents a network logon. A suspicious sequence can therefore be investigated by looking for failed authentication attempts followed by a successful login and then examining what happened during that session.

The **Logon ID** is particularly useful because it can be used to correlate related events from the same session.

### Windows User Management

I have also studied Windows account and group-management events that can indicate persistence or privilege escalation.

Important events include:

- **4720** – User created
- **4722** – User enabled
- **4738** – User changed
- **4725** – User disabled
- **4726** – User deleted
- **4723** – User changed password
- **4724** – Password reset
- **4732** – User added to security group
- **4733** – User removed from security group

A useful investigation technique is:

**Suspicious user-management event → Copy Logon ID → Find matching 4624 → Identify who performed the action**

This provides a way to connect an account change back to the login session that performed it.

### Process Monitoring

I have studied both Windows process creation logging and Sysmon.

- **Event ID 4688** records new process creation in the Security log.
- **Sysmon Event ID 1** provides more detailed process creation telemetry, including hashes, digital signatures and PE metadata.

I have learned to investigate:

- Process path and location
- Command line
- Parent process
- Parent-child relationships
- Process hash
- Digital signature
- User context
- Logon ID

Suspicious paths such as `C:\Temp` or `C:\Users\Public`, unusual executable names and unexpected parent-child relationships can provide useful investigation leads.

Following the process tree and correlating the process Logon ID with Windows Security events can help reconstruct what happened during a suspicious session.

The biggest lesson for me has been that an unusual event is not automatically an attack. It needs to be investigated in context, where baselines, correlation and knowledge of the environment become important.

## 3. Digital Forensics

Digital forensics is an area I am particularly interested in moving towards, although I am still building my practical experience.

The main principle I have taken from my studies is that an investigation needs to be **evidence-led**. Logs, files, metadata, authentication records, network traffic and other digital artefacts can help establish what happened, when it happened and which systems may have been affected.

I have also learned that finding an interesting artefact is only part of an investigation. Evidence needs to be considered in context, documented properly and distinguished from assumptions or conclusions. Maintaining evidence integrity and being able to explain how a finding was reached are just as important.

My Windows security monitoring work has also helped connect digital evidence to investigation. Event IDs, Logon IDs, process creation events, process trees and authentication activity can provide individual pieces of evidence that can then be correlated to understand a wider sequence of activity.

## 4. Threat Intelligence & OSINT

I have learned to distinguish between **open-source information** and **intelligence**. Open-source information is what can be collected from publicly available sources, while intelligence comes from analysing that information to answer a question or support a decision.

The threat intelligence process I have been taught is:

**Collect → Analyse → Understand the threat → Protect the organisation**

I have worked with OSINT and reconnaissance during my practical learning, using publicly available information to understand targets, technologies and potential security exposure. The main lesson I have taken from this is that collecting large amounts of information is not particularly useful on its own; the analysis and context are what turn information into intelligence.

### Unified Kill Chain

I have also studied the **Unified Kill Chain** as a way of understanding attack progression.

The stages covered include:

1. Reconnaissance
2. Weaponization
3. Delivery
4. Social Engineering
5. Exploitation
6. Persistence
7. Defense Evasion
8. Command & Control
9. Pivoting
10. Discovery
11. Privilege Escalation
12. Execution
13. Credential Access
14. Lateral Movement
15. Collection
16. Exfiltration
17. Impact
18. Objectives

Understanding an attack as a sequence of stages helps connect threat intelligence with detection and incident investigation. It also highlights opportunities where defenders may be able to detect or disrupt an attacker.

## 5. Vulnerability Management

My practical vulnerability work has mainly involved Nessus, but I have found that vulnerability management is much broader than running a scan.

The process is better thought of as:

**Identify → Assess → Prioritise → Remediate → Verify → Monitor**

A scanner can identify a vulnerability, but somebody still needs to understand what it means, how serious it is in context, what the business impact could be and what needs to happen next. I have also used CVE resources when researching known vulnerabilities.

One thing I have found particularly useful is understanding that technical severity and business risk are not always the same thing. A finding needs to be considered in the context of the affected asset, potential impact, exploitability and the wider environment.

The WannaCry case study reinforced this understanding. The attack demonstrated how an unpatched vulnerability can become a much larger organisational risk when vulnerable systems are exposed and connected to one another.

## 6. Active Directory & Identity

I have studied the difference between **authentication** and **authorisation**, along with Active Directory, NTLM and Kerberos.

What has made this particularly useful is connecting identity concepts with security monitoring. Authentication activity, account changes, group membership and Windows security events can provide useful information during an investigation.

I have used this knowledge alongside Splunk-based monitoring exercises, looking at authentication behaviour and Windows security events. It has helped me understand why identity is such an important part of investigating suspicious activity rather than treating a login as an isolated event.

My newer Windows monitoring work has expanded this further by looking at account creation, account changes, password activity and group membership events. These can be particularly useful when investigating persistence and privilege escalation.

## 7. Networking

Networking has become increasingly important to my cybersecurity learning because network activity can provide both an attack surface and evidence during an investigation.

I have studied the OSI and TCP/IP models, TCP and UDP, ports and common protocols including DNS, HTTP/HTTPS, SSH, FTP and SMTP. I have also completed Wireshark training, which helped connect the theory to actual network traffic.

One of the more useful things I have taken from this is being able to look at network communication as something that can be investigated. Understanding what a protocol normally does makes unusual traffic much easier to recognise.

I have also connected networking concepts to real attacks through case-study work such as WannaCry, where SMB was used as the mechanism for exploitation and propagation between vulnerable Windows systems.

## 8. Web Security

I have studied how web applications are structured across frontend components, backend application logic, databases and supporting infrastructure.

A lot of my understanding comes from learning how HTTP actually works. Requests contain things such as methods, headers, parameters, cookies and request bodies, while responses contain status codes, headers and returned content. Understanding that interaction makes it easier to understand where application security weaknesses can occur.

I have also studied SQL injection and its different forms in controlled learning environments. The main lesson I have taken from this is that application security is often about how trusted backend systems process input supplied by users.

## 9. Security Testing

My course has introduced me to several forms of security testing, including reconnaissance, vulnerability testing, penetration testing, red teaming and social engineering testing.

The common principle across all of them is **authorisation and scope**. Having the ability to run a scan or test a system does not mean I am entitled to do so. Testing needs to be conducted against agreed targets and within defined boundaries.

I have applied this through controlled practical learning, including Nessus vulnerability scanning, reconnaissance with Shodan and security exercises through TryHackMe. I have also studied web application security and SQL injection in controlled environments.

### Metasploit Framework

I have also studied the **Metasploit Framework**, a penetration-testing framework used for tasks including scanning, exploitation and post-exploitation.

An important relationship I have learned is:

**Vulnerability → Exploit → Payload → Desired Result**

A vulnerability is the weakness, an exploit is code that takes advantage of that weakness, and the payload determines what happens after successful exploitation.

I have worked with the Metasploit console and studied concepts including:

- `msfconsole`
- Module selection with `use`
- `show options`
- `show payloads`
- `info`
- `search`
- Module configuration with `set`
- Target parameters such as `RHOSTS`
- Payload parameters such as `PAYLOAD`
- Listener parameters such as `LHOST` and `LPORT`

I have also studied the different Metasploit module categories, including auxiliary, exploit, payload, encoder, evasion, NOP and post modules.

The main lesson for me is that exploitation tools provide capabilities, but the tester still needs to understand the vulnerability, target, scope and likely impact before using them.

## 10. Governance & Risk

I have studied cybersecurity frameworks, standards, legislation and the role they play in managing security risk.

The main frameworks I have looked at are the **NIST Cybersecurity Framework, NCSC 10 Steps and CIS Controls**. I see them as different approaches rather than competing answers: NCSC provides broad UK-focused guidance, NIST provides a structured way of thinking about cybersecurity risk, and CIS provides more specific and prioritised safeguards.

I have also studied ISO/IEC standards including ISO/IEC 27001, along with UK legislation such as the Computer Misuse Act 1990, UK GDPR, the Data Protection Act 2018 and PECR.

One thing I have found important is understanding that a framework, a standard and a piece of legislation are not the same thing. They can work together, but they serve different purposes and the right approach depends on the organisation, its risks and what is being assessed.

### Risk and Governance

My project management study has also helped me understand the broader role of governance in organisations.

**Governance** is the framework within which decisions are made and accountability and responsibility are determined. Project governance defines how project decisions are made and how responsibility is assigned.

This connects closely with cybersecurity because security decisions also depend on clear ownership, risk management, policies, controls and accountability.

## 11. Security Reporting

One of the areas I think is often overlooked when people talk about cybersecurity is **reporting and documentation**.

My coursework has covered vulnerability reporting, incident reporting and post-mortem reporting. In particular, I have worked through the structure of an incident post-mortem covering the incident summary, lead-up, fault, impact, detection, response, recovery, timeline, root cause, recurrence and lessons learned.

The part I find most useful is the distinction between describing what happened and identifying **why it happened**. Root cause analysis and techniques such as the 5 Why approach can help move an investigation beyond the immediate symptom.

### Post-Mortem Reporting

I have studied three important principles when producing a post-mortem:

**Integrity** – Reports should support a collaborative and blameless process. A complex incident is rarely caused by one factor, and documentation should focus on understanding what happened and improving future response.

**Rigour** – Reports should contain enough detail to be useful, including timelines, evidence, actions taken, relevant records and supporting information such as screenshots or monitoring data where available.

**Discipline** – A post-mortem needs to be reviewed, completed, have its action items captured and be stored where others can access and learn from it.

Good technical work still needs to be communicated clearly if it is going to result in action.

## 12. Detection Engineering

I have begun studying **Detection Engineering** as part of my wider security monitoring development.

Detection Engineering is the systematic process of designing, building, testing and maintaining detections that support a SOC. Unlike an analyst who primarily reacts to alerts, detection engineering focuses on creating and improving the detections that identify suspicious activity.

The lifecycle I have studied is:

**Backlog Management → Threat Research → Data Review → Detection Design → Testing & Validation → Deployment → Maintenance**

### Detection Design and Testing

Before writing a detection, it is important to understand:

- What behaviour needs to be detected?
- Which data source is required?
- Is the required telemetry actually available?
- Is the data sufficiently useful and correctly parsed?
- What detection logic will identify the behaviour?
- How will the detection be tested?
- How many false positives does it produce?
- Does the detection remain useful over time?

A detection that fails testing should return to the design stage rather than simply being deployed.

### Detection Tuning

Detection tuning aims to reduce false positives without creating blind spots.

I have studied the importance of maintaining detections over time, including monitoring whether detections still provide value, whether they generate excessive noise and whether they should eventually be retired.

### Detection Gap and Durable Detection

One concept that stood out to me is the **Detection Gap** between attacker evasion capability and defender detection capability.

The goal is not necessarily to detect every possible technique, but to maintain useful coverage and reduce opportunities for attackers to move through the environment undetected.

I have also studied the value of focusing on attacker **behaviours and TTPs** rather than relying entirely on easily changed indicators such as IP addresses or hashes.

This connects to the Pyramid of Pain:

**Hashes / IP addresses → Tools → Behaviours / TTPs**

Behaviour-based detection can be more durable because changing infrastructure does not necessarily change the underlying technique.

### Precision and Recall

Two measures I have studied are:

**Precision** – Of all alerts generated, how many represent real threats?

**Recall** – Of all real attacks, how many were detected?

A false positive is an alert that fires without a genuine threat, while a false negative is a real attack that the detection fails to identify.

The aim is to maintain a useful balance between detection coverage and alert noise.

## 13. Project & Change Management

I completed the **Google Foundations of Project Management** course, which added a broader understanding of project planning, coordination, communication and organisational processes to my technical development.

A project is a **unique, temporary endeavour with a defined beginning and end**, aimed at achieving a specific outcome through a series of tasks.

The project lifecycle I studied is:

**Initiate → Plan → Execute & Complete → Close**

Project management involves planning and organising work, coordinating resources, managing tasks, budgeting, controlling costs, communicating with stakeholders and keeping projects aligned with their goals.

### Cross-Functional Teams

I studied how project managers work with **cross-functional teams**, where people with different specialist skills work towards a common goal.

Important responsibilities include:

- Clarifying goals
- Identifying the right skills
- Measuring progress
- Recognising contributions
- Communicating clearly between different functions

This is particularly relevant to cybersecurity because security work often involves IT, infrastructure, networking, management, users and other teams.

### Change Management

I studied change management as part of successful project delivery.

A project may be technically successful but still fail if the people affected by the change do not adopt it.

Key practices include:

- Being proactive
- Communicating upcoming changes
- Following a consistent process
- Practising empathy
- Using feedback mechanisms and other tools
- Demonstrating new deliverables to stakeholders
- Escalating when change management support is required

Understanding organisational culture is also important because values, communication styles, policies and processes can influence how people respond to change.

### Organisational Structures and Governance

I studied both **Classic** and **Matrix** organisational structures.

A Classic structure follows a more traditional top-down hierarchy, while a Matrix structure can involve multiple reporting relationships and greater cross-functional communication.

Understanding organisational structure helps identify:

- Communication routes
- Stakeholders
- Authority
- Resource availability
- Approval processes
- Where support or escalation should go

I also studied Project Management Offices (PMOs), which can provide standards, best practices, project governance, resource management, documentation and organisational consistency.

### Project Management Methodologies

I have studied several project management methodologies and approaches:

**Waterfall** – A sequential approach where phases are completed in order and requirements are generally established early.

**Agile** – An iterative approach using shorter cycles, collaboration, feedback and adaptation.

**Scrum** – An Agile framework using short Sprints and cross-functional teams.

**Kanban** – A visual method for managing work through stages such as:

**To Do → In Progress → Testing → Done**

**Lean** – Focuses on removing waste and improving efficiency.

The eight areas of waste I studied are:

- Defects
- Excess processing
- Overproduction
- Waiting
- Inventory
- Transportation
- Motion
- Non-utilised talent

Lean also uses the **5S** approach:

**Sort → Set in order → Shine → Standardize → Sustain**

**Six Sigma** – Focuses on reducing variation and improving quality through measurable processes.

**Lean Six Sigma** combines Lean efficiency improvements with Six Sigma quality improvement.

### DMAIC

I have also studied the Lean Six Sigma **DMAIC** process:

**Define → Measure → Analyse → Improve → Control**

DMAIC provides a structured, data-driven approach to identifying problems, finding root causes, implementing improvements and ensuring that improvements are maintained.

The project management course has reinforced skills that are also useful in cybersecurity, including structured planning, prioritisation, communication, stakeholder management, escalation, documentation, change management and understanding how different teams contribute towards a shared outcome.
