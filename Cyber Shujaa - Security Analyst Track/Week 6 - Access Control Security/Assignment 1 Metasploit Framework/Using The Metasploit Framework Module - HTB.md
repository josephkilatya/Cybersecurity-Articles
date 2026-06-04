# Using The Metasploit Framework Module - HTB
## Introduction 
Metasploit framework can be considered a swiss army knife for penetration testers. It is a handy tool during a penetration test.  
In this module we learn the following: 
- How the framework generally works 
- Introduction to MSFConsole 
- How to work with modules and payloads.  
- How to create and encode payloads for Firewall and IPS/IDS evasion. 
- Working with Meterpreter payload and how to interact with sessions and jobs. 
- Writing and Importing Metasploit Framework modules and more. 

With so much learned from the module, let’s delve into the labs covered. 

## Walkthrough 
## Section: Modules 
Question: Use the Metasploit-Framework to exploit the target with EternalRomance. Find the flag.txt file on Administrator's desktop and submit the contents as the answer. <br>
Answer: **HTB{MSF-W1nD0w5-3xPL01t4t10n}** <br>
<img width="974" height="233" alt="module flag" src="https://github.com/user-attachments/assets/d0f9d403-d7f1-443a-a87a-dd46a6f84b09" /><br>
_Administrator flag_
  
## Section: Payloads 
Question: Exploit the Apache Druid service and find the flag.txt file. Submit the contents of this file as the answer. <br>
Answer: **HTB{MSF_Expl01t4t10n}** <br>
<img width="819" height="512" alt="payloads flag" src="https://github.com/user-attachments/assets/e6a78ba4-b3f6-48e0-a4f6-8ad241229fe6" /><br>
_Apache Druid flag_ <br>
  
## Section: Sessions and Jobs 
Question: The target has a specific web application running that we can find by looking into the HTML source code. What is the name of that web application? <br>
Answer: **elFinder** <br>
<img width="1261" height="315" alt="sessions - web app name" src="https://github.com/user-attachments/assets/8a656f11-b962-4b3d-86a7-0541a8ffaef9" /><br>
_Running Web Application_
  
Question: Find the existing exploit in MSF and use it to get a shell on the target. What is the username of the user you obtained a shell with? <br>
Answer: **www-data** <br>
<img width="1261" height="315" alt="sessions - web app name" src="https://github.com/user-attachments/assets/7e0d3616-6240-44fd-ab19-7206cdaf096a" /><br>
_Connected username_ <br>
  
Question: The target system has an old version of Sudo running. Find the relevant exploit and get root access to the target system. Find the flag.txt file and submit the contents of it as the answer. <br>
Answer: **HTB{5e55ion5_4r3_sw33t}** <br>
<img width="866" height="196" alt="sessions - root flag" src="https://github.com/user-attachments/assets/599bdb0f-ddb8-4698-83d7-83e6d36d7b6e" /><br>
_Root user flag_ <br>
  
## Module completion 
Link: https://academy.hackthebox.com/achievement/1293352/39 

<Module completion screenshot> 
  
## Conclusion 
I love using Metasploit framework. The framework can save you time during a penetration test. According to me, it is a must have tool in a hacker’s arsenal. It is a tool worth knowing how to work with. 
