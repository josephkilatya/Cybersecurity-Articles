# Linux Fundamentals Module Report
## Introduction
Linux is an open-source operating system that has revolutionized the world of free software. It is widely used in cloud servers, embedded systems, routers, smartphones (Android OS), and more. Compared to Microsoft Windows, Linux is generally more secure, and its open-source nature allows users to customize the operating system to meet specific needs.

For these reasons, Linux has become an invaluable tool for cybersecurity researchers and is widely adopted in the field. This module covers the essential Linux skills required for security work.

## Walkthrough
## Section: System Information
Question: Find out the machine hardware name and submit it as the answer.
Answer: x86_64
<img width="1461" height="114" alt="1 1 system information" src="https://github.com/user-attachments/assets/a5e9c958-8711-49de-a8bc-16220eb73410" />


Question: What is the path to htb-student's home directory?
Answer: /home/htb-student
<img width="1459" height="108" alt="1 2 system information" src="https://github.com/user-attachments/assets/ee321f30-f806-4091-b645-4720f7b4006d" />


Question: What is the path to the htb-student's mail?
Answer: /var/mail/htb-student
<img width="1458" height="111" alt="1 3 system information" src="https://github.com/user-attachments/assets/be75eff8-6a8a-494d-ba11-c495a788e657" />

Question: Which shell is specified for the htb-student user?
Answer: /bin/bash
<img width="1460" height="104" alt="1 4 system information" src="https://github.com/user-attachments/assets/3d8219ee-41dc-4822-b10a-1421f8eb1eb2" />

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
This module was highly educational and provided deep insights into using and working with Linux. Key topics covered include:
- History of Linux
- Linux file system organization
- Shell operation and usage
- File system navigation
- Networking with Linux
- User management in Linux environments
- Security hardening in Linux

This learning experience has been valuable, and the skills acquired will be instrumental in my future career as a security analyst.
