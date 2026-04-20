# CyberChef: The Basics - TryHackMe Walkthrough
**Introduction**
From the room..."_CyberChef is a simple, intuitive web-based application designed to help with various “cyber” operation tasks within your web browser. Think of it as a Swiss Army knife for data - like having a toolbox of different tools designed to do a specific task. These tasks range from simple encodings like XOR or Base64 to complex operations like AES encryption or RSA decryption. CyberChef operates on recipes, a series of operations executed in order._"

This not being my first time to interact with CyberChef, I have been using it in my career to decode malware scripts. The tool is really reliable for any security professional be it a defender or offensive security individuals. To me, this room is going to be more of refresher.

# Walkthrough
## TASK 1: Introduction:
This section covers the introduction on what the tool is, the learning objectives and the prerequisites needed for the room.
The prerequisites listed are:
1. [Hashing Basics](https://tryhackme.com/r/room/hashingbasics)
2. [Cryptography Basics](https://tryhackme.com/r/room/cryptographybasics)

<br>   
<img width="1259" height="144" alt="image" src="https://github.com/user-attachments/assets/b12f402c-ea9f-4cee-b21d-7585f2a93f43" />
*Figure 1: No answers needed for questions in this section.*

## TASK 2: Accessing The Tool
According to the room, there are two ways to access CyberChef.
1. Online Access through a web browser [here](https://gchq.github.io/CyberChef)
2. Offline or Local Copy cloned from GitHub repo [here](https://github.com/gchq/cyberchef)

Personally, I use the Local Copy access from my malware analysis lab, Flare-VM. CyberChef comes by default with Flare-VM. You can find an article I wrote on how to set up Flare-VM [here](https://github.com/josephkilatya/Cybersecurity-Articles/blob/main/Articles/FLARE-VM%20-%20Building%20A%20Malware%20Analysis%20Lab.md) to guide you with setting up. Analysing malware in an isolated environment is a good practice as it prevents malware from accidentally infecting your host system.

For this room I will however be using the Online one for easy access and simplicity as the goal is to learn.
<br>
<br>
<img width="1919" height="988" alt="image" src="https://github.com/user-attachments/assets/36588f96-0b9e-477c-b6f7-a1bf5cc37cd4" />
*Figure 2: Online Web Access of CyberChef Platform. To access the online platform, click embeded link in the THM room or this article*

ANSWERING THE QUESTIONS
I have access to CyberChef and I’m ready to dive into it.
<br>
<br>
<img width="1267" height="123" alt="image" src="https://github.com/user-attachments/assets/7eea3308-5d93-4747-860d-d2f2e97ee8e4" />
*Figure 3: No answer required for question above.*

## TASK 3: Navigating The Interface
CyberChef interface has the following sections that make it whole and each serving different functionality.

Operations: Think of operations as functions. Some of the functions include:
1. URL Encode - Serves the purpose of encoding URLs,
2. To Base64 - Encodes ASCII text to Base64 format
     
Recipe: Once you select the operation you want it is added into this section. You can perform some tweaks/configurations to the operation to achieve desirable functioning. Kind of adding ingredients to your recipe when preparing a cake. The ingredinets you add will determine the taste of your cake (output)

Input: Input is basically the data that you want to process (cooking your recipe)
Output: The results from input data after processing running your selected operations over your input data 

ANSWERING THE QUESTIONS
<br>
_In which area can you find "From Base64"?_
<img width="1115" height="468" alt="image" src="https://github.com/user-attachments/assets/c6e1f03e-6453-4971-80ee-31e64b00f59a" />
 *Figure 7:  To get the answer to question above. Visit your CyberChef opened session from previous task. When you look around the platform, you will find **From Base64** operation pinned under Operations' section Favourites.*
<br>
<br>
<img width="1249" height="104" alt="image" src="https://github.com/user-attachments/assets/01d6d431-83ee-4995-8506-099ae1334902" />
*Figure 8: Answer submitted.*

_Which area is considered the heart of the tool?_
<br>
<br>
<br>
<img width="1252" height="157" alt="image" src="https://github.com/user-attachments/assets/8d0c827f-6efe-4e72-ba4f-5d8555ebf586" />
 *Figure 4:  You can find the answer to the above question in the task's notes*
 

<br>
<img width="1261" height="155" alt="image" src="https://github.com/user-attachments/assets/a6376e03-cf2d-40e6-a6f1-e83ff558cb02" />

*Figure 5: The correct Anser is **Recipe***

<br>
<br>


## TASK 4: Before Anything Else
This section highlights the thought process for achieving better results from using CyberChef:
Step 1: Set a clear objective - Knowing what you want to achieve really helps you in determining the operations you want. For example; I want to convert/encode ASCII text "I LOVE CYBERSECURITY" to base64.

Step 2: Put your data into the input area - From the example given above, this could involve typing or pasting the text "I LOVE CYBERSECURITY" in the data input field.

Step 3: Select the Operations you might want to use - Go to operations section and search "to base64". Next we double-click the operation to add it in the recipe section or drag-and-dropping it there. Once everything is ready, BAKE your recipe (processing your data through selected operations)

Step 4: Check the output to see if is the intended result - From the example used in my case, we would expect base64 version of "I LOVE CYBERSECURITY", which is "SSBMT1ZFIENZQkVSU0VDVVJJVFk="

ANSWERING THE QUESTIONS
<br><br>
_At which step would you determine, "What do I want to accomplish?_
<br>
<br>
<img width="1258" height="570" alt="image" src="https://github.com/user-attachments/assets/f77af77b-b7f7-4935-a1f3-0d09c7616eae" />

*Figure 9:  Answer to the question above can be found under the tasks notes as shown in screenshot above.*
<br>
<br>

<img width="1266" height="161" alt="image" src="https://github.com/user-attachments/assets/b9e4b724-629a-4d38-9fb7-879db693de03" />
*Figure 10: Correct Answer is Step 1*
 
## TASK 5: Practice, Practice, Practice
As the old saying goes, Practice makes perfect. So, getting ready to get your hands a little dirty.

Before we do that, there's a few new things introduced in this section:
1. Extractors: Honestly, I did not know about them until I went through this room (See why continuous learning helps). This are operations used to;
   - Extract IP addresses - Extracts all IPv4 and IPv6 addresses from input data
   - Extract URLs
   - Extract email addresses

2. Date and Time: Operations that help with converting Timestamps
   - **From UNIX Timestamp** to datetime string
   - **To UNIX Timestamp** - converts UTC datestring into corresponding timestamp
<br>
Suppose you are asking UNIX timestamp is, it is a system for representing a point in time by counting the number of seconds that have elapsed since January 1, 1970, at 00:00:00 UTC, which is known as the Unix Epoch. 
  
3. Data Format: These are operations that convert input data from one form to another. Some need to be combined in order to get the desired output. They include the following:
   - From Base64
   - URL Decode
   - From Base85
   - From Base58
   - To Base62
  
The section also teaches us how to change data from Base(64, 85, 58, 62) encodings and vice-versa manually. 

ANSWERING THIS TASK'S QUESTIONS:
First Download Task File attached in this section. Open the .txt using your favourite text editor (NotePad, Sublime Text, Notepad++ or any other)
<br>
<br>
_What is the hidden email address?_
<br>
<br>
<img width="1910" height="646" alt="image" src="https://github.com/user-attachments/assets/61633070-3b58-4b2a-94fc-9de80b1dda73" />
 *Figure 11:  Following the steps from the previous task, our goal is extract data from the data provided. Having the .txt file open in a text editor, copy the whole of it. Next, go to CyberChef Platform and paste the text in Input fiel. Search email under Operations search field and select Extract email address operation to add to Recipe by double clicking. Under Recipe section, Click Bake to run selected Operaration over our data input. Any found emails will be shown under Output Section, below our input data.*
<br>
<br>
<img width="686" height="128" alt="image" src="https://github.com/user-attachments/assets/5e143faa-f5c2-4f2e-848b-4327e72e83d9" />
 *Figure 12: Email found for this case is **hidden@hotmail.com***
<br>
<br>
_What is the hidden IP address that ends in .232?_
<br>
<br>
<img width="1919" height="681" alt="image" src="https://github.com/user-attachments/assets/c415ecd4-5a01-4b90-a146-686d0ea2ba4f" />
 *Figure 13: Proceeding to the above question. Clear the previous Operation from the Recipe by Clicking the trash icon under the same section. Search **Extract Ip** under Operations section, select **Extract IP addresses** as done in previous question to add to recipe. Bake as from previous question. You will get two IP address with one that ends with .232*
<br>
<br>
<img width="696" height="112" alt="image" src="https://github.com/user-attachments/assets/551c7ba6-1988-456a-a59e-01038fc4880a" />
 *Figure 14: From the output after baking the input data with the Recipe provided, the required IP is **102.20.11.232***

<br>

_Which domain address starts with the letter "T"?_
<br>
<br>
<img width="1918" height="670" alt="image" src="https://github.com/user-attachments/assets/54457945-d636-447b-af88-f0857fdce33a" />
 *Figure 15: Repeat steps from previous question to clear current Recipe. Search and Add Extract Domains Operation to our Recipe. Bake. Identified domains from the input data will be displayed under Output Section*
<br>
<br>
<img width="1256" height="117" alt="image" src="https://github.com/user-attachments/assets/919d7cbc-3db4-42d4-89fb-9f6a0fbefa29" />
*Figure 16: Based on the above question, the domain name that starts with "T" is `TryHackMe.com`*

<br>
<br>
_What is the binary value of the decimal number 78?_
<br>
<img width="1919" height="412" alt="image" src="https://github.com/user-attachments/assets/5b284e0a-229c-417c-9365-eb2702917913" />
 *Figure 17: Repeat previous steps. However, for this particular question, we will be using two operation combined **From Decimal** and **To Binary**. Reason: Computers see everything as a series of bytes. Think of a byte as a small "container" that can hold any decimal number from 0 to 255.
From Decimal: This tells CyberChef, "I am giving you a number (78). Treat this number as a single byte of data."
To Binary: This tells CyberChef, "Now, show me the 0s and 1s that make up that byte."
Because 78 is smaller than 255, it fits perfectly into one byte, and CyberChef reveals its binary "code" (01001110) instantly.*

<br>
<br>
<img width="686" height="94" alt="image" src="https://github.com/user-attachments/assets/6390f427-130a-4681-8cb3-12dda9ac79f4" />

 *Figure 18: Revealed binary after baking is `01001110`*
<br>
<br>

_What is the URL encoded value of https://tryhackme.com/r/careers?_
<br>
<img width="1691" height="451" alt="image" src="https://github.com/user-attachments/assets/9fa938d7-60d6-44f5-993c-8a1d4aad8050" />
 *Figure 19: Clear input data by clicking the trash icon in the Input section. Paste the URL from the question. Search **URL Encode** under Operations section. Add the operation to Recipe and check the box **Encode all special chars**. By checking the Encode all special chars box, we ensure that every symbol—including those with special functions like &, ?, and /—is converted into its percent-encoded format so it is treated as plain data and doesn't accidentally break the structure of the URL.*

<br>
<br>
<img width="1255" height="99" alt="image" src="https://github.com/user-attachments/assets/7aa6c456-d965-4567-9a0f-3b77ba67e11a" />

*Figure 20: The Encoded URL is `https%3A%2F%2Ftryhackme%2Ecom%2Fr%2Fcareers`*


## TASK 6: Your First Official Cook
Time for more practice.

This section notes down a key point, _"It's best to try to answer the questions first without using the hints."_

ANSWERING THE QUESTIONS:
_Using the file you downloaded in Task 5, which IP starts and ends with "10"?_
<br>
<br>
<img width="1919" height="493" alt="image" src="https://github.com/user-attachments/assets/edb4f944-6711-40ad-ac3c-db2d9db6153f" />
*Figure 21:how to find the answer.*

<br>
<br>
<img width="1274" height="117" alt="image" src="https://github.com/user-attachments/assets/e700c92f-f7b7-4c7a-a5be-6801c913d412" />

_Figure 22: Answer submitted._
 
_What is the base64 encoded value of the string "Nice Room!"?_
<br>
<br>
<img width="1355" height="471" alt="image" src="https://github.com/user-attachments/assets/b7abe56f-719c-449e-b290-39cf8f42f1b7" />
*Figure 23: Steps to how to find the answer.*
 
<br>
<br>
<img width="1270" height="101" alt="image" src="https://github.com/user-attachments/assets/0a68e3d4-11b4-4677-ba45-a9540430381d" />

*Figure 24: Answer submitted*
 
_What is the URL decoded value for https%3A%2F%2Ftryhackme%2Ecom%2Fr%2Froom%2Fcyberchefbasics?_
<br>
<br>
<img width="1468" height="468" alt="image" src="https://github.com/user-attachments/assets/d3c9c85b-87f7-4db3-a207-7558bb3660a9" />
 *Figure 25: Steps to how to find the answer.*
 
<br>
<br>
<img width="1257" height="97" alt="image" src="https://github.com/user-attachments/assets/d681e68a-55af-4ddc-bd55-ada4f9818333" />

*Figure 26: Answer submitted*
 
_What is the datetime string for the Unix timestamp 1725151258?_
<br>
<img width="1434" height="461" alt="image" src="https://github.com/user-attachments/assets/794ac64a-1302-460f-977d-88f1a06bd92b" />
*Figure 27:Steps to getting answer*

<br>
<img width="1276" height="96" alt="image" src="https://github.com/user-attachments/assets/86189e28-d7ff-4c96-8487-b6be01d1174f" />

*Figure 28: Answer submitted.*
 
_What is the Base85 decoded string of the value <+oue+DGm>Ap%u7?_
<br>
<img width="1529" height="500" alt="image" src="https://github.com/user-attachments/assets/26184d4d-3cac-435f-86f6-cbc78ea3cae3" />
*Figure 29: Steps to getting answer.*

<br>
<br>
<img width="1246" height="112" alt="image" src="https://github.com/user-attachments/assets/096d4a2a-d0c7-4e3f-823e-4b2c214ea20b" />

*Figure 30: Answer submitted.*

## TASK 7: Conclusion
This section covers a summary of what was learned from the room.

ANSWERING THE QUESTIONS
_I will have CyberChef, the Swiss Army knife of cyber security, ready for my upcoming journeys!_
<br>
<img width="680" height="115" alt="image" src="https://github.com/user-attachments/assets/13fed1de-e64f-489f-8cdf-f09bbb7bb519" />
*Figure 31: No Answers Needed for above question.*

# CONCLUSION
Overall this was really an informative room. A good knowledge refresher for me and grabbed a couple of new things such working with Extractor Operations. I will leave it there folks. Happy Hacking :)










