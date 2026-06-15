# MITRE Room Report 
## Introduction 
This TryHackMe room introduces the MITRE security framework. According to MITRE's website: *"At MITRE, we solve problems for a safer world. Through our federally funded R&D centers and public-private partnerships, we work across government to tackle challenges to the safety, stability, and well-being of our nation."*

MITRE's frameworks are excellent for threat intelligence — whether you're doing threat defence, detection, or emulation. The room covers five key frameworks:

- ATT&CK® (Adversarial Tactics, Techniques, and Common Knowledge) Framework
- CAR (Cyber Analytics Repository) Knowledge Base
- ENGAGE (sorry, not a fancy acronym)
- D3FEND (Detection, Denial, and Disruption Framework Empowering Network Defense)
- AEP (ATT&CK Emulation Plans)
   
## Walkthrough 
## Task 1: ATT&CK® Framework
The ATT&CK (Adversarial Tactics, Techniques, and Common Knowledge) Framework provides a structured knowledge base of adversary TTPs. Use it to identify, prioritize, and track attacker behavior based on real-world observations.

**Question:** Besides Blue teamers, who else will use the ATT&CK Matrix? (Red Teamers, Purple Teamers, SOC Managers?) <br>
**Answer:** Red Teamers <br>

To answer the above question, you need some fundamental knowledge. SOC Managaers are Blue Teamers, while Purple Teamers fall between both Red and Blue Teaming. So, the answer we are left with is Red Teamers. Red teamers can use the ATT&CK Framework for engegements such as Threat Simulation Attacks to try and mimick APTs.

**Question:** What is the ID for this technique? <br>
**Answer:** T1566 <br>

**Question:** Based on this technique, what mitigation covers identifying social engineering techniques? <br>
**Answer:** User Training <br>

**Question:** What are the data sources for Detection? (format: source1,source2,source3 with no spaces after commas) <br>
**Answer:** Application Log,File,Network Traffic <br>

**Question:** What groups have used spear-phishing in their campaigns? (format: group1,group2) <br>
**Answer:** Axiom,GOLD SOUTHFIELD <br>

**Question:** Based on the information for the first group, what are their associated groups? <br>
**Answer:** Group 72 <br>

**Question:** What software is associated with this group that lists phishing as a technique? <br>
**Answer:** Hikit <br>

**Question:** What is the description for this software? <br>
**Answer:**   Hikit is malware that has been used by Axiom for late-stage persistence and exfiltration after the initial compromise. <br>

**Question:** This group overlaps (slightly) with which other group? <br>
**Answer:** Winnti Group <br>

**Question:** How many techniques are attributed to this group? <br>
**Answer:** 15 <br>

## Task 2: CAR Knowledge Base 
CAR (Cyber Analytics Repository) Knowledge Base offers analytics focused on detecting specific ATT&CK techniques. Acts as a bridge between TTP intelligence and detection engineering.

**Question:** For the above analytic, what is the pseudocode a representation of?
**Answer:** Splunk search

**Question:** What tactic has an ID of TA0003? <br>
**Answer:** Persistence <br>

**Question:** What is the name of the library that is a collection of Zeek (BRO) scripts? <br>
**Answer:** BZAR <br>

**Question:** What is the name of the technique for running executables with the same hash and different names? <br> 
Answer: Masquerading <br>

**Question:** Examine CAR-2013-05-004, besides Implementations, what additional information is provided to analysts to ensure coverage for this technique? <br>
**Answer:** Unit Testsg <br>

## Section: MITRE Engage 
MITRE ENGAGE (sorry, not a fancy acronym) focuses on adversary engagement strategies. Useful for proactive CTI — understanding how to interact with and deceive attackers.

**Question:** Under Prepare, what is ID SAC0002? <br>
**Answer:** PERSONA CREATION <br>

**Question:** What is the name of the resource to aid you with the engagement activity from the previous question? <br>
**Answer:** person profile worksheet <br>

**Question:** Which engagement activity baits a specific response from the adversary? <br>
**Answer:** Lures <br>

**Question:** What is the definition of Threat Model? <br>
**Answer:** A risk assessment that models organizational strengths and weaknesses. <br>

## Section: MITRE D3FEND 
D3FEND (Detection, Denial, and Disruption Framework Empowering Network Defense) maps countermeasures to ATT&CK techniques. Helps CTI analysts recommend specific defensive actions based on observed threats.

**Question:** What is the first MITRE ATT&CK technique listed in the ATT&CK Lookup dropdown? <br>
**Answer:** data obfuscation <br>

**Question:** In D3FEND Inferred Relationships, what does the ATT&CK technique from the previous question produce? <br>
**Answer:** Outbound internet traffic network <br>

## Task 3: ATT&CK® Emulation Plans 
**Question:** In Phase 1 for the APT3 Emulation Plan, what is listed first? <br> 
**Answer:** c2 setup <br>

**Question:** Under Persistence, what binary was replaced with cmd.exe? <br>
**Answer:** sethc.exe <br>

**Question:** Examining APT29, what  C2 frameworks are listed in Scenario 1 Infrastructure? (format: tool1,tool2) <br>
**Answer:** pupy,metasploit framework <br>

**Question:** What C2 framework is listed in Scenario 2 Infrastructure? <br>
**Answer:** poshc2 <br>

**Question:** Examine the emulation plan for Sandworm. What webshell is used for Scenario 1? Check MITRE ATT&CK for the Software ID for the webshell. What is the id? (format: webshell,id) <br>
**Answer:** P.A.S.,S0598 <br>

## Task 4: ATT&CK® and Threat Intelligence 
**Question:** What is a group that targets your sector who has been in operation since at least 2013? <br>
**Answer:** APT33 <br>

Question: As your organization is migrating to the cloud, is there anything attributed to this APT group that you should focus on? If so, what is it? <br>
Answer: **cloud accounts** <br>

**Question:** What tool is associated with the technique from the previous question? <br>
**Answer:** Ruler <br>

**NOTE:** Ruler is a tool that interacts with Exchange services and is associated with APT33's cloud account attacks.

**Question:** Referring to the technique from question 2, what mitigation method suggests using SMS messages as an alternative for its implementation? <br>
**Answer:** abnormal or malicious behaviour <br>

**Question:** What platforms does the technique from question #2 affect? <br>
**Answer:** Azure AD, Google Workspace, IaaS, Office 365, SaaS <br>

## Conclusion 
MITRE's projects are incredibly useful to the cybersecurity community. The intelligence on these platforms benefits everyone — from blue teamers to red teamers.

I first went through this module about a while ago. After revisiting it, I'm even more convinced that MITRE's frameworks are invaluable. I'm definitely planning to go deeper into these projects to better understand and apply them in my future career as a security analyst.
