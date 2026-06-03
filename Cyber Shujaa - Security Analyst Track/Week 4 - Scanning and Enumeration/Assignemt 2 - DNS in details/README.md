# DNS in detail Room
## Introduction 
In this room we explore DNS (Domain Name System) in detail. DNS maps domain name into IP addresses of respective web servers.  

The room covers DNS hierarchy, Record Types and how DNS works in making a request.  The room contains a simple lab that demonstrates how to make enumerate DNS using a tool called nslookup. 

## Walkthrough 
## Section: What is DNS? 
Question: What does DNS stand for? 
Answer: Domain Name System 

## Section: Domain Hierarchy 
Question: What is the maximum length of a subdomain? 
Answer: 63 

Question: Which of the following characters cannot be used in a subdomain ( 3 b _ - )? 
Answer: _ 

Question: What is the maximum length of a domain name? 
Answer: 253 

Question: What type of TLD is .co.uk? 
Answer: ccTLD 

## Section: Record Types 
Question: What type of record would be used to advise where to send email? 
Answer: MX 

Question: What type of record handles IPv6 addresses? 
Answer: AAAA 

## Section: Making a Request 
Question: What field specifies how long a DNS record should be cached for? 
Answer: TTL  

Question: What type of DNS Server is usually provided by your ISP? 
Answer: recursive 

Question: What type of server holds all the records for a domain? 
Answer: authoritative 

## Section: Practical 
Question: What is the CNAME of shop.website.thm? 
Answer: shops.myshopify.com 

Question: What is the value of the TXT record of website.thm? 
Answer: THM{7012BBA60997F35A9516C2E16D2944FF} 

Question: What is the numerical priority value for the MX record? 
Answer: 30 

Question: What is the IP address for the A record of www.website.thm? 
Answer: 10.10.10.10 

## Module Completion 
TryHackMe Profile Link: https://tryhackme.com/p/kl45h 

## Conclusion 
DNS is an important protocol as it saves us from having to remember each and web server’s IP address. All we need to know is the domain or subdomain of a web server and DNS will work out the rest for us behind the scenes. 

DNS can also be enumerated by ethical hackers to gather more information during a penetration testing exercise to try penetrate a poorly configured domain name server. 
