---
published: false
layout: post
---
## A Personal Review on OSCP Certificate

### 0x00 - Prologue
OSCP - Offensive Security Certified Professional, is an ethical hacking certificate that is gaining much popularity around the globe in recent years. 

Contrary to most security certificates (CEH, CISSP, CISM, CISA, etc), OSCP is very unique in the following ways:
1. There is no official textbook, no classroom training. You will be given a virtual lab environment to practise by yourself.
2. The exam is not Multiple-Choice based. You will need to conduct a simulated penetration test.
3. You don't need to pay to renew the certificate every year.
4. You really need to Try Harder. (I mean HARDER)

In short, it's a challenging while rewarding certificate to get for us infosec people. 

### 0x01 - Why OSCP
Like the name suggests, OSCP's focus is ***offensive security***. In Sunzi's Art of War, there is a famous idiom "Know yourself and know your enemy, and you will never be defeated". (知己知彼，百战不殆) Same concept here, in order to prevent a hacker's attack, you have to understand how a hacker will attack. The course is all about real world techniques used by modern hackers and real world examples that you would see out there in corporate environment.

I myself has been doing penetration testing as my job for many years, but I kind of feel that I still need a systematically training, particularly on some very specific technical aspects, like the exploitation of Buffer Overflow vulnerabilities (in my daily job there is no chance for me to exploit such a vulnerability in a client environment.). And it turned out that the OSCP learning experiences didn't at all let me down!

One more good thing about OSCP is that obtaining the certificate will award you as many as 40 CPE hours, that is a whole year's requirement! One more good thing for those working working in UK/AU/NZ/SG, obtaining OSCP can also grant you the CREST Registered Tester certificate, after you have passed their level 1 exam which is CREST Practitioner Security Analyst. (normally you need to take CRT exam after the CPSA exam)

### 0x03 - How to get OSCP
So the overall process towards your OSCP is like:
1. Submit the application to Offensive Security and pay for it
2. Receive course materials(PDF+video) and lab connection package
3. Read through everything and try harder in your lab session (optional extensions can be bought)
4. Take the 24 hour exam and submit a exam report
5. If pass, get the certificate

In the next couple of sections I will share my experiences. 

### 0x04 - Preparation Studies
Although I am quite familar with penetration test side of things, I would not consider myself to be an advanced programer. Note that your lab session starts to count as soon as you received your course materials. If you have a full time job, then probably you might need 1 week to go through all the videos and the PDF. So it's better to have some preparation studies first before you made the purchase. You can skip this section if:
1. You don't mind spending a lot of money on purchasing additional lab time (US$250 for a month)
2. You already know how to do a proper penetration test (Not merely a automatic vulnerability scan)

For those who haven't skipped, here I briefly summarised the required knowledge you should have before you go into the charged lab environment:
1. How to use security tools like Nmap, Nikto, Dirb, Metasploit.
A good tutorial is:[https://www.offensive-security.com/metasploit-unleashed/](https://www.offensive-security.com/metasploit-unleashed/)

2. How to read and modify programs written in C, Python, shell script 
(You don't need to be an super advanced programer, but occationally you might need to modify a particular part to make things work)

3. How to exploit common web application vulnerabilities.
A good tutorial is bWapp: [http://www.itsecgames.com/](http://www.itsecgames.com/)

4. Have an idea about Buffer Overflow.
A good tutorial is [http://www.primalsecurity.net/0x0-exploit-tutorial-buffer-overflow-vanilla-eip-overwrite-2/](http://www.primalsecurity.net/0x0-exploit-tutorial-buffer-overflow-vanilla-eip-overwrite-2/)

4. Get familar with what a lab machine will look like.
On Vulnhub.com there are plenty of CTF style VMs for you to play with. A good start will be the Kioptrix series: [https://www.vulnhub.com/series/kioptrix,8/](https://www.vulnhub.com/series/kioptrix,8/) [This step is optional, as the lab is just like this kind of format]

### 0x05 - Course materials and Lab session
The course materials are pretty straight forward, in an easy to understand way it covers all the aspects in a penetration test from enumeration to service discovery to gaining access to privilege escalation. Topics like AV bypass, SSH tunneling and pivoting will also be mentioned. 