---
layout: post
title: ADFS and OAC lab
subtitle: Azure cloud and Oracle cloud trials
---

##The Scenario##

I was giving a presentation at Oracle Open World 2018 on Active Directory Integration and Single Sign-on with Oracle Analytics Cloud (OAC). Slides [here](https://www.slideshare.net/secret/qERdzGtv9SZTpj). I love to do live demos but I was cautioned by many many many people to avoid it if possible. So I needed to setup some lab environments and video the steps. A big thank you to [Kellyn](https://twitter.com/DBAKevlar) for pointing me to so many MSFT resources.

##Option 1 - Roll it yourself ADFS lab##

I tend to think of myself as rather capable of setting up VMs and Environments for demos I plan to use, so I went to go find some nice set of instructions for setting up a windows server with Active Directory Federation Service (ADFS) setup. And I did find some great instructions here:

https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/deployment/set-up-the-lab-environment-for-ad-fs-in-windows-server-2012-r2.

I downloaded my iso for Windows 2012 R2, fired up my VMwareFusion (Why yes, I am using a Mac.), and got started. However, when I got to the point where I had created the AD domain controller, and started reading ahead, I realized I would need a Cert Authority and ADFS all on separate servers. At that point I decide I do not want to do all of this on my Mac or spend the next two weeks teaching myself CAs all in order to get some screenshots of ADFS setting up a Relying Trust Party. So after many many many searches, I stumbled across the secret sauce.

##Option 2 - The Secret Sauce - Click a button ADFS lab##

https://github.com/Azure-Samples/active-directory-lab-hybrid-adfs

So in all honesty, I saw this when I was searching the very first time for an ADFS lab, but didn't give it much attention because github + Azure account made me steer clear. It seemed like two other things I would need to teach myself in order to get started. (Yes, yes, I do realize I have hosted my blog on github. Hush, you more evolved tech person, you.) So once I ran into this again, I started reading all of the readme to try to understand what I needed to do. (This is not required, by the way. You can just click the link with the broken image and away you go.) I gingerly went and setup an [Azure trial account](https://azure.microsoft.com/en-us/free/), not sure what was going to be expected. Then I went back to readme, and re-read again. I really didn't get what I was supposed to do next. Finally I clicked (almost accidentally) on the broken image icon in the Links box (The one without the client machines). This opened a new window with my Azure info already logged in. I assume it would have taken me to the login first if I hadn't just setup an account and was still in Azure in another tab in the browser. There were a couple of prompts to fill out, and I had to reduce the compute size due to my trial limit. But then I clicked a button and it magically went and setup my servers for me. It was prepopulated with a few users and groups in the Contoso domain. CA and ADFS were properly setup for a demo as well. It was so easy, I am still kicking myself for how much trouble and trepidation I put myself through.

##Coming soon - OAC Cloud Trial setup##

Also, and I know this should also get plenty of time and attention, but I setup an [Oracle Cloud](https://myservices.us.oraclecloud.com/mycloud/signup) trial account. I've done this so many times now that I am almost out of email addresses to use. :) I was going to tell you to go check out the [US-Analytics blog](https://www.us-analytics.com/hyperionblog) post on my company website, but I went searching for it, and I didn't see one. I've done [several](https://stxhug.org/) [live](http://coug.us/2018-06-26-chicago-oracle-users-group-meeting-sponsored-by-quest/) [demos](https://www.meetup.com/ODTUGers/events/250377840/) on setting up your first OAC instance, how could I have not blogged it? Watch here for another blog next week on it.