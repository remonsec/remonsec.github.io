---
title: Passive Recon with Spyse (Part-II)
author:
  name: remonsec
  link: https://github.com/remonsec
# date: 2019-08-08 11:33:00 +0800
categories: [Bugbounty]
tags: [bugbounty]
pin: true
---

## Passive Recon with Spyse (Part-II)

**بسم الله الرحمن الرحيم**

Assalamu Alaikum
peace be upon you

## Introduction

In part-1 I showed mass attack technique like subdomain takeover. in part-2 I will show some more about mass attacks and also about specific target recon. Last week I get some bounties by doing my recon with [Spyse](https://medium.com/u/943b150c124e?source=post_page-----3d6bce47365-----------------------------------). Let me share my experience with you

## Mass Attack

So last time we saw some mass subdomain takeover

![](https://cdn-images-1.medium.com/max/2588/0*T9XwBhMsJCJAJSI_.png)

what about other issues ! let me share a query that [**Markroze**](https://twitter.com/_markroze) shared with me

![](https://cdn-images-1.medium.com/max/2718/1*RUHHhy-C84XCbaVW9zcEnw.png)

![](https://cdn-images-1.medium.com/max/2716/1*ZTkFR3m5W8_7MqmNICwaiQ.png)

we can search for specific things. like here we have WATTrouter service you can do more query like jira, openvpn, wordpress so and so on
But this act can be extremely evil hacking on random assets makes no sense.

Now it’s time to filter those things to find out websites with responsible disclosure policy

![](https://cdn-images-1.medium.com/max/2000/1*boQZr5Ot155F-N3th4WIOg.png)

Download your search result in CSV format, cut the end url and bruteforce the list with some common disclosure endpoint 
You may need a pro account to download your search result.

![](https://cdn-images-1.medium.com/max/2384/1*PVjOMV5DlXdxgb93t_YyDQ.png)

After that you can FUZZ like this to get out all hosts with disclosure program
**NOTE**: FFUF -mr flag not working properly for me. If you face similar let me know, btw you can do similar with bash, python . . .

![](https://cdn-images-1.medium.com/max/2000/1*H8BxeY_dhe3XWJgfbITrcQ.png)

Okay enough. we are done with mass attack things. do your own research to find out more interesting query and attacks.

## Recon your Target

![](https://cdn-images-1.medium.com/max/2000/1*m1NH5uG5ic86rhaewgzHuA.png)

After searching your target you will see things in crawler section. there’s a panel called related. that one really helps. you will see similar data there like if any other host is using similar icon of your target website

![](https://cdn-images-1.medium.com/max/2196/1*LJqEgauOEgAUqglKXT1GbA.jpeg)

You will be getting AWS buckets that target company use to host assets. Now you can look for access control issues for those buckets. you will also get interesting 3rd party hosting services that your target may using for their asset hosting or any other work. so those 3rd party hosts also can lead security issue for your target

![](https://cdn-images-1.medium.com/max/2000/1*0wehjS7wAqpZQhQ3dzTr4g.png)

If you move into DNS history & related category again you will see some options there to look into. This feature of Spyse helped me to earn some $cash last week

![](https://cdn-images-1.medium.com/max/2000/1*ggboRCNC1pPWXBlG03jlaA.jpeg)

webapp hosted on server from Canada was secure but same webapp hosted from US server was vulnerable with multiple server side attacks. 
That program was live from 2014. In 2021 they resolved 10 reports 6 of them is mine.

![](https://cdn-images-1.medium.com/max/2000/0*rZePHnRuXQP3Ro2A)

![](https://cdn-images-1.medium.com/max/2000/0*kzSpkUpZzxo4R6f8)

![](https://cdn-images-1.medium.com/max/2000/0*8tjTO4R6KBi073H8)

![](https://cdn-images-1.medium.com/max/2000/0*Z1MzMU7Eb9Dfncfw)

![](https://cdn-images-1.medium.com/max/2000/0*2LVAq6mNdtYZalY2)

![](https://cdn-images-1.medium.com/max/2000/0*960RGfz4RFyFipFd)

No one was looking there so it was easy for me to find bugs.

I attached all reward and resource screenshot as reference material. 
You should not believe in a random boy from internet at all. 
There should some kind of proof what I am saying.
 
Now some will show offence that I am doing show off, if I don’t attach screenshot then also some will show offence that I am not telling the truth.

Whatever I am leaving it to you, you can show love or hate it’s your choice I am already broken so it make no changes to me :)

Those are things I found interesting for BugBounty hunters on [Spyse](https://medium.com/u/943b150c124e?source=post_page-----3d6bce47365-----------------------------------). You also can look into your own for other features. This recon writeup series sponsored by Spyse. They offered me their pro account to use and let them know my feedback about their service.

You can see it your own how I used [Spyse](https://medium.com/u/943b150c124e?source=post_page-----3d6bce47365-----------------------------------) for BugBounty stuff and earned some cash. Thanks [Spyse](https://medium.com/u/943b150c124e?source=post_page-----3d6bce47365-----------------------------------) for the sponsorship and your amazing service

I am ending this writeup here. If you have any question you can ask me on Twitter at this handle **remonsec**. If you have general questions then instead of DM you can mention me on your tweet. So other also may get benefit from your question or if I don’t know the answare I may mention someone who knows

Have a sweet day everyone
Allah Hafiz

![](https://cdn-images-1.medium.com/max/2000/1*WVOxP0DnLiD8LpLty3NJXQ.jpeg)
