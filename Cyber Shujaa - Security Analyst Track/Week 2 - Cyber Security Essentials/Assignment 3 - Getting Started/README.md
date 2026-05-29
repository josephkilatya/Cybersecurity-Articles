# Getting Started Module - HTB
## Introduction 
In this module we are introduced into the world of hands-on hacking (penetration testing). The module was quite extensive and engaging with a lot to learn. Some of things learned from the module include: 

Selecting a penetration testing distro, recommended Kali and Parrot VMs, and how to put things organized professionally.  

We are taken through some of the basic tools used in a pentest such as ssh, netcat, tmux and vim.  

We are also taken through various phases of pentest. These phases include service scanning using nmap; Web enumeration using gobuster, whatweb and other tools; Gaining initial hold of a target computer and escalating privileges. 

The module has two target machines. Nibbles machine with a walkthrough and GetSimple Machine as our practice machine. 

## Walkthrough 
## Section: Basic Tools 
Question: Apply what you learned in this section to grab the banner of the above server and submit it as the answer. 
Answer: SSH-2.0-OpenSSH_8.2p1 Ubuntu-4ubuntu0.1 
<img width="1142" height="824" alt="1 1 basic tools" src="https://github.com/user-attachments/assets/f93a9e46-f612-4763-b9f0-20c92093524c" />
_Banner grabbing using netcat_
  
## Section: Service Scanning 
Question: Perform an Nmap scan of the target. What does Nmap display as the version of the service running on port 8080? 
Answer: Apache Tomcat 
<img width="1104" height="699" alt="2 1 service scannin" src="https://github.com/user-attachments/assets/f8c62e98-4756-464e-934a-2db4a158189f" />
_Service version running on port 8080_

Question: Perform an Nmap scan of the target and identify the non-default port that the telnet service is running on. 
Answer: 2323 
<img width="1217" height="972" alt="2 2 service scanning" src="https://github.com/user-attachments/assets/e04acb87-a7c0-4d79-b9bc-2ed6c3d105e0" />
_discovered telnet port_
  
Question: List the SMB shares available on the target host. Connect to the available share as the bob user. Once connected, access the folder called 'flag' and submit the contents of the flag.txt file. 
Answer: dceece590f3284c3866305eb2473d099 
<img width="1920" height="975" alt="2 3 service scanning" src="https://github.com/user-attachments/assets/42d17863-6cce-4d85-a29e-70707f69e8d7" />
_SMB enumeration flag_
  
## Section: Web Enumeration 
Question: Try running some of the web enumeration techniques you learned in this section on the server above, and use the info you get to get the flag. 
Answer: HTB{w3b_3num3r4710n_r3v34l5_53cr375} 
<img width="959" height="869" alt="3 1 web enumeration" src="https://github.com/user-attachments/assets/78150bc0-1f8c-4fe9-82d1-2a3039d5fa97" />
_Step 1: directory/file scan _

<img width="944" height="857" alt="3 2 web enumeration" src="https://github.com/user-attachments/assets/91cc9e68-081d-4ace-b4a4-8044bfd3c882" />
_Step 2: Checking robots.txt which is interesting to look for juicy information _

<img width="851" height="668" alt="3 3 web enumeration" src="https://github.com/user-attachments/assets/ef5ae1b7-2b1c-4ebf-8905-6ce4d3e943aa" />
_Step 3: Getting our flag by visiting the page listed in robots.txt_

## Section: Public Exploits 
Question: Try to identify the services running on the server above, and then try to search to find public exploits to exploit them. Once you do, try to get the content of the '/flag.txt' file. (note: the web server may take a few seconds to start) 
Answer: HTB{my_f1r57_h4ck} 

<Exploiting target machine with Metasploit framework> 
  
## Section: Privilege Escalation 
Question: SSH into the server above with the provided credentials, and use the '-p xxxxxx' to specify the port shown above. Once you login, try to find a way to move to 'user2', to get the flag in '/home/user2/flag.txt'. 
Answer: HTB{l473r4l_m0v3m3n7_70_4n07h3r_u53r} 

<user flag> 
  
Question: Once you gain access to 'user2', try to find a way to escalate your privileges to root, to get the flag in '/root/flag.txt'. 
Answer: HTB{pr1v1l363_35c4l4710n_2_r007} 

<Root flag> 
  
## Nibbles Sections: Attacking Your Box  
### Enumeration 
Question: Run an nmap script scan on the target. What is the Apache version running on the server? (answer format: X.X.XX) 
Answer: 2.4.18 

<Nibbles Enumeration> 
  
### Initial Foothold 
Question: Gain a foothold on the target and submit the user.txt flag 
Answer: 79c03865431abf47b90ef24b9695e148 

<Getting user flag> 
  
### Privilege Escalation 
Question: Escalate privileges and submit the root.txt flag. 
Answer: de5e5d6619862a8aa5b9b212314e0cdd 

<Getting root flag> 
  
## Section: Knowledge Check 
Question: Spawn the target, gain a foothold and submit the contents of the user.txt flag. 
Answer: 7002d65b149b0a4d19132a66feed21d8 

<Getting user flag> 
  
Question: After obtaining a foothold on the target, escalate privileges to root and submit the contents of the root.txt flag. 
Answer: f1fba6e9f71efb2630e6e34da6387842 

<Getting root flag> 
  
## Module Completion 
Link: https://academy.hackthebox.com/achievement/1293352/77 

## Conclusion 
I learned a lot from this module. I even hacked my first computer. However, just as the module name states, I’m just getting started. I’m excited to learn more and hack more machines in my journey as a cybersecurity analyst. 
