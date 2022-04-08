# Project 8 - Pentesting Live Targets

Time spent: **3** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:

* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each color is vulnerable to only 2 of the 6 possible exploits. First discover which color has the specific vulnerability, then write a short description of how to exploit it, and finally demonstrate it using screenshots compiled into a GIF.

## Blue

Vulnerability #1: __________________

Description:

<img src="blue-vuln1.gif">

Vulnerability #2: __________________

Description:

<img src="blue-vuln2.gif">

## Green

Vulnerability #1: Cross-Site Scripting (XSS)

Description:  A stored xss can be put into the website through the Contact Us portion of the main menu. The user can leave a script in the comment box and the script will be executed when the admin goes to check the feedback for the website. This was probably left there because the comment was not properly sanitized and escaped. 

<img width="300" alt="Screen Shot 2022-04-07 at 22 37 02" src="https://user-images.githubusercontent.com/62517289/162352116-d6812f98-ed8a-4c3b-a058-da5cbeb5fa41.png">

Vulnerability #2: SQL Injection (SQLi)

Description: Green website has an error messaged when the user types a sql query that is different from the other websites. It is a very small difference but can potentially be exploited more. For example, the error message "Log in was unsuccessful." is not bolded on the Green website like it is on the other websites. 

<img width="447" alt="Screen Shot 2022-04-07 at 23 50 56" src="https://user-images.githubusercontent.com/62517289/162359176-6bc532b1-75dd-492e-b80b-843207ef4705.png"><img width="474" alt="Screen Shot 2022-04-07 at 23 51 01" src="https://user-images.githubusercontent.com/62517289/162359178-064c9531-1a17-4175-817e-c7e89fb1d6bd.png">




## Red

Vulnerability #1: Insecure Direct Object Reference (IDOR)

Description: The Salesperson page has an id field where the user can enter the specified ID. Specifically, users can access Salesperson id = 10 that was not supposed to be public and visible yet. This can be done by changing the id to 11 as well. 

<img width="200" alt="Screen Shot 2022-04-07 at 22 21 50" src="https://user-images.githubusercontent.com/62517289/162350638-4c2c24ac-d215-4e83-82b7-d6bc3c304e44.png">
<img width="200" alt="Screen Shot 2022-04-07 at 22 25 13" src="https://user-images.githubusercontent.com/62517289/162350941-9a95be32-2781-4d0a-b49a-c6ce6394e763.png">
<img width="200" alt="Screen Shot 2022-04-07 at 23 51 05" src="https://user-images.githubusercontent.com/62517289/162359183-5e0948c7-2fc8-4d6d-8591-1f155cb01152.png">



Vulnerability #2: __________________

Description:

<img src="red-vuln2.gif">


## Notes

Describe any challenges encountered while doing the work
Lot of the material I personally needed to review, so it took a little longer to grasp. Also this is the first live pentesting on a live real website that had specific vulnerabilities. Although difficult, it was fun figuring and playing around with the websites. 
