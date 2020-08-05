+++
author = "Pranav Bansal"
title = "How to test for XSS Vulnerabilities"
date = "2020-08-05"
description = "A brief introduction to XSS for testers"
tags = [
    "security",
]
draft = false
+++

#### A) Description

XSS is cross-site scripting.
XSS is a client side code injection attack.
Attacker executes the malicious scripts in a web browser of the victim by incuding the malicious code in the web browser or web application.
The web page or web application becomes a vehicle to deliver the malicious script to the user’s browser
A web page or web application is vulnerable to XSS if it uses unsanitized user input in the output that it generates
It can be done by using html tags or javascripts.

How Cross-site Scripting Works
There are two stages to a typical XSS attack:

1) To run malicious JavaScript code in a victim’s browser, an attacker must first find a way to inject malicious code (payload) into a web page that the victim visits.
2) After that, the victim must visit the web page with the malicious code.

#### B) EXAMPLE

Go to website : http://testphp.vulnweb.com/
User can see the search box
Type anything in the search box and clock go.
User is able to see the output as per input searched.

##### Now to perform XSS

Insert any script in the search box. 
Lets start with the basic html tag :

In the search box type
<Script>alert(I am Evil)</script>
Now click on go

User will be able to see a prompt with text "I am evil"

#### C)Latest XSS attacks

Samy (also known as JS.Spacehero) is a XSS worm that was designed to propagate across the MySpace social-networking site written by 
Samy Kamkar. Within just 20 hours of its October 4, 2005 release, over one million users had run the payload making Samy the fastest 
spreading virus of all time.

The worm itself was relatively harmless, it carried a payload that would display the string "but most of all, samy is my hero" on a 
victim's MySpace profile page. When a user viewed that profile page, the payload would then be replicated and planted on their own 
profile page continuing the distribution of the worm. MySpace has since secured its site against the vulnerability, however certain 
MySpace profiles still display evidence of the worm to this day.
