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
<img width="1920" height="1080" alt="1 1 basic tools" src="https://github.com/user-attachments/assets/4f60a02c-2459-48f6-a28c-3fd1afc737d6" />

Question: To how many IPv4 addresses does clinic.thmredteam.com resolve? <br>
Answer: **2** <br>
<img width="1913" height="1080" alt="1 2 basic tools" src="https://github.com/user-attachments/assets/8a245444-4a28-4de7-90fa-79105d974e0a" />

Question: To how many IPv6 addresses does clinic.thmredteam.com resolve? <br>
Answer: **2** <br>

## Section: Advanced Searching 
Question: How would you search using Google for xls indexed for http://clinic.thmredteam.com? <br>
Answer: **filetype:xls site:clinic.thmredteam.com** <br>
<img width="1020" height="327" alt="image" src="https://github.com/user-attachments/assets/3ac42e11-c6dc-4e7a-981e-bc919299d06f" />

Question: How would you search using Google for files with the word passwords for http://clinic.thmredteam.com? <br>
Answer: **passwords site:clinic.thmredteam.com** <br>
<img width="1031" height="317" alt="image" src="https://github.com/user-attachments/assets/c8dda70c-c951-4351-9176-479cc89345aa" />

## Section: Specialized Search Engines 
Question: What is the shodan command to get your Internet-facing IP address? <br>
Answer: **shodan myip** <br>

## Section: Recon-ng 
Question: How do you start recon-ng with the workspace clinicredteam? <br>
Answer: **recon-ng -w clinicredteam** <br>

Question: How many modules with the name virustotal exist? <br>
Answer: **2** <br>
<img width="1026" height="1006" alt="2 1 recon-ng" src="https://github.com/user-attachments/assets/3a547b0e-8c77-4a1c-8398-12985ed1784e" />

Question: There is a single module under hosts-domains. What is its name? <br>
Answer: **migrate_hosts** <br>
<img width="1022" height="1004" alt="2 2 recon-ng" src="https://github.com/user-attachments/assets/f510913b-bb50-499d-8078-bcc761c8716a" />

Question: censys_email_address is a module that “retrieves email addresses from the TLS certificates for a company.” Who is the author? <br>
Answer: **Censys Team** <br>
<img width="1025" height="1007" alt="2 3 recon-ng" src="https://github.com/user-attachments/assets/1a13f78a-7c78-420e-a7c7-deb2d85fdb09" />

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
