# Passive Reconnaissance Room
## Introduction 
Passive reconnaissance is a technique used to gather information without directly engaging the target. It is a reliable technique as it does not create alerts to the client’s network infrastructure. 

In this module we are introduced to various tools that are helpful for passive recon. They include whois, nslookup, dig, DNSDumpster and Shodan.io. If well used, this tools can extract massive information from the target systems/network infrastructure. 

## Walkthrough 
## Task: Introduction 
Question: This room does not use a target virtual machine (VM) to demonstrate the discussed topics. Instead, we will query public WHOIS servers and DNS servers for domains owned by TryHackMe. Start the AttackBox and make sure it is ready. You will use the AttackBox to answer the questions in later tasks, especially tasks 3 and 4. <br>
Answer: **No answer needed** <br>

## Task: Passive Versus Active Recon 
Question: You visit the Facebook page of the target company, hoping to get some of their employee names. What kind of reconnaissance activity is this? (A for active, P for passive) <br>
Answer: **P** <br>

Question: You ping the IP address of the company webserver to check if ICMP traffic is blocked. What kind of reconnaissance activity is this? (A for active, P for passive) <br>
Answer: **A** 

Question: You happen to meet the IT administrator of the target company at a party. You try to use social engineering to get more information about their systems and network infrastructure. What kind of reconnaissance activity is this? (A for active, P for passive) <br>
Answer: **P** <br>

## Task: Whois 
Question: When was TryHackMe.com registered? <br>
Answer: **20180705** <br>

Question: What is the registrar of TryHackMe.com? <br>
Answer: **namecheap.com** <br>

Question: Which company is TryHackMe.com using for name servers? <br>
Answer: **cloudflare.com** <br>

<Screenshot of answers to the above questions numbered in their respective order> <br>
  
## Task: nslookup and dig 
Question: Check the TXT records of thmlabs.com. What is the flag there? <br>
Answer: **THM{a5b83929888ed36acb0272971e438d78}** <br>

## Task: DNSDumpster 
Question: Lookup tryhackme.com on DNSDumpster. What is one interesting subdomain that you would discover in addition to www and blog? <br> 
Answer: **remote** <br>

## Task: Shodan.io 
Question: According to Shodan.io, what is the 2nd country in the world in terms of the number of publicly accessible Apache servers? <br>
Answer: **Germany** <br>

Question: Based on Shodan.io, what is the 3rd most common port used for Apache? <br>
Answer: **8080** <br>

<Answers to the first and second questions of this task> 
  
Question: Based on Shodan.io, what is the 3rd most common port used for nginx? <br>
Answer: **5001** <br>

<3rd most common port used for nginx> <br>

## Module Completion 
TryHackMe profile link: https://tryhackme.com/p/kl45h 

## Conclusion 
Passive recon is skill that is essential for all penetration testers to gather and collect 
information about the client’s target network. We can achieve this through the help of 
tools like whois, nslookup, dig, DNSDumpster and Shodan.io. The more information you 
have, the better the planning for the next penetration phases. 
Passive reconnaissance can also be used by defensive team to identify how much 
information an attacker can gather about the network infrastructure. 
Having learned much from this room, it is time to put the knowledge into practise. 
