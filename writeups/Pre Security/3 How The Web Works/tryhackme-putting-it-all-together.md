TryHackMe — Putting It All Together

Platform: TryHackMe

Room: Putting It All Together

Difficulty: Easy

Category: Web Fundamentals

Date Completed: April 2026

Status: ✅ Completed



Overview

Completed the Putting It All Together room on TryHackMe. This is the final room in the How The Web Works module, consolidating everything covered across DNS in Detail, HTTP in Detail, and How Websites Work into one cohesive picture of what happens when you load a website. Also introduces additional infrastructure components like load balancers, CDNs, WAFs, and web servers.



Objectives



Consolidate knowledge of DNS, HTTP, and web fundamentals

Understand the full journey of a web request from browser to server and back

Learn about additional infrastructure components that sit between clients and servers

Understand how web servers handle multiple sites and serve dynamic content





Key Concepts

The Full Web Request Journey

When you type a URL into a browser, the following happens in order:



DNS lookup — the domain is resolved to an IP address via recursive → root → TLD → authoritative DNS servers

TCP connection — the browser establishes a connection to the web server's IP

HTTP request — the browser sends an HTTP GET request for the page

Server processing — the web server handles the request, potentially querying a database for dynamic content

HTTP response — the server returns the HTML, CSS, and JS to the browser

Rendering — the browser renders the page for the user





Additional Infrastructure Components

CDN (Content Delivery Network)

Used to host static files (images, CSS, JS) across multiple servers globally. Speeds up page load times by serving content from the server closest to the user.

Load Balancer

Distributes incoming traffic across multiple servers to prevent any single server from being overwhelmed. Performs health checks to ensure servers are still alive and responsive before routing traffic to them.

WAF (Web Application Firewall)

Sits between the client and the web server to inspect incoming requests and block malicious traffic. Used to help protect against web attacks such as SQLi, XSS, and DDoS.

Web Server

Software (e.g. Apache, Nginx) that receives HTTP requests and returns responses. Uses Virtual Hosts to serve multiple websites from the same server by matching the Host header to the correct site configuration.



Static vs Dynamic Content



Static content — files that don't change (images, CSS, plain HTML files)

Dynamic content — content generated on the fly by the server (e.g. a personalised dashboard, search results from a database)



The client (browser) never sees the backend code that generates dynamic content — only the resulting HTML is returned.



Questions \& Answers

QuestionAnswerWhat can be used to host static files and speed up a client's visit?CDNWhat does a load balancer perform to check a host is still alive?health checkWhat can be used to help against the hacking of a website?WAFWhat does web server software use to host multiple sites?Virtual HostsWhat is the name for the type of content that can change?DynamicDoes the client see the backend code?Nay



What I Learned

This room tied everything together in a way that made the full picture clear. Before this module, I had a surface-level understanding of how the web worked — now I understand the complete chain: DNS resolution, TCP connection, HTTP request/response, server-side processing, and browser rendering. The addition of CDNs, load balancers, and WAFs was useful context for understanding real-world infrastructure, and relevant to pentesting — a WAF is often the first thing you have to work around when assessing a web application.



Challenges

No technical challenges — this is a consolidation room. The value is in connecting all the previous concepts rather than introducing new ones.



Takeaways



Every web page load involves DNS, TCP, HTTP, and rendering — all working together

CDNs, load balancers, and WAFs are common in production environments and affect how pentesting is approached

Web servers use Virtual Hosts to serve multiple sites — relevant for subdomain enumeration in pentesting

Dynamic content is generated server-side — the client never sees the backend code

WAFs are a real obstacle in web app pentesting and require evasion techniques





Module Completed

✅ How The Web Works module fully completed:



DNS in Detail

HTTP in Detail

How Websites Work

Putting It All Together





Next Steps



Begin Linux Fundamentals Part 1

Start exploring web application pentesting tools (Burp Suite, FFUF)

Look into WAF evasion techniques for future pentesting work

