---
title: My Experience of Hacking Dutch Government
author:
  name: remonsec
  link: https://github.com/remonsec
# date: 2019-08-08 11:33:00 +0800
categories: [Bugbounty]
tags: [bugbounty]
pin: true
---

## My Experience of Hacking Dutch Government

*Bismillahi-r-Rahmani-r-Rahim*
*(In the name of Allah, the Compassionate, the Merciful)
Assalamu Alaikum (peace be upon you)*

## **Background**

Long story short,
I just get started with Bug Bounty in 2020 and saw this Bounty Boy ([**Mohammad Abdullah**](https://www.facebook.com/Abdul1ah)) with his Dutch Government swag.

[![1-Hl1u-Jc-QAb-Qyb-BQCEp-m-WA.jpg](https://i.postimg.cc/PrmrVYVG/1-Hl1u-Jc-QAb-Qyb-BQCEp-m-WA.jpg)](https://postimg.cc/vcZscgdX)

Just look at the Quote line. The word government was the killer one.
So now what, I need this swag badly. But wait, i just get started few weeks ago even don’t know how to run burpsuite. As like all other newbie i DM that guy for the tip how he got that. Then he just gave me a github repo and told me to try harder. 
Seriously man i was expecting he will give me something by running that script i will get the swag, at least some secret method. But what he gave me a list of domain for Dutch Gov websites. Here is the [**repo**](https://gist.github.com/random-robbie/f985ad14fede2c04ac82dd89653f52ad). It contain 650+ host to find bugs.

## My Approach

If i be honest i was so confuse coz i have to look into 650+ host and i dont know how to do basic vulnerability assesment. 
So i just reported some SPF & Clickjack but no luck they close as N/A. Fine, i have to do something else. After passing couple of days i understood that, with this knowledge it’s not possible to break into their security. I took a step back and start learning about some basics. Please note that during that whole week i visited most of that websites and saw that there is no authentication for those hosts so it means no more authentication related easy bugs. 
From a beginner point of view, it just sound insane and damn hard to hit. But we don’t care how hard it is right !

During that break time i start learning about Recon. Yes, you hear it right recon. This PentesterLand [**resources**](https://pentester.land/cheatsheets/2019/04/15/recon-resources.html) just worked awesome for me. I read all of them, every single one. After study couple of weeks i got a good basic understanding about how to approach a target in general

## Final Methodology

So we have lot’s of hosts with no authentication. So i call this workflow is, fly over the target

**Get Only Live Hosts**

```while read domain; do if host “$domain” > /dev/null; then echo $domain;fi;done<DutchGov.txt >> domains.txt```

**Get All Subdomain**

```for sub in $(cat domains.txt);do subfinder -d $sub -o $sub.dutch;done```

**Gather All Subdomain**

```cat *.dutch > all.sub```

**Fuzz All The Things**

```for i in $(cat all.sub); do echo””; echo “Subdomain of $i”;echo “”;gobuster dir -w wordlist.txt -u $i -e -o tmp ;cat tmp >> dutch.fuzz; echo “”; done```

**Server Details for CVE**

```for sub in $(cat all.sub);do echo “[*] Domain Name is => “ $sub;echo “[*] Server Header is => “ $(http — verify=no -h $sub | grep Server);echo “ “;done```

**Scan Ports**
well when i was doing i have done this process with nmap manually, i only scanned those hosts where i found juicy staff during previous steps
But now there lots of fast scanner available to automate this process. I didn’t check them yet, so do some research yourself

**Web ScreensShot**
I already have visited all of those sites so no need for me, but you can try

You may notice i didn’t check for any parameter or any kind of Injection attack. The truth is, that time i actually didn’t know how to test parameters. If you want you can follow this one

**Wayback Machine Urls**

```cat domains.txt | waybackurls | urlprobe -t 50 -c 100 | grep “=”```

## **End Story**

I had a vps so for me it was not that much hard to do. every nigh i run them with tmux and in morning i got juicy staff. After reporting couple of bugs one got triage as High impact and finally Alhamdulillah (All praise is due to Allah alone) i got that lousy T-Shirt

[![1-OCSji1b0-Nd3-A-56-Xc-Fmz-A.jpg](https://i.postimg.cc/VsjFVFKC/1-OCSji1b0-Nd3-A-56-Xc-Fmz-A.jpg)](https://postimg.cc/Wt1rD0LN)

## Author

**Name**: Mehedi Hasan Remon
**Handle**: @remonsec

___
wanna support my work! well just buy me a coffee

[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/remonsec)
