# Introduction
From the room..."_CyberChef is a simple, intuitive web-based application designed to help with various “cyber” operation tasks within your web browser. Think of it as a Swiss Army knife for data - like having a toolbox of different tools designed to do a specific task. These tasks range from simple encodings like XOR or Base64 to complex operations like AES encryption or RSA decryption. CyberChef operates on recipes, a series of operations executed in order._"

This not being my first time to interact with CyberChef, I have been using it in my career to decode malware scripts. The tool is really reliable for any security professional be it a defender or offensive security individuals. To me, this room is going to be more of refresher.

# Walkthrough
## TASK 1: Introduction:
This section covers the introduction on what the tool is, the learning objectives and the prerequisites needed for the room.
The prerequisites listed are:
1. [Hashing Basics](https://tryhackme.com/r/room/hashingbasics)
2. [Cryptography Basics](https://tryhackme.com/r/room/cryptographybasics)
   
<img width="1259" height="144" alt="image" src="https://github.com/user-attachments/assets/b12f402c-ea9f-4cee-b21d-7585f2a93f43" />
_Figure 1: No answers needed for questions in this section._

## TASK 2: Accessing The Tool
Accorind to the room, there are two ways to access CyberChef.
1. Online Access through a web browser
2. Offline or Local Copy

Personally I use the Local Copy access from my malware analysis lab, Flare-VM. You can find an article I wrote on how to set up Flare-VM. Anlysing malware in an isolated is a good practice as it helps prevents infecting your host system with malware accidentaly.

For this room I will however be using the Online one for easy access and simplicity as the goal is to learn.
<img width="1919" height="988" alt="image" src="https://github.com/user-attachments/assets/36588f96-0b9e-477c-b6f7-a1bf5cc37cd4" />
*Figure 2: Online Web Access of CyberChef Platfrom.*

Answer the questions below
I have access to CyberChef and I’m ready to dive into it.
<img width="676" height="173" alt="image" src="https://github.com/user-attachments/assets/0afd9180-6d9d-40f3-9688-4f2ff2f54830" /><br>
*Figure 3: Answers to Questions in this section. None required.*

## TASK 3: Navigating The Interface
CyberChef interface has the following sections that make it whole and each serving different functionality.

Operations: Think of operations as functions. Some of the functions include:
1. URL Encode - Serves the purpose of encoding URLs,
2. To Base64 - Encodes ASCII text to Base64 formart
     
Recipe: Once you select the operation you want it is added into this section. You can perform some tweaks/configurations to the operation to achieve desirables functioning. Kind of adding ingridients to your recipe when preparing a meal. The ingridinets you add will determine the taste of your meal (output)

Input: Input is basically the data that you want to process (cooking your recipe)
Output: The results from input data after processing running your selected operations over your input data 

ANSWERING THE QUESTIONS:
_In which area can you find "From Base64"?_
 <img width="1252" height="157" alt="image" src="https://github.com/user-attachments/assets/8d0c827f-6efe-4e72-ba4f-5d8555ebf586" />

 <img width="1261" height="155" alt="image" src="https://github.com/user-attachments/assets/a6376e03-cf2d-40e6-a6f1-e83ff558cb02" />

_Which area is considered the heart of the tool?_
<img width="1115" height="468" alt="image" src="https://github.com/user-attachments/assets/c6e1f03e-6453-4971-80ee-31e64b00f59a" />

<img width="1249" height="104" alt="image" src="https://github.com/user-attachments/assets/01d6d431-83ee-4995-8506-099ae1334902" />

## TASK 4: Before Anaything Else
This section highlights the thought process for achieving better results from using CyberChef:
Step 1: Set a clear objective - Knowing what you want to achieve really helps you in determining the operations you want. For example; I want to convert/encode ASCII text "I LOVE CYBERSECURITY" to Base64.

Step 2: Put your data into the input area - From the example given above, this could involve typing or pasting the text "I LOVE CYBERSECURITY" in the data input field.

Step 3: Select the Operations you might want to use - Go to operations section and search "to bas64". Next we double-click the operation to add it in the recipe section or drag-and-dropping it there. Once everything is ready, BAKE your recipe (processing your data through selected operations)

Step 4: Check the output to see if is the intended result - From the example used in my case, we would expect base64 version of "I LOVE CYBERSECURITY", which is "SSBMT1ZFIENZQkVSU0VDVVJJVFk="

ANSWERING THE QUESTIONS
<img width="1266" height="161" alt="image" src="https://github.com/user-attachments/assets/b9e4b724-629a-4d38-9fb7-879db693de03" />

<img width="1258" height="570" alt="image" src="https://github.com/user-attachments/assets/f77af77b-b7f7-4935-a1f3-0d09c7616eae" />

## TASK 5: Practice, Practice, Practice
As the old saying goes, Practice makes perfect. That's is what this section helps by getting our hands a little dirty 😅.

Before we do that, there's a few new things introduced here:
1. Extractors: Honestly, I did not know about them until I went through this room (See why continous learning helps 🙂). This are operations used to extract data such as
   - Extract IP addresses - Extracts all IPv4 and IPv6 addresses from input data
   - Extract URLs
   - Extract email addresses

2. Date and Time: Operataions that help with converting Timestamps
   - **From UNIX Timestamp** to datetime string
   - **To UNIX Timestamp** - converts UTC datestring into corresponding timestamp
  
3. Data Format: This are operations that convert input data from one form to another. Some need to be combined in order to get the desired output. They include the following:
   - From Base64
   - URL Decode
   - From Base85
   - From Base58
   - To Base62
  
This section also describes how to change data from Base encodings or vice-versa using manual technique.

ANSWERING THE QUESTIONS:
_What is the hidden email address?_
<img width="1910" height="646" alt="image" src="https://github.com/user-attachments/assets/61633070-3b58-4b2a-94fc-9de80b1dda73" />

<img width="686" height="128" alt="image" src="https://github.com/user-attachments/assets/5e143faa-f5c2-4f2e-848b-4327e72e83d9" />
     
_What is the hidden IP address that ends in .232?_
<img width="1919" height="681" alt="image" src="https://github.com/user-attachments/assets/c415ecd4-5a01-4b90-a146-686d0ea2ba4f" />

<img width="696" height="112" alt="image" src="https://github.com/user-attachments/assets/551c7ba6-1988-456a-a59e-01038fc4880a" />

_Which domain address starts with the letter "T"?_
<img width="1918" height="670" alt="image" src="https://github.com/user-attachments/assets/54457945-d636-447b-af88-f0857fdce33a" />

<img width="676" height="109" alt="image" src="https://github.com/user-attachments/assets/fdcc59a8-9b71-4641-9cd5-36ed460885fc" />

_What is the binary value of the decimal number 78?_
<img width="1919" height="412" alt="image" src="https://github.com/user-attachments/assets/5b284e0a-229c-417c-9365-eb2702917913" />

<img width="686" height="94" alt="image" src="https://github.com/user-attachments/assets/6390f427-130a-4681-8cb3-12dda9ac79f4" />

_What is the URL encoded value of https://tryhackme.com/r/careers?_
<img width="1691" height="451" alt="image" src="https://github.com/user-attachments/assets/9fa938d7-60d6-44f5-993c-8a1d4aad8050" />

<img width="680" height="118" alt="image" src="https://github.com/user-attachments/assets/fc5d0f09-7a9b-483d-994c-77a8c60594ea" />

## TASK 6: Your First Official Cook
Time for more practice.

This section notes down a key point, _"It's best to try to answer the questions first without using the hints."_

ANSWERING THE QUESTIONS:
_Using the file you downloaded in Task 5, which IP starts and ends with "10"?_
<img width="1919" height="493" alt="image" src="https://github.com/user-attachments/assets/edb4f944-6711-40ad-ac3c-db2d9db6153f" />

<img width="1274" height="117" alt="image" src="https://github.com/user-attachments/assets/e700c92f-f7b7-4c7a-a5be-6801c913d412" />

_What is the base64 encoded value of the string "Nice Room!"?_
<img width="1355" height="471" alt="image" src="https://github.com/user-attachments/assets/b7abe56f-719c-449e-b290-39cf8f42f1b7" />

<img width="1270" height="101" alt="image" src="https://github.com/user-attachments/assets/0a68e3d4-11b4-4677-ba45-a9540430381d" />

_What is the URL decoded value for https%3A%2F%2Ftryhackme%2Ecom%2Fr%2Froom%2Fcyberchefbasics?_
<img width="1468" height="468" alt="image" src="https://github.com/user-attachments/assets/d3c9c85b-87f7-4db3-a207-7558bb3660a9" />

<img width="1257" height="97" alt="image" src="https://github.com/user-attachments/assets/d681e68a-55af-4ddc-bd55-ada4f9818333" />

_What is the datetime string for the Unix timestamp 1725151258?_
<img width="1434" height="461" alt="image" src="https://github.com/user-attachments/assets/794ac64a-1302-460f-977d-88f1a06bd92b" />

<img width="1276" height="96" alt="image" src="https://github.com/user-attachments/assets/86189e28-d7ff-4c96-8487-b6be01d1174f" />

_What is the Base85 decoded string of the value <+oue+DGm>Ap%u7?_
<img width="1529" height="500" alt="image" src="https://github.com/user-attachments/assets/26184d4d-3cac-435f-86f6-cbc78ea3cae3" />

<img width="1246" height="112" alt="image" src="https://github.com/user-attachments/assets/096d4a2a-d0c7-4e3f-823e-4b2c214ea20b" />

## TASK 7: Conclusion
This section covers a summary of what was learned from the room.

ANSWERING THE QUESTIONS
_I will have CyberChef, the Swiss Army knife of cyber security, ready for my upcoming journeys!_
<img width="680" height="115" alt="image" src="https://github.com/user-attachments/assets/13fed1de-e64f-489f-8cdf-f09bbb7bb519" />
*Figure: No Anwers Needed for above question*

# CONCLUSION
Overall this was really an informative room. A good knowledge refresher for me and grabbed a couple of knew things such working with Extractor Operataions. I will leave it there folks. Happy Haccking :)










