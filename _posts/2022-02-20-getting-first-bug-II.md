---
title: Getting Your First Bug (Part II)
author:
  name: remonsec
  link: https://github.com/remonsec
# date: 2019-08-08 11:33:00 +0800
categories: [Bugbounty]
tags: [bugbounty]
pin: true
---

## Getting Your First Bug (Part II)

**بسم الله الرحمن الرحيم**


Assalamu Alaikum
peace be upon you

**Note**
This is not a How To Get Started type of write up. I assume you already know the basics now struggling to get your first bug.

In part-1 I explained two different categories of BugBounty. That’s the thing everyone was hiding. I am not inspiring or demotivating with those categories. I am just showing beginners a clear pitcher of BugBounty. that’s all

I see from Twitter everyone is interested in Active BugBounty stuff. So today I will focus more on that

## Passive BugBounty

Passive BugBounty is kind of passive earning something like that. Invest time & energy and get back the result. Most of the time people with no infosec interest or people with no basic knowledge about infosec start BugBounty passively. But yes you will see top pro hunters doing passive BugBounty as well. But their setup and understanding is another level. They use to put all of their past experience and skill to build a master passive workflow for them. Don’t even expect something from today's writeup. Today's passive workflow will be easy and simple.

**Workflow**

- Subdomain Takeover

- Nuclei Scan

As Nuclei will cover most of the known surface level bugs, so I don’t think I should waste my time writing all those bugs here one by one. But then why I mentioned Subdomain Takeover differently! Well let’s have a look

I have done some research before writing this write-up. I tried both passive & active hunting on my own to experience the real environment that beginners will face with those ideas. To make you feel good I want to say that I found bugs with both the Active and Passive BugBounty method, also earned some cash $$$ for my findings. Sounds cool at least for me xD

**Subdomain Takeover**

This bug is nothing just telling companies that, hey you are no longer using that service for your subdomain. I am using this on behalf of you. Now shut up and pay me for not abusing

All you have to do pick a massive amount of targets & gather as much subdomain as you can. Run multiple subdomain takeover scanners and verify them on your own manually.

I tried with bash, by creating a shell script that takes a large amount of domain as input and enumerates subdomains, checks for takeover & stores the data for manual verification. You don’t have to go that far just make sure you have a good amount of target to check their subdomain takeover issues

[![1-e3-DVJMm-ZX5-Hi-Db-Db-JF3-YA.png](https://i.postimg.cc/2yzhNHfW/1-e3-DVJMm-ZX5-Hi-Db-Db-JF3-YA.png)](https://postimg.cc/WFHhMwzp)

As you can see It scanned over 984 domains and end up having 20 detections and after manually verifying the amount was less than that. But hey It works. I found one takeover on Amazon but Subdomain Takeover on Amazon was out of scope, I didn’t notice that but it was their core subdomain so they resolved it but didn’t pay any bounty for my finding

[![1-8-Q-MWio4kk1na-KDte3-P6-Q.jpg](https://i.postimg.cc/dQyVJR0k/1-8-Q-MWio4kk1na-KDte3-P6-Q.jpg)](https://postimg.cc/4nXg59Vs)

Got some over self-hosted Responsible Disclosure Programs. Takeovers on Heroku, AWS, GitHub was common there & received bounties as well

[![1-Vk8adw-L9d-GFautaaa46n-AQ.png](https://i.postimg.cc/1XGSwHgv/1-Vk8adw-L9d-GFautaaa46n-AQ.png)](https://postimg.cc/Mfpg81mB)

If you target small companies like this your chance is high to get paid out there. You will get several BugBounty google dork on GitHub use them or make your own

If you want to go with platforms like HackerOne BugCrowd then I recommend going with external programs. Like they are not listed on HackerOne directly they may invite after reporting on their security email. then they pay the reward from HackerOne directly. You can take Mcafee as an example. As people don’t know much about those external programs it's a good place to make hands dirty

**Nuclei Scan**

Well, this is also going to be the same as like Subdomain Takeover workflow. Make sure you have a massive amount of targets that's all

Build a similar bash script for Nuclei scan that take targets as input and check for issues and store the result

[![1-Bdf5pfkwb-J1-Ec-V952-NVA.png](https://i.postimg.cc/52khHG7x/1-Bdf5pfkwb-J1-Ec-V952-NVA.png)](https://postimg.cc/DSLjHC3D)

You are going to have issues like log file disclosure, config file disclosure, Jira wp issues, basic misconfiguration, etc. Most of the time you are just going to have low issues that the company even doesn't care about. But at some point, you will receive some small to big bounties depend on the bug you have

Here I scanned once and got some low, medium issues. Also received bounties as well, the payout was so low tho

[![1-e-RSZKw5-Ieot-Bgpy-RJo-Ba-IQ.jpg](https://i.postimg.cc/zX2tphn7/1-e-RSZKw5-Ieot-Bgpy-RJo-Ba-IQ.jpg)](https://postimg.cc/D8sPw8p4)

I just can’t report those low-hanging fruits again & again so wrote some templates to automate the reporting part as well. I don’t want to waste my time in those areas

[![1-Soh-JHJm5b5lzv-V5-Fmw-KXWA.png](https://i.postimg.cc/8PLB3nfZ/1-Soh-JHJm5b5lzv-V5-Fmw-KXWA.png)](https://postimg.cc/ykYZ3jPR)

**Note**

I even don’t know where those programs came from. I didn’t even visit any of those sites to see how they look like. I tried with python to build a scraping tool but I failed for my poor programming knowledge, then I just somehow manage to build one with bash and fetching data from some GraphQL DB as well. Don’t inbox me how I did that. This is something I like to keep in my secret box, but will expose in the future for sure :)

## Active BugBounty

Now the real hacking & fun start from here. If I am honest I didn’t enjoy while doing passive BugBounty. That kinda boring and not challenging as anyone can do those things. I just passed 1 day to build that scarping tool and 10–20 minutes for subdomain takeover and nuclei automation script. that's all. it took 2-3 days to scan over all the targets and then took 1–2 hours to report them. Learned nothing, My skill level was the same as before.

From InsiderPHD BugBounty series I saw she mentioned IDOR as a beginner-friendly bug. I didn’t try with IDOR that much before. So it's a good chance for me to learn something new and do my experiments as well. Why I am not recommending XSS! it’s not actually that beginner-friendly for modern web apps at least not from my experience. I have wasted my previous week with passive BugBounty, maybe earned some $$$ but still, it’s just a waste of time for me so I started doing my experiments as fast and as deep as I can

**Workflow**

- Pick a bug then Learn & Earn

- IDOR

- CSRF

- Information Disclosure

- More you will discover yourself ;-)

## **IDOR**

This is something where you are able to steal other user data can perform actions on behalf of another user so and so on. Just google a little bit and research your own to understand the basics of IDOR what this issue actually is and why it occurs. After you have learned the basics now see how you can approach to find them!

**By not touching the target at all**

Well, this is called passive hunting. You use 3rd party sources to collect data about your target and exploit it depend on what you have. Enough talk let’s give it a shot

**workflow**

- Crawl

- Verify

- Exploit

You can use tools like waybackurls, gau to crawl over your target to collect endpoints and js files. from those js files, you also can collect more endpoints then verify based on their parameters. you can use tools like GF or just manually poke around those endpoints. Then exploit that endpoint depend on its behavior or structure.

I just can’t write something like do this, do that, you will find IDOR. I just can show you the general approach there is no fixed way to hack into stuff. you have to figure things out depending on the situation and environment 
Let me show you mine, how I get one yesterday

[![1-ZZNm9u71klt-B5-YS09y-P0q-Q.jpg](https://i.postimg.cc/YSC6vrnP/1-ZZNm9u71klt-B5-YS09y-P0q-Q.jpg)](https://postimg.cc/K1CkV2y7)

Like here you have a JS file. You can use LinkFinder to collect endpoint from that file. Here it clearly shows that it takes input and gives back user info. So what! just have to put a random number that’s all.

They applied a temporary fix there and will let me know if that asset was in scope for reward or not. As I expended so far with my recon So it looks like I crossed in scope boundary xD

**Poking around each and every request**

Well, I have exploited another IDOR. That was on their API. I use to get that API endpoint from their main web app. like checking logger++ logs and retesting every request. I am not sure how to show you that IDOR exploitation. As it sounds a little bit sensitive and they are still working on it to fix the issue. Then they will reward for it. I am just giving a SS that shows how things look like. But don’t angry with me if I hide too much

[![1-ty-ROJ4-IAHr-BVf3bkgl-rj-A.jpg](https://i.postimg.cc/c1RvNqTt/1-ty-ROJ4-IAHr-BVf3bkgl-rj-A.jpg)](https://postimg.cc/t7gqhMK9)

[https://targetapi/api/path/$username/notices](https://targetapi/api/path/$username/notices)

It fails to validate the token and give back a response for any client. I know why it still out there even it's a public RDP program. that endpoint was a little bit confusing to find. Another endpoint was referred to this endpoint so if I didn’t check for all requests I also may miss it as well

Oh dude, I can’t write more. I am writing this for the last 2 hours. Seriously I am too much slow. Anyway let’s continue

## **CSRF**

With CSRF you fool the victim to do actions that the victim doesn’t want to do at all. My words making no sense! then what stopping you to do some googling!

Nowadays you will not see CSRF like before, where no token was available and you just can copy-paste burp CSRF payload and exploit. Now as they are using CSRF tokens so what you can do check if they actually validating CSRF tokens well. it's so simple and you can use your own creativity to expand the attack methods

I found one on Harvard marked as valid and they resolved as well. But my bad luck that subdomain was out of scope so didn’t receive any letter.
Mentioning the reproduce part POC video also available

1 login with your account 
2 change the email address and capture the requests
3 take the CSRF token from /CSRF endpoint and use it in /change email endpoint instead of X-CSRF final token (those token are not same) 
4 send a request in /CSRF endpoint again see they change the token
5 use that old token in /change-email endpoint
6 you see it still working even there is a new CSRF token

[![csrf_poc](https://img.youtube.com/vi/dDCKhoIFEtE/0.jpg)](https://www.youtube.com/watch?v=dDCKhoIFEtE)

## Information Disclosure

Anything that exposes your GF phone number! kidding man, So the thing here is you have to think about what information your target is collecting or giving importance. Then based on that target you can look for several methods to collect maybe some data or at least view something that you should not

It can be separated in two different way

- Client-Side Information

- Server-Side Information

**Client-Side Information**

Just aim for the users. look for the places where you can see your own information and then try to play around the request to check if you can view other data instead of your own. it can be some IDOR, SQLI, or whatever. I am not showing you here what you have to do just showing you how to think when you will be there.

You are lucky that I have a for you that shows how IDOR can leak clientside information

[![idor](https://img.youtube.com/vi/R0dIk0fY5ro/0.jpg)](https://www.youtube.com/watch?v=R0dIk0fY5ro)


**Server-Side Information**

Well, here our main aim is to collect backend data as much as we can. It can be source code, web components, config files, anything that the server will not feel good to give in response

You can also aim for firewall bypasses to view what the firewall trying to protect from you. It’s not easy as you must have basic understanding well, without knowing the basics you will not get the idea where you have to hit hard

I have good findings in this area. Most of the time it was deep FUZZ and 403 bypasses. I have a writeup on 403 bypasses check this out this Guide for bypass 403 endpoints 
[**KathanP19/HowToHunt**](https://github.com/KathanP19/HowToHunt/blob/master/Status_Code_Bypass/403Bypass.md) 

[![1-2-Ebp-Pi-L7f-G8-OHo-D1l-Z22-Q.png](https://i.postimg.cc/26FrgYmz/1-2-Ebp-Pi-L7f-G8-OHo-D1l-Z22-Q.png)](https://postimg.cc/sQXkZtv8)

[![info_bypass](https://img.youtube.com/vi/7kcK8JYinLI/0.jpg)](https://www.youtube.com/watch?v=7kcK8JYinLI)


## EndNote

Enough dude, I can’t write more. Seriously I can’t even focus on what to write next. I also don’t know how you still reading this. I only can see you are the next Hero of the InfoSec world, who is just going to use his power for the good.

Make sure your words and character inspire others. As a BugHunter, you can leave a good impact on society. Oh one more thing, don’t forget your origin & who you was before, support every one of them who supported you when you was lost. Pray for a better life & Fight for a better world

[![1-Qgm9-Tyht-Hr-LMDxa-Rp2-XQqg.jpg](https://i.postimg.cc/nzkf01Yr/1-Qgm9-Tyht-Hr-LMDxa-Rp2-XQqg.jpg)](https://postimg.cc/vgcKmfKw)

Welcome my boy, can’t wait for more to see you Rising & Fighting
Allah Hafiz

___
wanna support my work! well just buy me a coffee

[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/remonsec)
