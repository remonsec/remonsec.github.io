---
title: How I get my first SWAG from SIDN (Sensitive Data Exposer)
author:
  name: remonsec
  link: https://github.com/remonsec
# date: 2019-08-08 11:33:00 +0800
categories: [Bugbounty]
tags: [bugbounty]
pin: true
---

## How I get my first SWAG from SIDN (Sensitive Data Expose)

**بسم الله الرحمن الرحيم**

## Introduction

Assalamu Alaikum 
(Peace Be Upon You)

I am Mehedi Hasan Remon. 
Student of Computer Science Engineering. I am learning about Web Penetration Testing and doing Bug Bounty as a side activity.

Let's start the story

## Background

I just weak up and start scrolling on my Facebook timeline. I saw someone posted in the Bug Bounty Poc group that he got a SWAG from SIDN for reporting a vulnerability. That T-Shirt was really awesome and I also have a friend [**Asif Farabi**](https://www.facebook.com/asiffarabi000) who has that same SWAG from SIDN. So my mind said 
“Let’s Give it a Shot”

## How I found the Bug

I fire up my Kali Linux, start my recon with [**Sublist3r**](https://github.com/aboul3la/Sublist3r)

From Sublist3r I found an interesting domain called 
mailman.sidn.nl

![](https://cdn-images-1.medium.com/max/2000/1*rpF4-XnBw3HpS5C-KtJFHA.jpeg)

After playing around the target I found a directory called 
mailman.sidn.nl/pipermail
But there was a 403 for that directory

![](https://cdn-images-1.medium.com/max/2000/1*pZu8Ti8QcEObC09WBY5v4A.png)

But then I put a ‘/’ after the pipermail directory 
Like This: mailman.sidn.nl/pipermail/

![](https://cdn-images-1.medium.com/max/2000/1*a2l0W9j5tyTwqlvHZbm4jw.png)

Boom … 
It takes me inside the directory. Inside that directory, I found lots of private emails about the company. like their product relates emails, production emails, internal dev mails, etc.

![](https://cdn-images-1.medium.com/max/2000/1*6GlFrxctXnuyvr6Vz9bPpg.jpeg)

Then immediately I send them that Bug Report and asked Allah for the success

![](https://cdn-images-1.medium.com/max/2000/1*0IvKqZmHeEww27jZMMs59Q.png)

And then
Alhamdulillah (all praise is due to Allah)
Got this sweet SWAG

![](https://cdn-images-1.medium.com/max/3072/1*a_0VWzmqcOO-jDYFOpWzWw.jpeg)

![](https://cdn-images-1.medium.com/max/3072/1*L-IhWzE-SLYPRCh6XITMrQ.jpeg)

![](https://cdn-images-1.medium.com/max/4096/1*ySHOopXvlTVMMtIgpb5LBQ.jpeg)

## Bug POC

 [**PoC Video**](https://medium.com/media/c128e4ead6ce9f547d1ac75360f5a5a5)

## Conclusion

Thanks for reading till the end. If you want something then just take the action for it. Don’t just keep thinking that I will do it, I will do it. 
Work Hard
Try Insane
Rest of all your lord will decide
 
Be Secure Be Safe
Allah Hafiz (May Allah be your Protector)

Report: Jan / 21 / 2020
Trigger: Jan / 21 / 2020
Receive Swag: Jan / 29 / 2020
