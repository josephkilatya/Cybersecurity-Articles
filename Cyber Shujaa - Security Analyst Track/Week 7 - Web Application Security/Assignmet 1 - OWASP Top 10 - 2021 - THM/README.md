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
Question: Read the above.
Answer: No answer needed

## Section: Accessing Machines
Question: Connect to our network or deploy the AttackBox.
Answer: No answer needed

## Section: 1. Broken Access Control
Question: Read and understand what broken access control is.
Answer: No answer needed

## Section: Broken Access Control (IDOR Challenge)
Question: Read and understand how IDOR works.
Answer: No answer needed

Question: Deploy the machine and go to http://MACHINE_IP with the username noot and the password test1234
Answer: No answer needed

Question: Look at other users' notes. What is the flag?
Answer: flag{fivefourthree}

## Section: 2. Cryptographic Failures- Login
Question: Read the introduction to Cryptographic Failures and deploy the machine.
Answer: No answer needed

## Section: Cryptographic Failures (Supporting Material 1)
Question: Read and understand the supporting material on SQLite Databases.
Answer: No answer needed

## Section: Cryptographic Failures (Supporting Material 2)
Question: Read the supporting material about cracking hashes.
Answer: No answer needed

## Section: Cryptographic Failures (Challenge)
Question: Have a look around the web app. The developer has left themselves a note indicating that there is sensitive data in a
specific directory.What is the name of the mentioned directory?
Answer: /assets

<Mentioned directory>
  
Question: Navigate to the directory you found in question one. What file stands out as being likely to contain sensitive data?
Answer: webapp.db

<Exposed database file on server>
  
Question: Use the supporting material to access the sensitive data. What is the password hash of the admin user?
Answer: 6eea9b7ef19179a06954edd0f6c05ceb

<Admin password hash found in the database file>
  
Question: Crack the hash.What is the admin's plaintext password?
Answer: qwertyuiop

<Cracked admin password>
  
Question: Log in as the admin. What is the flag?
Answer: THM{Yzc2YjdkMjE5N2VjMzNhOTE3NjdiMjdl}

<Admin flag>
  
## Section: 3. Injection
Question: I've understood Injection attacks.
Answer: No answer needed

## Section: 3. 1. Command Injection
Question: What strange text file is in the website's root directory?
Answer: drpepper.txt

<strange text file in the website's root directory>

Question: How many non-root/non-service/non-daemon users are there?
Answer: 0

Question: What user is this app running as?
Answer: apache

<app user>
  
Question: What is the user's shell set as?
Answer: /sbin/nologin

<Set user shell>
  
Question: What version of Alpine Linux is running?
Answer: 3.16.0

<running Alpine Linux version>
  
## Section: 4. Insecure Design
Question: Try to reset joseph's password. Keep in mind the method used by the site to validate if you are indeed joseph.
Answer: No answer needed

Question: What is the value of the flag in joseph's account?
Answer: THM{Not_3ven_c4tz_c0uld_sav3_U!}

<Flag>
  
## Section: 5. Security Misconfiguration
Question: Navigate to http://MACHINE_IP:86/console Werkzeug console
Answer: No answer needed

Question: Use the Werkzeug console to run the following Python code to execute the `ls-l` command on the server:
`import os; print(os.popen("ls-l").read())`
What is the database file name (the one with the .db extension) in the current directory?
Answer: todo.db

<Database file name>
  
Question: Modify the code to read the contents of the app.py file, which contains the application's source code. What is the value of the secret_flag variable in the source code?
Answer: THM{Just_a_tiny_misconfiguration}

<Flag>
  
## Section: 6. Vulnerable and Outdated Components
Question: Read about the vulnerability.
Answer: No answer needed

## Section: Vulnerable and Outdated Components- Exploit
Question: Read the above!
Answer: No answer needed

## Section: Vulnerable and Outdated Components- Lab
Question: What is the content of the /opt/flag.txt file?
Answer: THM{But_1ts_n0t_my_f4ult!}

<Flag>
  
## Section: 7. Identification and Authentication Failures
Question: I've understood broken authentication mechanisms.
Answer: No answer needed

## Section: Identification and Authentication Failures Practical
Question: What is the flag that you found in darren's account?
Answer: fe86079416a21a3c99937fea8874b667

<Darren’s flag>

Question: Now try to do the same trick and see if you can log in as arthur.
Answer: No answer needed

Question: What is the flag that you found in arthur's account?
Answer: d9ac0f7db4fda460ac3edeb75d75e16e

<Arthur’s flag>

## Section: 8. Software and Data Integrity Failures
Question: Read the above and continue!
Answer: No answer needed

## Section: Software Integrity Failures
Question: What is the SHA-256 hash of https://code.jquery.com/jquery1.12.4.min.js?
Answer: sha256-ZosEbRLbNQzLpnKIkEdrPv7lOy9C27hHQ+Xp8a4MxAQ=

<SHA256 Hash value>
  
## Section: Data Integrity Failures
Question: Try logging into the application as guest. What is guest's account password?
Answer: guest

<guest account password>
  
Question: What is the name of the website's cookie containing a JWT token?
Answer: jwt-session

<JWT cookie name>
  
Question: Use the knowledge gained in this task to modify the JWT token so that the application thinks you are the user "admin".
Answer: No answer needed

Question: What is the flag presented to the admin user?
Answer: THM{Dont_take_cookies_from_strangers}

<Flag>
  
Section: 9. Security Logging and Monitoring
Question: What IP address is the attacker using?
Answer: 49.99.13.16

<Attacker IP>
  
Question: What kind of attack is being carried out?
Answer: Brute Force

## Section: Server-Side Request Forgery (SSRF)
Question: Explore the website. What is the only host allowed to access the admin area?
Answer: localhost

<Allowed host>
  
Question: Check the "Download Resume" button. Where does the server parameter point to?
Answer: secure-file-storage.com

<Download server>
  
Question: Using SSRF, make the application send the request to your AttackBox instead of the secure file storage. Are there any API keys
in the intercepted request?
Answer: THM{Hello_Im_just_an_API_key}

<Flag>
  
## Conclusion
Myexperience with this room was amazing. The room gave me a bigger picture on the OWASP Top 10- 2021. Testing Web Applications is fun, and guess who is going to have fun, me.
