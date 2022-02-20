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


If I be honest, I was learning Python for a while. But I didn’t know how to use it in the real world. As an example, I know this is a loop but how can I use it in real world, that's my main question to myself. So end of the day, I know the syntax but I don’t know how to deal with it.


Everything was running like before, one day somehow I visited a profile on Facebook. There I saw that guy using a specific name for himself everywhere, and that name is really a unique one. I would like to mention that profile so you can understand it clearly. That guy’s profile name is [**Prial Islam Khan**](https://www.facebook.com/prial261), if you are from **Bangladesh **and connected with **Cyber Security** then you already know him.

![](https://cdn-images-1.medium.com/max/2000/1*Rpo_k8m5tx3YnrDnxqdWxw.png)

So as you can see he is using **prial261** as his unique name. When I search with this name on Google, I saw everything about him.

![](https://cdn-images-1.medium.com/max/2000/1*_kGb00AWO6NsXgvygw7few.png)

That SEO concept inspired me a lot. Now I also want a unique name for me, so that I can use it everywhere over the internet. Then I start searching a unique name for me. I found some websites there they match your name on different social platform and return you the available social media for use that name

![](https://cdn-images-1.medium.com/max/2694/1*zouCLWzeAul3YxzVNgDXIA.png)

As you can see I have to give a username again and again till I get the unique one. But it really so boring and I also have to check some other platforms like Hackerone, Bugcrowd, etc for a unique username. So end of the day those websites not helping me to find a unique name for me

Then I thought why not I create a tool with python to automate this process. I will learn how to use Python practically and I will also get a unique name for me. Then I start making a tool and I named it **UniqMe**

As a super-duper noob, I actually didn’t know where and how to start. I draw a concept on my mind that, I will take input from the user then I will generate a list of names based on that input and finally I will match them on different websites. I start googling about how to generate a list with python, how to check website response with python etc.


After lots of failing attempts finally, I wrote a script that giving me available names from Hackerone, Facebook, Twitter, Instagram. I tried a lot with Bugcrowd but it gave me a 403 status code. Still, it's not the main problem, the main problem is this tool is super duper slow and not showing the result while matching the usernames. It’s really so boring and not that much fun.

Again after lots of failing attempts finally it working smoothly at least better than before. So now let’s see the codes how actually it works

![](https://cdn-images-1.medium.com/max/2000/1*6QXUezfS73pztamB7PcHKw.png)

 1. I imported the module requests and store all the websites in variable

![](https://cdn-images-1.medium.com/max/2000/1*nXUpqCuaC7K3wAYzOlIN-Q.png)

2. Then I set some condition to generate the name list

![](https://cdn-images-1.medium.com/max/2000/1*PsPkKWaeNgu5duhhSUVXZA.png)

3. with requests I send the names to the websites then if it gives 404 it means that name is not available there so I can use that name

![](https://cdn-images-1.medium.com/max/2000/1*qu4s-IXKG0Y0MMqfSyBLqQ.png)

4. Last but not the least I filter and print all the names that can be used in all websites

 <iframe src="https://medium.com/media/c3f4b5ab0a15c26d1fb4576834fbae1b" frameborder=0></iframe>

That's how I create my first tool with **Python**. I found a unique name for me. It’s **mehedi1194**

![](https://cdn-images-1.medium.com/max/2048/1*NuLdgqxP49lJD45ccpZj2A.png)

So end of the day I also have a unique name.

If you are also searching for a unique name then it may help you. I am giving this tool link below

Thank You for reading till the end

Be Secure Be Safe

Allah Hafiz

![](https://cdn-images-1.medium.com/max/2732/1*CffMGhkCVqwh1GOGfPVMdw.jpeg)

## **UniqMe : [**https://uniqme.netlify.com**](https://uniqme.netlify.com)**
