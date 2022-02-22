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

[![](https://i.postimg.cc/x8Rmfm5q/0-T9-Xw-Bh-Ms-JCJAJSI.png)](https://postimg.cc/CnR5JzWV)

what about other issues ! let me share a query that [**Markroze**](https://twitter.com/_markroze) shared with me

[![1-RUHHhy-C84-XCba-VW9zc-Enw.png](https://i.postimg.cc/ydSvsQc8/1-RUHHhy-C84-XCba-VW9zc-Enw.png)](https://postimg.cc/34YgZZts)

[![1-ZTk-FR3m5-W8-7-Mqm-NICwai-Q.png](https://i.postimg.cc/Qd4b5GqM/1-ZTk-FR3m5-W8-7-Mqm-NICwai-Q.png)](https://postimg.cc/HrMXDNRG)

we can search for specific things. like here we have WATTrouter service you can do more query like jira, openvpn, wordpress so and so on
But this act can be extremely evil hacking on random assets makes no sense.

Now it’s time to filter those things to find out websites with responsible disclosure policy

[![1-bo-QZr5-Ot155-F-N3th4-WIOg.png](https://i.postimg.cc/Wpw0gcNP/1-bo-QZr5-Ot155-F-N3th4-WIOg.png)](https://postimg.cc/7bbCrcJB)

Download your search result in CSV format, cut the end url and bruteforce the list with some common disclosure endpoint 
You may need a pro account to download your search result.

[![1-PVj-OMV5-Dl-Xdxgb93t-Yy-DQ.png](https://i.postimg.cc/8z9vN1HL/1-PVj-OMV5-Dl-Xdxgb93t-Yy-DQ.png)](https://postimg.cc/gxyjKb10)

After that you can FUZZ like this to get out all hosts with disclosure program
**NOTE**: FFUF -mr flag not working properly for me. If you face similar let me know, btw you can do similar with bash, python . . .

[![1-H8-Bxe-Y-dhe3-XWJgfb-ITrc-Q.png](https://i.postimg.cc/tC1CyFmm/1-H8-Bxe-Y-dhe3-XWJgfb-ITrc-Q.png)](https://postimg.cc/JGLW5H8b)

Okay enough. we are done with mass attack things. do your own research to find out more interesting query and attacks.

## Recon your Target

[![1-m1-NH5u-G5ic86rhaewgz-Hu-A.png](https://i.postimg.cc/fb7YKGcX/1-m1-NH5u-G5ic86rhaewgz-Hu-A.png)](https://postimg.cc/7C6CPQQY)

After searching your target you will see things in crawler section. there’s a panel called related. that one really helps. you will see similar data there like if any other host is using similar icon of your target website

[![1-LJq-Egau-OEg-AUqgl-KXT1-Gb-A.jpg](https://i.postimg.cc/vmm6r4mR/1-LJq-Egau-OEg-AUqgl-KXT1-Gb-A.jpg)](https://postimg.cc/TKZwGYmQ)

You will be getting AWS buckets that target company use to host assets. Now you can look for access control issues for those buckets. you will also get interesting 3rd party hosting services that your target may using for their asset hosting or any other work. so those 3rd party hosts also can lead security issue for your target

[![1-0wehj-S7w-Aqp-ZQh-Q3dz-Tr4g.png](https://i.postimg.cc/vZ04ZGt0/1-0wehj-S7w-Aqp-ZQh-Q3dz-Tr4g.png)](https://postimg.cc/VJbf7QTt)

If you move into DNS history & related category again you will see some options there to look into. This feature of Spyse helped me to earn some $cash last week

[![1-ggbo-RCNC1p-PWXBl-G03jla-A.jpg](https://i.postimg.cc/TPmvH91n/1-ggbo-RCNC1p-PWXBl-G03jla-A.jpg)](https://postimg.cc/4KJ0Ypz3)

webapp hosted on server from Canada was secure but same webapp hosted from US server was vulnerable with multiple server side attacks. 
That program was live from 2014. In 2021 they resolved 10 reports 6 of them is mine.

[![0-r-Ze-PHn-Ru-XQP3-Ro2-A.jpg](https://i.postimg.cc/rFdnJpKr/0-r-Ze-PHn-Ru-XQP3-Ro2-A.jpg)](https://postimg.cc/2VD7jrdk)

[![0-kz-Spk-Up-Zzxo4-R6f8.jpg](https://i.postimg.cc/HxZz0Gmz/0-kz-Spk-Up-Zzxo4-R6f8.jpg)](https://postimg.cc/5Yz81R6Q)

[![0-8tj-TO4-R6-KBi073-H8.jpg](https://i.postimg.cc/xTS5KPDW/0-8tj-TO4-R6-KBi073-H8.jpg)](https://postimg.cc/9zJy2Zfp)

[![0-Z1-Mz-MU7-Eb9-Dfncfw.jpg](https://i.postimg.cc/1zTc4Gr7/0-Z1-Mz-MU7-Eb9-Dfncfw.jpg)](https://postimg.cc/xkvb4b7L)

[![0-2-LVAq6m-Ndt-YZal-Y2.png](https://i.postimg.cc/hjTxjHjh/0-2-LVAq6m-Ndt-YZal-Y2.png)](https://postimg.cc/xJjqppLS)

[![0-960-RGfz4-RFy-Fip-Fd.jpg](https://i.postimg.cc/LXKYrNTS/0-960-RGfz4-RFy-Fip-Fd.jpg)](https://postimg.cc/PLy5Db9V)

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

[![1-WVOx-P0-Dn-Li-D8-Lp-Lty3-NJXQ.jpg](https://i.postimg.cc/d15F80Df/1-WVOx-P0-Dn-Li-D8-Lp-Lty3-NJXQ.jpg)](https://postimg.cc/cgtPW0R7)
