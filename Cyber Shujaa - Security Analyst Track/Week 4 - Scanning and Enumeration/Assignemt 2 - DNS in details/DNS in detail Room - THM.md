# DNS in detail Room - THM
## Introduction 
In this room we explore DNS (Domain Name System) in detail. DNS maps domain name into IP addresses of respective web servers.  

The room covers DNS hierarchy, Record Types and how DNS works in making a request.  The room contains a simple lab that demonstrates how to make enumerate DNS using a tool called nslookup. 

## Walkthrough 
## Section: What is DNS? 
Question: What does DNS stand for? <br>
Answer: **Domain Name System** <br>

## Section: Domain Hierarchy 
Question: What is the maximum length of a subdomain? <br>
Answer: **63** <br>

Question: Which of the following characters cannot be used in a subdomain ( 3 b _ - )? <br>
Answer: **_** <br>

Question: What is the maximum length of a domain name? <br>
Answer: **253** <br>

Question: What type of TLD is .co.uk? <br>
Answer: **ccTLD** <br>

## Section: Record Types 
Question: What type of record would be used to advise where to send email? <br>
Answer: **MX** <br>

Question: What type of record handles IPv6 addresses? <br>
Answer: **AAAA** <br>

## Section: Making a Request 
Question: What field specifies how long a DNS record should be cached for? <br>
Answer: **TTL**  <br>

Question: What type of DNS Server is usually provided by your ISP? <br>
Answer: **recursive** <br>

Question: What type of server holds all the records for a domain? <br>
Answer: **authoritative** <br>

## Section: Practical 
Question: What is the CNAME of shop.website.thm? <br>
Answer: **shops.myshopify.com** <br>
<img width="1914" height="1008" alt="1 1 shop cname" src="https://github.com/user-attachments/assets/51e12121-3373-424d-88a2-25168e47bf3b" />

Question: What is the value of the TXT record of website.thm? <br>
Answer: **THM{7012BBA60997F35A9516C2E16D2944FF}** <br>
<img width="1920" height="1003" alt="1 2 website txt values" src="https://github.com/user-attachments/assets/363ce13b-d07b-4f83-89c8-defdb57d0a4d" />

Question: What is the numerical priority value for the MX record? <br>
Answer: **30** <br>
<img width="1920" height="1000" alt="1 3 mx record priority values" src="https://github.com/user-attachments/assets/2ef273b7-8eb8-4ca5-91fd-989d3a1ddbf2" />

Question: What is the IP address for the A record of www.website.thm? <br>
Answer: **10.10.10.10** <br>
<img width="1919" height="1005" alt="1 4 www A record IP address" src="https://github.com/user-attachments/assets/487a7aff-150d-43bf-8147-428ffe84b394" />

## Module Completion 
TryHackMe Profile Link: https://tryhackme.com/p/kl45h 

## Conclusion 
DNS is an important protocol as it saves us from having to remember each and web server’s IP address. All we need to know is the domain or subdomain of a web server and DNS will work out the rest for us behind the scenes. 

DNS can also be enumerated by ethical hackers to gather more information during a penetration testing exercise to try penetrate a poorly configured domain name server. 
