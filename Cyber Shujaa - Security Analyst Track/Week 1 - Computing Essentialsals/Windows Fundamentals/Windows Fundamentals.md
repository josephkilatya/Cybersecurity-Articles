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
_Screenshot showing powershell command to get build number and Windows NT version_


### Section: Operating System Structure

**Question:** Find the non-standard directory in the C drive. Submit the contents of the flag file saved in this directory.  
**Answer:** `c8fe8d977d3a0c655ed7cf81e4d13c75`

<img width="1081" height="975" alt="2 1 operating system structure answer" src="https://github.com/user-attachments/assets/dae52f47-deb8-4c5f-a81a-055add221e7e" />

_Screenshot showing steps and command to get the flag_

### Section: File System

**Question:** What system user has full control over the `C:\Users` directory?  
**Answer:** `bob.smith`

<img width="1099" height="374" alt="file system" src="https://github.com/user-attachments/assets/4ab1bde5-4213-4cbc-a68a-cd55b7875b55" />
_Screenshot showing how to get users control right using `icacls` command_


### Section: NTFS vs. Share Permissions

**Question:** What protocol discussed in this section is used to share resources on the network using Windows? (Format: case sensitive)  
**Answer:** `SMB`

<img width="1920" height="1080" alt="4 1 ntfs vs share permissons" src="https://github.com/user-attachments/assets/4bffba42-92d3-46a2-9935-45a77aef7ce1" />
_Screenshot showing filesharing protocol used in Windows Systems_

### Section: Logs & Shares

**Question:** What is the name of the utility that can be used to view logs made by a Windows system? (Format: 2 words, 1 space, not case sensitive)  
**Answer:** `Event Viewer`

**Question:** What is the full directory path to the Company Data share we created?  
**Answer:** `C:\Users\htb-student\Desktop\Company Data`

### Section: Windows Services & Processes

**Question:** Identify one of the non-standard update services running on the host. Submit the full name of the service executable (not the DisplayName) as your answer.  
**Answer:** `FoxitReaderUpdateService.exe`

### Section: Interacting with the Windows Operating System

**Question:** What is the alias set for the `ipconfig.exe` command?  
**Answer:** `ifconfig`

**Question:** Find the Execution Policy set for the LocalMachine scope.  
**Answer:** `Unrestricted`

### Section: Windows Management Instrumentation (WMI)

**Question:** Use WMI to find the serial number of the system.  
**Answer:** `00329-10280-00000-AA938`

### Section: Windows Security

**Question:** Find the SID of the `bob.smith` user.  
**Answer:** `S-1-5-21-2614195641-1726409526-3792725429-1003`

**Question:** What 3rd party security application is disabled at startup for the current user? (The answer is case sensitive).  
**Answer:** `NordVPN`

### Section: Skills Assessment - Windows Fundamentals

**Question:** What is the name of the group that is present in the Company Data Share Permissions ACL by default?  
**Answer:** `Everyone`

**Question:** What is the name of the tab that allows you to configure NTFS permissions?  
**Answer:** `Security`

**Question:** What is the name of the service associated with Windows Update?  
**Answer:** `wuauserv`

**Question:** List the SID associated with the user account Jim you created.  
**Answer:** `S-1-5-21-2614195641-1726409526-3792725429-1006`

**Question:** List the SID associated with the HR security group you created.  
**Answer:** `S-1-5-21-2614195641-1726409526-3792725429-1007`

## Module Completion

**Achievement Link:** [https://academy.hackthebox.com/achievement/1293352/49](https://academy.hackthebox.com/achievement/1293352/49)

## Conclusion

The knowledge covered in this module is highly valuable. Although I previously believed I had a good understanding of Microsoft Windows, this module revealed many deeper aspects worth exploring. My favorite part was learning to leverage PowerShell for various administrative and investigative tasks.

This module has significantly increased my confidence in working with Windows environments. These skills are crucial for troubleshooting, system hardening, and performing effective analysis during incident response as a security analyst.

---

**Report Prepared:** May 2026  
**Student:** [Your Name]
