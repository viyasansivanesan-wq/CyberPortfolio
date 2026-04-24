TryHackMe — How Websites Work

Platform: TryHackMe

Room: How Websites Work

Difficulty: Easy

Category: Web Fundamentals

Date Completed: April 2026

Status: ✅ Completed



Overview

Completed the How Websites Work room on TryHackMe. This room covers the fundamentals of how websites are built and delivered — HTML structure, JavaScript interactivity, sensitive data exposure in source code, and HTML injection. Includes four hands-on practical tasks using a browser-based HTML/JS editor and live vulnerable sites.



Objectives



Understand how websites are structured using HTML

Learn how JavaScript adds interactivity to web pages

Understand what sensitive data exposure is and how to find it in source code

Learn what HTML injection is and how unsanitised input leads to it





Key Concepts

HTML

HTML (HyperText Markup Language) is the language used to build the structure of web pages. It uses tags to define elements:



<head> — contains page metadata (title, scripts, styles)

<body> — contains the visible content of the page

<h1> — defines a large heading

<p> — defines a paragraph

<img src="..."> — embeds an image

<button> — creates a clickable button



Tags can have attributes that modify their behaviour, e.g. class, id, src. The id attribute is unique per element and is used by JavaScript to target specific elements.



JavaScript

JavaScript (JS) makes web pages interactive and dynamic. It can update page content in real time without reloading. JS is added via <script> tags or loaded from external files.

Key example from the room:

javascriptdocument.getElementById("demo").innerHTML = "Hack the Planet";

This finds the element with id demo and changes its content. Events like onclick can trigger JS functions when a user interacts with an element.



Sensitive Data Exposure

Sensitive data exposure occurs when a website fails to remove or protect sensitive information from its frontend source code. Developers sometimes leave credentials, hidden links, or internal comments in HTML/JS that anyone can view with "View Page Source".

Example from the room: A <!-- TODO: remove test credentials admin:password123 --> comment left in the HTML source exposed login credentials.

Password found in source code: testpasswd

This is a real-world vulnerability — always check page source when assessing a web application.



HTML Injection

HTML injection occurs when a website takes user input and renders it directly on the page without sanitising it first. If a user can inject their own HTML tags, they can manipulate what other users see — including malicious links, fake login forms, or redirects.

Example from the room: A form passed user input directly into a JavaScript function which wrote it to the page with innerHTML. By inputting <a href="http://hacker.com">Click me</a>, a malicious link was rendered on the page.

The fix is to always sanitise user input — strip or escape HTML tags before using input in the DOM.

Flag: HTML\_INJ3CTION



Practical Tasks \& Flags

TaskActionFlag/AnswerHTML EditorRender provided HTML with cat imagesNo answer neededFix broken imageCorrect the broken <img> src attributeHTMLHEROAdd dog imageAdd <img src='img/dog-1.png'> on line 11DOGHTMLJavaScriptUse JS to change demo element to "Hack the Planet"JSISFUNSensitive Data ExposureFind password hidden in page source codetestpasswdHTML InjectionInject <a href="http://hacker.com">Click me</a>HTML\_INJ3CTION



Questions \& Answers

QuestionAnswerFix the broken image on the cat websiteHTMLHEROAdd a dog image on line 11DOGHTMLJS — change demo element to "Hack the Planet"JSISFUNWhat is the password hidden in the source code?testpasswdHTML injection flagHTML\_INJ3CTION



What I Learned

This room connected the dots between how websites are built and how they can be attacked. Sensitive data exposure is surprisingly common in real applications — developers leaving credentials or debug info in comments is a genuine vulnerability that's easy to miss during development. HTML injection was a good introduction to why input sanitisation matters — if you trust user input and render it directly, you hand control of the page to whoever is typing. This is the foundation for understanding XSS (Cross-Site Scripting), which takes injection much further.



Challenges

The HTML editor task required understanding which line to add the <img> tag on — reading the existing code structure carefully was necessary to get the right answer.



Takeaways



Websites are built from HTML (structure), CSS (style), and JavaScript (behaviour)

Always check page source when assessing a web app — credentials and hidden links are commonly left there

Never trust user input — sanitise everything before rendering it in the DOM

HTML injection is a stepping stone to understanding XSS

innerHTML is dangerous when used with unsanitised input





Tools Used



Browser-based HTML/JS editor (TryHackMe lab)

View Page Source (browser built-in)





Next Steps



Continue with Linux Fundamentals

Learn about Cross-Site Scripting (XSS) in depth

Explore OWASP Top 10 — Injection and Sensitive Data Exposure categories

