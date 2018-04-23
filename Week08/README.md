# Project 8 - Pentesting Live Targets

Time spent: 4 hours spent in total

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

Vulnerability #1: SQL Injection (SQLi)
![](https://github.com/ahamedbashir/WebSecurityCodepath/blob/master/Week08/Blue1%20SQLi.gif)

GIF description: As we can see in the gif above, trying to use ' or '1=1' injection in Blue color successfully modifed the database while it cannot do any change to the Red or Green colored system.

Vulnerability #2: Session Hijacking/Fixation
![](https://github.com/ahamedbashir/WebSecurityCodepath/blob/master/Week08/Blue2%20Session%20Hijack.gif)

GIF description: In this hacking method, we can see that using another users session ID, random person without log in credectials can access the Blue system.


## Green

Vulnerability #1: Cross-Site Scripting (XSS)
![](https://github.com/ahamedbashir/WebSecurityCodepath/blob/master/Week08/Green1%20XSS.gif)

GIF description: Using Cross-Site Script <script>alter();</script> we can see that an user is executing an script without prior knowledge when opeing the feedback section leading to an hacked web page

Vulnerability #2: Username Enumeration
![](https://github.com/ahamedbashir/WebSecurityCodepath/blob/master/Week08/Green2%20User%20Enum.gif)

GIF description: In this exploit, we can see that when a possible hacker tries to use random username to log into the system, the response after unsuccessful log in gives different feedback. When the usernamne is valid, the response class is "Failure" and if the user name is invalid, the response class is "failure". Aslo the font format is different for valid and invalid username.


## Red

Vulnerability #1: Insecure Direct Object Reference (IDOR)
![](https://github.com/ahamedbashir/WebSecurityCodepath/blob/master/Week08/Red1%20IDOR.gif)

GIF description: In this exploit, we can see that the list of salesperson that are not listed can be accessed by changing the user id in url. The ID=10 and ID=11 give two saleperson that are not listed on the visible list of salesperson.

Vulnerability #2: Cross-Site Request Forgery (CSRF)
![](https://github.com/ahamedbashir/WebSecurityCodepath/blob/master/Week08/Red2%20CSRF.gif)

GIF description: In this exploit, we can see that the user who doesn't have admin previlege can access data and change it even though that particular user doesn't have permisssion to do so using the action form. An non-admin user can run any script without prior knowledge made by anyone else and let Cross-site request forgery by running autamated script.

## Bonus Objective 2 (Green)

Vulnerability #1: Cross-Site Scripting (XSS) 2

![](https://github.com/ahamedbashir/WebSecurityCodepath/blob/master/Week08/Green3%20XSS%20Bonus.gif)

GIF description: As we can see in the gif above, when a log in user access the feedback section, the feedback containing unwanted script redirect the user to a different webpage leading to a possible hacked site.
