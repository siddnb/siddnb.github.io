---
title: "This Week in Security #5"
layout: post
headerImage: true
image: /assets/images/cyber_blog/week5/cover.JPG
date: 2024-06-03 16:00
tag:
- Tech
- Cybersecurity
category: blog
author: sidd
---
> Navigating the ever-evolving landscape of cybersecurity can feel like a whirlwind—new threats, innovations, and incidents that are constantly reshaping the digital world. This week's post breaks down some of the developments and that took place last week.

<h4 style="font-weight:bold;">Rapid-fire:</h4>

- Researchers [crack password](https://www.wired.com/story/roboform-password-3-million-dollar-crypto-wallet/) to a $3 million crypto wallet
- 911 S5, one of the largest botnets ever, [taken down](https://krebsonsecurity.com/2024/05/is-your-computer-part-of-the-largest-botnet-ever/#more-67679)

### [Operation Endgame](https://www.europol.europa.eu/media-press/newsroom/news/largest-ever-operation-against-botnets-hits-dropper-malware-ecosystem)
Are the Avengers back in action for yet another movie? Thankfully not.

Coordinated by Europol, Operation Endgame was a coordinated effort by several EU countries (as well as the UK and US) to take down the botnets behind some of the most prolific malware systems out there.

- From May 27-29 the operation took down or disrupted more than 100 servers and arrested 4 individuals

The operation targeted a kind of malware called “Droppers”.

- Droppers are a kind of trojan which help download other malware. These are used as a catalyst for many other malware systems.
- Often they will infiltrate a system through channels like email attachments and compromised websites

**What’s next?** By targeting droppers such as IcedID and Pikabot, the hope is that it will disrupt the activities of many other cybercriminals who will have to find another way to infiltrate their targets. According to the europol website “Operation Endgame does not end today”, as they plan to launch more activities in the near future.

_Updates can be found on the operation endgame [website](https://www.operation-endgame.com/)._

<figure>
        <img class="image" src="/assets/images/cyber_blog/week5/dinosaur.JPG" alt="Me in front of dinosaur fossils.">
        <figcaption class="caption">Me in front of dinosaur fossils</figcaption>
</figure>

### [Snowflake Customers Breached](https://www.wired.com/story/snowflake-breach-ticketmaster-santander-ticketek-hacked/)

Ticketmaster experienced a data breach in late May, with a hacker group claiming that they have information on approximately 560 million customers. 

Another Snowflake customer, Santander (a banking firm) was also [reportedly breached](https://www.bbc.com/news/articles/c6ppv06e3n8o) by the same group. 

Initial investigations suggested that the hacks were related to Snowflake’s systems, however the original article which alleged this has been taken down since. Snowflake claims they were [not breached](https://www.theverge.com/2024/6/3/24170876/snowflake-ticketmaster-santander-data-breach-details) due to a vulnerability but rather by brute forcing client credentials. 

Platforms generally prevent malicious actors from guessing a user’s password too many times, but by using a technique called password spraying (using the same common password and varying the username) this protection can be circumvented. 

**Please use 2FA where possible to limit the possibility of these kinds of issues.**

<figure>
        <img class="image" src="/assets/images/cyber_blog/week5/flowers.JPG" alt="Me with some flowers.">
        <figcaption class="caption">Me with some flowers</figcaption>
</figure>

### Security Fundamentals
**Botnet**: A botnet is a network of machines infected by a malicious user to be used for their own purposes. By agglomerating many machines, the malicious party has access to much more compute and can launch more powerful attack\\
The machines can be infected through many means, one is through droppers which we discussed earlier.

<figure>
        <img class="image" src="/assets/images/cyber_blog/week5/arms_out.JPG" alt="I'm done">
        <figcaption class="caption">Elation</figcaption>
</figure>