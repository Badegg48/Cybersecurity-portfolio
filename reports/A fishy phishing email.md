# Phishing Incident Investigation

## Overview

This report documents a simulated phishing incident based on an incident response and post-mortem exercise completed as part of my NCFE Level 3 Certificate in Cyber Security Practices.

The exercise focused on investigating a suspected phishing email, documenting the incident, assessing the potential impact and identifying lessons that could reduce the likelihood or impact of similar incidents in the future.

This is a coursework-based simulated incident and not an investigation of a real organisation or customer environment.

---

## Objective

The objective of the exercise was to:

- Investigate a suspected phishing email.
- Identify the potential security risk.
- Document how the incident was detected and handled.
- Establish the likely root cause.
- Create an incident timeline.
- Identify lessons learned and potential improvements.

A post-mortem should provide a blame-free analysis of what happened, why it happened and how the organisation's incident response worked, with the aim of learning from the incident and preventing similar incidents in the future.

---

## Scenario

A staff member reported receiving a suspected phishing email.

The message appeared to be from the HR department and was disguised as a holiday request form. The email asked the recipient to follow a link to download a PDF titled:

`Holiday request form`

The suspicious link created a potential security risk if the recipient interacted with it.

---

## Initial Report

The incident was initially identified by the staff member, who recognised the email as suspicious and reported it to the security team.

The message was then investigated to determine whether it represented a genuine security threat.

---

## Investigation

The security team investigated the reported email and confirmed that it was malicious.

The investigation established that the message used social engineering techniques to make the email appear legitimate and encourage the recipient to interact with the supplied link.

The main concern was not simply that the email reached the inbox, but that interaction with the malicious link could potentially have resulted in a wider compromise.

The exercise therefore considered the incident from both a detection and response perspective.

---

## Findings

The investigation identified the following:

### Phishing email

The message was designed to appear as a legitimate HR communication relating to a holiday request.

### Social engineering

The attacker attempted to make the recipient trust the message by disguising it as an internal HR request.

### Suspicious link

The email contained a link that directed the recipient towards downloading a PDF.

### Potential impact

The primary risks identified were:

- Malware infection.
- Unauthorised access.

No further compromise was identified during the exercise.

---

## Incident Timeline

| Time | Event |
|---|---|
| 09:12 AM | Phishing email received by staff member |
| 09:16 AM | Staff member identifies the email as suspicious |
| 09:18 AM | Suspected phishing email reported to the security team |
| 09:25 AM | Security team begins investigation |
| 09:34 AM | Email confirmed as malicious |
| 09:40 AM | Malicious email removed from the affected inbox |
| 09:47 AM | Staff account checked for signs of compromise |
| 10:05 AM | Incident response completed and incident closed |

---

## Impact Assessment

The potential impact of the incident was the compromise of a staff member through a malicious phishing link.

The identified risks were malware infection and unauthorised access.

The incident was detected and reported before a further breach occurred, and the account was checked for signs of compromise.

Based on the information available in the exercise, no further threat was identified and the incident was considered resolved.

---

## Response Actions

The response included:

1. Investigating the reported email.
2. Confirming that the email was malicious.
3. Blocking the sending address.
4. Removing the malicious email from the affected inbox.
5. Checking the user's account for signs of compromise.
6. Reminding staff to check email addresses carefully.
7. Closing the incident once no further threat was identified.

---

## Root Cause

The root cause was the successful delivery of a phishing email to a staff member's inbox.

The attack relied on social engineering to make a malicious message appear to be a legitimate HR communication and encourage the recipient to follow an unsafe link.

The exercise demonstrates that phishing is not solely a technical problem. User awareness and email security controls both form part of the defence against this type of attack.

---

## Detection

Detection in this case relied on the staff member recognising that the email was suspicious and reporting it to the security team.

This highlights the importance of user awareness as part of an organisation's overall detection capability.

It also demonstrates why security monitoring and other detection mechanisms should complement user reporting rather than relying on a single source of detection.

---

## Recovery

Recovery consisted of removing the malicious email and checking the affected user account for signs of compromise.

The incident was considered resolved once no further threat was identified.

The exercise did not provide evidence of an actual system compromise, so no wider system recovery or rebuilding was required.

---

## Lessons Learned

Several lessons can be taken from the incident.

### Security awareness

The incident demonstrates the value of staff being able to recognise suspicious emails and report them quickly.

### Email security

The exercise also highlights the importance of effective email security controls to reduce the likelihood of malicious messages reaching users.

### Early reporting

The time between the suspicious email being identified and being reported to the security team was short. Early reporting allowed the security team to investigate and respond before further compromise occurred.

### Incident response

The exercise reinforced the importance of documenting the incident, maintaining a clear timeline and reviewing how the response worked.

---

## Recommendations

Based on the exercise, the following improvements could help reduce the likelihood or impact of similar incidents:

- Continue security awareness training for staff.
- Reinforce the process for reporting suspicious emails.
- Maintain effective email security controls.
- Review phishing detection and filtering capabilities.
- Continue testing and reviewing the incident response process.
- Use lessons learned from incidents to improve future response procedures.

These recommendations are based on the scenario and the lessons identified during the exercise.

---

## Incident Response Process

This exercise relates closely to the incident response lifecycle studied during the course.

The wider incident response process includes preparation, identification, containment, eradication, recovery and lessons learned.

For this incident, the practical exercise primarily demonstrated identification, response, recovery and lessons learned.

Post-incident activities should also include reviewing what happened, updating response procedures where necessary and confirming that the security risk has been removed.

---

## What I Learned

This exercise helped me understand that incident response is not simply about reacting to a technical compromise.

A suspected phishing email still requires a structured process:

**Report → Investigate → Confirm → Contain → Check for compromise → Recover → Learn**

One of the most useful parts of the exercise was creating the timeline. Recording exactly when the email was received, reported, investigated and resolved makes it much easier to understand how quickly the incident was detected and how effectively it was handled.

The exercise also reinforced the importance of documentation. A good incident report should explain what happened, what the impact could have been, what actions were taken and what should be improved afterwards.

---

## Skills & Techniques Demonstrated

- Incident identification
- Phishing analysis
- Social engineering awareness
- Incident response lifecycle
- Incident timeline construction
- Impact assessment
- Root cause identification
- Incident documentation
- Post-mortem analysis
- Lessons learned
- Security awareness
- Risk identification

---

## Classification

**Type:** Coursework / Simulated Incident  
**Area:** Incident Response  
**Scenario:** Phishing / Social Engineering  
**Status:** Completed  
**Platform:** NCFE Level 3 Certificate in Cyber Security Practices
