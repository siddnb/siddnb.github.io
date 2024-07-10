---
title: "What's Happening In Security #10"
layout: post
headerImage: true
image: /assets/images/cyber_blog/week10/happy.JPG
date: 2024-07-09 16:00
tag:
- Tech
- Cybersecurity
category: blog
author: sidd
---
> Navigating the ever-evolving landscape of cybersecurity can feel like a whirlwind—new threats, innovations, and incidents that are constantly reshaping the digital world. Let's take a look at what's been brewing around the web, shall we?

<h4 style="font-weight:bold;">Rapid-fire:</h4>

- [Apple’s vs Android’s approach to AI](https://www.wired.com/story/apple-intelligence-android-hybrid-ai-privacy/)
- This week in privacy concerns: [Live-streaming bars to scope out the scene](https://sfstandard.com/2024/06/29/2night-live-stream-bars-privacy-concerns/)

### [Public Wi-Fi: Not Even 30,000ft in the Air](https://www.darkreading.com/remote-workforce/hacker-busted-for-evil-twin-wi-fi-that-steals-airline-passenger-data)

I remember when public wi-fi access became commonplace in malls and restaurants. It felt like a whole new world of connectivity, but even back then I had heard using it came with risks. However, since then security measures have come a long way. 
- The introduction of TLS in 1999 aimed to secure our network traffic as it made its way across the network. In following years,
- TLS underwent multiple large updates due to vulnerabilities that were found along the way, and our comfort with using public wi-fi networks is as high as ever. *But maybe it shouldn’t be.*

While today it is certainly harder for someone to read the contents of your web traffic than it was before, cybercriminals have found ways to steal your data anyway. One such technique is called an “evil twin” attack. 
- In an evil twin attack, the hacker mimics a legitimate wi-fi connection. Once a user connects to it, the hacker can monitor their internet activity

Passengers on a flight to Perth, Australia had no idea that their data was being stolen by someone on their flight who had implemented one of these attacks. The malicious party set up his own wi-fi access points on the plane and got his victims to input their personal information including social media credentials.

_Once the plane landed, police apprehended the criminal._

<figure>
        <img class="image" src="/assets/images/cyber_blog/week10/hello.JPG" alt="Can you see me?">
        <figcaption class="caption">A Curious Little Squirrel</figcaption>
</figure>

### [Effects of the TikTok and Kaspersky Bans](https://www.wired.com/story/tiktok-kaspersky-us-ban-internet-freedom/)

A couple of weeks ago I wrote about the US’ ban on products sold by Kaspersky Lab and I wanted to briefly discuss some important points raised in the article I linked.

In 2024 the US has banned two behemoths of their fields, foreign based TikTok and Kaspersky (Chinese and Russian respectively), for fairly nebulous reasons. Both companies rejected the premises of their bans complaining that they are based on issues of geopolitics rather than concrete issues of misuse. TikTok has even gone as far as to sue the US government for violating the First Amendment in banning their app.

While neither of these bans gone into effect yet, the US government’s willingness to ban foreign tech companies without “damning evidence” doesn’t give much reason for confidence in the way they may handle such situations in the future. Stanford policy researcher, Riana Pfefferkorn believes the government should “set basic privacy and security requirements for *all* software, not just foreign-owned apps”.

I’ll be curious to see how the TikTok potential ban pans out, and how far reaching the fallout of it ends up being.

<figure>
        <img class="image" src="/assets/images/cyber_blog/week10/lemonade.JPG" alt="Serving some lemonade.">
        <figcaption class="caption">Lemonade on a Hot Day</figcaption>
</figure>

### Security Fundamentals
This week I thought I’d do a little something different and follow on from the “Public Wi-Fi: Not Even 30,000ft in the Air” story.

How can we protect ourselves in our daily lives? Here are a few tips:

- Don’t do anything which involves sensitive information like banking on public networks
- Don’t let your phone automatically connect to available networks
    - By connecting manually you can look out for potential red flags
- We’ve all heard that you shouldn’t click on random links, right? Recently I learned you shouldn’t scan random QR codes either for the same reason!