# Introduction To Web Applications Report 
## Introduction 
This module was informative with so much to learn about web applications.  
The module covers web application from end technologies, that is HTML, CSS and 
Javascript. HTML stands for HyperText Markup Language, it is the skeleton of a web 
application. CSS, Cascading Style Sheet, is used to beautify the html content and make 
the web application more appealing in terms of looks. On the other hand, Javascript is 
used to make web applications more user interactive by adding more functionalities to its 
core. 

The module also covered common front-end vulnerabilities in web applications. This 
included HTML injection, Cross-Site Scripting (XSS) and Cross-Site Request Forgery 
(CSRF). These vulnerabilities are all based on improper user input sanitization. If exploited, 
they can pose a significant impact on the web applications. 

Finally, the module covers different web application back-end technologies such as the 
types of servers, databases and development frameworks. Web server technologies 
include Apache, Nginx, WAMP and more. For the databases we have structed databases 
(SQL) and non-structured databases (NoSQL). Development frameworks include Laravel 
for PHP, Express for Node.JS, Django for Python and Rails for Ruby. 

For common back-end vulnerabilities they include Broken Authentication/Access Control, 
Malicious File Upload, Command Injection and SQL Injection (SQLi). Another key thing 
discussed was Public vulnerablities, commonly referred to as CVE (Common Vulnerability 
and Exposure) and Identifying vulnerability score using CVSS (Common Vulnerability 
Scoring System) 

## Walkthrough 
## Section: HTML 
Question: What is the HTML tag used to show an image? 
Answer: <img> 

## Section: Cascading Style Sheets (CSS) 
Question: What is the CSS "property: value" used to make an HTML element's text aligned 
to the left? 
Answer: text-align: left; 

## Section: Sensitive Data Exposure 
Question: Check the above login form for exposed passwords. Submit the password as the 
answer. 
Answer: HiddenInPlainSight 

## Section: HTML Injection 
Question: What text would be displayed on the page if we use the following payload as our 
input: <a href="http://www.hackthebox.com">Click Me</a> 
Answer: Your name is Click Me 
The answer is revealed after injecting the payload.

## Section: Cross-Site Scripting (XSS) 
Question: Try to use XSS to get the cookie value in the above page 
Answer: XSSisFun 
The cookie is revealed after injecting the following XSS payload in the input field of the 
target website: #"><img src=/ onerror=alert(document.cookie)> 

## Section: Back End Servers 
Question: What operating system is 'WAMP' used with? 
Answer: Windows 

## Section: Web Servers 
Question: If a web server returns an HTTP code 201, what does it stand for? 
Answer: Created 

## Section: Databases 
Question: What type of database is Google's Firebase Database? 
Answer: NoSQL 

## Section: Development Frameworks & APIs 
Question: Use GET request '/index.php?id=0' to search for the name of the user with id 
number 1? 
Answer: superadmin 

## Section: Common Web Vulnerabilities 
Question: To which of the above categories does public vulnerability 'CVE-2014-6271' 
belongs to? 
Answer: Command Injection 

## Section: Public Vulnerabilities 
Question: What is the CVSS score of the public vulnerability CVE-2017-0144? 
Answer: 9.3 
More CVE Details: https://nvd.nist.gov/vuln/detail/cve-2017-0144 

## Module Completion 
Link: https://academy.hackthebox.com/achievement/1293352/75 

## Conclusion 
In conclusion, the knowledge covered in this module was informative. I believe this will 
help me when performing web application analysis to identify vulnerabilities. It is a growth 
point for my future career as a security analyst. 
