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

![Excited GIF](https://media2.giphy.com/media/XyaQAnihoZBU3GmFPl/giphy.webp "Excited")

## Background

I just weak up and start scrolling on my Facebook timeline. I saw someone posted in the Bug Bounty Poc group that he got a SWAG from SIDN for reporting a vulnerability. That T-Shirt was really awesome and I also have a friend [**Asif Farabi**](https://www.facebook.com/asiffarabi000) who has that same SWAG from SIDN. So my mind said 
“Let’s Give it a Shot”

## How I found the Bug

I fire up my Kali Linux, start my recon with [**Sublist3r**](https://github.com/aboul3la/Sublist3r)

From Sublist3r I found an interesting domain called 
mailman.sidn.nl

[![1-rp-F4-Xn-Bw3-Hp-S5-C-Kt-JFHA.jpg](https://i.postimg.cc/43k6P7p5/1-rp-F4-Xn-Bw3-Hp-S5-C-Kt-JFHA.jpg)](https://postimg.cc/v4hxHmqg)


After playing around the target I found a directory called 
mailman.sidn.nl/pipermail
But there was a 403 for that directory

[![1-p-Zu8-Ti8-Qc-EOb-C09-WBY5v4-A.png](https://i.postimg.cc/y6Q05rFW/1-p-Zu8-Ti8-Qc-EOb-C09-WBY5v4-A.png)](https://postimg.cc/Thby50NX)

But then I put a ‘/’ after the pipermail directory 
Like This: mailman.sidn.nl/pipermail/

[![1-a2l0-W9j5ty-Twqlv-HZbm4jw.png](https://i.postimg.cc/5y6Qbbwy/1-a2l0-W9j5ty-Twqlv-HZbm4jw.png)](https://postimg.cc/7JrZNvtr)

Boom … 
It takes me inside the directory. Inside that directory, I found lots of private emails about the company. like their product relates emails, production emails, internal dev mails, etc.

[![1-0-Iv-Kq-Zm-He-Eww27j-ZMMs59-Q.png](https://i.postimg.cc/GhTTf3LS/1-0-Iv-Kq-Zm-He-Eww27j-ZMMs59-Q.png)](https://postimg.cc/bs8vDh2Q)

Then immediately I send them that Bug Report and asked Allah for the success

[![1-6-Gl-Frxct-Xnuyvr6-Vz9b-Ppg.jpg](https://i.postimg.cc/fWr05SN9/1-6-Gl-Frxct-Xnuyvr6-Vz9b-Ppg.jpg)](https://postimg.cc/Jtjnzntr)

And then
Alhamdulillah (all praise is due to Allah)
Got this sweet SWAG

[![1-a-0-VWzmqc-OO-j-DYFOp-Wz-Ww.jpg](https://i.postimg.cc/qvXqfz9Q/1-a-0-VWzmqc-OO-j-DYFOp-Wz-Ww.jpg)](https://postimg.cc/Js0MZ47B)

[![1-L-Ih-Wz-E-SLYPRCh6-XITMr-Q.jpg](https://i.postimg.cc/qR9CLghr/1-L-Ih-Wz-E-SLYPRCh6-XITMr-Q.jpg)](https://postimg.cc/YGz92rzD)

[![1-y-SHOop-Xvl-TVMMt-Igpb5-LBQ.jpg](https://i.postimg.cc/fRhfsqbs/1-y-SHOop-Xvl-TVMMt-Igpb5-LBQ.jpg)](https://postimg.cc/3dnvCBpf)

## Bug POC

[![poc](https://img.youtube.com/vi/J30KmyQetO0/0.jpg)](https://www.youtube.com/watch?v=J30KmyQetO0)

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

___
wanna support my work! well just buy me a coffee

[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/remonsec)
