---
title: How I Create My First Tool With Python (UniqMe)
author:
  name: remonsec
  link: https://github.com/remonsec
# date: 2019-08-08 11:33:00 +0800
categories: [Bugbounty]
tags: [bugbounty]
pin: true
---

## How I Create My First Tool With Python (UniqMe)

**بسم الله الرحمن الرحيم**


Assalamu Alaikum

I am Mehedi Hasan Remon.

Right now I am 20 years old & A student in Computer Science.

Without more intro, let’s get into the story

[![letgo-lets-goooo.gif](https://i.postimg.cc/02TzD8tQ/letgo-lets-goooo.gif)](https://postimg.cc/HVtWCC1D)

If I be honest, I was learning Python for a while. But I didn’t know how to use it in the real world. As an example, I know this is a loop but how can I use it in real world, that's my main question to myself. So end of the day, I know the syntax but I don’t know how to deal with it.

[![huh-what.gif](https://i.postimg.cc/2SnVxPJx/huh-what.gif)](https://postimg.cc/v4HYYSG1)

Everything was running like before, one day somehow I visited a profile on Facebook. There I saw that guy using a specific name for himself everywhere, and that name is really a unique one. I would like to mention that profile so you can understand it clearly. That guy’s profile name is [**Prial Islam Khan**](https://www.facebook.com/prial261), if you are from **Bangladesh** and connected with **Cyber Security** then you already know him.

[![1-Rpo-k8m5tx3-Ynr-Dnxqd-Wxw.png](https://i.postimg.cc/rpmzLKsf/1-Rpo-k8m5tx3-Ynr-Dnxqd-Wxw.png)](https://postimg.cc/k207QMxS)

So as you can see he is using **prial261** as his unique name. When I search with this name on Google, I saw everything about him.

[![1-k-Gb00-AWO6-Ns-Xgvygw7few.png](https://i.postimg.cc/c1Qx2QTs/1-k-Gb00-AWO6-Ns-Xgvygw7few.png)](https://postimg.cc/jCSYJnG9)

That SEO concept inspired me a lot. Now I also want a unique name for me, so that I can use it everywhere over the internet. Then I start searching a unique name for me. I found some websites there they match your name on different social platform and return you the available social media for use that name

[![1-zou-CLWze-Aul3-Yxz-VNg-DXIA.png](https://i.postimg.cc/mrv46DHz/1-zou-CLWze-Aul3-Yxz-VNg-DXIA.png)](https://postimg.cc/WDwxdsST)

As you can see I have to give a username again and again till I get the unique one. But it really so boring and I also have to check some other platforms like Hackerone, Bugcrowd, etc for a unique username. So end of the day those websites not helping me to find a unique name for me

[![crying-boy.gif](https://i.postimg.cc/Bvst7mff/crying-boy.gif)](https://postimg.cc/xXx0cyd6)

Then I thought why not I create a tool with python to automate this process. I will learn how to use Python practically and I will also get a unique name for me. Then I start making a tool and I named it **UniqMe**

[![celebrate-confetti.gif](https://i.postimg.cc/8CHc2LTJ/celebrate-confetti.gif)](https://postimg.cc/jWDRNwwt)

As a super-duper noob, I actually didn’t know where and how to start. I draw a concept on my mind that, I will take input from the user then I will generate a list of names based on that input and finally I will match them on different websites. I start googling about how to generate a list with python, how to check website response with python etc.

[![typing-jim-carrey.gif](https://i.postimg.cc/W3Y33jFs/typing-jim-carrey.gif)](https://postimg.cc/nj7ZRyGW)

After lots of failing attempts finally, I wrote a script that giving me available names from Hackerone, Facebook, Twitter, Instagram. I tried a lot with Bugcrowd but it gave me a 403 status code. Still, it's not the main problem, the main problem is this tool is super duper slow and not showing the result while matching the usernames. It’s really so boring and not that much fun.

[![work-sucks.gif](https://i.postimg.cc/VvSN0Tnn/work-sucks.gif)](https://postimg.cc/9wh2vLxQ)

Again after lots of failing attempts finally it working smoothly at least better than before. So now let’s see the codes how actually it works

[![1-6-QXUezf-S73pztam-B7-Pc-HKw.png](https://i.postimg.cc/q7nSqGNq/1-6-QXUezf-S73pztam-B7-Pc-HKw.png)](https://postimg.cc/VSfDHnBP)

 1. I imported the module requests and store all the websites in variable

[![1-n-XUpq-Cua-C7-K3w-AYz-Ol-IN-Q.png](https://i.postimg.cc/Y0ybb4vT/1-n-XUpq-Cua-C7-K3w-AYz-Ol-IN-Q.png)](https://postimg.cc/xNMvd1yP)

2. Then I set some condition to generate the name list

[![1-Ps-Pk-KWae-Ngu5duhh-SUVXZA.png](https://i.postimg.cc/gkZvftQx/1-Ps-Pk-KWae-Ngu5duhh-SUVXZA.png)](https://postimg.cc/JGRDXx18)

3. with requests I send the names to the websites then if it gives 404 it means that name is not available there so I can use that name

[![1-qu4s-IXKG0-Y0-MMqf-Sy-BLq-Q.png](https://i.postimg.cc/YjKmrkZh/1-qu4s-IXKG0-Y0-MMqf-Sy-BLq-Q.png)](https://postimg.cc/n92LT8HJ)

4. Last but not the least I filter and print all the names that can be used in all websites

[![napoleon-dynamite-yes.gif](https://i.postimg.cc/mZqkWLWw/napoleon-dynamite-yes.gif)](https://postimg.cc/BtT4xG6L)

That's how I create my first tool with **Python**. I found a unique name for me. It’s **mehedi1194**

[![1-Nu-Ldgqx-P49l-JD45ccp-Zj2-A.png](https://i.postimg.cc/SsHGMBHp/1-Nu-Ldgqx-P49l-JD45ccp-Zj2-A.png)](https://postimg.cc/cgMYqbsD)

So end of the day I also have a unique name.

If you are also searching for a unique name then it may help you. I am giving this tool link below

Thank You for reading till the end

Be Secure Be Safe

Allah Hafiz

[![1-Cff-MGhk-CVqwh1-GOGf-PVMdw.jpg](https://i.postimg.cc/MpzmVb3X/1-Cff-MGhk-CVqwh1-GOGf-PVMdw.jpg)](https://postimg.cc/2VXWfvDf)

## UniqMe : [**https://uniqme.netlify.com**](https://uniqme.netlify.com)

___
wanna support my work! well just buy me a coffee  

[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/remonsec)

