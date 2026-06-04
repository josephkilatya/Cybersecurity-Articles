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

<Mentioned directory> <br>
  
Question: Navigate to the directory you found in question one. What file stands out as being likely to contain sensitive data? <br>
Answer: webapp.db <br>

<Exposed database file on server> <br>
  
Question: Use the supporting material to access the sensitive data. What is the password hash of the admin user? <br>
Answer: 6eea9b7ef19179a06954edd0f6c05ceb <br>

<Admin password hash found in the database file> <br>
  
Question: Crack the hash.What is the admin's plaintext password? <br>
Answer: qwertyuiop <br>

<Cracked admin password> <br>
  
Question: Log in as the admin. What is the flag? <br>
Answer: THM{Yzc2YjdkMjE5N2VjMzNhOTE3NjdiMjdl} <br>

<Admin flag> <br>
  
## Section: 3. Injection
Question: I've understood Injection attacks. <br>
Answer: No answer needed <br>

## Section: 3. 1. Command Injection
Question: What strange text file is in the website's root directory? <br>
Answer: drpepper.txt <br>

<strange text file in the website's root directory> <br>

Question: How many non-root/non-service/non-daemon users are there? <br>
Answer: 0 <br>

Question: What user is this app running as? <br>
Answer: apache <br>

<app user> <br>
  
Question: What is the user's shell set as? <br>
Answer: /sbin/nologin <br>

<Set user shell> <br>
  
Question: What version of Alpine Linux is running? <br>
Answer: 3.16.0 <br>

<running Alpine Linux version> <br>
  
## Section: 4. Insecure Design
Question: Try to reset joseph's password. Keep in mind the method used by the site to validate if you are indeed joseph. <br>
Answer: No answer needed <br>

Question: What is the value of the flag in joseph's account? <br>
Answer: THM{Not_3ven_c4tz_c0uld_sav3_U!} <br>

<Flag> <br>
  
## Section: 5. Security Misconfiguration
Question: Navigate to http://MACHINE_IP:86/console Werkzeug console <br>
Answer: No answer needed <br>

Question: Use the Werkzeug console to run the following Python code to execute the `ls-l` command on the server: `import os; print(os.popen("ls-l").read())` What is the database file name (the one with the .db extension) in the current directory? <br>
Answer: todo.db <br>

<Database file name> <br>
  
Question: Modify the code to read the contents of the app.py file, which contains the application's source code. What is the value of the secret_flag variable in the source code? <br>
Answer: THM{Just_a_tiny_misconfiguration} <br>

<Flag> <br>
  
## Section: 6. Vulnerable and Outdated Components
Question: Read about the vulnerability. <br>
Answer: No answer needed <br>

## Section: Vulnerable and Outdated Components- Exploit
Question: Read the above! <br>
Answer: No answer needed <br>

## Section: Vulnerable and Outdated Components- Lab
Question: What is the content of the /opt/flag.txt file? <br>
Answer: THM{But_1ts_n0t_my_f4ult!} <br>

<Flag> <br>
  
## Section: 7. Identification and Authentication Failures
Question: I've understood broken authentication mechanisms. <br>
Answer: No answer needed <br>

## Section: Identification and Authentication Failures Practical
Question: What is the flag that you found in darren's account? <br>
Answer: fe86079416a21a3c99937fea8874b667 <br>

<Darren’s flag> <br>

Question: Now try to do the same trick and see if you can log in as arthur. <br>
Answer: No answer needed <br>

Question: What is the flag that you found in arthur's account? <br>
Answer: d9ac0f7db4fda460ac3edeb75d75e16e <br>

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

<guest account password> <br>
  
Question: What is the name of the website's cookie containing a JWT token? <br>
Answer: jwt-session <br>

<JWT cookie name> <br>
  
Question: Use the knowledge gained in this task to modify the JWT token so that the application thinks you are the user "admin". <br>
Answer: No answer needed <br>

Question: What is the flag presented to the admin user? <br>
Answer: THM{Dont_take_cookies_from_strangers} <br>

<Flag> <br>
  
Section: 9. Security Logging and Monitoring
Question: What IP address is the attacker using? <br>
Answer: 49.99.13.16 <br>

<Attacker IP> <br>
  
Question: What kind of attack is being carried out? <br>
Answer: Brute Force <br>

## Section: Server-Side Request Forgery (SSRF)
Question: Explore the website. What is the only host allowed to access the admin area? <br>
Answer: localhost <br>

<Allowed host> <br>
  
Question: Check the "Download Resume" button. Where does the server parameter point to? <br>
Answer: secure-file-storage.com <br>

<Download server> <br>
  
Question: Using SSRF, make the application send the request to your AttackBox instead of the secure file storage. Are there any API keys in the intercepted request? <br>
Answer: THM{Hello_Im_just_an_API_key} <br>

<Flag> <br>
  
## Conclusion
Myexperience with this room was amazing. The room gave me a bigger picture on the OWASP Top 10- 2021. Testing Web Applications is fun, and guess who is going to have fun, me.
