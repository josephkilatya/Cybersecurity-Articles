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

<Nameoffirst database shown in screen-shot above>

## Section: SQL Statements
Question: What is the department number for the 'Development' department? <br>
Answer: **d005** <br>

<Development' department number>

## Section: Query Results
Question: What is the last name of the employee whose first name starts with "Bar" AND who was hired on 1990-01-01? <br>
Answer: **Mitchem** <br>

<Query results>

## SQL Operations
Question: In the 'titles' table, what is the number of records WHERE the employee number is greater than 10000 OR their title does NOT contain 'engineer'? <br>
Answer: **654** <br>

<Number of records shown> <br>
  
## Section: Subverting Query Logic
Question: Try to log in as the user 'tom'. What is the flag value shown after you successfully log in? <br>
Answer: **202a1d1a8b195d5e9a57e434cc16000c** <br>

<User tom flag> <br>
  
## Section: Using Comments
Question: Login as the user with the id 5 to get the flag. <br>
Answer: **cdad9ecdf6f14b45ff5c4de32909caec** <br>

<Flag>
  
## Section: Union Clause
Question: Connect to the above MySQL server with the 'mysql' tool, and find the number of records returned when doing a 'Union' of all records in the 'employees' table and all records in the 'departments' table. <br>
Answer: **663** <br>

<Total number of records shown>
  
## Section: Union Injection
Question: Use a Union injection to get the result of 'user()' <br>
Answer: **root@localhost** <br>

<User found>
  
## Database Enumeration
Question: What is the password hash for 'newuser' stored in the 'users' table in the 'ilfreight' database? <br>
Answer: **9da2c9bcdf39d8610954e0e11ea8f45f** <br>

<newuser password>
  
## Section: Reading Files
Question: We see in the above PHP code that '$conn' is not defined, so it must be imported using the PHP include command. Check the imported page to obtain the database password. <br>
Answer: **dB_pAssw0rd_iS_flag!** <br>

<Flag>
  
## Section: Writing Files
Question: Find the flag by using a webshell. <br>
Answer: **d2b5b27ae688b6a0f1d21b7d3a0798cd** <br>

<Flag>
  
## Section: Skills Assessment- SQL Injection Fundamentals
Question: Assess the web application and use a variety of techniques to gain remote code execution and find a flag in the / root directory of the file system. Submit the contents of the flag as your answer. <br>
Answer: **528d6d9cedc2c7aab146ef226e918396** <br>

For this assessment I followed the cheat sheet with a little modification of the SQL injection payloads. Solving this challenge was quite fun and educative.

<Flag>
  
## Module completion
URL Link: https://academy.hackthebox.com/achievement/1293352/33

## Conclusion
The content covered in this module is invaluable. SQL injection is still found in todays websites and still in the OWASP Top 10 making it a must have skill for ethical hackers. I was amazed byhowSQLinjection can be used to drop web shell payloads and be able to perform execution. I liked the content.
