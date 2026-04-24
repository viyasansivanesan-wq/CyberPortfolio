TryHackMe — HTTP in Detail

Platform: TryHackMe

Room: HTTP in Detail

Difficulty: Easy

Category: Networking / Web Fundamentals

Date Completed: April 2026

Status: ✅ Completed



Overview

Completed the HTTP in Detail room on TryHackMe. This room covers how HTTP and HTTPS work — the protocol that powers all web communication. Topics include request/response structure, HTTP methods, headers, status codes, and cookies. Ends with a practical task making real HTTP requests using a browser-based emulator.



Objectives



Understand what HTTP and HTTPS are and how they differ

Learn the structure of HTTP requests and responses

Understand HTTP methods (GET, POST, PUT, DELETE)

Learn key request and response headers

Understand what cookies are and how they work

Make HTTP requests practically using a request emulator





Key Concepts

What is HTTP/HTTPS?

HTTP (HyperText Transfer Protocol) is the set of rules used for communicating with web servers to transmit web page data (HTML, images, video etc.).

HTTPS (HyperText Transfer Protocol Secure) is the encrypted version of HTTP. Data is encrypted using TLS/SSL, preventing interception. When a site uses HTTPS incorrectly (e.g. invalid certificate), browsers warn the user — this is the issue flagged in the practical task.

Flag (invalid cert task): THM{INVALID\_HTTP\_CERT}



HTTP Requests and Responses

An HTTP request is sent by the client (browser) to the server and includes:



Method — what action to perform (GET, POST etc.)

Path — the page/resource being requested

HTTP version — e.g. HTTP/1.1

Headers — additional information sent with the request



An HTTP response from the server includes:



HTTP version and status code — e.g. HTTP/1.1 200 OK

Headers — metadata about the response

Body — the actual content (HTML, JSON etc.)





HTTP Methods

MethodPurposeGETRetrieve information/data from the serverPOSTSubmit data to create a new resourcePUTSubmit data to update an existing resourceDELETEDelete a resource from the server



HTTP Headers

Request headers (sent by the client):

HeaderPurposeHostTells the server which website is being requestedUser-AgentIdentifies the browser and version being usedContent-TypeDescribes the format of data being sent (e.g. JSON, form data)

Response headers (sent by the server):

HeaderPurposeContent-TypeTells the browser what type of data is being returnedContent-LengthTells the browser how much data to expectSet-CookieInstructs the browser to save a cookie



HTTP Status Codes

RangeMeaning100–199Informational200–299Success300–399Redirection400–499Client errors500–599Server errors

Common codes: 200 OK, 201 Created, 301 Moved Permanently, 302 Found, 400 Bad Request, 401 Unauthorised, 403 Forbidden, 404 Not Found, 500 Internal Server Error



Cookies

Cookies are small pieces of data stored in the browser by a web server via the Set-Cookie response header. They are sent back to the server with every subsequent request, allowing the server to remember state (e.g. login sessions). Cookies are a core part of web authentication and session management — and a key target in web application attacks.



Practical Task — HTTP Request Emulator

Used the browser-based HTTP request emulator to make real requests and retrieve flags:

RequestFlagGET /roomTHM{YOU'RE\_IN\_THE\_ROOM}GET /blog with id=1THM{YOU\_FOUND\_THE\_BLOG}DELETE /user/1THM{USER\_IS\_DELETED}PUT /user/2 with username=adminTHM{USER\_HAS\_UPDATED}POST /login with username=thm\&password=letmeinTHM{HTTP\_REQUEST\_MASTER}



Questions \& Answers

QuestionAnswerWhat does HTTP stand for?HyperText Transfer ProtocolWhat does the S in HTTPS stand for?SecureInvalid certificate challenge flagTHM{INVALID\_HTTP\_CERT}What HTTP protocol version is used in the example?HTTP/1.1What response header tells the browser how much data to expect?Content-LengthWhat method creates a new user account?POSTWhat method updates an email address?PUTWhat method removes an uploaded picture?DELETEWhat method views a news article?GETWhat header tells the server what browser is being used?User-AgentWhat header tells the browser what type of data is returned?Content-TypeWhat header tells the server which website is being requested?HostWhich header saves cookies to your computer?Set-CookieGET /room flagTHM{YOU'RE\_IN\_THE\_ROOM}GET /blog?id=1 flagTHM{YOU\_FOUND\_THE\_BLOG}DELETE /user/1 flagTHM{USER\_IS\_DELETED}PUT /user/2 username=admin flagTHM{USER\_HAS\_UPDATED}POST /login flagTHM{HTTP\_REQUEST\_MASTER}



What I Learned

This room filled in a lot of gaps about how web communication actually works under the hood. I knew what GET and POST were at a surface level, but understanding PUT and DELETE in context — and how they map to real actions like updating or removing a resource — made REST APIs click properly. The cookies section is directly relevant to web app pentesting: session hijacking, cookie theft, and CSRF all rely on how cookies behave. The Set-Cookie header and how browsers automatically send cookies back with every request is a key attack surface.



Challenges

No major technical challenges. The request emulator was intuitive once I understood how to set body and URI parameters using the gear icon.



Takeaways



HTTP is the foundation of all web communication — understanding it is essential for web app pentesting

HTTPS encrypts HTTP traffic — an invalid certificate is a real security warning, not just a browser quirk

HTTP methods map to CRUD operations: GET (read), POST (create), PUT (update), DELETE (delete)

Headers carry critical metadata — User-Agent, Host, Content-Type, Set-Cookie are all relevant to security

Cookies are the primary mechanism for maintaining sessions — and a major attack target





Tools Used



Browser-based HTTP request emulator (TryHackMe lab)

Burp Suite (introduced conceptually for real-world HTTP interception)





Next Steps



Continue with How Websites Work

Start using Burp Suite to intercept and modify real HTTP requests

Explore OWASP Top 10 web vulnerabilities

