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

Vulnerability #1: __________________

Vulnerability #2: __________________


## Green

**Vulnerability #1:** Stored Cross-Site Scripting (XSS)

1. An attacker injects script as a feedback comment in the *Contact Us* form.  
  ![xss-1.gif](./green/xss/xss-1.gif)
2. When a logged on user loads the feedback page, the script is executed.  
  ![xss-2.gif](./green/xss/xss-2.gif)

<br>

Vulnerability #2: __________________


## Red

**Vulnerability #1:** Cross-Site Request Forgery (CSRF)

1. Before the attack this is the user data stored by the site.  
  ![csrf-1](./red/csrf/csrf-1.gif)
2. A logged on user loads a malicious page carefully crafted by an attacker. After the attack, the name and last name of first user is modified.  
  ![csrf-2](./red/csrf/csrf-2.gif)

<br>

Vulnerability #2: __________________


## Notes

Describe any challenges encountered while doing the work

