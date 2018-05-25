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

Vulnerability #2: SESSION HIGHJACKING



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
## Concept Review
Which attacks were easiest to execute? Which were the most difficult?
The easiest attack to execute was XSS. The most difficult attack was SQL injection.

What is a good rule of thumb which would prevent accidentally username enumeration vulnerabilities like the one created here?
When developing applications, make sure that you leave no trace of user login activity

Since you should be somewhat familiar with the CMS and how it was coded, can you think of another resource which could be made vulnerable to an Insecure Direct Object Reference? What code could be removed which would expose it? (Hint: It was also the answer to the first bonus objective to the Weekly Assignment for week 3.)
The indirect object reference must be deleted completley that way there is not trace of it. Other information that could be leaked is person information such as credit cards or social security numbers.

Many SQL Injections use OR as part of the injected code. (For example: ' OR 1=1 --'.) Could AND work just as well in place of OR? (For example: ' AND 1=1 --'.) Why or why not?
IF an individual were to try to find more information about the database yes. The only matter to consider is that if an AND statment were used, both conditions MUST be met.

A stored XSS attack requires patience because it could be stored for months before being triggered. Because of this, what important ingredient would an attacker most likely include in a stored XSS attack script?
Scripts that could obtain information such as cookies. Other functions could also be used such as mining for crypto currency in some cases.

Imagine that one of your classmates is an authorized admin for the site's CMS and you are not. How would you get them to visit the self-submitting, hidden form page you created in Objective #5 (CSRF)?
I would disguise the link via html and send it to them.

Compare session hijacking and session fixation. Which attack do you think is easier for an attacker to execute? Why? One of them is much easier to defend against than the other. Which one and why?
I think sessioin hijacking would be much easier. This is because once an authentication cookie is taken, the attacker could use it with ease if no proper security measures are met.


