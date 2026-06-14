# Threat Intelligence Tools - THM
## Introduction 
According to [CrowdStrike](https://www.crowdstrike.com/en-us/cybersecurity-101/threat-intelligence/), Threat intelligence refers to the collection, processing, and analysis of data to understand a threat actor’s motives, targets, and attack methods. It is also commonly referred to as Cyber Threat Intelligence (CTI).

This room brings an introductory guide to some of the worlds top CTI platforms which are as follows: 
- [Urlscan.io](https://urlscan.io/) – Free platform used to scan and analyse website or specific URL links in a sandboxed environment. 
- [Abuse.ch](https://abuse.ch/) – A free platform that tracks and shares data on malware, botnets, and malicious domains.
- [PhishTool](https://www.phishtool.com/) – Is a forensic phishing email analysis and incident response platform. 
- [Cisco Talos Intelligence](https://talosintelligence.com/) – Is a leading threat intelligence team providing expert security research, analysis, and incident response to protect users globally. It is a commercial service unlike some of the previously mentioned platforms.

With that brief introduction, let's keep it going.

## Walkthrough 
## Section: Room Outline 
Question: Read the description! Continue to the next task. <br>
Answer: **No answer needed** <br>

## Section: Threat Intelligence Tools 
Question: I've read on Threat Intel and the classifications <br>
Answer: **No answer needed** <br>

## Section: UrlScan.io 
To answer the questions in this section, we will not need to visit Urlscan but rather use the screenshot provided. 
Question: What was TryHackMe's Cisco Umbrella Rank based on the screenshot? <br>
Answer: **345612** <br>

To identify THM's Cisco Umbrella Rank, we will have to give a closer look at the Summary section of the attached screenshot as show in image below. <img width="563" height="155" alt="image" src="https://github.com/user-attachments/assets/068c6e47-13c3-48bc-8af6-37880580cf2d" />

Question: How many domains did UrlScan.io identify on the screenshot? <br>
Answer: **13** <br>

The answer to this question can be found as in previous section, that is under Summary section of provided screenshot.
<img width="1094" height="104" alt="image" src="https://github.com/user-attachments/assets/4067af13-aeca-4cfe-bbb4-2529394332ed" />

Question: What was the main domain registrar listed on the screenshot? <br>
Answer: **NAMECHEAP INC** <br>

From the attached screenshot, we are able to identify the registrar of the domain to be namecheap.
<img width="1095" height="137" alt="image" src="https://github.com/user-attachments/assets/c03d777c-ed0d-4bca-9f7f-f4652a4f611a" />

Question: What was the main IP address identified for TryHackMe on the screenshot? <br>
Answer: **2606:4700:10::ac43:1b0a** <br>

The IP address can be found just at the top of the attached screenshot of this section.

<img width="1391" height="152" alt="image" src="https://github.com/user-attachments/assets/a235f8cf-e863-40d7-99d3-ba7fdd99c9ea" />

## Section: Abuse.ch 
Question: The IOC 212.192.246.30:5555 is identified under which malware alias name on ThreatFox? <br>
Answer: Katana <br>

Question: Which malware is associated with the JA3 Fingerprint 51c64c77e60f3980eea90869b68c58a8 on SSL Blacklist? <br>
Answer: Dridex <br>

Question: From the statistics page on URLHaus, what malware-hosting network has the ASN number AS14061? <br>
Answer: DIGITALOCEAN-ASN <br>

Question: Which country is the botnet IP address 178.134.47.166 associated with according to FeodoTracker? <br>
Answer: Georgia <br>

## Section: PhishTool 
**Scenario:**
You are a SOC Analyst and have been tasked to analyse a suspicious email, Email1.eml. To solve the task, open the email using Thunderbird on the attached VM, analyse it and answer the questions below. 

Question: What social media platform is the attacker trying to pose as in the email? <br>
Answer: LinkedIn <br>

Question: What is the senders email address? <br>
Answer: darkabutla@sc500.whpservers.com <br>

Question: What is the recipient's email address? <br>
Answer: cabbagecare@hotsmail.com <br>

<Question 1 to 3 answers> 

Question: What is the Originating IP address? Defang the IP address. <br>
Answer: 204[.]93[.]183[.]11 <br>

<Sender IP which is also the originating IP> <br>
  
Question: How many hops did the email go through to get to the recipient? <br>
Answer: 4 <br>

<Number of hops of the email from sender to receiver> 
  
## Section: Cisco Talos Intelligence 
Question: What is the listed domain of the IP address from the previous task? <br>
Answer: scnet.net <br>

<Ip address reverse domain name> <br>
  
Question: What is the customer name of the IP address? <br>
Answer: Complete Web Reviews <br>

(When I first did the lab, about a year ago, I was able to get the whois records. However this time round I could not get the records which was interesting) 

## Section: Scenario 1 
Scenario: You are a SOC Analyst. Several suspicious emails have been forwarded to you from other coworkers. You must obtain details from each email to triage the incidents reported. Task: Use the tools and knowledge discussed throughout this room (or use your resources) to help you analyze Email2.eml found on the VM attached to Task 5 and use the information to answer the questions. 

Question: According to Email2.eml, what is the recipient's email address? <br>
Answer: chris.lyons@supercarcenterdetroit.com <br>

<Recipient’s email address> 

Question: From Talos Intelligence, the attached file can also be identified by the Detection Alias that starts with an H... <br>
Answer: HIDDENEXT/Worm.Gen <br>

<Attached file Alias from Cisco Talos Intelligence platform> <br>

Section: Scenario 2 
Scenario: You are a SOC Analyst. Several suspicious emails have been forwarded to you from other coworkers. You must obtain details from each email to triage the incidents reported.  

Task: Use the tools and knowledge discussed throughout this room (or use your resources) to help you analyze Email3.eml found on the VM attached to Task 5 and use the information to answer the questions. 

Question: What is the name of the attachment on Email3.eml? <br>
Answer: Sales_Receipt 5606.xls <br>

<Attached file name> <br>
  
Question: What malware family is associated with the attachment on Email3.eml? <br>
Answer: Dridex <br>

<Malware family name> 
  
## Section: Conclusion 
Question: Read the above and completed the room <br>
Answer: No answer needed <br>

Conclusion 

Threat Intelligence is one of my favourite areas in cyber security. It saves an analyst time during digital forensics and incident response, and malware analysis. I had gone through this room before but it was a good experience to relearn some aspects that I had not well grasped initially. 

Oh, I also have my own version of PhishTool project that I’m working on. However, unlike PhishTool, this tool is to be used offline. You can check out the project on my github account https://github.com/josephkilatya/MyProject. It is still under development and open for contributions.  
