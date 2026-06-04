#OWASP Top 10 - 2021 - THM
## Introduction
This TryHackMe room covers the OWASP Top 10- 2021at a beginner level. The content is well explained making it easy to read and understand. The OWASP top 10 covers the following:
Broken Access Control
2. Cryptographic Failure
3. Injection
4. Insecure Design
5. Security Misconfiguration
6. Vulnerable and Outdated Components
7. Identification and Authentication Failures
8. Software and Data Integrity Failures
9. Security Logging and Monitoring
10. Server-Side Request Forgery (SSRF)

This sections are not only clearly explained, but there are also labs for practice in this room. The following sections answers the questions asked in the room labs.

## Walkthrough
## Section: Introduction
Question: Read the above. <br>
Answer: No answer needed <br>

## Section: Accessing Machines
Question: Connect to our network or deploy the AttackBox. <br>
Answer: No answer needed <br>

## Section: 1. Broken Access Control
Question: Read and understand what broken access control is. <br>
Answer: No answer needed <br>

## Section: Broken Access Control (IDOR Challenge)
Question: Read and understand how IDOR works. <br>
Answer: No answer needed <br>

Question: Deploy the machine and go to http://MACHINE_IP with the username noot and the password test1234 <br>
Answer: No answer needed <br>

Question: Look at other users' notes. What is the flag? <br>
Answer: flag{fivefourthree} <br>
<img width="959" height="525" alt="IDOR hint" src="https://github.com/user-attachments/assets/3a8617a5-8f72-4bab-876a-c794da89cdc7" />

<img width="947" height="497" alt="IDOR flag" src="https://github.com/user-attachments/assets/2eebe6d3-5ea8-46b2-9dc4-2c8ae633a0e5" />
## Section: 2. Cryptographic Failures- Login
Question: Read the introduction to Cryptographic Failures and deploy the machine. <br>
Answer: No answer needed <br>

## Section: Cryptographic Failures (Supporting Material 1)
Question: Read and understand the supporting material on SQLite Databases. <br>
Answer: No answer needed <br>

## Section: Cryptographic Failures (Supporting Material 2)
Question: Read the supporting material about cracking hashes. <br>
Answer: No answer needed <br>

## Section: Cryptographic Failures (Challenge)
Question: Have a look around the web app. The developer has left themselves a note indicating that there is sensitive data in a
specific directory.What is the name of the mentioned directory? <br>
Answer: /assets <br>
<img width="835" height="407" alt="crypto - dir namew" src="https://github.com/user-attachments/assets/e30c93a3-e9ba-49e5-9448-75e5e807bd6e" />
<Mentioned directory> <br>
  
Question: Navigate to the directory you found in question one. What file stands out as being likely to contain sensitive data? <br>
Answer: webapp.db <br>
<img width="653" height="225" alt="crypto - db file name" src="https://github.com/user-attachments/assets/03e864d4-6b1c-4707-b493-4767bfa21f93" />
<Exposed database file on server> <br>
  
Question: Use the supporting material to access the sensitive data. What is the password hash of the admin user? <br>
Answer: 6eea9b7ef19179a06954edd0f6c05ceb <br>
<img width="786" height="103" alt="crypto - admin hash" src="https://github.com/user-attachments/assets/9bd3f4fb-32be-4c4a-8b83-43aa41c49d1f" />
<Admin password hash found in the database file> <br>
  
Question: Crack the hash.What is the admin's plaintext password? <br>
Answer: qwertyuiop <br>
<img width="1060" height="290" alt="crypto - admin password" src="https://github.com/user-attachments/assets/0705394f-b3be-4548-afab-5eb495e7c738" />
<Cracked admin password> <br>
  
Question: Log in as the admin. What is the flag? <br>
Answer: THM{Yzc2YjdkMjE5N2VjMzNhOTE3NjdiMjdl} <br>
<img width="752" height="287" alt="crypto - admin flag" src="https://github.com/user-attachments/assets/191521b9-a508-4f3e-9633-fb18f78a4719" />

<Admin flag> <br>
  
## Section: 3. Injection
Question: I've understood Injection attacks. <br>
Answer: No answer needed <br>

## Section: 3. 1. Command Injection
Question: What strange text file is in the website's root directory? <br>
Answer: drpepper.txt <br>
<img width="625" height="371" alt="command injection - strange file" src="https://github.com/user-attachments/assets/9a8f94c5-3124-4adf-8184-6af8db821712" />
<strange text file in the website's root directory> <br>

Question: How many non-root/non-service/non-daemon users are there? <br>
Answer: 0 <br>

Question: What user is this app running as? <br>
Answer: apache <br>
<img width="630" height="437" alt="command injection - app user" src="https://github.com/user-attachments/assets/78b0391b-8d77-4839-8a71-7a0b55b9aae7" />
<app user> <br>
  
Question: What is the user's shell set as? <br>
Answer: /sbin/nologin <br>
<img width="585" height="429" alt="command injection - set user shell" src="https://github.com/user-attachments/assets/213d86fe-b11e-49fd-823b-c4794d19cfec" />
<Set user shell> <br>
  
Question: What version of Alpine Linux is running? <br>
Answer: 3.16.0 <br>
<img width="572" height="389" alt="command injection - alpine version" src="https://github.com/user-attachments/assets/b0b2ceac-6cf2-4c33-a36e-71d5a362d142" />
<running Alpine Linux version> <br>
  
## Section: 4. Insecure Design
Question: Try to reset joseph's password. Keep in mind the method used by the site to validate if you are indeed joseph. <br>
Answer: No answer needed <br>
<img width="1907" height="594" alt="insecure design - joseph password" src="https://github.com/user-attachments/assets/3e01df06-d61a-4daf-8d2c-5b5c98d32231" />

Question: What is the value of the flag in joseph's account? <br>
Answer: THM{Not_3ven_c4tz_c0uld_sav3_U!} <br>
<img width="851" height="380" alt="insecure design - flag" src="https://github.com/user-attachments/assets/f9fc3fe6-90b3-4f5a-9ecb-c71232dcceef" />
<Flag> <br>
  
## Section: 5. Security Misconfiguration
Question: Navigate to http://MACHINE_IP:86/console Werkzeug console <br>
Answer: No answer needed <br>

Question: Use the Werkzeug console to run the following Python code to execute the `ls-l` command on the server: `import os; print(os.popen("ls-l").read())` What is the database file name (the one with the .db extension) in the current directory? <br>
Answer: todo.db <br>
<img width="1177" height="354" alt="security misconfiguration - ls -l output" src="https://github.com/user-attachments/assets/7f1dc5df-110f-4b1a-bf62-b3e440757c53" />
<Database file name> <br>
  
Question: Modify the code to read the contents of the app.py file, which contains the application's source code. What is the value of the secret_flag variable in the source code? <br>
Answer: THM{Just_a_tiny_misconfiguration} <br>
<img width="1196" height="619" alt="security misconfiguration - flag" src="https://github.com/user-attachments/assets/261c4d22-095b-471c-9ff4-a7fd73970186" />
<Flag> <br>
  
## Section: 6. Vulnerable and Outdated Components
Question: Read about the vulnerability. <br>
Answer: No answer needed <br>

## Section: Vulnerable and Outdated Components- Exploit
Question: Read the above! <br>
Answer: No answer needed <br>
<img width="1890" height="199" alt="outdated - searchsploit" src="https://github.com/user-attachments/assets/d40b9e62-8047-48bf-b919-da01f1968c5a" />

## Section: Vulnerable and Outdated Components- Lab
Question: What is the content of the /opt/flag.txt file? <br>
Answer: THM{But_1ts_n0t_my_f4ult!} <br>
<img width="762" height="137" alt="outdated - flag" src="https://github.com/user-attachments/assets/c0a336e0-27a6-4c17-98b3-775813c94a35" />

<Flag> <br>
  
## Section: 7. Identification and Authentication Failures
Question: I've understood broken authentication mechanisms. <br>
Answer: No answer needed <br>

## Section: Identification and Authentication Failures Practical
Question: What is the flag that you found in darren's account? <br>
Answer: fe86079416a21a3c99937fea8874b667 <br>
<img width="1543" height="214" alt="id and auth - darren flag" src="https://github.com/user-attachments/assets/e790e08b-561a-4dcb-b61f-4aa7085edba4" />
<Darren’s flag> <br>

Question: Now try to do the same trick and see if you can log in as arthur. <br>
Answer: No answer needed <br>

Question: What is the flag that you found in arthur's account? <br>
Answer: d9ac0f7db4fda460ac3edeb75d75e16e <br>
<img width="1542" height="199" alt="id and auth - arther flag" src="https://github.com/user-attachments/assets/9876ab20-ef57-47f2-9cbd-5535a1d6c606" />
<Arthur’s flag> <br>

## Section: 8. Software and Data Integrity Failures
Question: Read the above and continue! <br>
Answer: No answer needed <br>

## Section: Software Integrity Failures
Question: What is the SHA-256 hash of https://code.jquery.com/jquery1.12.4.min.js? <br>
Answer: sha256-ZosEbRLbNQzLpnKIkEdrPv7lOy9C27hHQ+Xp8a4MxAQ= <br>

<SHA256 Hash value> <br>
  
## Section: Data Integrity Failures
Question: Try logging into the application as guest. What is guest's account password? <br>
Answer: guest <br>
<img width="388" height="497" alt="data integrity failures - guest password" src="https://github.com/user-attachments/assets/b9de6f9a-0362-46ea-9ed7-81d948328987" />
<guest account password> <br>
  
Question: What is the name of the website's cookie containing a JWT token? <br>
Answer: jwt-session <br>
<img width="1080" height="378" alt="data integrity failures - jwt cookie name" src="https://github.com/user-attachments/assets/9e4c9636-cc7d-4dc8-ad94-4c2ba2152cdf" />
<JWT cookie name> <br>
  
Question: Use the knowledge gained in this task to modify the JWT token so that the application thinks you are the user "admin". <br>
Answer: No answer needed <br>

Question: What is the flag presented to the admin user? <br>
Answer: THM{Dont_take_cookies_from_strangers} <br>
<img width="1620" height="704" alt="data integrity failures - flag" src="https://github.com/user-attachments/assets/2b318951-c2b7-4369-a848-6559e52d1f60" />
<Flag> <br>
  
Section: 9. Security Logging and Monitoring
Question: What IP address is the attacker using? <br>
Answer: 49.99.13.16 <br>
<img width="939" height="233" alt="security logging and monitoring - attacker ip" src="https://github.com/user-attachments/assets/d2147374-425e-4622-a1b2-e17c17312599" />
<Attacker IP> <br>
  
Question: What kind of attack is being carried out? <br>
Answer: Brute Force <br>

## Section: Server-Side Request Forgery (SSRF)
Question: Explore the website. What is the only host allowed to access the admin area? <br>
Answer: localhost <br>
<img width="776" height="138" alt="ssrf - host allowed by admin area" src="https://github.com/user-attachments/assets/62c8c69f-9119-46d6-8732-bb7f808dd8aa" />
<Allowed host> <br>
  
Question: Check the "Download Resume" button. Where does the server parameter point to? <br>
Answer: secure-file-storage.com <br>
<img width="1346" height="355" alt="ssrf download server" src="https://github.com/user-attachments/assets/8be46110-e9a7-4775-9b87-c3781e0cf1ba" />
<Download server> <br>
  
Question: Using SSRF, make the application send the request to your AttackBox instead of the secure file storage. Are there any API keys in the intercepted request? <br>
Answer: THM{Hello_Im_just_an_API_key} <br>
<img width="767" height="184" alt="ssrf - final flag" src="https://github.com/user-attachments/assets/479fd37d-6f3a-4d6b-9144-fbb1d220cc37" />
<Flag> <br>
  
## Conclusion
Myexperience with this room was amazing. The room gave me a bigger picture on the OWASP Top 10- 2021. Testing Web Applications is fun, and guess who is going to have fun, me.
