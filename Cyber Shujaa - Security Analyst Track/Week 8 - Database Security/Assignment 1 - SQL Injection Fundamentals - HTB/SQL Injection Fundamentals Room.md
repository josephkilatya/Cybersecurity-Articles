# SQL Injection Fundamentals
## Introduction
This modules teaches us the fundamentals required to perform SQL injection. The module covers, but not limited to, the following:
Whatdatabasesare,howthey workandthedifferent types of databases, that is relational and non-relational databases.
- How to connect to MySQL database using the mysql command-line utility.
- How to performdifferent queries on theDBMS.
- How to perform different types of SQL injection attacks such as authentication bypass, querying databases to read and write data and more advanced techniques.
  
The module includes labs for practice with a final security assessment lab. The following section covers the labs’ questions and answers with screenshots supporting the the answers.

## Walkthrough
## Section: Intro to MySQL
Question: Connect to the database using the MySQL client from the command line. Use the 'show databases;' command to list databases in the DBMS. What is the name of the first database? <br>
Answer: **employees** <br>
<img width="606" height="280" alt="show databases" src="https://github.com/user-attachments/assets/86d91cf5-a677-448a-82ed-7e2ab689ffe8" />
**Name of first database shown in screen-shot above**

## Section: SQL Statements
Question: What is the department number for the 'Development' department? <br>
Answer: **d005** <br>
<img width="545" height="306" alt="development department id" src="https://github.com/user-attachments/assets/33ea3e73-8378-4296-84b3-9700768e2020" />
_Development' department number_

## Section: Query Results
Question: What is the last name of the employee whose first name starts with "Bar" AND who was hired on 1990-01-01? <br>
Answer: **Mitchem** <br>
<img width="1054" height="158" alt="Bar employee" src="https://github.com/user-attachments/assets/6ef6f29d-3360-4467-a422-b22553946a25" />
_Query results_

## SQL Operations
Question: In the 'titles' table, what is the number of records WHERE the employee number is greater than 10000 OR their title does NOT contain 'engineer'? <br>
Answer: **654** <br>
<img width="595" height="532" alt="sql operators" src="https://github.com/user-attachments/assets/5077ff05-d546-42bb-9bc1-3c65fc551372" />
_Number of records shown_ <br>
  
## Section: Subverting Query Logic
Question: Try to log in as the user 'tom'. What is the flag value shown after you successfully log in? <br>
Answer: **202a1d1a8b195d5e9a57e434cc16000c** <br>
<img width="1198" height="441" alt="subverting query logic" src="https://github.com/user-attachments/assets/d475f317-232d-4a0a-bdd8-a87398d4a8ea" />
_User tom flag_ <br>
  
## Section: Using Comments
Question: Login as the user with the id 5 to get the flag. <br>
Answer: **cdad9ecdf6f14b45ff5c4de32909caec** <br>
<img width="1240" height="457" alt="using comments" src="https://github.com/user-attachments/assets/c9378f16-b18d-46b1-be10-0c2f65c46fdc" />
_Flag_
  
## Section: Union Clause
Question: Connect to the above MySQL server with the 'mysql' tool, and find the number of records returned when doing a 'Union' of all records in the 'employees' table and all records in the 'departments' table. <br>
Answer: **663** <br>
<img width="726" height="80" alt="union - number of records" src="https://github.com/user-attachments/assets/95a15ace-e507-4759-88c5-23b72451ac8a" />
_Total number of records shown_
  
## Section: Union Injection
Question: Use a Union injection to get the result of 'user()' <br>
Answer: **root@localhost** <br>
<img width="1094" height="347" alt="union injection" src="https://github.com/user-attachments/assets/602efb9b-72bb-452b-bf30-76f370c8a399" />
_User found_
  
## Database Enumeration
Question: What is the password hash for 'newuser' stored in the 'users' table in the 'ilfreight' database? <br>
Answer: **9da2c9bcdf39d8610954e0e11ea8f45f** <br>
<img width="1244" height="386" alt="database enumeration" src="https://github.com/user-attachments/assets/fa411d39-4157-420c-91d4-8e17ca779518" />
_newuser password_
  
## Section: Reading Files
Question: We see in the above PHP code that '$conn' is not defined, so it must be imported using the PHP include command. Check the imported page to obtain the database password. <br>
Answer: **dB_pAssw0rd_iS_flag!** <br>
<img width="1254" height="505" alt="reading files" src="https://github.com/user-attachments/assets/a50ee859-accc-40f7-85b4-ac0ad0e34d76" />
_Flag_
  
## Section: Writing Files
Question: Find the flag by using a webshell. <br>
Answer: **d2b5b27ae688b6a0f1d21b7d3a0798cd** <br>
<img width="897" height="148" alt="writing files" src="https://github.com/user-attachments/assets/f50c4414-db5b-4031-b408-4be66a5ecee4" />
_Flag_
  
## Section: Skills Assessment- SQL Injection Fundamentals
Question: Assess the web application and use a variety of techniques to gain remote code execution and find a flag in the / root directory of the file system. Submit the contents of the flag as your answer. <br>
Answer: **528d6d9cedc2c7aab146ef226e918396** <br>
<img width="1001" height="114" alt="skill assessment flag" src="https://github.com/user-attachments/assets/7b40e321-3657-4ce5-9acf-27186465d260" />

For this assessment I followed the cheat sheet with a little modification of the SQL injection payloads. Solving this challenge was quite fun and educative.

<Flag>
  
## Module completion
URL Link: https://academy.hackthebox.com/achievement/1293352/33

## Conclusion
The content covered in this module is invaluable. SQL injection is still found in todays websites and still in the OWASP Top 10 making it a must have skill for ethical hackers. I was amazed byhowSQLinjection can be used to drop web shell payloads and be able to perform execution. I liked the content.
