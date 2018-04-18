# Project 8 - Pentesting Live Targets

Time spent: **X** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

**Vulnerability #1:** Session Hijacking

1. An attacker can obtain the session id of a logged on user by many means (XSS or sniffing WiFi packets, for example). Here, we use Burp to get the user's PHPSESSID. 
  ![sh-1](./blue/session-hijacking/sh-1.gif) 
2. Then, the attacker can use cURL from the command line to forge a GET request with such session id. Here, the command ```curl --insecure --cookie "PHPSESSID=6f4i5sk14cdrjtotdvdu8lmjd5" --request GET https://35.226.155.72/blue/public/staff/index.php``` is issued.   
  ![sh-2](./blue/session-hijacking/sh-2.gif)
3. The same attacker could also use its browser to request access to the user’s page. Google Chrome allows to change a page’s cookies through the console. Below, the command ```document.cookie="PHPSESSID=6f4i5sk14cdrjtotdvdu8lmjd5"``` is typed in the console.  
  ![sh-3](./blue/session-hijacking/sh-3.gif)

<br>

**Vulnerability #2:** 


## Green

**Vulnerability #1:** Stored Cross-Site Scripting (XSS)

1. An attacker injects script as a feedback comment in the *Contact Us* form.  
  ![xss-1.gif](./green/xss/xss-1.gif)
2. When a logged on user loads the feedback page, the script is executed.  
  ![xss-2.gif](./green/xss/xss-2.gif)

<br>

**Vulnerability #2:** 


## Red

**Vulnerability #1:** Cross-Site Request Forgery (CSRF)

1. Before the attack this is the user data stored by the site.  
  ![csrf-1](./red/csrf/csrf-1.gif)
2. A logged on user loads a [malicious page](./red/csrf/index.html) carefully crafted by an attacker. After the attack, the name and last name of first user is modified.  
  ![csrf-2](./red/csrf/csrf-2.gif)

<br>

**Vulnerability #2:**


## Notes

Describe any challenges encountered while doing the work

