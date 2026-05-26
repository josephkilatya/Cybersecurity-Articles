# Windows Forensics 1
## Introduction
This module covers Windows Forensics with a focus on the registry hives. Registry
hives can provide invaluable information during Windows Forensics examination and
analysis processes.

## Walkthrough
## Task 1: Introduction to Windows Forensics
Question: What is the most used Desktop Operating System right now? <br>
Answer: **Microsoft Windows**  <br>
<img width="1568" height="146" alt="task 1" src="https://github.com/user-attachments/assets/8101e579-4677-4230-91ac-f290e9d661a3" />

## Task 2: Windows Registry and Forensics
Question: What is the short form for HKEY_LOCAL_MACHINE?  <br>
Answer: **HKLM**  <br>
<img width="1267" height="63" alt="task 2" src="https://github.com/user-attachments/assets/10e1077f-cd64-4db8-86e0-989b042b902b" />

## Task 3: Accessing Registry hives offline
Question: What is the path for the five main registry hives, DEFAULT, SAM, SECURITY, SOFTWARE, and SYSTEM?  <br>
Answer: **C:\Windows\System32\Config**  <br>
<img width="1504" height="302" alt="task 3 1" src="https://github.com/user-attachments/assets/d2108bd0-b72d-4df9-9eb5-fb49207f97be" />

Question: What is the path for the AmCache hive?  <br>
Answer: **C:\Windows\AppCompat\Programs\Amcache.hve**  <br>
<img width="1536" height="142" alt="task 3 2" src="https://github.com/user-attachments/assets/d6472c3f-e189-46db-ae9c-597ec8f961f0" />

## Task 4: Data Acquisition
Question: Try collecting data on your own system or the attached VM using one of the above mentioned tools.  <br>
Answer: **No answer needed.**  <br>

## Task 5: Exploring Windows Registry
Question: Study the above material to understand the difference between the different tools  <br>
Answer: **No answer needed.**  <br>

## Task 6: Sysytem Information and System Accounts
Question: What is the Current Build Number of the machine whose data is being investigated?  <br>
Answer: **19044**  <br>
<img width="1374" height="681" alt="task 4 1" src="https://github.com/user-attachments/assets/05bb858f-356b-4727-bcb1-6811eadbba2d" />

Question: Which ControlSet contains the last known good configuration?  <br>
Answer: **1** <br>
<img width="1298" height="209" alt="task 4 3" src="https://github.com/user-attachments/assets/2845c355-f5d6-40a5-9a18-fb47e68e8512" />

Question: What is the Computer Name of the computer?  <br>
Answer: **THM-4n6**  <br>
<img width="1370" height="371" alt="task 4 4" src="https://github.com/user-attachments/assets/7a16787c-0181-4c1d-8bcf-3d3a86830378" />

Question: What is the value of the TimeZoneKeyName?  <br>
Answer: **Pakistan Standard Time**  <br>

Question: What is the DHCP IP address  <br>
Answer: **192.168.100.58**  <br>

Question: What is the RID of the Guest User account?
Answer: **501** <br>

## Task 7: Usage or knowledge of files/folders
Question: When was EZtools opened?  <br>
Answer: **2021-12-01 13:00:34**  <br>

Question: At what time was My Computer last interacted with?
Answer: **2021-12-01 13:06:47**  <br>

Question: What is the Absolute Path of the file opened using notepad.exe?  <br>
Answer: **C:\Program Files\Amazon\Ec2ConfigService\Settings**  <br>

Question: When was this file opened?  <br>
Answer: **2021-11-30 10:56:19**  <br>

## Task 8: Evidence of Execution
Question: How many times was the File Explorer launched?  <br>
Answer: **26**  <br>

Question: What is another name for ShimCache?  <br>
Answer: **AppCompatCache**  <br>

Question: Which of the artifacts also saves SHA1 hashes of the executed programs?  <br>
Answer: **AmCache**  <br>

Question: Which of the artifacts saves the full path of the executed programs?  <br>
Answer: **BAM/DAM**  <br>

## Task 9: External Devices/USB device forensics 
Question: What is the serial number of the device from the manufacturer 'Kingston'?  <br>
Answer: **1C6f654E59A3B0C179D366AE&0** <br>

Question: What is the name of this device?  <br>
Answer: **Kingston Data Traveler 2.0 USB Device**  <br>

Question: What is the friendly name of the device from the manufacturer 'Kingston'?  <br>
Answer: **USB**  <br>

## Task 10: Hands-on Challenge
Question: How many user created accounts are present on the system?  <br>
Answer: **3** <br>
<img width="928" height="355" alt="task 10 1" src="https://github.com/user-attachments/assets/cff1b81a-11ec-4f8e-a1b5-c76c384aa09b" />

Question: What is the username of the account that has never been logged in?  <br>
Answer: **thm-user2**  <br>
<img width="739" height="364" alt="task 10 2" src="https://github.com/user-attachments/assets/77c24a1e-d028-474f-9c50-12b9a342527d" />

Question: What's the password hint for the user THM-4n6?  <br>
Answer: **count**  <br>
<img width="576" height="503" alt="task 10 3" src="https://github.com/user-attachments/assets/eb31aaba-791f-4ebf-bf38-7d976388fd38" />

Question: When was the file 'Changelog.txt' accessed?  <br>
Answer: **2021-11-21 18:18:48**  <br>
<img width="1326" height="422" alt="task 10 4" src="https://github.com/user-attachments/assets/36f4088e-6076-43b5-8e1c-aa6bc762c3f7" />

Question: What is the complete path from where the python 3.8.2 installer was run?  <br>
Answer: **Z:\setups\python-3.8.2.exe**  <br>
<img width="1322" height="422" alt="task 10 5" src="https://github.com/user-attachments/assets/ee4f83aa-9fe5-459e-9ab7-146672f4dc50" />

Question: When was the USB device with the friendly name 'USB' last connected?  <br>
<img width="1233" height="173" alt="task 10 6" src="https://github.com/user-attachments/assets/5bc62e19-91cd-4141-8bee-9a0cffe090f1" />

## Task 11: Conclusion
Question: Review the provided resources.  <br>
Answer: **No answer needed.**  <br>

## Module completion
TryHackMe Profile Link: https://tryhackme.com/p/kl45h

## Conclusion
Whatcan I say? With my passion in digital forensics, I can not describe how much valuable this room was to my skill-set. As a matter of fact, I had gone through this roomawhile ago andstill enjoyed going through it once again and getting a refresher of the knowledge. I love digital forensics. Solving mysteries is my thing.
