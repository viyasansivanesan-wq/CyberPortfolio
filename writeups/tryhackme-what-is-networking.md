TryHackMe — What is Networking?
Platform: TryHackMe
Room: What is Networking?
Difficulty: Easy
Category: Networking / Fundamentals
Date Completed: April 2026
Status: ✅ Completed

Overview
Completed the What is Networking? room on TryHackMe. This room introduces the core concepts of computer networking — what networks are, how the internet works, how devices are identified, and how tools like ping are used to test connectivity. Part of the Pre-Security learning path.

Objectives

Understand what a network is and why they exist
Learn how the internet works at a high level
Understand IP addresses (IPv4 and IPv6) and MAC addresses
Learn what MAC spoofing is and why it's a security concern
Use ping/ICMP to test connectivity


Key Concepts
What is a Network?
A network is simply devices connected together to share resources and communicate. Networks can be private (e.g. a home or office LAN) or public (the internet). The internet is essentially a massive network of networks.
The internet originated from the ARPANET project in the late 1960s, funded by the US Department of Defense. The modern internet as we know it wasn't established until 1989 when Tim Berners-Lee created the World Wide Web.

Identifying Devices — IP Addresses
An IP address (Internet Protocol address) identifies a device on a network. IPv4 addresses are made up of four octets (e.g. 192.168.1.1), each ranging from 0–255, giving ~4.29 billion possible addresses.

Private IP — used within a local network (e.g. 192.168.1.77)
Public IP — used to identify a device on the internet, assigned by an ISP

Due to IPv4 address exhaustion, IPv6 was introduced — supporting up to 2^128 addresses (340 trillion+) and being more efficient overall.

Identifying Devices — MAC Addresses
A MAC address (Media Access Control) is a unique 12-character hexadecimal identifier assigned to a device's network interface at the factory. Example: a4:c3:f0:85:ac:2d

First 6 characters = vendor/manufacturer identifier
Last 6 characters = unique device identifier

Unlike IP addresses, MAC addresses are hardware-level identifiers — but they can be spoofed.

MAC Spoofing
MAC spoofing is when a device pretends to be another by faking its MAC address. This can bypass poorly implemented security controls that trust devices based on MAC address alone — such as guest Wi-Fi networks that only allow pre-approved devices.
Practical scenario: In the interactive lab, Bob's packets were being blocked by the router and dropped (bin). Alice had an authorised MAC address and could access the network freely. By changing Bob's MAC address to match Alice's (00:12:32:2F:33:39), Bob's traffic was treated as authorised and passed through.
Flag: THM{YOU_GOT_ON_TRYHACKME}

Ping (ICMP)
Ping uses ICMP (Internet Control Message Protocol) to test the connectivity and performance of a connection between two devices. Basic syntax:
ping <IP address or URL>
Ping sends ICMP packets to the target and reports whether they were received, how many were lost, and the average response time. Available on both Windows and Linux by default.
Practical task: Pinged 8.8.8.8 (Google's DNS server) on the deployed site. After 4 packets the terminal returned the flag THM{I_PINGED_THE_SERVER}.

Questions & Answers
QuestionAnswerWhat is the key term for devices connected together?NetworkWho invented the World Wide Web?Tim Berners-LeeHow many octets does an IPv4 address have?4What does the term MAC stand for?Media Access ControlMAC spoofing flagTHM{YOU_GOT_ON_TRYHACKME}Ping the server flagTHM{I_PINGED_THE_SERVER}

What I Learned
This room gave me a solid grounding in how devices are identified and communicate on networks. The MAC spoofing lab was particularly useful — seeing the practical security implication of trusting MAC addresses made the concept stick. It also reinforced why defence-in-depth matters: relying on a single control like MAC filtering is easily bypassed. The distinction between private and public IPs, and why IPv6 exists, filled in some gaps I had from prior experience.

Challenges
The MAC spoofing flag format wasn't immediately obvious — the input box used underscores as placeholders and the flag itself needed to be derived from the simulation rather than the MAC address directly.

Takeaways

Networks are simply connected devices — the internet is a network of networks
Devices have two identifiers: IP (logical, changeable) and MAC (hardware, but spoofable)
MAC address filtering is a weak security control — easily bypassed via spoofing
Ping/ICMP is a fundamental tool for testing connectivity and diagnosing network issues
IPv6 exists because IPv4's ~4.29 billion addresses are running out


Tools Used

Ping / ICMP
Interactive MAC spoofing simulation (browser-based lab)


Next Steps

Continue with Intro to LAN
Build on IP addressing knowledge with subnetting
Explore how ARP works in relation to MAC addresses