---
title: "What's Happening In Security #19: Mamba 2FA"
layout: post
headerImage: true
image: /assets/images/cyber_blog/TD.JPG
date: 2024-10-24 16:00
tag:
- Tech
- Cybersecurity
- Scams
category: blog
author: sidd
---
<figure>
        <img class="image" src="/assets/images/cyber_blog/Mamba2FA_example.JPG" alt="phishing">
        <figcaption class="caption">An instance 1 of 4 phishing sites</figcaption>
</figure>

## Mamba 2FA Phishing-as-a-Service Platform

In a world where SaaS products are everywhere, it’s no surprise that scammers want to get in on the lucrative revenue structure too. Mamba 2FA is a Phishing-as-a-Service (PaaS) platform which has been in service since at least May of this year when the cybersecurity company Sekoia, began tracking it.

### What is it?

The phishing kit’s primary target is users with Microsoft 365 accounts. The kit allows its users to not only send very convincing phishing emails, but it also aids in bypassing certain MFA methods.

This is a form of an Adversary-in-the-Middle (AitM) attack. A classic Man-in-the-Middle attack involves an attacker positioning themselves between two machines to eavesdrop or change messages, the AitM variant manipulates authentication protocols specifically.

The platform’s architecture involves a relay server which communicates with the phishing website. After a victim inputs their credentials they get sent to the malicious website which forwards it to the relay server. This server can then just input the these credentials into Microsoft’s real website.

While MFA is generally a powerful tool in stopping phishing attacks, not all MFA is built the same and this can be an issue for more advanced threats. In a situation like this AitM attack, you may receive an SMS OTP and input that on the platform which they can then relay to the Microsoft, effectively bypassing the MFA.

### An Aside on MFA

Not all MFA is built the same.

The point of MFA is that if your credentials are stolen, an attacker shouldn’t be able to login. Unfortunately some implementations of MFA, namely SMS OTPs and app notifications are vulnerable to being exploited.

**OTPs:** It’s possible to get your phone number switched to a different SIM card by contacting your telecom provider. Unfortunately, sometimes the questions asked to authenticate you are weak and attackers can often get the answers from data brokers. After performing this “SIM swap” the attacker will receive your SMS OTPs

**App Notifications:** MFA fatigue attacks, also known as push-bombing, involves bombarding a user with notifications by attempting to login repeatedly until the victim decides to say yes just to get the notifications to stop.

### Repercussions of these platforms vs normal phishing

In a word, the problem is “accessibility”. Building and maintaining the infrastructure for these scams is no mean feat, but now anyone can find these services for sale on Telegram for just $250 per month. Two hundred and fifty dollars is all you need to access this cutting edge technology. These sorts of services likely mean advanced phishing campaigns will become far more common.

*Following Pavel Durov’s (Telegram’s CEO) recent arrest in France, he pledged to be cooperate more with law enforcement to moderate illicit activities. It’ll be interesting to see whether he follows through.*
<div class="breaker"></div>
### Nerdy Details

- HTML file uses window.location.href to redirect user to the phishing website.
    - They encode the url also to make stealthier
    {% highlight html %}
    <script>
        window.location.href = atob("aHR0cHM6Ly...") + "#" + "[EMail]";
    </script>
    {% endhighlight %}
    
- On loading the pretty barebones HTML page, they load the [Socket.IO](http://Socket.IO) library and 1 of the 4 screen templates
- Using the [Socket.IO](http://Socket.IO) library, the page will communicate with the
- Since being found, devs have done more to be sneaky
    - The website checks to see if a bot clicked on the website, if so it goes to a broken 404
    - Now use proxy servers to make blocking the IPs harder