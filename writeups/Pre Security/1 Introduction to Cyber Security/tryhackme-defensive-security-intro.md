TryHackMe — Defensive Security Intro

Platform: TryHackMe

Room: Defensive Security Intro

Difficulty: Easy

Category: Blue Team / Fundamentals

Date Completed: April 2026

Status: ✅ Completed

Overview

Completed the Defensive Security Intro room on TryHackMe. This room introduced the core concepts of defensive security, the blue team mindset, and the tools and processes used to protect systems from attacks. It covers four key subfields — SOC, Threat Intelligence, DFIR, and Malware Analysis — and ends with a hands-on SIEM simulation.

Objectives

Understand what defensive security is and how it differs from offensive security

Learn about the role of a Security Operations Center (SOC)

Get introduced to Digital Forensics and Incident Response (DFIR)

Understand threat intelligence and malware analysis at a conceptual level

Complete a simulated SIEM alert triage scenario



Key Concepts

Defensive Security vs Offensive Security

Where offensive security focuses on finding and exploiting vulnerabilities, defensive security focuses on preventing intrusions and detecting/responding to them when they occur. Blue teamers are the defenders.


Security Operations Center (SOC)

A centralised team that monitors networks and systems 24/7 for malicious activity. Key responsibilities include vulnerability management, policy enforcement, detecting unauthorised access, and responding to network intrusions.


Threat Intelligence

The process of gathering and analysing information about adversaries to build proactive defences. Covers attacker TTPs (Tactics, Techniques, and Procedures) from internal logs, public feeds, and industry sharing groups.


Digital Forensics and Incident Response (DFIR)

Digital Forensics — post-incident investigation of file systems, memory, logs, and network traffic

Incident Response — structured four-phase process: Preparation → Detection & Analysis → Containment & Recovery → Post-Incident Review


Malware Analysis

Examining malicious software to understand its behaviour:

Static analysis — inspecting code without running it

Dynamic analysis — running malware in a sandbox to observe what it actually does


SIEM
Security Information and Event Management tools centralise log data from across an organisation for real-time monitoring and alerting. Used by SOC analysts to triage and investigate suspicious events.

Tools Introduced

SIEM (Security Information and Event Management)

Threat Intelligence platforms

Simulated SOC alert triage environment


Practical Task — SIEM Simulation

The room included a hands-on scenario inside a simulated SIEM environment:

Alert — Suspicious login flagged from an unknown IP at 3:00 AM

Investigation — IP checked against a threat intel platform; confirmed malicious

Escalation — Finding escalated to the SOC lead for approval

Remediation — Firewall rule created to block all inbound traffic from the malicious IP

Flag — THM{THREAT-BLOCKED}


Questions & Answers

Which team focuses on defensive security?Blue Team

What team monitors networks for malicious events?Security Operations Center

What does DFIR stand for?Digital Forensics and Incident Response

Which malware requires payment to restore file access?Ransomware

SIEM simulation flag: THM{THREAT-BLOCKED}


What I Learned

This room gave me a solid grounding in how the defensive side of cybersecurity operates. Rather than finding vulnerabilities, the blue team's job is to prevent attacks and respond effectively when they happen. The SIEM simulation made alert triage feel tangible — seeing the full workflow from detection to firewall remediation was more useful than just reading about it. Understanding both sides (red and blue) gives a much clearer picture of how real security works end to end.


Challenges

No major technical challenges. The focus was on understanding how the different subfields connect — SOC, threat intelligence, DFIR, and malware analysis all feed into each other in practice.


Takeaways

Defensive security is just as technical and specialised as offensive security

A SOC analyst's job is as much about process and escalation as it is about tools

Threat intelligence is what makes defence proactive rather than reactive

DFIR is the forensic backbone of incident response — evidence-first thinking


Next Steps

Continue with the Cybersecurity 101 pathway

Complete the Search Skills room

Begin exploring SOC analyst tools (Splunk, ELK) in more depth
