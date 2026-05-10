---
layout: post
title: Application Security Learning Materials 
date: 2026-04-22 15:09:00
description: Some of my favourite resources to learn with, putting my procrastination to some use.  
tags: AppSec
categories: Resource
featured: false
---

{% include figure.liquid 
   path="assets/img/books.jpeg" 
   alt="description" 
%}



In the past, I have often found myself falling down rabbit holes, 20 tabs deep, looking for resources to study with instead of actually studying. It's a habit I'm slowly breaking but I realise I’m definitely not alone with this cycle. 

When I decided to double down on my Application security study this year, I felt like there are a bunch of structured paths in software engineering, other areas of cyber and I’ve even noticed whilst studying for the OSCP there are numerous resources or knowledge banks for this.

However, I found AppSec stuff to be a bit scattered, specifically around secure code review, so I have decided to pull together all the resources I regularly use (or have used) so that it saves others time and allows people to just jump into studying. This is by no means comprehensive, or saying they are the best, I am just listing resources I have really enjoyed and found helpful (Also -  I thought I should turn my rabbit hole of procrastination research into something useful! 😅 ) 


## Books

First, I think it's important to get some book mentions out of the way. People often mention [Web Application Hackers Handbook](https://www.amazon.ca/Web-Application-Hackers-Handbook-Exploiting/dp/1118026470) as the bible. These people are far more experienced than myself so I can't argue with this, however the writers themselves referenced instead of producing a 3rd edition book, [Port Swigger replaces the need for this](https://portswigger.net/web-security/web-application-hackers-handbook) (Portswigger is created by the authors of that book!). I personally prefer the hands-on nature of the labs so it is up to you what you would prefer! 

A series of books I have found to be really useful are the books by Tanya Janca called [Alice and Bob Learn Secure Coding](https://www.amazon.ca/Alice-Bob-Learn-Application-Security/dp/1119687357/ref=pd_lpo_d_sccl_1/140-2147415-2317935?pd_rd_w=NklO1&content-id=amzn1.sym.d3f44101-6e04-446e-916c-a6ec5616982b&pf_rd_p=d3f44101-6e04-446e-916c-a6ec5616982b&pf_rd_r=XJ8E0TYQ32S39CMYRX3N&pd_rd_wg=NZhw5&pd_rd_r=90f19ac8-0313-4a0a-b6fa-873bbe203339&pd_rd_i=1119687357&psc=1) and [Alice and Bob Learn Application Security](https://www.amazon.ca/Alice-Bob-Learn-Secure-Coding/dp/1394171706). The latter is a comprehensive guide of what is expected of those concerned with Application Security whilst the former focuses on specifically how we can write secure code and identify when this isn’t the case. 

That leads me on to my final book recommendation [‘Bug Bounty Bootcamp: The Guide to Finding and Reporting Web Vulnerabilities’](https://www.amazon.ca/Bug-Bounty-Bootcamp-Reporting-Vulnerabilities/dp/1718501544/ref=sr_1_1?crid=3SM11MX1JL65P&dib=eyJ2IjoiMSJ9.XhNIvB8wr0b74nz4K_imnT11EjcADUu29A6cSHWGKp6C2_-ewQFPc2UMFGGVNL-GFigNIyf6tZq3Y211MrbHApEqKOVgbst7_YHDb5XmqUk.MTi92oXV4KnEdYsiuUidZn3Wd2JAVTRN2-0VnaSr_ys&dib_tag=se&keywords=bug+bounty+vickie+li&qid=1778454720&s=books&sprefix=bug+bounty+vickie+li%2Cstripbooks%2C109&sr=1-1) by Vickie Li. This book focuses on taking you from 0 to finding your first Bug Bounty. Whilst it focuses on bug bounties I think its a really good practical look into locating vulnerabilities on web applications. The chapter I have found really helpful is Chapter 22 ‘Conducting Code Reviews’ which covers popular vulnerable functions and identifying dangerous patterns with grep. 



### Secure Code Review

Following on from highlighting this chapter on code reviews I want to highlight specific resources I have used to continually work on my code review skills. Whilst manual code review is less frequent due to automated scanners, it's something that comes up in interviews, and at the end of the day if you can't read the code the scanners have highlighted then it will prove to be difficult to recommend remediation. 

As I mentioned - Tanya Janca’s Alice and Bob Learn Secure Coding is great, as is chapter 22 of Vickie Li’s Bug Bounty Bootcamp. In my MSc I had to write a paper on conducting a secure code review of some .NET code, I relied heavily on [OWASP Code Review Guide](https://owasp.org/www-project-code-review-guide/assets/OWASP_Code_Review_Guide_v2.pdf). This guide was written in 2017 but is still extremely useful.

I have found the OWASP cheat sheet series to be a resource that is more regularly updated and therefore the [OWASP Secure Code Review Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Secure_Code_Review_Cheat_Sheet.html) to also be a great reference. 

Now the problem I had was - ‘ok I now have these resources, I have a rough idea of what to look for - where do I practice this ? “. 

Firstly I’ll list some paid resources I use: [Pentester Lab](https://pentesterlab.com/) has a plethora of different vulnerable code snippets in different languages, with either videos explaining where the vulnerable code is or providing code snippets with the fix implemented in some code so you can compare between them. Hack The Box has specific ‘secure coding’ modules. The ones I have used and enjoyed are  [Introduction to WhiteBox Pentesting (500 Cubes)](https://academy.hackthebox.com/course/preview/intro-to-whitebox-pentesting) and 
[Parameter Logic Bugs (500 Cubes)](https://academy.hackthebox.com/app/module/239). This cost me a month of HTB platinum subscription - which is around $60 dollars. I plan to do a write up of my experience with this in the coming weeks. Additionally they have [HTB Secure Coding 101 - JavaScript (1000 Cubes)](httpshttps://academy.hackthebox.com/app/module/38://academy.hackthebox.com/app/module/38) and [White Box Attacks (500 Cubes)](https://academy.hackthebox.com/app/module/205) which I haven’t tried yet - with the former being quite expensive for 1000 cubes. 


Two corresponding articles by HTB and Pentester Labs on code review 
- https://www.hackthebox.com/blog/secure-code-reviews
- https://pentesterlab.com/exercises/codereview


If you are looking for free resources, there are plenty of these too: 
- [OWASP Secure Coding Dojo](https://owasp.org/SecureCodingDojo/codereview101/) These are snippet comparisons where you chose what you think is the vulnerable code, it refreshes each time you visit so you can keep testing so it sinks in. 
- A huge bank of vulnerable code to analyse in secure code review challenges has been created by dub-flow on Github which can be found [here](https://github.com/dub-flow/secure-code-review-challenges). Some of these have video walk throughs. This is a great resource for exposure to as many examples as possible.
- I haven’t dived into this repo but its worth mentioning : https://github.com/dehvCurtis/vulnerable-code-examples
- VulnHub has specific code review boxes (Secure Code, Pipe, Crypto Bank, Zorz, Potato, Ted).

Finally - I think its worth mentioning this [handy resource bank on Github](https://github.com/d3lb3/security-code-review?tab=readme-ov-file#training-materials) (I know im trying to avoid big banks with lots of links by writing this blog post but It's worth bookmarking for when you need more to learn from! )


## Getting more hands on 

So I covered some books, made an obligatory mention of WAHH and Port Swigger and now I want to mention some more platforms that allow more hands-on learning which I think is most important. These don't cover just secure code reviews but more broader Application Security. 

- Portswigger, you can either do their [curated paths](https://portswigger.net/web-security/learning-paths) , or just pick a [specific topic](https://portswigger.net/web-security/all-topics) 
- [SnykLearn](https://learn.snyk.io/user/learning-progress)
- AppSec Master(https://www.appsecmaster.net/en/challenges?tab=snippets)
- https://websec.fr/ (Web App CTF’s) 
- [Kontra Labs](https://application.security/free/owasp-top-10)

Hack The Box CVE & OWASP related boxes 
- [HTB Track - Hottest CVEs List](https://app.hackthebox.com/tracks/51)
- [HTB Track - OWASP 2021](https://app.hackthebox.com/tracks/68)
- [HTB Track - OWASP 2025](https://app.hackthebox.com/tracks/82)
