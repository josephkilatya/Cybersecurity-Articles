# MITRE Room Report 
## Introduction 
This MITRE Room on TryHackMe platform is an educative room that introduces the learner to the MITRE security framework. A statement from MITRE Corporation website: "At MITRE, we solve problems for a safer world. Through our federally funded R&D centers and public-private partnerships, we work across government to tackle challenges to the safety, stability, and well-being of our nation." The MITRE projects are a great point perform Cyber Threat Intelligence for threat defence, detection and emulation. 

The various frameworks covered include: 
- ATT&CK® (Adversarial Tactics, Techniques, and Common Knowledge) Framework
- CAR (Cyber Analytics Repository) Knowledge Base
- ENGAGE (sorry, not a fancy acronym)
- D3FEND (Detection, Denial, and Disruption Framework Empowering Network Defense)
- AEP (ATT&CK Emulation Plans)
   
## Walkthrough 
## Section: ATT&CK® Framework 
Question: Besides Blue teamers, who else will use the ATT&CK Matrix? (Red Teamers, Purpe Teamers, SOC Managers?) 
Answer: Red Teamers 

Question: What is the ID for this technique? 
Answer: T1566 

Question: Based on this technique, what mitigation covers identifying social 
engineering techniques? 

Answer: User Training 
Question: What are the data sources for Detection? (format: source1,source2,source3 with no spaces after commas) 
Answer: Application Log,File,Network Traffic 

Question: What groups have used spear-phishing in their campaigns? (format: group1,group2) 
Answer: Axiom,GOLD SOUTHFIELD 

Question: Based on the information for the first group, what are their associated groups? 
Answer: Group 72 

Question: What software is associated with this group that lists phishing as a technique? 
Answer: Hikit 

Question: What is the description for this software? 
Answer:   Hikit is malware that has been used by Axiom for late-stage persistence and exfiltration after the initial compromise. 

Question: This group overlaps (slightly) with which other group? 
Answer: Winnti Group 

Question: How many techniques are attributed to this group? 
Answer: 15 

## Section: CAR Knowledge Base 
Question: What tactic has an ID of TA0003? 
Answer: Splunk Search 

Question: What is the name of the library that is a collection of Zeek (BRO) scripts? 
Answer: Persistence 

Question: What is the name of the technique for running executables with the same hash and different names? 
Answer: BZAR 

Question: Examine CAR-2013-05-004, besides Implementations, what additional information is provided to analysts to ensure coverage for this technique? 
Answer: Masquerading 

## Section: MITRE Engage 
Question: Under Prepare, what is ID SAC0002? 
Answer: PERSONA CREATION 

Question: What is the name of the resource to aid you with the engagement activity from the previous question? 
Answer: person profile worksheet 

Question: Which engagement activity baits a specific response from the adversary? 
Answer: Lures 

Question: What is the definition of Threat Model? 
Answer: A risk assessment that models organizational strengths and weaknesses 

## Section: MITRE D3FEND 
Question: What is the first MITRE ATT&CK technique listed in the ATT&CK Lookup dropdown? 
Answer: data obfuscation 

Question: In D3FEND Inferred Relationships, what does the ATT&CK technique from the previous question produce? 
Answer: Outbound internet traffic network 

## Section: ATT&CK® Emulation Plans 
Question: In Phase 1 for the APT3 Emulation Plan, what is listed first? 
Answer: c2 setup 

Question: Under Persistence, what binary was replaced with cmd.exe? 
Answer: sethc.exe 

Question: Examining APT29, what  C2 frameworks are listed in Scenario 1 Infrastructure? (format: tool1,tool2) 
Answer: pupy,metasploit framework 

Question: What C2 framework is listed in Scenario 2 Infrastructure? 
Answer: poshc2 

Question: Examine the emulation plan for Sandworm. What webshell is used for Scenario 1? Check MITRE ATT&CK for the Software ID for the webshell. What is the id? (format: webshell,id) 
Answer: P.A.S.,S0598 

## Section: ATT&CK® and Threat Intelligence 
Question: What is a group that targets your sector who has been in operation since at least 2013? 
Answer: APT33 

Question: As your organization is migrating to the cloud, is there anything attributed to this APT group that you should focus on? If so, what is it? 
Answer: cloud accounts 

Question: What tool is associated with the technique from the previous question? 
Answer: Ruler 

Question: Referring to the technique from question 2, what mitigation method suggests using SMS messages as an alternative for its implementation? 
Answer: abnormal or malicious behaviour 

Question: What platforms does the technique from question #2 affect? 
Answer: Azure AD, Google Workspace, IaaS, Office 365, SaaS 

## Conclusion 
The MITRE projects are really useful to the cyber security community. The information on these platforms can be used by all the cyber security folks from blue teamers to red teamers.  
I had learned this module about a year but after going through it once again I’m convinced that the MITRE projects are invaluable to the cyber security community. I am now intrigued to go deeper into these projects for better understanding and application in my future career as security analyst. 
