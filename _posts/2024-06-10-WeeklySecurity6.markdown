---
title: "This Week in Security #6"
hidden: true
layout: post
headerImage: true
image: /assets/images/cyber_blog/week6/books.JPG
date: 2024-05-27 16:00
tag:
- Tech
- Cybersecurity
category: blog
author: sidd
---
> Navigating the ever-evolving landscape of cybersecurity can feel like a whirlwind—new threats, innovations, and incidents that are constantly reshaping the digital world. This week's post breaks down some of the developments and that took place last week.

<h4 style="font-weight:bold;">Rapid-fire:</h4>

- Club penguin fans [steal Disney strategy information](https://www.bleepingcomputer.com/news/security/club-penguin-fans-breached-disney-confluence-server-stole-25gb-of-data/) while trying to find information on the game
- [More Snowflake customers have information leaked](https://www.wired.com/story/snowflake-breach-advanced-auto-parts-lendingtree/); lack of 2FA still seems to be the culprit
- [750,000 Social Security Numbers leaked](https://therecord.media/frontier-provides-new-details-april-ransomware-attack) in April cyberattack

### [Working Your Way Around an ACL](https://www.tiraniddo.dev/2024/06/working-your-way-around-acl.html)

This article doesn’t contain advice on how to rehab a serious injury, rather it outlines an easy method to crack Microsoft’s Recall feature.

[A couple of weeks ago](https://siddnb.github.io/WeeklySecurity4/) we talked about a widely maligned new Windows 11 feature, Recall. There was plenty of criticism directed towards the project, most of which revolved around privacy issues.

While some workarounds have shown it’s possible to breach the database containing a user’s Recall data through privilege escalation, James Forshaw, a google researcher showed that it’s possible to bypass the security even without admin rights. Recall’s data is protected by an  Access Control List (ACL, discussed at the end of this post). Forshaw has demonstrated that these ACLs can sometimes be circumvented as is the case for Recall.

As more data is stored and used for increasingly powerful features, companies need to be careful to not rush to market with half-baked security measures and reviews.

_Microsoft is in the process of [making changes](https://www.computerworld.com/article/2140187/microsoft-makes-windows-recall-opt-in-after-privacy-security-backlash.html) to the feature and its rollout in response to widespread criticism._

<figure>
        <img class="image" src="/assets/images/cyber_blog/week6/car.JPG" alt="Red interior of a car">
        <figcaption class="caption">A cool car</figcaption>
</figure>

**Interesting Read**

### [Privacy and Overfishing](https://spectrum.ieee.org/online-privacy)

Yes, that’s overfishing with an ‘f’, not a ‘ph’. 

Scientists calculate the “acceptable catch size” for fisheries, based on the baseline population level that needs to be sustained. In the mid-1900’s scientists realized fish populations were dropping dramatically even with these catch size guidelines. How could that be?

A marine biologist, Daniel Pauly concluded that researchers were making a big mistake in their calculations. Borrowing the concept of “shifting baselines” from architecture, he concluded that each new generation of researchers was their own concept of a “baseline”. 

- Their baseline was whatever population they inherited when they began their work.
- So although the decline relative to *their* baseline wasn’t significant, the drop off over generations was large.

These shifting baselines parallel our relationship with privacy over time. Initially we would run relatively isolated machines with little oversight or monitoring, but as cloud computing has become the standard data is more easily monitored. 

In recent years this issue seems to have come to the forefront with AI training on any and everything. Where do we go from here? Time and policies will tell.

<figure>
        <img class="image" src="/assets/images/cyber_blog/week6/yarn.JPG" alt="Wrapped up hammocks">
        <figcaption class="caption">Some hammocks waiting to be hung up</figcaption>
</figure>

### Security Fundamentals
**Access Control List (ACL)**: In the third edition I explained [access control generally.](https://siddnb.github.io/WeeklySecurity3/) 

An ACL is a set of rules that determines the permissions for various users or systems to access resources within a network. Although similar conceptually, compared to something like Role-based Access Control (RBAC), ACLs are better suited for individual users rather than a company-wide system. 

Conditional access control entries simply require an additional condition to be met to allow access (e.g. whether an attribute exists or not). This is what Forshaw worked around in his hack.