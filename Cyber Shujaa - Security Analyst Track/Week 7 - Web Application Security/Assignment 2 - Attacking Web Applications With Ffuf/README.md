# Attacking Web Applications With FFUF Module Report
## Introduction
FFUF is a powerful tool for directory and parameter fuzzing/brute-forcing. In this module we learn how touse ffuf for the following cases:
- Fuzzing for directories.
- Fuzzing for files and extensions.
- Identifying hidden vhosts.
- Fuzzing for PHP parameters.
- Fuzzing for parameter values.
  
The module contains a skill assessment lab for practise. Below are the labs covered in the module and screenshots showing the answers.

## Walkthrough
## Section: Directory Fuzzing
Question: In addition to the directory we found above, there is another directory that can be found. What is it? <br>
Answer: **forum** <br>

<Additional directory discovered>
  
## Section: Page Fuzzing
Question: Try to use what you learned in this section to fuzz the '/blog' directory and find all pages. One of them should contain a flag. What is the flag? <br>
Answer: **HTB{bru73_f0r_c0mm0n_p455w0rd5}** <br>

<flag>
  
## Section: Recursive Fuzzing
Question: Try to repeat what you learned so far to find more files/directories. One of them should give you a flag. What is the content of the flag? <br>
Answer: **HTB{fuzz1n6_7h3_w3b!}** <br>
<flag>

## Section: Sub-domain Fuzzing
Question: Try running a sub-domain fuzzing test on 'inlanefreight.com' to find a customer sub-domain portal. What is the full domain of it? <br>
Answer: **customer.inlanefreight.com** <br>

<Customer sub-domain>
  
## Section: Filtering Results
Question: Try running a VHost fuzzing scan on 'academy.htb', and see what other VHosts you get. What other VHosts did you get? <br>
Answer: **test.academy.htb** <br>

<Other discovered vhost>
  
## Section: Parameter Fuzzing- GET
Question: Using what you learned in this section, run a parameter fuzzing scan on this page. what is the parameter accepted by this webpage? <br>
Answer: **user** <br>

<Accepted parameter>
  
## Section: Value Fuzzing
Question: ry to create the 'ids.txt' wordlist, identify the accepted value with a fuzzing scan, and then use it in a 'POST' request with 'curl' to collect the flag. What is the content of the flag? <br>
Answer: **HTB{p4r4m373r_fuzz1n6_15_k3y!}** <br>
<flag>

## Section: Skill Assessment- Web Fuzzing
Question: Run a sub-domain/vhost fuzzing scan on '*.academy.htb' for the IP shown above. What are all the sub-domains you can identify? (Only write the sub-domain name) <br>
Answer: **test,archive,faculty** <br>
<Discovered sub-domains>

## Question: Before you run your page fuzzing scan, you should first run an extension fuzzing scan. What are the different extensions accepted by the domains? <br>
Answer: **.php,.phps,.php7** <br>

<Discovered file extensions under test sub-domain> <br>
  
<Discovered file extensions under archive sub-domain> <br>
  
<Discovered file extensions under faculty sub-domain> <br>
  
Question: One of the pages you will identify should say 'You don't have access!'. What is the full page URL? <br>
Answer: **http://faculty.academy.htb:PORT/courses/linux-security.php7** <br>

<Url with no access permissions> <br>
  
Question: In the page from the previous question, you should be able to find multiple parameters that are accepted by the page. What are they? <br>
Answer: **user,username** <br>

<Discovered parameters>
  
Question: Try fuzzing the parameters you identified for working values. One of them should return a flag. What is the content of the flag? <br>
Answer: **HTB{w3b_fuzz1n6_m4573r}** <br>

<Final flag>
  
## Module Completion
Link: https://academy.hackthebox.com/achievement/1293352/54

## Conclusion
Wow!Ican’t describe how much knowledge I gained from this module. It was a good learning experiencing and will keep using tool in future Web Application Penetration Tests.
