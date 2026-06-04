# Attactive Directory Room Report 
## Introduction 
Just as the room name indicates, the room is about hacking an Active Directory Environment. 99% of Corporate networks run off of Active Directory. Poor AD configurations can leave the environment vulnerable to attacks. 

In this room, we familiarize ourselves with tools during AD penetration testing. The tools include Impacket, Bloodhound, Neo4j. Other tools used but not covered in the room include smbclient, kerbrute and hashcat. 

## Walkthrough 
## Section: Deploy The Machine 
Question: You're now ready to start hacking!  
Answer: **no answer needed** 

Question: Alternatively, you can deploy the In-Browser Kali or Attack Box and automatically be connected to the TryHackMe Network. 
Answer: **no answer needed** 

Question: Once connected to the VPN, deploy the machine and get hacking! 
Answer: **no answer needed** 

## Section: Setup 
Question: Install Impacket, Bloodhound and Neo4j 
Answer: **no answer needed**

## Section: Welcome to Attactive Directory 
Question: What tool will allow us to enumerate port 139/445? 
Answer: **enum4linux** 

Question: What is the NetBIOS-Domain Name of the machine? 
Answer: **THM-AD** 
<img width="996" height="158" alt="1 1 domain name" src="https://github.com/user-attachments/assets/b73e5bdf-3f9a-4473-aa4c-1a14b8ed50eb" />
_Target machine NetBIOS-Domain Name_
  
Question: What invalid TLD do people commonly use for their Active Directory Domain? <br>
Answer: **.local** <br>
<img width="893" height="677" alt="1 2 notable accounts" src="https://github.com/user-attachments/assets/2e88bbb6-5ef1-4fa3-bcd1-19becb5263d6" /> <br>

## Section: Enumerating Users via Kerberos 
Question: What command within Kerbrute will allow us to enumerate valid usernames? <br>
Answer: **userenum** <br>
 
Question: What notable account is discovered? (These should jump out at you) <br>
Answer: **svc-admin** <br>

Question: What is the other notable account is discovered? (These should jump out at you) <br>
Answer: **backup** <br>
<img width="893" height="677" alt="1 2 notable accounts" src="https://github.com/user-attachments/assets/bf2d237e-f2ae-44c7-8633-457476b12894" /> <br>
_Notable accounts_ <br>
  
## Section: Abusing Kerberos 
Question: We have two user accounts that we could potentially query a ticket from. Which user account can you query a ticket from with no password? <br>
Answer: **svc-admin** <br>
<img width="1002" height="516" alt="2 1 user with no password auth" src="https://github.com/user-attachments/assets/95fbb677-e147-4226-abf2-bfa49918ec52" /> <br>
_svc-admin Kerberos ticket_ <br>
  
Question: Looking at the Hashcat Examples Wiki page, what type of Kerberos hash did we retrieve from the KDC? (Specify the full name) <br> 
Answer: **Kerberos 5 AS-REP etype 23** <br>
<img width="1927" height="961" alt="2 2 hashcat type and mode" src="https://github.com/user-attachments/assets/7151bb89-ddec-4912-b9c4-40a7be278444" /> <br>

Question: What mode is the hash? <br>
Answer: **18200** <br>
<img width="1927" height="961" alt="2 2 hashcat type and mode" src="https://github.com/user-attachments/assets/b0c67d60-41bc-441b-8113-9588b8029774" /> <br>
_Retrieved Kerberos hash name and types_ 
  
Question: Now crack the hash with the modified password list provided, what is the user accounts password? <br>
Answer: **management2005** <br>
<img width="947" height="417" alt="2 3 cracked password" src="https://github.com/user-attachments/assets/a028b3c9-3c2c-4b6f-b4c6-9f280e57e074" /> <br>
_cracked hash password_ <br>
  
## Seciton: Back to Basics 
Question: What utility can we use to map remote SMB shares? <br>
Answer: **smbclient** <br>

Question: Which option will list shares? <br>
Answer: **-L** <br>

Question: How many remote shares is the server listing? <br>
Answer: **6** <br>
<img width="839" height="260" alt="3 1 smb shares" src="https://github.com/user-attachments/assets/05727b56-2fe3-41c7-bb96-6535ee82159c" /> <br>
_Remote AD shares listed_ <br>
  
Question: There is one particular share that we have access to that contains a text file. Which share is it? <br>
Answer: **backup** <br>
<img width="1227" height="256" alt="3 1 share with a txt file" src="https://github.com/user-attachments/assets/729a8f35-927d-4bd1-a20d-0e34d81b6620" /> <br>
_Share with a text file_ <br>
  
Question: What is the content of the file? <br>
Answer: **YmFja3VwQHNwb29reXNlYy5sb2NhbDpiYWNrdXAyNTE3ODYw** <br>
<img width="522" height="53" alt="3 3 encoded text" src="https://github.com/user-attachments/assets/c9b785df-05ca-4400-9552-c9af0ee26741" /> <br>
_Encoded file contents_ <br>
  
Question: Decoding the contents of the file, what is the full contents? <br>
Answer: **backup@spookysec.local:backup2517860** <br>
<img width="737" height="88" alt="3 4 decoded text" src="https://github.com/user-attachments/assets/68235da4-4eb0-449c-87de-ab49d73a66c7" /> <br>
_decoded contents of the file_ <br>
  
## Section: Elevating Privileges within the Domain 
Question: What method allowed us to dump NTDS.DIT? <br>
Answer: **DRSUAPI** <br>

Question: What is the Administrators NTLM hash? <br>
Answer: **0e0363213e37b94221497260b0bcb4fc** <br>
<img width="1089" height="512" alt="method and ntlm hash" src="https://github.com/user-attachments/assets/d6265f34-c2a0-41e4-9877-18676144eaa4" /> <br>
_NTDS.DIT dump showing Administrator NTLM hash and method used to dump the hashes_ <br>

Question: What method of attack could allow us to authenticate as the user without the password? <br>
Answer: **Pass The Hash** <br>

Question: Using a tool called Evil-WinRM what option will allow us to use a hash? <br>
Answer: -H <br>

## Section: Flag Submission Panel 
Question: svc-admin <br>
Answer: **TryHackMe{K3rb3r0s_Pr3_4uth}** <br>
<img width="725" height="299" alt="4 1 svc-admin user flag" src="https://github.com/user-attachments/assets/a02d8c81-9870-4420-a4e4-4e2ffe9e12db" /> <br>
_svc-admin user flag_ <br>
  
Question: backup <br>
Answer: **TryHackMe{B4ckM3UpSc0tty!}** <br>
<img width="663" height="289" alt="3 2 backup flag" src="https://github.com/user-attachments/assets/0d7da9d2-49f3-4c07-a68e-fe0bc0e0fd2b" />
_backup user flag_
Question: Administrator <br>
Answer: **TryHackMe{4ctiveD1rectoryM4st3r}** <br>
<img width="772" height="318" alt="4 3 admin root flag" src="https://github.com/user-attachments/assets/5ce3d359-6421-4cc7-8133-1ea84ab8422d" /> <br>
_Administrator root flag_ <br>
  
## Module completion 
TryHackMe profile link: https://tryhackme.com/p/kl45h 

## Conclusion 
Overall the room was fun with a lot to run. This my first time hacking an AD environment. Since AD is widely used in corporate networks, I am going to invest my time in learning how to exploit and secure AD environments. 
