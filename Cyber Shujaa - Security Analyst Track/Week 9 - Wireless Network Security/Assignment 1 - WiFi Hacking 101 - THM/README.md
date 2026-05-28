# Wifi Hacking 101 Room
## Introduction
Wi-Fi hacking is a type of attack that focuses on capturing WPA handshake and brute-force them to get the Wi-Fi pass-phrase. It is an easy attack to perform but might require some higher computing power to crack the WPA handshake. 

This TryHackMe room discusses how exactly to perform that. Let’s get started and try to answer the question asked in the room.

## Walkthrough
## Task 1: The Basics-An Intro to WPA
Question: What type of attack on the encryption can you perform on WPA(2) personal? <br>
Answer: **brute force** <br>

From the question hint we can be able to identify the type of attack asked.

Question: Can this method be used to attack WPA2-EAP handshakes? (Yea/Nay) <br>
Answer: **Nay** <br>

Question: What three letter abbreviation is the technical term for the "wifi code/password/passphrase"? <br>
Answer: **PSK** <br>

Question: What's the minimum length of a WPA2 Personal password? <br>
Answer: **8** <br>

## Task 2: You’re being watched- Capturing packets to attack
Question: How do you put the interface “wlan0” into monitor mode with Aircrack tools? (Full command) <br>
Answer: **airmon-ng start wlan0** <br>

Question: What is the new interface name likely to be after you enable monitor mode? <br>
Answer: **wlan0mon** <br>

Question: What do you do if other processes are currently trying to use that network adapter? <br>
Answer: **airmon-ng check kill** <br>

Question: What tool from the aircrack-ng suite is used to create a capture? <br>
Answer: **airodump-ng** <br>

Question: What flag do you use to set the BSSID to monitor? <br>
Answer: **--bssid** <br>

Question: And to set the channel? <br>
Answer: **--channel** <br>

Question: And how do you tell it to capture packets to a file? <br>
Answer: **-w** <br>

## Task 3: Aircrack-ng- Let’s Get Cracking
Question: What flag do we use to specify a BSSID to attack? <br>
Answer: **-b** <br>

Question: What flag do we use to specify a wordlist? <br>
Answer: **-w** <br>

Question: How do we create a HCCAPX in order to use hashcat to crack the password? <br>
Answer: **-j** <br>

Question: Using the rockyou wordlist, crack the password in the attached capture. What's the password? <br>
Answer: **greeneggsandham** <br>

<Commandissued to crack the password>
  
<Cracked password>
   
Question: Where is password cracking likely to be fastest, CPU or GPU? <br>
Answer: **GPU** <br>

The answer to this answer can be found from the task notes

## Conclusion
To me, this room was more of a refresher, nothing new learned as this was the first I leared when I
got started with cyber security. Trying to crack my neighbors Wi-Fi. However, do not try that as I later learned it is illegal to hack into a system without permision to do so.
