---
title: "What's Happening In Security #12"
layout: post
headerImage: true
image: /assets/images/cyber_blog/week12/BSOD.JPG
date: 2024-07-22 16:00
tag:
- Tech
- Cybersecurity
category: blog
author: sidd
---
## CrowdStrike Debacle: An Early Post-mortem

At this point we all know what happened. On Friday morning millions of Windows computers greeted users with the signature blue screen of death (BSOD). The fallout of this issue meant that countless critical systems were shutdown and were suddenly thrust back into the age of paper and pens. Even if the outage caused by a CrowdStrike update didn't affect you directly, you likely still heard about it. Let’s get into what happened and where we should go from here.

**What happened?** CrowdStrike released a configuration update to their Windows product which is considered to be a regular part of their process. According to CrowdStrike, their Falcon platform (the buggy software in question) undergoes extensive stress testing including the use of a “Content Validator” which checks content before it is published. A bug in the *Content Validator* itself let faulty content data through to production. The faulty software resulted in an out-of-bounds exception leading to the BSOD.

**Remediation:** Soon after the issue was found, CrowdStrike patched the issue and machines that hadn’t come online yet avoided impact. However, because machines couldn’t boot up, CrowdStrike was unable to patch affected computers. This meant that each computer had to be fixed on-site by IT professionals. This was resource intensive and meant that once a fix was found, it still took hours upon hours to get systems back online.

At the time of writing, [Delta airlines is still struggling](https://www.cbsnews.com/news/delta-flight-cancellations-today-dot-investigation-crowdstrike-outage/) to get flights off the ground and is facing a federal investigation. 

**Where do we go from here?** 

This is the big question. Whenever disastrous events occur and we’ve come down from our collective shock, it’s important to take some time to reflect on what happened. It’s important to figure out how we can learn from the experience.

In a complex situation like this, the question can take you down many roads. The first I would like to address is a human one.

Everyone’s first reaction to news like this is to blame someone. **

*“Whose head will roll?! It must be the programmer who pushed the change! Or maybe the manager of the team! No no wait, [how about the CEO](https://timesofindia.indiatimes.com/technology/tech-news/crowdstrike-ceo-is-also-linked-to-this-software-update-that-brought-down-many-parts-of-the-internet-in-2010/articleshow/111916115.cms)!”*

Calm down. Let’s think it through. Is firing someone the right thing to do? Maybe, but it’s important to have a thorough investigation first. Is this a one-off issue that could happen to anyone or is it a systemic/culture issue? A few days on, we see that the issue may have been due to testing practices which are far too lax for such a critical product. Even if the conclusion is that someone needs to be fired, knee jerk reactions are no good for anyone. Whoever is at fault already likely feels the weight of what they did, and unnecessary abuses from strangers probably isn’t constructive. 

Next there’s a technical aspect to reflect on.

1. When developing software products, we understand that our code could have bugs and so we test them over and over. However, we rarely treat out automated tests with the same level of scrutiny. Passing all your tests doesn’t mean your code is perfect, it just means your code passes the tests you wrote. Let’s put care into our tests shall we?
2. How quickly should you act before installing updates to your software? It’s generally recommended that you should immediately install critical updates (patches to some kind of security issue) but for less pressing updates like the CrowdStrike one it’s a good idea to wait a few days and see if any issues are uncovered.
3. The tech community is always there to help with many people posting tutorials on how to fix the issue for various scenarios. Companies and individuals released tools to fix the problem, but unfortunately criminals are also around, trying to take advantage of the chaos. In Latin America, [malware masquerading as a fix](https://thehackernews.com/2024/07/cybercriminals-exploit-crowdstrike.html) was being passed around. Even in times of panic it’s important to keep your wits about you.
4. Lastly, CrowdStrike was able to cause such mayhem because their software acts directly in the kernel which means it ran with full privileges. CrowdStrike’s product was given this access because it needs to react to attacks as quickly as possible, but maybe there’s another way of going about it. Apple uses something called [system extensions](https://support.apple.com/en-ca/guide/deployment/depa5fb8376f/web) instead which provide certain guardrails

I couldn't cover everything I wanted to (eg. supply chain issues), as this is a much broader incident and plenty has been said already by others. Let's make sure we don't forget about it in a few months. This incident has already had significant implications, and new developments will continue to emerge, so stay tuned as the story unfolds.

*[Here’s a link](https://www.crowdstrike.com/falcon-content-update-remediation-and-guidance-hub/) to CrowdStrike’s preliminary post incident review*