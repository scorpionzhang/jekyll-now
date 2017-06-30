---
published: true
layout: post
---
OSCP Review - A STORY ABOUT TRYING HARDER!!!

### 0x00 - Prologue
OSCP - Offensive Security Certified Professional, is an ethical hacking certificate that is gaining much popularity around the globe in recent years. 

Contrary to most security certificates (CEH, CISSP, CISM, CISA, etc.), OSCP is very unique in the following ways:
1. There is no official textbook, no classroom training. You will be given a virtual lab environment to practise by yourself.
2. The exam is not Multiple-Choice based. You will need to conduct a simulated penetration test.
3. You don't need to pay to renew the certificate every year.
4. You really need to Try Harder. (I mean HARDER)

In short, it's a challenging while rewarding certificate to get for us infosec people. 

### 0x01 - Why OSCP
Like the name suggests, OSCP's focus is ***offensive security***. In Sunzi's *Art of War*, there is a famous idiom "Know yourself and know your enemy, and you will never be defeated". (知己知彼，百战不殆) Same concept here, in order to prevent a hacker's attack, you have to understand how a hacker will attack. The course is all about real world techniques used by modern hackers and real world examples that you would see out there in corporate environment.

I myself have been doing penetration testing as my job for many years, but I kind of feel that I still need a systematic training, particularly on some very specific technical aspects, like the exploitation of Buffer Overflow vulnerabilities (in my daily job there is no chance for me to exploit such a vulnerability in a client environment.). And it turned out that the OSCP learning experiences didn't at all let me down!

One more good thing about OSCP is that obtaining the certificate will award you as many as **40 CPE hours**, that is a whole year's requirement! One more good thing for those working in UK/AU/NZ/SG, obtaining OSCP can also grant you the **CREST Registered Tester** certificate, after you have passed their level 1 exam which is CREST Practitioner Security Analyst. (normally you need to take CRT exam after the CPSA exam)

### 0x03 - How to get OSCP
So the overall process towards your OSCP is like:
1. Submit the application to Offensive Security and pay for it
2. Receive course materials(PDF+video) and lab connection package
3. Read through everything and try harder in your lab session (optional extensions can be bought)
4. Take the 24 hours exam and submit an exam report in the next 24 hours
5. If pass, get the certificate

In the next couple of sections I will share my experiences. 

### 0x04 - Preparation Studies
Although I am quite familiar with penetration test side of things, I would not consider myself to be an advanced programmer. Note that your lab session starts to count as soon as you received your course materials. If you have a full time job, then probably you might need 1 week to go through all the videos and the PDF. So it's better to have some preparation studies first before you made the purchase. You can skip this section if:
1. You don't mind spending a lot of money on purchasing additional lab time (US$250 for a month)
2. You already know how to do a proper penetration test (Not merely an automatic vulnerability scan)

For those who haven't skipped, here I briefly summarised the required knowledge you should have before you go into the charged lab environment:
1. How to use security tools like Nmap, Nikto, Dirb, Metasploit.
A good tutorial is:[https://www.offensive-security.com/metasploit-unleashed/](https://www.offensive-security.com/metasploit-unleashed/)

2. How to read and modify programs written in C, Python, shell script 
(You don't need to be an super advanced programmer, but occasionally you might need to modify a particular part to make things work)

3. How to exploit common web application vulnerabilities.
A good tutorial is bWapp: [http://www.itsecgames.com/](http://www.itsecgames.com/)

4. Have an idea about Buffer Overflow.
A good tutorial is [http://www.primalsecurity.net/0x0-exploit-tutorial-buffer-overflow-vanilla-eip-overwrite-2/](http://www.primalsecurity.net/0x0-exploit-tutorial-buffer-overflow-vanilla-eip-overwrite-2/)

4. Get familiar with what a lab machine will look like.
On Vulnhub.com there are plenty of CTF style VMs for you to play with. A good start will be the Kioptrix series: [https://www.vulnhub.com/series/kioptrix,8/](https://www.vulnhub.com/series/kioptrix,8/) [This step is optional, as the lab is just like this kind of format]

### 0x05 - Course materials and Lab session
The course materials are pretty straight forward, in an easy to understand way it covers all the aspects in a penetration test from enumeration to service discovery to gaining access to privilege escalation. Topics like AV bypass, SSH tunnelling and pivoting will also be mentioned. There will be course exercises in each section.

Once you feel you are good to go, you are in the most interesting part of the journey which is the lab session. 

You will be given a virtual coporate network consisting of 50+ vulnerable hosts of different nature. There will be out-dated Windows XP and 2003, as well as new versions like Windows 2008 and 2012. There will be FreeBSD and various Linux distributions. Each host can be exploited in one or more ways, with or without Metasploit. 

After you have pwned the hosts, you can find evidence text files as loots, as also in the exam hosts. In the end of the lab session / exam, you will need to submit the loots back to Offensive Security.

Some of the lab hosts were quite straight forward, and one exploit without modification would get things done. But some of them are really troublesome, in these cases you need to combine clues from different places to form a big picture, and some of the clues were even hiding in other lab hosts...

In some of the lab hosts you will find a network key file, which is used to unlock other subnet you can play with. If time is limited I think it's okay if you don't go into other subnets. Just focus on the environment you are initially in.

Many people's comment on OSCP involve a saying that "It's all about enumeration!" and I think it's also true in a real world pentest. In security we often say that "People is the weakest link" as humans will make all kinds of mistakes. If you can identify these mistakes then you know how to conduct a successful attack. It's kind of like in military actions, ancient or modern, reconnaissance is the most important thing.

**NOTE ABOUT EXERCISE REPORT AND LAB REPORT**

The reports for course exercises and lab hosts are optional. But they do give you the opportunity to have 5+5 extra points during the exam. Personally I didn't go for the 10 points as I found it too time consuming to write them (must be several hundred page long). And like I mentioned above, I do pentest in my daily job so I know how to write a proper pentest report.

If you are not familiar with how to write a pentest report I would suggest you take the chance and practice. You will not waste your time.

**NOTE ABOUT METASPLOIT**

In the lab, you are free to use Metasploit as you wish, and in many cases it will definitely make your life a lot easier. But remember that in the exam, you are only allowed to use Metasploit on **ONE** host. (This will including the use of Auxiliary modules, Exploit modules, POST modules as well as Meterpreter. But you are free to use Multi Handler as long as the payload is not meterpreter.)

So for your own good, you should practice to pwn things without Metasploit. For me, the joy of pwning a system through the hard way (without Metasploit) is much higher compared to the one-click-exploit way, especially when you have gone through endless frustrations during the exploitation phase.

### 0x06 - Exam and Report

The exam is also an unforgettable experience as it's a continuous 24 hour simulated pentest for 5 hosts, and then followed by 24 hours for you to complete a detailed report. They hosts will have different scores from 10 to 25. In the end you will need 70 out of 100 to pass. That is, any 4 out of the 5 hosts in your exam network.

I have scheduled my exam on 5pm on a Friday (I took an annual leave for that day) and worked until 2pm in the evening (I had a quick light dinner on 8:00pm). I didn't consume any Redbull or Coffee but I did had some Coke and green tea. By that time I already knew I would pass as I already had 80 points. So I took a good sleep and continued the next day on 9:30am but finally I could not successfully pwn the last one. It was SOOOOOOOO close and I don't know what has gone wrong. 

I used the last hour to go through all my notes, to make sure I didn't miss any important step screenshots. And I did! It's suggested that you at least reserve 45 minutes time for this step. (the exam VPN connection will terminates at 23:45 hours, so don't expect to do anything in the last 15 minutes)

Already knowing I would be a pass, I went out with my families for a BIG dinner and played HOTS with my wife afterwards. (Yay I am a Blizzard fans) 

It turned out on the next day I was too happy to get up early, and later I found myself nearly not having enough time for the report. 

A OSCP exam report is not like the pentest report I would write in my daily job, it has to follow a particular format (Although you are free to use your own, I think it's safer to follow the official standards). The Offensive Security template is available at this URL: [https://www.offensive-security.com/pwk-online/PWKv1-REPORT.doc](https://www.offensive-security.com/pwk-online/PWKv1-REPORT.doc)

At least you need the following contents:
1. A detailed walkthrough of how you pwned each host (initial shell, PE)
2. A list of vulnerabilities you have exploited, and how to fix them

Note that not all the sections in the template are needed, and you can add new sections to suit your needs. In fact I spent more than 1 hour fine-tuning my report template before I start to work on the real report. I was so nervous about not being able to finish the report in time so I even asked my pregnant wife to feed me during lunch hours so that I can keep my hands on the keyboard. 

Finally I was so lucky to have finished everything 1 hour before the deadline.

After a few days I am so happy to receive the email from Offsec:
![oscp-msg.png]({{site.baseurl}}/_posts/oscp-msg.png)

Such a relief!!!

### 0x07 PostScript
I can't reveal more details about the exam but my general tips is that:

- Read through the exam guide and pay attention to all the requirements! (VERY IMPORTANT)
- Make your own cheatsheet!
- Get a good rest on the exam day and the day before.
- Don't overestimate the difficulty of the exam boxes. They are generally easier than those most frustrating lab boxes. 
- Focus on ENUERATION!!! Focus on ENUERATION!!! Focus on ENUERATION!!! 
- Be careful and don't fall into rabbit holes. But if you believe you have found some obvious clues just go for it.
- Google is your best friend.
- Take notes and screenshots along the way, especially during key steps. You will need them to complete your reports. 
- Write you report earlier! 

### 0x08 Post Postscript
Some useful materials I have used during the course:

Reverseshell cheat sheet: [https://highon.coffee/blog/reverse-shell-cheat-sheet/](https://highon.coffee/blog/reverse-shell-cheat-sheet/)

MSFVenom cheat sheet: [http://netsec.ws/?p=331](http://netsec.ws/?p=331)

SQL Injection Cheat Sheet: [https://websec.ca/kb/sql_injection](https://websec.ca/kb/sql_injection)

LFI Cheat Sheet: [https://highon.coffee/blog/lfi-cheat-sheet/](https://highon.coffee/blog/lfi-cheat-sheet/)

Kernel Exploit Search: [https://www.kernel-exploits.com/](https://www.kernel-exploits.com/)

Windows Hacking Pack: [https://github.com/51x/WHP](https://github.com/51x/WHP)

Windows Privilege Escalation Fundamentals: [http://www.fuzzysecurity.com/tutorials/16.html](http://www.fuzzysecurity.com/tutorials/16.html)

Linux Privilege Escalation Scripts: [https://netsec.ws/?p=309](https://netsec.ws/?p=309)


### 0x09 ALWAYS TRY HARDER!!!