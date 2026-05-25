# Linux Fundamentals Module Report
## Introduction
Linux powers the backbone of the modern internet — from web servers and cloud infrastructure to security tools and penetration testing labs. As a security analyst (or aspiring one), mastering Linux isn't optional; it's fundamental.

Compared to Windows, Linux offers greater transparency, customizability, and built-in security features. Its open-source nature lets you inspect, modify, and harden systems deeply — skills critical for threat hunting, incident response, forensics, and red teaming.

In this post, I'll share key takeaways from the **HackTheBox Linux Fundamentals module**, explain important concepts, and provide practical commands with cybersecurity context.

## Why Linux Matters in Cybersecurity

- **Servers & Infrastructure**: Most web servers, databases, and cloud instances run Linux.
- **Tools**: Kali Linux, tools like `nmap`, `Wireshark`, `Metasploit`, and SIEMs thrive on Linux.
- **Security Advantages**: Strong permission model, SELinux/AppArmor, easier auditing.
- **Job Relevance**: Many SOC, DFIR, and Blue Team roles require solid Linux CLI proficiency.

## Walkthrough
## Section: System Information
Question: Find out the machine hardware name and submit it as the answer.<br>
Answer: **x86_64**
<img width="1461" height="114" alt="1 1 system information" src="https://github.com/user-attachments/assets/a5e9c958-8711-49de-a8bc-16220eb73410" />
_Figure 1: using `uname -i` command to get the hardware architecture_


Question: What is the path to htb-student's home directory?<br>
Answer: **/home/htb-student**
<img width="1459" height="108" alt="1 2 system information" src="https://github.com/user-attachments/assets/ee321f30-f806-4091-b645-4720f7b4006d" />
_Fingure 2: using `pwd` to get the full path for htb_student's home directory. **pwd** in full stands for **print working directory**_

Question: What is the path to the htb-student's mail?<br>
Answer: **/var/mail/htb-student**
<img width="1458" height="111" alt="1 3 system information" src="https://github.com/user-attachments/assets/be75eff8-6a8a-494d-ba11-c495a788e657" />
_Figure 3: using `echo $MAIL` command to get the path. what the command does is look for the passed variable **$MAIL** return it's path_

Question: Which shell is specified for the htb-student user?<br>
Answer:**/bin/bash**
<img width="1460" height="104" alt="1 4 system information" src="https://github.com/user-attachments/assets/3d8219ee-41dc-4822-b10a-1421f8eb1eb2" />
_Figure 4: Using the command `echo $SHELL` to get the user specified bash. Command works the same as in previous question_

Question: Which kernel version is installed on the system? (Format: 1.22.3)
Answer: 4.15.0
<img width="1457" height="105" alt="1 5 system information" src="https://github.com/user-attachments/assets/f0c0f6b9-1a22-4092-92ce-6389840ff0bd" />

Question: What is the name of the network interface that MTU is set to 1500?
Answer: ens192
<img width="1460" height="504" alt="1 6 system information" src="https://github.com/user-attachments/assets/82842ce7-2f16-4fae-9124-9c503f233af7" />

## Section: Navigation
Question: What is the name of the hidden "history" file in the htb-user's home directory?
Answer: .bash_history
<img width="1459" height="311" alt="2 1 navigation" src="https://github.com/user-attachments/assets/cf006a93-c256-4dc6-9033-d2b63b27097c" />


Question: What is the index number of the "sudoers" file in the "/etc" directory?
Answer: 147627
<img width="1462" height="110" alt="2 2 navigation" src="https://github.com/user-attachments/assets/a84e3cfb-96f1-4ed3-af48-77b54f46224d" />


## Section: Working with Files and Directories
Question: What is the name of the last modified file in the "/var/backups" directory?
Answer: apt.extended_states.0
<img width="1460" height="831" alt="3 1 working with files and directories" src="https://github.com/user-attachments/assets/0acb235c-eaa3-43df-a60c-38fdfaae6d34" />


Question: What is the inode number of the "shadow.bak" file in the "/var/backups" 
directory?
Answer: 265293
<img width="1463" height="108" alt="3 2 working with files and directories" src="https://github.com/user-attachments/assets/b67645e1-39d3-439f-b84c-0348426f15b1" />


## Section: Find Files and Directories
Question: What is the name of the config file that has been created after 2020-03-03 and is 
smaller than 28k but larger than 25k?
Answer: 00-mesa-defaults.conf
<img width="1457" height="108" alt="4 1 files and directories" src="https://github.com/user-attachments/assets/062d32df-d79e-44a1-bfcd-d7dd10a8ea7c" />

Question: How many files exist on the system that have the ".bak" extension?
Answer: 4
<img width="1463" height="295" alt="4 2 files and directories" src="https://github.com/user-attachments/assets/28967212-1eea-4e87-855a-1118dfda5950" />

Question: Submit the full path of the "xxd" binary.
Answer: /usr/bin/xxd
<img width="1459" height="172" alt="4 3 files and directories" src="https://github.com/user-attachments/assets/eb9c9423-998a-41d0-93e8-7980bacb4b75" />

## Section: File Descriptors and Redirections
Question: How many files exist on the system that have the ".log" file extension?
Answer: 32
<img width="1458" height="114" alt="5 1 file descriptors and redirections" src="https://github.com/user-attachments/assets/6e5572e7-9695-47d2-bfbc-bab46436a1fd" />


Question: How many total packages are installed on the target system?
Answer: 737
<img width="1454" height="174" alt="5 2 file descriptors and redirections" src="https://github.com/user-attachments/assets/ded9c5d0-5ec6-451d-b6ab-c911b77ce5dc" />


## Section: Filter Contents
Question: Determine what user the ProFTPd server is running under. Submit the username 
as the answer.
Answer: proftpd
<img width="1461" height="187" alt="6 1 filtercontents" src="https://github.com/user-attachments/assets/08e95037-dc80-44ff-a65c-5c40e0dfb0c3" />


Question: Use cURL from your Pwnbox (not the target machine) to obtain the source code 
of the "https://www.inlanefreight.com" website and filter all unique paths of that domain. 
Submit the number of these paths as the answer.
Answer: 34
<img width="1464" height="125" alt="6 2 filtercontents" src="https://github.com/user-attachments/assets/5e48a0e9-929a-4b41-ab30-a475c92b13e3" />


## Section: User Management
Question: Which option needs to be set to create a home directory for a new user using 
"useradd" command?
Answer: -m
<img width="1432" height="871" alt="7 1 user management" src="https://github.com/user-attachments/assets/419aa1e7-a1b9-453b-a422-13866838cda9" />


Question: Which option needs to be set to lock a user account using the "usermod" 
command? (long version of the option)
Answer: --lock

Question: Which option needs to be set to execute a command as a different user using 
the "su" command? (long version of the option)
Answer: --command

## Section: Service and Process Management
Question: Use the "systemctl" command to list all units of services and submit the unit 
name with the description "Load AppArmor profiles managed internally by snapd" as the 
answer.
Answer: snapd.apparmor.service
<img width="1812" height="127" alt="8 1 service and process managent" src="https://github.com/user-attachments/assets/0495aee2-16e3-4d79-9544-79f1ed77a116" />


## Section: Task Scheduling
Question: What is the type of the service of the "syslog.service"?
Answer: notify
<img width="1330" height="103" alt="9 1 task scheduling" src="https://github.com/user-attachments/assets/12e1032f-eed9-40c6-9ca5-be46bee5a9e9" />

## Section: Working with Web Services
Question: Find a way to start a simple HTTP server inside Pwnbox or your local VM using 
"npm". Submit the command that starts the web server on port 8080 (use the short 
argument to specify the port number).
Answer: http-server -p 8080
<img width="808" height="388" alt="11 1 file system management" src="https://github.com/user-attachments/assets/65bf7e4f-2fea-409f-8c6a-f4ef7421056b" />


Question: Find a way to start a simple HTTP server inside Pwnbox or your local VM using 
"php". Submit the command that starts the web server on the localhost (127.0.0.1) on port 
8080.
Answer: php -S 127.0.0.1:8080
<img width="808" height="388" alt="image" src="https://github.com/user-attachments/assets/b7476e3a-5213-422c-932f-01d9ab8a10f1" />


## Section: File System Management
Question: How many partitions exist in our Pwnbox? (Format: 0)
Answer: 3
<img width="808" height="388" alt="image" src="https://github.com/user-attachments/assets/f624c86b-250f-474e-b2d3-f92fb5b23a18" />


Module Completion
Link: https://academy.hackthebox.com/achievement/1293352/18

## Conclusion
This module built a strong foundation in Linux CLI — essential for any cybersecurity career. The skills learned here will directly support log analysis, vulnerability scanning, incident response, and more.Next Recommendations:Practice on TryHackMe/HackTheBox Linux rooms.
Set up your own Kali/Parrot VM.
Learn Bash scripting basics.
Move to Linux Privilege Escalation module.
