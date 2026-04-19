TryHackMe — Offensive Security Intro

Platform: TryHackMe

Room: Offensive Security Intro

Difficulty: Easy

Category: Offensive Security / Fundamentals

Date Completed: April 2026

Status: ✅ Completed



Overview

Completed the Offensive Security Intro room on TryHackMe. This room introduced the mindset and core concepts behind offensive security and ethical hacking, with a hands-on practical task involving directory enumeration and exploiting a fake banking web application.



Objectives



Understand what offensive security is and how it differs from defensive security

Learn how ethical hackers think and operate

Use Gobuster to discover hidden directories on a web server

Exploit an exposed admin portal to perform an unauthorised bank transfer





Key Concepts

Offensive vs Defensive Security

Offensive security simulates attacker behaviour to find vulnerabilities before malicious actors do. Rather than defending systems, offensive security professionals actively probe them for weaknesses. The mindset is: to beat a hacker, you need to think like one.

Ethical Hacking

Ethical hackers (penetration testers) perform the same actions as malicious attackers, but with explicit legal permission. The goal is to identify and report vulnerabilities so they can be fixed — not exploited for personal gain.

Directory Enumeration

Tools like Gobuster brute-force web servers using wordlists to discover hidden directories and files that aren't publicly linked. This is a core technique in web application penetration testing.

Security Through Obscurity

Hiding pages or admin portals by using non-obvious URLs is not a valid security control. If a path exists on a server, it can be found through enumeration — as demonstrated in this room.



Tools Used



Gobuster — directory and file brute-forcing tool

FakeBank — simulated vulnerable web application (TryHackMe lab)

Linux terminal





Practical Task — Hacking FakeBank

The room deployed a fake banking web application called FakeBank. The objective was to find a hidden admin portal and use it to transfer funds.

Steps:



Ran Gobuster against the FakeBank web server to enumerate hidden directories:



&#x20;  gobuster -u http://fakebank.thm -w wordlist.txt dir



Discovered the hidden /bank-transfer directory (not linked anywhere on the site)

Accessed the staff portal — found a deposit/transfer form requiring no authentication

Transferred funds to account 8881 using the exposed admin form

Returned to the account page — balance updated and flag revealed



Flag: BANK-HACKED



Questions \& Answers

QuestionAnswerWhich option represents simulating a hacker's actions to find vulnerabilities?Offensive SecurityWhat is the flag on your bank balance page after the transfer?BANK-HACKED



What I Learned

This room made the concept of offensive security tangible immediately. Running Gobuster and finding a hidden admin portal that required no authentication showed how real-world vulnerabilities work — an attacker doesn't need to break encryption if an unprotected admin page is just sitting there waiting to be found. It reinforced that obscurity is not security, and that even simple enumeration tools can have a massive impact.



Challenges

No major technical challenges. The Gobuster command syntax was straightforward and the lab environment was guided. The main learning curve was understanding what directory enumeration actually achieves in practice.



Takeaways



Offensive security is about finding vulnerabilities before attackers do — legally and ethically

Hidden directories are not secure — they can be discovered through automated enumeration

Exposed admin portals with no authentication are a critical vulnerability

This room is the foundation for penetration testing and ethical hacking





Next Steps



Continue with Linux fundamentals

Start learning Nmap for network enumeration

Explore more web application hacking techniques (Burp Suite, OWASP Top 10)

