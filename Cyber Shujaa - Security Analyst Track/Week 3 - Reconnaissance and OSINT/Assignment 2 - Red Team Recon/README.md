# Red Team Recon Room - THM
## Introduction 
This room covers a vast of tools used by red teamers to perform reconnaissance during penetration testing. Knowing and understanding your target/client’s infrastructure is handy during penetration testing as it enables you to be tactical during the exercise. Tools covered in this room include; whois, dig, nslookup, host, traceroute/tracert. These tools can be used for network troubleshooting and performing reconnaissance during a penetration test. 

We are taught how to perform advanced searching using google docking and OSINT. Advanced searching can be used to collect much information about a client’s target network. This information is publicly available on the internet. 

The room introduces us to specialized search engines and online tools such as ViewDNS.info, Threat Intelligence Platform, Censys and shodan. These tools are powerful and can be useful during reconnaissance stage of a penetration test. 

A powerful reconnaissance framework, recon-ng, is also covered in the room. This tool combines most of the tools mentioned earlier into a framework. This can save our time from jumping from one tool to another. 

Another famous OSINT tool, Maltego, is also covered in the room. This tool is powerful and can come in handy during reconnaissance. 

## Walkthrough 
## Section: Introduction 
Task: We suggest you start the AttackBox and experiment with every command and tool we demonstrate. <br>
Answer: **No answer needed**<br>

## Section: Taxonomy of Reconnaissance 
Task: Ensure you have a clear understanding of the different types of recon activities before proceeding. <br>
Answer: **No answer needed** <br>

## Section: Built-in Tools 
Question:  When was thmredteam.com created (registered)? (YYYY-MM-DD) <br>
Answer: **2021-09-24** <br>

Question: To how many IPv4 addresses does clinic.thmredteam.com resolve? <br>
Answer: **2** <br>

Question: To how many IPv6 addresses does clinic.thmredteam.com resolve? <br>
Answer: **2** <br>

## Section: Advanced Searching 
Question: How would you search using Google for xls indexed for http://clinic.thmredteam.com? <br>
Answer: **filetype:xls site:clinic.thmredteam.com** <br>

Question: How would you search using Google for files with the word passwords for http://clinic.thmredteam.com? <br>
Answer: **passwords site:clinic.thmredteam.com** <br>

## Section: Specialized Search Engines 
Question: What is the shodan command to get your Internet-facing IP address? <br>
Answer: **shodan myip** <br>

## Section: Recon-ng 
Question: How do you start recon-ng with the workspace clinicredteam? <br>
Answer: **recon-ng -w clinicredteam** <br>

Question: How many modules with the name virustotal exist? <br>
Answer: **2** <br>

Question: There is a single module under hosts-domains. What is its name? <br>
Answer: **migrate_hosts** <br>

Question: censys_email_address is a module that “retrieves email addresses from the TLS certificates for a company.” Who is the author? <br>
Answer: **Censys Team** <br>

## Section: Maltego 
Question: What is the name of the transform that queries NIST’s National Vulnerability Database? <br>
Answer: **NIST NVD** <br>

Question: What is the name of the project that offers a transform based on ATT&CK? <br>
Answer: **MISP Project** <br>

## Module Completion 
TryHackMe profile link: https://tryhackme.com/p/kl45h 

## Conclusion 
This module has taught me a lot on reconnaissance and how crucial it is to perform thorough recon during a penetration test. It is phase I will invest my time in, in order to master it well.  

Key take away, the more information you have about your target/client network, the better you will plan for the next phases of the penetration test.  
