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

To identify THM's Cisco Umbrella Rank, we will have to give a closer look at the Summary section of the attached screenshot as show in image below. <br>
<img width="563" height="155" alt="image" src="https://github.com/user-attachments/assets/068c6e47-13c3-48bc-8af6-37880580cf2d" />

Question: How many domains did UrlScan.io identify on the screenshot? <br>
Answer: **13** <br>

The answer to this question can be found as in previous section, that is under Summary section of provided screenshot. <br>
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
Abuse.ch is a widely respected, non-profit cybersecurity project dedicated to tracking and fighting global malware, botnets, and cybercrime infrastructure. Founded in 2009 by researcher Roman Hüssy, it is operated out of the Bern University of Applied Sciences in Switzerland and partnered with the Spamhaus Project. It relies on a global network of security researchers to crowd-source and share live threat data completely free of charge.

Instead of running a single tool, Abuse.ch operates several specialized tracking platforms:
- MalwareBazaar: A crowdsourced repository for sharing and downloading known malware samples for analysis.
- URLhaus: A project that tracks malicious domains and URLs used to distribute malware.
- ThreatFox: A platform for sharing validated indicators of compromise (IOCs) with the community.
- Feodo Tracker: Focuses specifically on mapping and blocking botnet Command and Control (C2) server IP addresses.
- SSLBL: A project that tracks malicious SSL/TLS certificates and JA3 fingerprints linked to malware botnets.

With that in mind, let's dive into the questions in this section.

Question: The IOC 212.192.246.30:5555 is identified under which malware alias name on ThreatFox? <br>
Answer: **Katana** <br>

To get the answer to this question, we will first need to visit [ThreatFox](https://threatfox.abuse.ch/) directly or fromm Abuse.ch. Next Go to the ThreatFox Database to search for the given IOC. ThreatFox database has a search syntax which you can find by clicking "**Search Syntax**" just below the search bar. For the given IOC, we wiil use this syntaxt `ioc:<ioc>` which will be `ioc:212.192.246.30:5555`. The search gives a single hit which we can click to start the analysis.

<img width="1341" height="290" alt="image" src="https://github.com/user-attachments/assets/5316304b-e734-4326-90c3-f6c4bcb7d054" />
_Malware alias is **Katana** while oriniginal name is **Mirai**_

There is additional information provided which can also be useful intelligence. Feel free to look around the intelligence. 

Question: Which malware is associated with the JA3 Fingerprint 51c64c77e60f3980eea90869b68c58a8 on SSL Blacklist? <br>
Answer: **Dridex** <br>

Let's visit [SSL Blacklist](https://sslbl.abuse.ch/) directly from embedded link or from Abuse.ch. While on this page, click **view details** under **JA3 Fingerprints** as the given IOC is JA3 Fingerprint. You can learn more about JA3 Fingerprints [here](https://medium.com/@ggabrielhd/all-you-need-to-know-about-ja3-ja4-fingerprints-and-how-to-collect-them-8f189085b61f) Next, copy the given fingerprint and search from present SSL Blacklist page. From the search, you will get a single hit. Click to analyze. 

<img width="1180" height="380" alt="image" src="https://github.com/user-attachments/assets/d923bcb1-ec80-4b20-9256-71b7d1e50587" />
_The given JA3 Fingerprint is associated with **Dridex** Malware_

Question: From the statistics page on URLHaus, what malware-hosting network has the ASN number AS14061? <br>
Answer: **DIGITALOCEAN-ASN** <br>

Question: Which country is the botnet IP address 178.134.47.166 associated with according to FeodoTracker? <br>
Answer: Georgia <br>

To get the country associated with given botnet IP, first visit [FedoFracker](https://feodotracker.abuse.ch/) from embeded link or from Abuse.ch page. Next, click **view details** under **Botnet C&Cs** and proceed to search the given IP address from the search bar.

<img width="1183" height="286" alt="image" src="https://github.com/user-attachments/assets/aa8ada73-bafd-4de4-b7a3-8fe6e5685d95" />
_From the search results, we find the Alpha-2 code of the associated country as GE. Further online searches reveal the Alpha-2 code country to be Georgia_

## Section: PhishTool 
**Scenario:**
You are a SOC Analyst and have been tasked to analyse a suspicious email, Email1.eml. To solve the task, open the email using Thunderbird on the attached VM, analyse it and answer the questions below. 

For my case, I will be downloading the Task Files and solve the Task Challenges from my analysis environment. Once opened on Thunderbird, we are able to identify the information/answers in relation to the questions 1-3 for this section as shown in screenshot below.

<img width="958" height="952" alt="2 1 quiz 1-to-3" src="https://github.com/user-attachments/assets/2b9b5386-9b06-436d-a006-b7e97cfd6cc7" /> 

Question: What social media platform is the attacker trying to pose as in the email? <br>
Answer: **LinkedIn** <br>

Question: What is the senders email address? <br>
Answer: **darkabutla@sc500.whpservers.com** <br>

Question: What is the recipient's email address? <br>
Answer: **cabbagecare@hotsmail.com** <br>

<Question 1 to 3 answers> 

Question: What is the Originating IP address? Defang the IP address. <br>
Answer: 204[.]93[.]183[.]11 <br>

To answer this question and the following one, we will be viewing the raw .eml file. You can achieve this by using a Text Editor such as Notepad ++ or using build-in THunderbird feature to view the raw email. This is one of the advantages of using Thunderbird during phishing email analysis as we've got almost all features available under one application thus little tool switching.

Click **More** drop down menu in Thunderbird > Then click **View Source** to view the raw email file. The originating IP address is 204.93.183.11 as shown in screenshot below without defanging. <br>

<img width="958" height="472" alt="image" src="https://github.com/user-attachments/assets/7f90f44a-b27f-4678-8319-21f784fd9881" />

What is defanging? It the practice of modifying potentially harmful digital indicators—such as URLs, domains, and IP addresses—to make them non-clickable and harmless. It is considered a best practice and advised to always have it in mind when preparing CTI or Malware Analysis reports. You can learn more about defanging and refanging from this article [here](https://medium.com/@ranemirusG/defanging-and-refanging-of-ioc-4eaf7852a6ac). To achieve defanging, there is another useful tool that will us with this, [CyberChef](https://gchq.github.io/CyberChef/). If you are not familiar, you check out this walkthough that I recently published or use the THM CyberChef room [here](https://tryhackme.com/room/cyberchefbasics). Defanged IP from CyberChef is shown in screenshot below.

<img width="1540" height="304" alt="image" src="https://github.com/user-attachments/assets/b234438e-4aac-43ee-94f4-bc95ba8376ce" />
  
Question: How many hops did the email go through to get to the recipient? <br>
Answer: 4 <br>

This question is a little bit tricky when trying to do the hops count manually. I will leave this to you as homework. From my count I did get 4 total hops made by the email as shown in screenshot below.

<img width="961" height="409" alt="2 3 number of hopes" src="https://github.com/user-attachments/assets/5d81dfa5-c0b7-4198-9b63-b5a9da62b9e2" />
 <br>
  
## Section: Cisco Talos Intelligence 
Question: What is the listed domain of the IP address from the previous task? <br>
Answer: scnet.net <br>
  
Question: What is the customer name of the IP address? <br>
Answer: Complete Web Reviews <br>

(When I first did the lab, about a year ago, I was able to get the whois records. However this time round I could not get the records which was interesting) 

## Section: Scenario 1 
Scenario: You are a SOC Analyst. Several suspicious emails have been forwarded to you from other coworkers. You must obtain details from each email to triage the incidents reported. Task: Use the tools and knowledge discussed throughout this room (or use your resources) to help you analyze Email2.eml found on the VM attached to Task 5 and use the information to answer the questions. 

Question: According to Email2.eml, what is the recipient's email address? <br>
Answer: chris.lyons@supercarcenterdetroit.com <br>

To proceed with analysis, download the file .eml file and open it with your analysis tool of choice. I will be using Thunderbird. Once the .eml file is opened in Thunderbird, it is easy to identify the Recipient address under **To** as shown in screenshot below.

<img width="960" height="901" alt="4 1 recipient email address" src="https://github.com/user-attachments/assets/40b421b2-1fa5-4b73-9f85-2ff2fa58ee6d" />

Question: From Talos Intelligence, the attached file can also be identified by the Detection Alias that starts with an H... <br>
Answer: HIDDENEXT/Worm.Gen <br>

Extract the file attachment from previous question to save it in your local system. Calculate the hash value. If you are not familiar with calucate hash values, you can learn to do so from the THM room [Hashing Basics](https://tryhackme.com/room/hashingbasics) from embedded link.

Once you have the hash value, use Cisco Talo Intelligence plaform here to get CTI on the file attachment. Once the analysis is done, we identify the file is indeed malicious and is associted with the Alias **HIDDENEXT/Worm.Gen** which starts with an H.. as in the question.

<img width="1900" height="984" alt="4 1 Alias" src="https://github.com/user-attachments/assets/bfdc7ec5-40f7-4721-a0cf-2fd4ed5ac32e" />

## Section: Scenario 2 
Scenario: You are a SOC Analyst. Several suspicious emails have been forwarded to you from other coworkers. You must obtain details from each email to triage the incidents reported.  

Task: Use the tools and knowledge discussed throughout this room (or use your resources) to help you analyze Email3.eml found on the VM attached to Task 5 and use the information to answer the questions. 

Question: What is the name of the attachment on Email3.eml? <br>
Answer: Sales_Receipt 5606.xls <br>

For this task, you can use PhishTool or any other tool of choice. For my case I will be using Thundernird to open the given .eml file. From Thunderbird, you can be able to see other sorts of useful information such as the Sender Address, Email Subject and Message. The attached file appears at the bottom of the Thunderbird Windows as shown in screenshot below.

<img width="953" height="912" alt="5 1 attached file name" src="https://github.com/user-attachments/assets/d94b74d0-9688-44af-9cfa-f404839273f3" /> <br>
  
Question: What malware family is associated with the attachment on Email3.eml? <br>
Answer: Dridex <br>

From the previous question, we can export the attached file by Saving it to the local system. Next step would be uploading the file attachment to CTI platform or calculate the file hash value and use it to conduct you intel gathering. I will be uploading the file directly to [Malware Bazaar](https://bazaar.abuse.ch/upload/) which is also part of Abuse.ch tools.

Let's see how we can achieve that. First visit Malware Bazaar directly from this link or from Abuse.ch. Under **Share malware samples** click the **upload samples** button to upload the file attachment from the email in previous question. **Note**: To upload malware to Malware Bazaar, you will need to login. If you do not have an account you can proceed to create one. Once uploaded, Malware Bazaar calculates the hash value for you and perfoms the hash search on it's internal database. The analysis show the file attachment to be a malware if the Dridex Family as show in screenshot below.

<img width="1915" height="996" alt="5 2 malware family" src="https://github.com/user-attachments/assets/cf1f82f8-a43a-4e0b-82dc-a5e39a0e4919" />
  
## Section: Conclusion 
Question: Read the above and completed the room <br>
Answer: No answer needed <br>

## Conclusion 
Cyber Threat Intelligence is one of my favourite areas in cyber security. It saves an analyst time during incident response, and malware analysis. While this room cover a lot on threat intelligence, there are notable platforms that I do use to aid with CTI.

1. VirusTotal
2. AlienVault
3. Joe Sandbox
4. Any.Run
