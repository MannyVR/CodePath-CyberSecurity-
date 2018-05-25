# Project 8 - Pentesting Live Targets

Time spent: **15** hours spent in total

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

Vulnerability #1: SQL INJECTION: Sleep SQL statment causes delay on the website.
![sql injection](https://user-images.githubusercontent.com/36680097/40519495-a20e819c-5f74-11e8-9374-c2dabee2d433.gif)

Vulnerability #2: __________________


## Green

Vulnerability #1: Username Enumeration, admin is not in bold, jmonroe99 is bold when noted as "Login not successful"
![username enumeration](https://user-images.githubusercontent.com/36680097/40452876-35d6c4f8-5e98-11e8-9d54-85c7babe2efd.gif)

Vulnerability #2: XSS Vulnerability in the feedback section.
![xss green](https://user-images.githubusercontent.com/36680097/40516010-f767775e-5f63-11e8-822f-d3ec088ffce5.gif)


## Red

Vulnerability #1: IDOR , id=11 exposes fired employee.
![idor](https://user-images.githubusercontent.com/36680097/40453084-e704f330-5e98-11e8-89d2-c74c087ee2f1.gif)

Vulnerability #2: CSRF, You can create a form that allows you to change certain permeters.
![csrf](https://user-images.githubusercontent.com/36680097/40513478-c0ce455a-5f5a-11e8-877b-219130add0ca.gif)


## Notes

Describe any challenges encountered while doing the work

