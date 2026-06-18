# Wifi Hacking 101 Room
## Introduction
Wi-Fi hacking is a type of attack that focuses on capturing WPA handshake and brute-force them to get the Wi-Fi pass-phrase. It is an easy attack to perform but might require some higher computing power to crack the WPA handshake. 

This TryHackMe room discusses how exactly to perform that. Let’s get started and try to answer the question asked in the room.

## Walkthrough
## Task 1: The Basics-An Intro to WPA
**Question:** What type of attack on the encryption can you perform on WPA(2) personal? <br>
**Answer:** `brute force` <br>
<img width="649" height="245" alt="task 1 1" src="https://github.com/user-attachments/assets/807f5759-01f7-48a9-9cfe-40f2e162f5ce" />

I got stuck in this question and had to use the question hint to identify the type of attack asked.

**Question:** Can this method be used to attack WPA2-EAP handshakes? (Yea/Nay) <br>
**Answer:** `Nay` <br>
<img width="1209" height="48" alt="task 1 2" src="https://github.com/user-attachments/assets/2fd779e6-ea05-4033-b0d8-bf11494999d7" />

**Question:** What three letter abbreviation is the technical term for the "wifi code/password/passphrase"? <br>
**Answer:** `PSK` <br>
<img width="624" height="282" alt="task 1 3" src="https://github.com/user-attachments/assets/6f665bc3-b2a5-4ed5-bb38-0d92ecbd2d91" />

**Question:** What's the minimum length of a WPA2 Personal password? <br>
**Answer:** `8` <br>
<img width="573" height="281" alt="task 1 4" src="https://github.com/user-attachments/assets/91a05564-5fe6-4dc8-af7e-9ebbe092e82d" />

## Task 2: You’re being watched- Capturing packets to attack
Question: How do you put the interface “wlan0” into monitor mode with Aircrack tools? (Full command) <br>
Answer: **airmon-ng start wlan0** <br>

**Command Explained:**
1. `airmon-ng` - is a core script within the Aircrack-ng suite used to enable and disable monitor mode on wireless network interfaces.
2. `start` - activates monitor mode on the designated wireless interface.
3. `wlan0` - the target Wi-Fi interface selected for wireless monitoring.
   
**Question:** What is the new interface name likely to be after you enable monitor mode? <br>
**Answer:** `wlan0mon` <br>

<img width="929" height="436" alt="task 2 1-2" src="https://github.com/user-attachments/assets/0484022e-d559-488d-8d64-f4aa95aed818" />

**Question:** What do you do if other processes are currently trying to use that network adapter? <br>
**Answer:** `airmon-ng check kill` <br>
<img width="931" height="249" alt="task 2 3" src="https://github.com/user-attachments/assets/fb873902-d1bc-45d7-b53e-ef9cc075e1be" />

**Command Explained:**
- `airmon-ng` - is a core script within the Aircrack-ng suite used to enable and disable monitor mode on wireless network interfaces.
- `check` - scans the system for running processes that might interfere with wireless sniffing and injection.
- `kill` - terminates all of those conflicting background processes (like NetworkManager or wpa_supplicant) to ensure clean access to the Wi-Fi card.
  
**Question:** What tool from the aircrack-ng suite is used to create a capture? <br>
**Answer:** `airodump-ng` <br>
<img width="720" height="189" alt="task 2 4" src="https://github.com/user-attachments/assets/5308e9fe-04d4-41b5-8928-3e52cacae5f4" />

**Question:** What flag do you use to set the BSSID to monitor? <br>
**Answer:** `--bssid` <br>
<img width="701" height="171" alt="task 2 5" src="https://github.com/user-attachments/assets/1f3688dd-9707-4184-bf75-7361f9ca15a3" />

**Question:** And to set the channel? <br>
**Answer:** `--channel` <br>
<img width="569" height="148" alt="task 2 6" src="https://github.com/user-attachments/assets/a76492d2-833d-41c5-8cf9-f95e1839bbcf" />

**Question:** And how do you tell it to capture packets to a file? <br>
**Answer:** `-w` <br>
<img width="699" height="200" alt="task 2 7" src="https://github.com/user-attachments/assets/ce99731b-bd1e-4873-bb4b-1ad1177b44ab" />

## Task 3: Aircrack-ng- Let’s Get Cracking
**Question:** What flag do we use to specify a BSSID to attack? <br>
**Answer:** `-b` <br>
<img width="945" height="322" alt="task 3 1" src="https://github.com/user-attachments/assets/705d2276-c8ea-4125-9dd3-37adb6e741aa" />

**Question:** What flag do we use to specify a wordlist? <br>
**Answer:** `-w` <br>
<img width="913" height="160" alt="task 3 2" src="https://github.com/user-attachments/assets/b2b987f6-5e79-491c-b57c-274bb1ed701d" />

**Question:** How do we create a HCCAPX in order to use hashcat to crack the password? <br>
**Answer:** **-j** <br>
<img width="957" height="278" alt="task 3 3" src="https://github.com/user-attachments/assets/ad004adf-b6ee-4e6e-91ab-d80fa56d6d9a" />

**Question:** Using the rockyou wordlist, crack the password in the attached capture. What's the password? <br>
**Answer:** `greeneggsandham` <br>
<img width="1314" height="51" alt="task 3 4 1 command used" src="https://github.com/user-attachments/assets/5bf292ef-1086-4f12-888f-0fd0f63f8534" />
_Commandissued to crack the password_

<img width="893" height="413" alt="task 3 4 2 password" src="https://github.com/user-attachments/assets/d3ef4261-dd79-4f6e-8804-7375262d0571" />
_Cracked password_
   
Question: Where is password cracking likely to be fastest, CPU or GPU? <br>
Answer: **GPU** <br>
<img width="1638" height="100" alt="task 3 5" src="https://github.com/user-attachments/assets/b49d3675-c7b8-481d-8786-6f57edc6cbee" />

The answer to this answer can be found from the task notes

## Conclusion
To me, this room was more of a refresher, nothing new learned as this was the first I leared when I
got started with cyber security. Trying to crack my neighbors Wi-Fi. However, do not try that as I later learned it is illegal to hack into a system without permision to do so.
