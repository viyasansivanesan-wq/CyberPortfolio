\# TryHackMe — Defensive Security Intro

&#x20;

\*\*Platform:\*\* TryHackMe

\*\*Room:\*\* \[Defensive Security Intro](https://tryhackme.com/room/defensivesecurityintro)

\*\*Difficulty:\*\* Easy

\*\*Category:\*\* Blue Team / Fundamentals

\*\*Date Completed:\*\* April 2026

\*\*Status:\*\* ✅ Completed

&#x20;

\---

&#x20;

\## Overview

&#x20;

Completed the Defensive Security Intro room on TryHackMe. This room introduced the core concepts of defensive security, the blue team mindset, and the tools and processes used to protect systems from attacks. It covers four key subfields — SOC, Threat Intelligence, DFIR, and Malware Analysis — and ends with a hands-on SIEM simulation.

&#x20;

\---

&#x20;

\## Objectives

&#x20;

\- Understand what defensive security is and how it differs from offensive security

\- Learn about the role of a Security Operations Center (SOC)

\- Get introduced to Digital Forensics and Incident Response (DFIR)

\- Understand threat intelligence and malware analysis at a conceptual level

\- Complete a simulated SIEM alert triage scenario

\---

&#x20;

\## Key Concepts

&#x20;

\### Defensive Security vs Offensive Security

&#x20;

Where offensive security focuses on finding and exploiting vulnerabilities, defensive security focuses on \*\*preventing intrusions\*\* and \*\*detecting/responding\*\* to them when they occur. Blue teamers are the defenders.

&#x20;

\### Security Operations Center (SOC)

&#x20;

A centralised team that monitors networks and systems 24/7 for malicious activity. Key responsibilities include vulnerability management, policy enforcement, detecting unauthorised access, and responding to network intrusions.

&#x20;

\### Threat Intelligence

&#x20;

The process of gathering and analysing information about adversaries to build proactive defences. Covers attacker TTPs (Tactics, Techniques, and Procedures) from internal logs, public feeds, and industry sharing groups.

&#x20;

\### Digital Forensics and Incident Response (DFIR)

&#x20;

\- \*\*Digital Forensics\*\* — post-incident investigation of file systems, memory, logs, and network traffic

\- \*\*Incident Response\*\* — structured four-phase process: Preparation → Detection \& Analysis → Containment \& Recovery → Post-Incident Review

\### Malware Analysis

&#x20;

Examining malicious software to understand its behaviour:

\- \*\*Static analysis\*\* — inspecting code without running it

\- \*\*Dynamic analysis\*\* — running malware in a sandbox to observe what it actually does

\### SIEM

&#x20;

Security Information and Event Management tools centralise log data from across an organisation for real-time monitoring and alerting. Used by SOC analysts to triage and investigate suspicious events.

&#x20;

\---

&#x20;

\## Tools Introduced

&#x20;

\- SIEM (Security Information and Event Management)

\- Threat Intelligence platforms

\- Simulated SOC alert triage environment

\---

&#x20;

\## Practical Task — SIEM Simulation

&#x20;

The room included a hands-on scenario inside a simulated SIEM environment:

&#x20;

1\. \*\*Alert\*\* — Suspicious login flagged from an unknown IP at 3:00 AM

2\. \*\*Investigation\*\* — IP checked against a threat intel platform; confirmed malicious

3\. \*\*Escalation\*\* — Finding escalated to the SOC lead for approval

4\. \*\*Remediation\*\* — Firewall rule created to block all inbound traffic from the malicious IP

5\. \*\*Flag\*\* — `THM{THREAT-BLOCKED}`

\---

&#x20;

\## Questions \& Answers

&#x20;

| Question | Answer |

|---|---|

| Which team focuses on defensive security? | Blue Team |

| What team monitors networks for malicious events? | Security Operations Center |

| What does DFIR stand for? | Digital Forensics and Incident Response |

| Which malware requires payment to restore file access? | Ransomware |

| SIEM simulation flag | `THM{THREAT-BLOCKED}` |

&#x20;

\---

&#x20;

\## What I Learned

&#x20;

This room gave me a solid grounding in how the defensive side of cybersecurity operates. Rather than finding vulnerabilities, the blue team's job is to prevent attacks and respond effectively when they happen. The SIEM simulation made alert triage feel tangible — seeing the full workflow from detection to firewall remediation was more useful than just reading about it. Understanding both sides (red and blue) gives a much clearer picture of how real security works end to end.

&#x20;

\---

&#x20;

\## Challenges

&#x20;

No major technical challenges. The focus was on understanding how the different subfields connect — SOC, threat intelligence, DFIR, and malware analysis all feed into each other in practice.

&#x20;

\---

&#x20;

\## Takeaways

&#x20;

\- Defensive security is just as technical and specialised as offensive security

\- A SOC analyst's job is as much about process and escalation as it is about tools

\- Threat intelligence is what makes defence proactive rather than reactive

\- DFIR is the forensic backbone of incident response — evidence-first thinking

\---

&#x20;

\## Next Steps

&#x20;

\- Continue with the Cybersecurity 101 pathway

\- Complete the Search Skills room

\- Begin exploring SOC analyst tools (Splunk, ELK) in more depth

