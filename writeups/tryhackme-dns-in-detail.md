TryHackMe — DNS in Detail

Platform: TryHackMe

Room: DNS in Detail

Difficulty: Easy

Category: Networking / Fundamentals

Date Completed: April 2026

Status: ✅ Completed



Overview

Completed the DNS in Detail room on TryHackMe. This room covers how the Domain Name System works — from what DNS is and why it exists, to domain structure, record types, and the full resolution process. Includes a practical task querying real DNS records using a browser-based tool.



Objectives



Understand what DNS is and why it's needed

Learn the structure of domain names (TLDs, subdomains, limits)

Understand the different types of DNS records

Learn how DNS requests are resolved step by step

Query DNS records practically using a simulated tool





Key Concepts

What is DNS?

DNS (Domain Name System) translates human-readable domain names (e.g. tryhackme.com) into IP addresses (e.g. 104.26.10.229) that computers use to communicate. Without DNS, you'd need to remember the IP address of every website you visit.



Domain Structure

A domain name is broken into hierarchical parts read right to left:



TLD (Top Level Domain) — the rightmost part, e.g. .com, .org, .co.uk



gTLD (generic TLD) — .com, .edu, .gov etc.

ccTLD (country code TLD) — .co.uk, .de, .fr etc.





Second Level Domain — the main domain name, e.g. tryhackme in tryhackme.com

Subdomain — prefix to the domain, e.g. admin in admin.tryhackme.com



Limits:



Maximum subdomain length: 63 characters

Maximum domain name length: 253 characters

Subdomains can only use letters, numbers, and hyphens — underscores (\_) are not allowed





DNS Record Types

RecordPurposeAMaps a domain to an IPv4 addressAAAAMaps a domain to an IPv6 addressCNAMEAliases one domain to another domainMXDirects email to the correct mail server (includes priority value)TXTStores arbitrary text — used for verification, SPF records, etc.



DNS Resolution Process

When you request a domain, the following happens:



Local cache — browser checks if it already has the answer cached

Recursive DNS server — usually provided by your ISP; checks its own cache, then queries further

Root DNS servers — directs the query to the correct TLD server

TLD DNS server — holds records for all domains under that TLD, directs to the authoritative server

Authoritative DNS server — holds the actual DNS records for the domain; returns the answer



Each record has a TTL (Time To Live) value — this determines how long the result is cached before a fresh lookup is needed.



Practical Task — DNS Query Tool

Used the browser-based DNS query tool to look up records for website.thm:



Queried CNAME for shop.website.thm → shops.myshopify.com

Queried TXT record for website.thm → THM{7012BBA60997F35A9516C2E16D2944FF}

Queried MX record priority for website.thm → 30

Queried A record for www.website.thm → 10.10.10.10



Flag: THM{7012BBA60997F35A9516C2E16D2944FF}



Questions \& Answers

QuestionAnswerWhat does DNS stand for?Domain Name SystemWhat is the maximum length of a subdomain?63Which character cannot be used in a subdomain?\_What is the maximum length of a domain name?253What type of TLD is .co.uk?ccTLDWhat type of record is used to advise where to send email?MXWhat type of record handles IPv6 addresses?AAAAWhat field specifies how long a DNS record should be cached?TTLWhat type of DNS server is usually provided by your ISP?RecursiveWhat type of server holds all the records for a domain?AuthoritativeWhat is the CNAME of shop.website.thm?shops.myshopify.comWhat is the TXT record value for website.thm?THM{7012BBA60997F35A9516C2E16D2944FF}What is the MX record priority value?30What is the A record IP for www.website.thm?10.10.10.10



What I Learned

DNS is one of those protocols that runs silently behind everything — this room made the full resolution chain click properly. I hadn't fully understood the distinction between recursive, root, TLD, and authoritative servers before. The practical task of querying different record types reinforced how each one serves a different purpose — MX for email, CNAME for aliasing, TXT for verification, AAAA for IPv6. TTL is also relevant from a security perspective — a low TTL can be used in DNS-based attacks to rapidly redirect traffic.



Challenges

No major technical challenges. The DNS query tool was straightforward and the room walked through the resolution process clearly.



Takeaways



DNS translates domain names to IPs — it's the phonebook of the internet

Domain names have strict length and character limits

Different record types serve different purposes — knowing them is essential for both networking and pentesting

The resolution process involves multiple server types: recursive → root → TLD → authoritative

TTL controls caching — relevant for both performance and security





Tools Used



Browser-based DNS query simulation tool (TryHackMe lab)

nslookup / dig (introduced conceptually for real-world use)





Next Steps



Continue with HTTP in Detail

Explore DNS enumeration tools (e.g. dig, nslookup, dnsx)

Look into DNS-based attacks (DNS spoofing, cache poisoning)

