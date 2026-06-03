# Threat Intelligence Tools Room Report 
## Introduction 
Threat intelligence, the usage of threat intelligence platforms to gather already existing cyber threat intelligence during digital forensics and incidence response, and malware analysis. These platforms/tools are useful to cyber security professionals as they help save time during investigation of security incidents. 

In this room on TryHackMe platform, we are introduced to some of threat intelligence tools. They include: 
- Urlscan.io – Used to scan suspicious URL links in a sandboxed environment. 
- Abuse.ch – Used to gather intel on malware and URL links 
- PhishTool – Used to investigate phishing emails. 
- Cisco Talos Intelligence – Used to gather intel during email and malware analysis. 

The room includes 3 test emails addresses to practice phishing email analysis. 

## Walkthrough 
## Section: Room Outline 
Question: Read the description! Continue to the next task. 
Answer: No answer needed 

Section: Threat Intelligence Tools 
Question: I've read on Threat Intel and the classifications 

Answer: No answer needed 
Section: UrlScan.io 

Question: What was TryHackMe's Cisco Umbrella Rank based on the screenshot? 
Answer: 345612 

Question: How many domains did UrlScan.io identify on the screenshot? 
Answer: 13 

Question: What was the main domain registrar listed on the screenshot? 
Answer: NAMECHEAP INC  

Question: What was the main IP address identified for TryHackMe on the screenshot? 
Answer: 2606:4700:10::ac43:1b0a 

< answers for this section questions numbered in order of questions> 

## Section: Abuse.ch 
Question: The IOC 212.192.246.30:5555 is identified under which malware alias name 
on ThreatFox? 
Answer: Katana 

Question: Which malware is associated with the JA3 
Fingerprint 51c64c77e60f3980eea90869b68c58a8 on SSL Blacklist? 
Answer: Dridex 

Question: From the statistics page on URLHaus, what malware-hosting network has the 
ASN number AS14061?  
Answer: DIGITALOCEAN-ASN 

Question: Which country is the botnet IP address 178.134.47.166 associated with 
according to FeodoTracker? 
Answer: Georgia 

## Section: PhishTool 
**Scenario:**
You are a SOC Analyst and have been tasked to analyse a suspicious email, Email1.eml. 
To solve the task, open the email using Thunderbird on the attached VM, analyse it 
and answer the questions below. 
Question: What social media platform is the attacker trying to pose as in the email? 
Answer: LinkedIn 

Question: What is the senders email address? 
Answer: darkabutla@sc500.whpservers.com 

Question: What is the recipient's email address? 
Answer: cabbagecare@hotsmail.com 

<Question 1 to 3 answers> 

Question: What is the Originating IP address? Defang the IP address. 
Answer: 204[.]93[.]183[.]11 

<Sender IP which is also the originating IP> 
  
Question: How many hops did the email go through to get to the recipient? 
Answer: 4 

<Number of hops of the email from sender to receiver> 
  
## Section: Cisco Talos Intelligence 
Question: What is the listed domain of the IP address from the previous task? 
Answer: scnet.net 

<Ip address reverse domain name> 
  
Question: What is the customer name of the IP address? 
Answer: Complete Web Reviews 

(When I first did the lab, about a year ago, I was able to get the whois records. However 
this time round I could not get the records which was interesting) 

## Section: Scenario 1 
Scenario: You are a SOC Analyst. Several suspicious emails have been forwarded to you 
from other coworkers. You must obtain details from each email to triage the incidents 
reported.  
Task: Use the tools and knowledge discussed throughout this room (or use your 
resources) to help you analyze Email2.eml found on the VM attached to Task 5 and use 
the information to answer the questions. 
Question: According to Email2.eml, what is the recipient's email address? 
Answer: chris.lyons@supercarcenterdetroit.com 
<Recipient’s email address> 
Question: From Talos Intelligence, the attached file can also be identified by the 
Detection Alias that starts with an H... 
Answer: HIDDENEXT/Worm.Gen 
<Attached file Alias from Cisco Talos Intelligence platform> 
Section: Scenario 2 
Scenario: You are a SOC Analyst. Several suspicious emails have been forwarded to you 
from other coworkers. You must obtain details from each email to triage the incidents 
reported.  
Task: Use the tools and knowledge discussed throughout this room (or use your 
resources) to help you analyze Email3.eml found on the VM attached to Task 5 and use 
the information to answer the questions. 
Question: What is the name of the attachment on Email3.eml? 
Answer: Sales_Receipt 5606.xls 
<Attached file name> 
Question: What malware family is associated with the attachment on Email3.eml? 
Answer: Dridex 
<Malware family name> 
Section: Conclusion 
Question: Read the above and completed the room 
Answer: No answer needed 
Conclusion 
Threat Intelligence is one of my favourite areas in cyber security. It saves an analyst time 
during digital forensics and incident response, and malware analysis. 
I had gone through this room before but it was a good experience to relearn some 
aspects that I had not well grasped initially. 
Oh, I also have my own version of PhishTool project that I’m working on. However, 
unlike PhishTool, this tool is to be used offline. You can check out the project on my 
github account https://github.com/josephkilatya/MyProject. It is still under 
development and open for contributions.  
