# Windows Fundamentals Module Report

## Introduction

This module introduces the learner to the world of Microsoft Windows, one of the most widely used operating systems globally. Due to its popularity, Windows is a frequent target for threat actors, making it essential for security analysts to understand its architecture, identify vulnerabilities, and defend against attacks.

The module provides a high-level overview of Microsoft Windows, covering the history of the operating system, its structure, file system, and permissions. It also teaches how to interact with processes and services using PowerShell, with special focus on the `Get-WmiObject` cmdlet. Security aspects are emphasized throughout, particularly user permissions and system hardening — critical skills for any security professional.

## Walkthrough

### Section: Introduction to Windows

**Question:** What is the Build Number of the target workstation?  
**Answer:** `19041`

**Question:** Which Windows NT version is installed on the workstation? (i.e. Windows X - case sensitive)  
**Answer:** `Windows 10`

<img width="983" height="834" alt="1 1 introduction answer" src="https://github.com/user-attachments/assets/c46521a7-3515-434a-ab29-bd9ff17b0343" />

_Screenshot showing PowerShell command to get build number and Windows NT version_


### Section: Operating System Structure

**Question:** Find the non-standard directory in the C drive. Submit the contents of the flag file saved in this directory.  
**Answer:** `c8fe8d977d3a0c655ed7cf81e4d13c75`

<img width="1081" height="975" alt="2 1 operating system structure answer" src="https://github.com/user-attachments/assets/dae52f47-deb8-4c5f-a81a-055add221e7e" />

_Screenshot showing steps and PowerShell commands to get the flag_

### Section: File System

**Question:** What system user has full control over the `C:\Users` directory?  
**Answer:** `bob.smith`

<img width="1099" height="374" alt="file system" src="https://github.com/user-attachments/assets/4ab1bde5-4213-4cbc-a68a-cd55b7875b55" />
_Screenshot showing how to get users control right using `icacls` command_


### Section: NTFS vs. Share Permissions

**Question:** What protocol discussed in this section is used to share resources on the network using Windows? (Format: case sensitive)  
**Answer:** `SMB`

<img width="1920" height="1080" alt="4 1 ntfs vs share permissons" src="https://github.com/user-attachments/assets/9915bad1-4aff-4f32-ad4f-2cf8375e8d5d" />

_Screenshot showing filesharing protocol used in Windows Systems_

**Question:** What is the name of the utility that can be used to view logs made by a Windows system? (Format: 2 words, 1 space, not case sensitive)  
**Answer:** `Event Viewer`

<img width="1920" height="1079" alt="4 2 ntfs vs share permission answer" src="https://github.com/user-attachments/assets/38010d4a-1ae1-4b29-a20d-9fe713346448" />

_Screenshot showing utility to view Windows Event Logs. **Event Viewer** utility is useful tool during Windows DFIR_

**Question:** What is the full directory path to the Company Data share we created?  
**Answer:** `C:\Users\htb-student\Desktop\Company Data`

<img width="1920" height="1080" alt="4 3 ntfs vs share permission answer" src="https://github.com/user-attachments/assets/9c6dd6c6-142e-40af-b409-51aed671b75b" />

_Screenshot showing directory full path to **Company Data** share_

### Section: Windows Services & Processes

**Question:** Identify one of the non-standard update services running on the host. Submit the full name of the service executable (not the DisplayName) as your answer.  
**Answer:** `FoxitReaderUpdateService.exe`

<img width="1102" height="984" alt="5  1 windows service and processes answer" src="https://github.com/user-attachments/assets/cb05580f-2351-48d6-af04-b6885264cdd4" />

_Screenshot showing Command to runnig services on the system while identifying the non-standard update service **FoxitReaderUpdateService.exe**. Useful command during Windows DFIR to view non-standard installed/running services (malware)_


### Section: Interacting with the Windows Operating System

**Question:** What is the alias set for the `ipconfig.exe` command?  
**Answer:** `ifconfig`

<img width="1104" height="1009" alt="6 1 interacting with windows os answer" src="https://github.com/user-attachments/assets/61ce519d-8b5e-46f6-802e-b36b2f91084e" />

_Screenshot showing `ifconfig` as the alias for **ipconfig.exe**_

**Question:** Find the Execution Policy set for the LocalMachine scope.  
**Answer:** `Unrestricted`

<img width="1100" height="560" alt="6 2 interacting with windows os answer" src="https://github.com/user-attachments/assets/0367175d-5ea6-4ed7-84b5-56e411e2db8d" />

_Screenshot shwoing command to get the **ExecutionPolicy** for the LocalMachine_

### Section: Windows Management Instrumentation (WMI)

**Question:** Use WMI to find the serial number of the system.  
**Answer:** `00329-10280-00000-AA938`

<img width="1101" height="211" alt="7 1 windows management instrumentation" src="https://github.com/user-attachments/assets/e1d76167-d134-4ea7-bcf8-17ee95d08cc2" />

_Screenshot showing **WMI** command to get the operating system serial number_


### Section: Windows Security

**Question:** Find the SID of the `bob.smith` user.  
**Answer:** `S-1-5-21-2614195641-1726409526-3792725429-1003`

<img width="1097" height="544" alt="81  windows security" src="https://github.com/user-attachments/assets/c7f143b2-c77f-436f-a327-877a35612869" />

_Screenshot showing command to get user bob.smith **SID**_

**Question:** What 3rd party security application is disabled at startup for the current user? (The answer is case sensitive).  
**Answer:** `NordVPN`

_Screenshot showing 3rd party security application disabled at startup from **Task Mananger's Startup** tab_

<img width="897" height="593" alt="8 2 windows security" src="https://github.com/user-attachments/assets/3c893fd1-75e5-4b73-81d2-ab2f4e2de832" />

### Section: Skills Assessment - Windows Fundamentals

**Question:** What is the name of the group that is present in the Company Data Share Permissions ACL by default?  
**Answer:** `Everyone`

<img width="1919" height="1078" alt="1 1 group" src="https://github.com/user-attachments/assets/fcb957d7-3a8e-42d1-a315-1260066e34fb" />

_Screenshot showing group with access to **Company Data Share**, Everyone_

**Question:** What is the name of the tab that allows you to configure NTFS permissions?  
**Answer:** `Security`

<img width="527" height="562" alt="security tab" src="https://github.com/user-attachments/assets/0e4975da-b9d2-4fd2-81d2-40bf1ad507f6" />

_Screenshot showing share properties tab used to configure NTFS permissions_

**Question:** What is the name of the service associated with Windows Update?  
**Answer:** `wuauserv`

<img width="1102" height="548" alt="1 2 windows update" src="https://github.com/user-attachments/assets/2b18600c-c28c-4a63-9f72-3e441d12fe62" />

_Screenshot showing command to get the service associated with Windows Update_

**Question:** List the SID associated with the user account Jim you created.  
**Answer:** `S-1-5-21-2614195641-1726409526-3792725429-1006`

<img width="1100" height="594" alt="1 3 jim sid" src="https://github.com/user-attachments/assets/39aa2124-b841-4d54-8763-0d5831e2e3f9" />

_Screenshot showing command to get user Jim's **SID**_

**Question:** List the SID associated with the HR security group you created.  
**Answer:** `S-1-5-21-2614195641-1726409526-3792725429-1007`

<img width="1097" height="681" alt="1 4 group sid" src="https://github.com/user-attachments/assets/a057d29f-03b9-48a8-bfcf-de534199740a" />

_Screenshot showing Command to get **HR** group **SID**_

## Module Completion

**Achievement Link:** [https://academy.hackthebox.com/achievement/1293352/49](https://academy.hackthebox.com/achievement/1293352/49)

## Conclusion

The knowledge covered in this module is highly valuable. Although I previously believed I had a good understanding of Microsoft Windows, this module revealed many deeper aspects worth exploring. My favorite part was learning to leverage PowerShell for various administrative and investigative tasks.

This module has significantly increased my confidence in working with Windows environments. These skills are crucial for troubleshooting, system hardening, and performing effective analysis during incident response as a security analyst.

---

**Report Prepared:** May 2024  
