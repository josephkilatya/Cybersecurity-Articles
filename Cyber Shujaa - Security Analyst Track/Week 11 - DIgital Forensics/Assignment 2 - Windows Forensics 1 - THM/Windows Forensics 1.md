# Windows Forensics 1
## Introduction
This TryHackMe Room covers Windows Forensics with a focus on the registry hives. Registry hives can provide invaluable information during Windows Forensics examination and analysis processes.

## Walkthrough
## Task 1: Introduction to Windows Forensics
**Question:** What is the most used Desktop Operating System right now? <br>
**Answer:** `Microsoft Windows`  <br>
<img width="1568" height="146" alt="task 1" src="https://github.com/user-attachments/assets/8101e579-4677-4230-91ac-f290e9d661a3" />

Explanation: Microsoft Windows continues to dominate the desktop OS market with a share of over 70%. This makes Windows forensics a critical skill for any Security Analyst or DFIR professional.

📸 Where to find screenshots: The TryHackMe room provides a visual of the desktop OS market share statistics. Look for the image showing the percentage breakdown of operating systems in the task description.

## Task 2: Windows Registry and Forensics
**Question:** What is the short form for HKEY_LOCAL_MACHINE?  <br>
**Answer:** `HKLM`  <br>
<img width="1267" height="63" alt="task 2" src="https://github.com/user-attachments/assets/10e1077f-cd64-4db8-86e0-989b042b902b" />

Explanation: HKLM is one of the main root keys in the Windows Registry. It stores configuration information for the machine itself (hardware, software installed, system settings). It is heavily used in forensics to understand system configuration and installed programs.

📸 Where to find screenshots: The room shows a screenshot of the Windows Registry Editor displaying the five main root keys. Look for the image labeled "Registry Editor" showing HKLM, HKU, HKCR, HKCC, and HKCU.

## Task 3: Accessing Registry hives offline
**Question:** What is the path for the five main registry hives, DEFAULT, SAM, SECURITY, SOFTWARE, and SYSTEM?  <br>
**Answer:** `C:\Windows\System32\Config`  <br>
<img width="1504" height="302" alt="task 3 1" src="https://github.com/user-attachments/assets/d2108bd0-b72d-4df9-9eb5-fb49207f97be" />

**Explanation:** These five hives are the core offline registry files. During incident response, analysts copy these files from a compromised machine for offline analysis without booting the original system.

- The SYSTEM hive contains configuration data regarding the computer's hardware, device drivers, and system services. It is a critical forensic artifact for building timelines because it tracks system time zones, network configurations, and the serial numbers of connected USB devices.
- The SOFTWARE hive stores information about the operating system configuration, file associations, and installed third-party applications. It is a vital resource for forensic investigators to identify malware persistence mechanisms—such as automatic boot triggers—and to determine exactly what software was available to a user.
- The SAM (Security Accounts Manager) hive serves as the local database for user accounts, groups, and their associated security descriptors. It is an essential artifact during an investigation for uncovering unauthorized backdoor profiles, tracking user login metrics, and extracting password hashes for credential analysis.
- The SECURITY hive manages system-wide security policies, user privileges, and local security audit settings. Its importance in digital forensics lies in revealing active event logging configurations and exposing cached domain credentials or sensitive service account passwords.
- The DEFAULT hive acts as the registry configuration template applied to any new user profile created on the system. It is important in forensics because investigators inspect it to establish baseline settings and ensure attackers have not modified the template to automatically infect new users.

**Question:** What is the path for the AmCache hive?  <br>
**Answer:** `C:\Windows\AppCompat\Programs\Amcache.hve`  <br>
<img width="1536" height="142" alt="task 3 2" src="https://github.com/user-attachments/assets/d6472c3f-e189-46db-ae9c-597ec8f961f0" />

Explanation: AmCache.hve is a very important artifact for evidence of execution. It tracks programs that have been executed on the system and can contain SHA-1 hashes of executables.

📸 Where to find screenshots: The room shows a screenshot of the File Explorer navigating to C:\Windows\System32\config and another to C:\Windows\AppCompat\Programs. Look for images showing these exact paths with the files highlighted.

## Task 4: Data Acquisition
**Question:** Try collecting data on your own system or the attached VM using one of the above mentioned tools.  <br>
**Answer:** `No answer needed.`  <br>

Explanation: In a real investigation, this step involves using tools like FTK Imager, Magnet RAM Capture, triaging with KAPE or simply copying the registry hives (SYSTEM, SAM, SOFTWARE, etc.) while maintaining chain of custody.

📸 Where to find screenshots: The room displays screenshots of FTK Imager showing how to:
1. Launch FTK Imager
2. Navigate to the C:\Windows\System32\config folder
3. Add the registry hives for acquisition
4. Export the files for offline analysis.

## Task 5: Exploring Windows Registry
**Question:** Study the above material to understand the difference between the different tools  <br>
**Answer:** `No answer needed.`  <br>

Explanation: Different tools (Registry Explorer, RegRipper, Autoruns, etc.) offer different strengths. Registry Explorer is excellent for manual browsing with tagging, while RegRipper is great for automated extraction of common artifacts.

📸 Where to find screenshots: The room shows comparative screenshots of:
- Registry Explorer: Showing the GUI interface with loaded hives and the ability to bookmark artifacts
- RegRipper: Displaying the command-line interface and output of extracted artifacts
- EZTools: The combined tool interface used in the hands-on section

## Task 6: Sysytem Information and System Accounts
**Question:** What is the Current Build Number of the machine whose data is being investigated?  <br>
**Answer:** `19044`  <br>
<img width="1374" height="681" alt="task 4 1" src="https://github.com/user-attachments/assets/05bb858f-356b-4727-bcb1-6811eadbba2d" />

Explanation: This corresponds to Windows 10 version 21H2. Build numbers help analysts identify the exact OS version and patch level, which is useful for knowing which vulnerabilities may be present.

🔍 How to find it:
1. Load the SOFTWARE hive in Registry Explorer
2. Navigate to SOFTWARE\Microsoft\Windows NT\CurrentVersion
3. Look for the CurrentBuildNumber value

**Question:** Which ControlSet contains the last known good configuration?  <br>
**Answer:** 1 <br>
<img width="1063" height="339" alt="task 4 2" src="https://github.com/user-attachments/assets/400c46d0-3ab2-49cd-9153-57317221629a" />

Explanation: Windows maintains ControlSet001 and ControlSet002. The CurrentControlSet and LastKnownGood values in the SYSTEM hive tell us which one was used during the last successful boot.

🔍 How to find it:
1. Load the SYSTEM hive in Registry Explorer
2. Navigate to SYSTEM\Select
3. Look at the LastKnownGood value (it will show 1)

**Question:** What is the Computer Name of the computer?  <br>
**Answer:** `THM-4n6`  <br>
<img width="1298" height="209" alt="task 4 3" src="https://github.com/user-attachments/assets/ce8f517a-9b65-40fa-9c7e-afb639c0395c" />

Explanation: Hostname is a basic but essential IOC. It helps correlate this machine with logs from other systems or network traffic.

🔍 How to find it:
1. Load the SYSTEM hive
2. Navigate to SYSTEM\CurrentControlSet\Control\ComputerName\ComputerName
3. Look for the ComputerName value

**Question:** What is the value of the TimeZoneKeyName?  <br>
**Answer:** `Pakistan Standard Time`  <br>
<img width="1370" height="371" alt="task 4 4" src="https://github.com/user-attachments/assets/433bc7c2-97ed-428c-9e8d-ea6fe35012c8" />

Explanation: Timezone information is critical for accurate timeline analysis across multiple systems or when correlating with external logs.

🔍 How to find it:
1. Load the SYSTEM hive
2. Navigate to SYSTEM\CurrentControlSet\Control\TimeZoneInformation
3. Look for the TimeZoneKeyName value

**Question:** What is the DHCP IP address  <br>
**Answer:** `192.168.100.58`  <br>
<img width="1330" height="575" alt="task 4 5" src="https://github.com/user-attachments/assets/79afa356-5fa4-4f34-8c2a-bb37eddb31bb" />

Explanation: This helps map the machine on the network and can be correlated with DHCP server logs or firewall records.

🔍 How to find it:
1. Load the SYSTEM hive
2. Navigate to SYSTEM\CurrentControlSet\Services\Tcpip\Parameters\Interfaces

Check each network adapter's subkey for DhcpIPAddress
**Question:** What is the RID of the Guest User account? <br>
**Answer:** `501` <br>
<img width="1351" height="538" alt="task 4 6" src="https://github.com/user-attachments/assets/16ef020b-1db3-4adc-8801-5b6da5e4f0c2" />

Explanation: Relative Identifiers (RIDs) are unique within a domain/machine. RID 500 is Administrator, 501 is Guest. This helps identify built-in accounts quickly.

🔍 How to find it:
1. Load the SAM hive in Registry Explorer
2. Navigate to SAM\Domains\Account\Users\Names\Guest
3. The RID is embedded in the value data

📸 Where to find screenshots: The room shows screenshots for each of these steps:
- Navigating to SOFTWARE\Microsoft\Windows NT\CurrentVersion to find the build number
- The SYSTEM\Select key showing the LastKnownGood value
- SYSTEM\CurrentControlSet\Control\ComputerName\ComputerName for the hostname
- The TimeZoneInformation key showing the timezone
- Network interface keys showing the DHCP IP address

SAM\Domains\Account\Users\Names\Guest showing the RID value

## Task 7: Usage or knowledge of files/folders
**Question:** When was EZtools opened?  <br>
**Answer:** `2021-12-01 13:00:34`  <br>
<img width="1318" height="498" alt="task 7 1" src="https://github.com/user-attachments/assets/3ae63e46-70e8-4ae3-bd8a-247fb3d4976a" />

Explanation: This timestamp (often from UserAssist or RunMRU) shows when the investigator or attacker opened forensic tools — useful to understand the sequence of actions.

🔍 How to find it:
1. Load the NTUSER.DAT hive (found in the user's profile folder)
2. Navigate to Software\Microsoft\Windows\CurrentVersion\Explorer\UserAssist
3. Check the GUID subkeys for EZtools execution

**Question:** At what time was My Computer last interacted with?
**Answer:** `2021-12-01 13:06:47`  <br>
<img width="1328" height="316" alt="task 7 2" src="https://github.com/user-attachments/assets/8ceb3e6f-78d2-4424-be7f-0ae6e8a5bb00" />

Explanation: This is typically recorded in the ShellBags or UserAssist keys.

🔍 How to find it:
1. Load the NTUSER.DAT hive
2. Navigate to Software\Microsoft\Windows\Shell\BagMRU or UserAssist
3. Look for entries related to "My Computer"

**Question:** What is the Absolute Path of the file opened using notepad.exe?  <br>
**Answer:** `C:\Program Files\Amazon\Ec2ConfigService\Settings`  <br>
<img width="1352" height="174" alt="task 7 3" src="https://github.com/user-attachments/assets/18832633-3c3b-4860-8157-6ff14f9b68f5" />

Explanation: Notepad.exe usage can reveal which configuration or log files an attacker viewed.

🔍 How to find it:
1. Load the NTUSER.DAT hive
2. Navigate to Software\Microsoft\Windows\CurrentVersion\Explorer\RecentDocs
3. Check for .txt files or look in UserAssist for notepad.exe executions

**Question:** When was this file opened?  <br>
**Answer:** `2021-11-30 10:56:19`  <br>
<img width="1353" height="191" alt="task 7 4" src="https://github.com/user-attachments/assets/f8714c8a-0712-4e69-861e-113f08af8b6e" />

📸 Where to find screenshots: 
- The room shows these key locations:
- The UserAssist key in NTUSER.DAT showing execution times
- ShellBags location for folder interactions
- RecentDocs showing recently opened files with timestamps
  
## Task 8: Evidence of Execution
**Question:** How many times was the File Explorer launched?  <br>
**Answer:** `26`  <br>
<img width="1775" height="478" alt="task 8 1" src="https://github.com/user-attachments/assets/8981859c-e1af-4b61-a136-d7f3a9c72e2e" />

Explanation: This is usually found in the UserAssist registry key, which tracks GUI application execution count and last run time.

🔍 How to find it:
1. Load the NTUSER.DAT hive
2. Navigate to Software\Microsoft\Windows\CurrentVersion\Explorer\UserAssist
3. Look for the GUID that references explorer.exe
4. The value data contains the count

**Question:** What is another name for ShimCache?  <br>
**Answer:** `AppCompatCache`  <br>
<img width="1462" height="220" alt="task 8 2" src="https://github.com/user-attachments/assets/b061e384-4592-4da4-9ba7-d954f01cfd2e" />

Explanation: ShimCache tracks executed applications and is very useful for identifying malware that ran on a system.

🔍 How to find it:
1. Load the SYSTEM hive
2. Navigate to SYSTEM\CurrentControlSet\Control\Session Manager\AppCompatCache
3. This data provides evidence of program execution

**Question:** Which of the artifacts also saves SHA1 hashes of the executed programs?  <br>
**Answer:** `AmCache`  <br>
<img width="1482" height="189" alt="task 8 4" src="https://github.com/user-attachments/assets/1848718b-88bb-45f4-a591-c0a2df0153a9" />

Explanation: AmCache is one of the richest sources for evidence of execution and often includes file hashes.

🔍 How to find it:
1. Locate the Amcache.hve file at C:\Windows\AppCompat\Programs\Amcache.hve
2. Load it in Registry Explorer
3. Browse to view execution entries with SHA1 hashes

**Question:** Which of the artifacts saves the full path of the executed programs?  <br>
**Answer:** `BAM/DAM`  <br>
<img width="1508" height="314" alt="task 8 5" src="https://github.com/user-attachments/assets/42694200-d51c-4bda-97fb-12e816cc6e5c" />

Explanation: Background Activity Moderator (BAM) and Desktop Activity Moderator (DAM) keys record full paths and last execution times for applications.

🔍 How to find it:
1. Load the SYSTEM hive
2. Navigate to SYSTEM\CurrentControlSet\Services\bam\State\UserSettings
3. Or check SYSTEM\CurrentControlSet\Services\dam\State\UserSettings

📸 Where to find screenshots: The room displays:
- UserAssist key with the count and execution times (showing the encoded format)
- AppCompatCache (ShimCache) data in the SYSTEM hive
- AmCache loaded in Registry Explorer showing SHA1 hashes
- BAM/DAM keys showing full executable paths

## Task 9: External Devices/USB device forensics 
**Question:** What is the serial number of the device from the manufacturer 'Kingston'?  <br>
**Answer:** `1C6f654E59A3B0C179D366AE&0` <br>
<img width="1767" height="241" alt="task 9 1" src="https://github.com/user-attachments/assets/29dc8dad-c041-4350-8ecc-45be4516ea31" />

Explanation: USB device serial numbers are stored in the SYSTEM hive under Enum\USBSTOR. They are excellent for tracking removable media.

🔍 How to find it:
1. Load the SYSTEM hive
2. Navigate to SYSTEM\CurrentControlSet\Enum\USBSTOR
3. Browse the subkeys to find the Kingston device

**Question:** What is the name of this device?  <br>
**Answer:** `Kingston Data Traveler 2.0 USB Device`  <br>
<img width="1786" height="286" alt="task 9 2" src="https://github.com/user-attachments/assets/afde7863-bf00-436a-a831-dc451184bada" />
🔍 How to find it:
1. Continue in the same location as above
2. The device name appears in the subkey details

**Question:** What is the friendly name of the device from the manufacturer 'Kingston'?  <br>
**Answer:** `USB`  <br>
<img width="1766" height="219" alt="task 9 3" src="https://github.com/user-attachments/assets/e441848f-e211-4908-9a96-1d78d74f24f7" />

Explanation: USB forensics helps determine if data was exfiltrated or if malware was introduced via removable media.

🔍 How to find it:
1. Load the SOFTWARE hive
2. Navigate to SOFTWARE\Microsoft\Windows Portable Devices\Devices
3. Find the entry matching the Kingston device

📸 Where to find screenshots: The room shows:
- The SYSTEM\CurrentControlSet\Enum\USBSTOR key with expanded subkeys showing Kingston devices
- The SOFTWARE\Microsoft\Windows Portable Devices\Devices key with friendly names
- Steps to cross-reference between both hives for complete device information

## Task 10: Hands-on Challenge
This challenge combines multiple artifacts (SAM hive for user accounts, AmCache for execution, USBSTOR for devices, etc.) to simulate a real investigation.

🔧 Tools to use: Registry Explorer (EZTools) is the primary tool for this challenge.
🎯 Recommended workflow:
- Load all necessary hives (SYSTEM, SOFTWARE, SAM, NTUSER.DAT, AmCache)
- Use the built-in search functionality to find specific artifacts
- Bookmark important findings for easy reference

**Question:** How many user created accounts are present on the system?  <br>
**Answer:** `3` <br>
<img width="928" height="355" alt="task 10 1" src="https://github.com/user-attachments/assets/cff1b81a-11ec-4f8e-a1b5-c76c384aa09b" />

🔍 How to find it:
1. Load the SAM hive
2. Navigate to SAM\Domains\Account\Users\Names
3. Count the user-created accounts (excluding built-in ones like Administrator and Guest)

**Question:** What is the username of the account that has never been logged in?  <br>
**Answer:** `thm-user2`  <br>
<img width="739" height="364" alt="task 10 2" src="https://github.com/user-attachments/assets/77c24a1e-d028-474f-9c50-12b9a342527d" />

🔍 How to find it:
1. In the SAM hive
2. Check each user's information in SAM\Domains\Account\Users
3. Look for the F key timestamp (empty or zero indicates never logged in)

**Question:** What's the password hint for the user THM-4n6?  <br>
**Answer:** `count`  <br>
<img width="576" height="503" alt="task 10 3" src="https://github.com/user-attachments/assets/eb31aaba-791f-4ebf-bf38-7d976388fd38" />

🔍 How to find it:
1. Load the SAM hive
2. Navigate to SAM\Domains\Account\Users\Names\THM-4n6
3. Look for the password hint value

**Question:** When was the file 'Changelog.txt' accessed?  <br>
**Answer:** `2021-11-21 18:18:48`  <br>
<img width="1326" height="422" alt="task 10 4" src="https://github.com/user-attachments/assets/36f4088e-6076-43b5-8e1c-aa6bc762c3f7" />

🔍 How to find it:
1. Load the NTUSER.DAT hive
2. Navigate to Software\Microsoft\Windows\CurrentVersion\Explorer\RecentDocs
3. Find the entry for 'Changelog.txt'

**Question:** What is the complete path from where the python 3.8.2 installer was run?  <br>
**Answer:** Z:\setups\python-3.8.2.exe`  <br>
<img width="1322" height="422" alt="task 10 5" src="https://github.com/user-attachments/assets/ee4f83aa-9fe5-459e-9ab7-146672f4dc50" />

🔍 How to find it:
1. Load the NTUSER.DAT hive
2. Navigate to Software\Microsoft\Windows\CurrentVersion\Explorer\UserAssist
3. Search for python-related entries
4. The full path is encoded in the value data

**Question:** When was the USB device with the friendly name 'USB' last connected?  <br>
Answer: 2021-11-24 18:40:06
<img width="1233" height="173" alt="task 10 6" src="https://github.com/user-attachments/assets/5bc62e19-91cd-4141-8bee-9a0cffe090f1" />

🔍 How to find it:
1. Load the SYSTEM hive
2. Navigate to SYSTEM\CurrentControlSet\Enum\USBSTOR
3. Find the Kingston device subkey
4. Look at the Properties key for the last connection timestamp

**Explanation for Task 10:** This challenge combines multiple artifacts (SAM hive for user accounts, AmCache for execution, USBSTOR for devices, etc.) to simulate a real investigation.

## Task 11: Conclusion
**Question:** Review the provided resources.  <br>
**Answer:** `No answer needed.`  <br>

## Conclusion
With my passion for digital forensics, I cannot describe how valuable this room was to my skill set. I had gone through this room a while ago and still enjoyed revisiting it. Solving mysteries through forensics is definitely my thing.
In this room, I mainly used Registry Explorer and EZTools for registry analysis. However, other important forensics tools every analyst should know include:
1. [FTK Imager](https://medium.com/@tojopthomas/ftk-imager-5df0c870074) – For creating forensic images and extracting files/hives.
2. [OSForensics](https://medium.com/@careertechnologymiraroad/osforensics-79d96202d5ef) – All-in-one tool for fast searching and registry analysis.
3. [Volatility](https://medium.com/@cyberengage.org/step-by-step-guide-to-uncovering-threats-with-volatility-a-beginners-memory-forensics-0213072b2bd8) – For memory forensics and analyzing RAM dumps.
4. [Wireshark](https://jacob-e-stickney.medium.com/wireshark-for-network-forensics-ecd2baa136cd) – For network forensics and traffic analysis.
5. [Autopsy / Sleuth Kit](https://www.sans.org/blog/a-step-by-step-introduction-to-using-the-autopsy-forensic-browser) – Open-source tools for disk and file system forensics.

Key Takeaway: Strong registry knowledge combined with the right tools is very powerful in digital investigations.
