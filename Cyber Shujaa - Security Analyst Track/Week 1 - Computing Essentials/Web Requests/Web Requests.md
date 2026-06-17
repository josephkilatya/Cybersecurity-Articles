# Web Requests Module Report 
## Introduction 
This module covered the general working of requests in a web server. This entails the various 
protocols used to facilitate communication between the Client (browser such as Firefox and 
Google Chrome) and the web server (such as Apache and WAMP). The protocols included HTTP, 
Hypertext Transfer Protocol which transfers. The module also covers the various request methods 
such as POST, GET and working with API. 

The module also had challenge questions for practice and enhancement for what is learned. 
Overall, this was an informative module with a lot to learn  

## Walkthrough 
## Section: Hypertext Transfer Protocol (HTTP) 
The first question in HTTP section of this module was to find the flag by using cURL tool to 
download the file returned by '/donwload.php' from the target server spawned.  
To solve this question, I used the curl command line tool in my Kali Linux. I used curl to 
read the download.php file hosted on the target server. This was easy and got the flag 
immediately after running the command in the screenshot. 
For section two there were no challenges to solve. I however got insights on how to handle 
https using cURL tool. 

## Section: HTTP Requests and Responses 
This section illustrated how web server communicates with client. The client issues a GET 
request and is then redirected to the server resources if they are available or accessible 
through the internet.  
The section had two questions to work around with. 
The first one was to find the HTTP method being used by the spawned target web server. 
To solve this question, I used the curl command together with the –v to check the headers 
in the request. The method used was GET method. This is a common method used when 
making web requests to access certain resources on the server. 
The next question wanted the learner to find out the Apache version running on the server. 
To find the answer I used the same command as in the previous question to the Apache 
server version that was running on the target web server. The server was running Apache 
version 2.4.41. 

## Section: HTTP Headers 
This section had only one question or challenge. The question required the learner to use 
devtools in a web browser to find the flag in the network tab. 
To solve this question, I opened the spawned target web server link in a Firefox browser. I 
then opened the devtools using the keys CTRL + SHIFT + I. After that I then navigated to 
the network tab and refreshed the page loaded. I noticed this file text with the name flag 
and some random character being one of the requested resources by the client. 
I copied the file location URL and opened it in a new tab and then boom, I found the flag. 

## Section: GET 
This section explored how the GET method works with illustration using the curl tool and 
the browser devtools. It had only one question which required the leaner to identify the 
method used by the target server during search and locate the flag on the server using the 
curl command. 
Let's start with finding the request method used by the search field of the target server. I 
opened the target server on a new tab and logged-in using the credentials provided 
admin:admin. I then opened the devtools using the same command as in the previous 
section. I refreshed the page and found the GET method was the method used by the 
search section of the target server. 
For the next part of the question, I used curl command to search the flag which I got 
effortlessly. 

## Section: POST 
The question in this section had two parts. First get a session cookie through a valid login, 
then use that cookie with curl to search for the flag. 
I logged-in using curl command using the –i flag to view the headers returned when I 
logged-in. I found the cookie on the header Set-Cookie. 
Now that I had a valid session cookie, I substituted this with the login credentials. I then 
performed flag search using the flag search using curl. In the command I provided the 
Content-Type header to application/json as the and passed the session cookie using the  -b flag. With the enhanced command I was able to get the flag. 

## Section: CRUD API 
APIs (Application Program Interfaces) provide an easier way to make requests from the 
web server. In this section, I learned to manipulate API requests to Read, Create, Update, 
and Delete data from a web server using the CRUD API. 
The question in this section required the learner to use curl command line tool to update a 
city name in the target server to flag, delete any city and search for the flag. 
Let's start with the first part of the question. I used the curl tool to PUT update the London 
city name entry to flag. The command ran without any errors which indicated a success. 
I then proceed to delete a city from the target server. The steps are indicated in the screenshot 
below. 
1. I searched for the city I wanted to delete and present the output in json using jg command 
line tool. For this case I searched lee and got one results ouput, Leeds city in UK. 
2. I then proceeded to delete the selected city from the server with the DELETE method. The 
command ran successfully without any errors indicating success. 
3. To confirm if indeed I had deleted Leeds city from the target server. I searched for it once 
again with no results displayed. This indicates that the command ran successfully and the 
entry for Leeds city was deleted from the target server. 
Now unto the last part, finding the flag. The sequence of steps is highlighted in the 
screenshot below. 
1. I searched for the flag directly, however I got the flag entry I had updated in the first 
part of this question. I wasn't sure why I was getting that until I checked the hint. The 
hint revealed that I had to delete some city entries for me to get the flag. 
2. I did so by deleting the city entry I had created for Nairobi city.  
3. After that I searched for the flag again and this time got the flag. 
4. The output results weren't that presentable, so I searched again this time specifying 
the output results to be in json format for easy readability. 

## Module Completion 
Link: https://academy.hackthebox.com/achievement/1293352/35

## Conclusion 
This module was informative. I learned how client-server requests work by using different 
request methods. I also learned the different protocols for client-server communication, 
that is, HTTP and HTTPS with the latter considered more secure than the former. HTTP 
response and request codes were also covered in this module, not forgetting the HTTP 
headers.  

I had a glimpse at how the GET and POST request methods work in a client-server 
architecture.  

The last section of this module covered APIs, specifically CRUD API. APIs are a different 
way of making requests in a client-server architecture.  
Above all, I learned how to work with web browser devtools to inspect web page requests. 
The other tool covered was curl, a tool for command line interactions with a web server 
and useful one for inspecting website requests. 
