---
layout: post
title: OAS 5.5 software download
subtitle: a lesson learned
---

OAS 5.5 software download

OAS 5.5 released Jan 31st!

## Some notes

For a very brief post - let me help you know exactly what software you will need to download for the install. (A quick shout out to the collaborative effort on a Saturday from several Oracle Aces over in the Telegram obihackers channel.)

Go to [Oracle Edelivery](https://edelivery.oracle.com/) and sign in.

Search for Oracle Analytics Server and pick the top option and click on + Add to Cart

<img src="https://BecWagner.github.io/img/oas1.png" alt="OAS1">

If you were to hit continue and go ahead, you are going to see that the server comes with Weblogic 12.2.1.4 software. However, this is the wrong software for what we need.

<img src="https://BecWagner.github.io/img/oas2.png" alt="OAS2">

So instead, go back to the search and look for Oracle Fusion Middleware 12c Infrastructure and add the top line to the cart.
 
<img src="https://BecWagner.github.io/img/oas3.png" alt="OAS3">

Okay, so now when you click checkout, you should get a screen that looks like the following. Uncheck the Weblogic under Oracle Analytics Server and select Linux for the Fusion Middleware. 

<img src="https://BecWagner.github.io/img/oas4.png" alt="OAS4">

This click Continue and read the license agreement and check the box that you accept the terms. (You actually read that, right?)
 
<img src="https://BecWagner.github.io/img/oas5.png" alt="OAS5">

Okay, now your screen will come to the actual links to download the software. Let me save you a little bit more space. Uncheck the VM Virtual Appliance. You won’t need that either.

<img src="https://BecWagner.github.io/img/oas6.png" alt="OAS6">

##Conclusion
 
Okay my friends, that is the 1st step in your journey for installing OAS 5.5. I do expect the Weblogic pieces for Oracle Analytics Server to be fixed in edelivery at some point in the future making this blog likely obsolete. There are SRs and bugs open to resolve this issue already.

Lastly, there are already docker images with OAS already installed available if you want to skip all of this. You can find those at Gianni Ceresa’s github [here](https://github.com/gianniceresa/docker-images/tree/master/OracleAnalyticsServer)

**Other places to get the correct weblogic 12.2.1.4 fusion middleware software:
[here](https://www.oracle.com/middleware/technologies/fusionmiddleware-downloads.html)
[and here](https://updates.oracle.com/Orion/PatchDetails/process_form?patch_num=30188255)
