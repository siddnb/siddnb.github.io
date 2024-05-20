---
title: "This Week in Security #3"
layout: post
headerImage: true
image: /assets/images/cyber_blog/week3/blenz.jpg
date: 2024-05-19 16:00
tag:
- Tech
- Cybersecurity
category: blog
author: sidd
---
> Navigating the ever-evolving landscape of cybersecurity can feel like a whirlwind—new threats, innovations, and incidents are constantly reshaping the digital world. This week's post breaks down some of the developments and that took place this past week.

<h4 style="font-weight:bold;">Rapid-fire:</h4>

- [$650 million raised](https://www.reuters.com/business/finance/vc-firm-accel-raises-650-mln-invest-ai-cybersecurity-startups-2024-05-13/) to invest in cybersecurity startups by VC firm
- More deep fakes in India, this time of the [incumbent PM dancing](https://www.reuters.com/world/india/dance-videos-modi-rival-turn-up-ai-heat-india-election-2024-05-16/)
- Every second Tuesday of the month, dubbed “Patch Tuesday”, sees a flurry of patches released by major companies, last Tuesday [Microsoft released more than 60 patches](https://krebsonsecurity.com/2024/05/patch-tuesday-may-2024-edition/#more-67337)

### [Palo Alto Networks Partnering with IBM](https://newsroom.ibm.com/2024-05-15-Palo-Alto-Networks-and-IBM-to-Jointly-Provide-AI-powered-Security-Offerings-IBM-to-Deliver-Security-Consulting-Services-Across-Palo-Alto-Networks-Security-Platforms)

As this partnership aims to become official sometime before October, IBM once again seems to be trying to consolidate security services in the industry. According to Arvind Krishna, IBM Chairman and CEO, “cyber is a very fragmented space” and this will allow the companies to provide a better answer for clients going forward.

- In late April HashiCorp announced that they had signed a deal to be [acquired by IBM](https://www.hashicorp.com/blog/hashicorp-joins-ibm)

One of the key elements of a company’s security architecture is a security operation center (SOC)

- An SOC is comprised of humans who monitor a company’s activity with the help of software to catch threats early
- Palo Alto Networks’ product Cortex XSIAM would incorporate IBM’s Watsonx large language models (LLMs) to assist the security analysts to help identify threats

Aside from possible ramifications of this deal regarding antitrust laws, another point of concern is how these successive deals could affect the quality of the services. Some in the industry feel IBM mismanages new acquisitions as the company chases financial goals ahead of a quality product.

<figure>
        <img class="image" src="/assets/images/cyber_blog/week3/bus.JPG" alt="Quiet morning on the 4">
        <figcaption class="caption">Quiet morning on the 4</figcaption>
</figure>
**Scams**
### [Bait-and-switch](https://bc.ctvnews.ca/think-twice-before-sharing-heartbreaking-social-media-posts-rcmp-warn-1.6890342)

You’re scrolling through Facebook and see a picture of a sweet looking child. The post’s caption says the child has been missing and they need help finding them! Once the post gains sufficient traction from kind-hearted people like yourself, the scammers change the post’s content.

- The new post will usually be an ad for a product which now has a lot of positive interactions
- Your friends and family might see that you’ve liked it and are more likely to trust the product

Another derivative/strain of this that I have personally encountered is on Amazon. 

- Sellers will take control of positively reviewed products and change the description/images for a different product.
- Scrolling down to the reviews reveals that the positive reviews are for [something else entirely](https://slate.com/technology/2021/12/amazon-listings-wrong-reviews-why.html)

To avoid falling for these traps, look into the person posting and also where they are posting the content. If the person doesn’t have much previous activity or if the page they post on is unrelated to the content, it’s likely a scam.

**Interesting Read**
### [Essay on LLMs data control](https://cacm.acm.org/opinion/llms-data-control-path-insecurity/)

Bruce Schneier, a well known American Cryptographer, draws parallels between the problems with LLMs (e.g chatGPT) and problems faced by early telecommunications technology.

In the 1960s, you could use a payphone for free by playing a certain tone into it because that tone was interpreted as a command by the phone. Only in the 1980s did the technology advance enough that commands were given through a different method, thereby removing the possibility of these previous workarounds. 

Schneier, cites SQL injection and buffer overflows as similar issues which arise from this problem of mixing data with commands. Now we have prompt injections. 

- A prompt injection is a type of attack where malicious inputs are crafted to manipulate the behavior of language models

**Now what?** Maybe, just maybe your product doesn’t have to be powered by chatGPT?! Not every software problem is a nail waiting for an LLM hammer, it introduces security risks we don’t really know how to handle. Try a less general purpose tool which you have better understanding of to reduce these security risks.
<figure>
        <img class="image" src="/assets/images/cyber_blog/week3/park.JPG" alt="Man on a bench under shade in a park">
        <figcaption class="caption">It doesn't get much better than sitting in the shade of a tree on a sunny day.</figcaption>
</figure>

### Security Fundamentals
**Access Control:** Not every resource needs to be accessed by everyone. Sometimes you want to keep things hidden from people, even people within your organization. Access control has a few different flavors, including DAC, MAC, and RBAC.
- **DAC:** Discretionary Access Control allows the person who own the data to decide what rights others have
- **MAC:** Mandatory Access Control sees a singular administrator managing all access rights
- **RBAC:** Role-Based Access Control means individuals are assigned roles (e.g. manager) and based on these roles access rights are granted

This concept is important in everything from unlocking your phone, to allowing someone to only  view your google doc, or even for the transit company to ensure you can use the bus.

### Glossary:

- **LLM**: A Large Language Model is a type of artificial intelligence trained on vast amounts of text data to understand and generate human-like language.
- **Security Operation Center (SOC)**: A centralized unit that monitors, detects, and responds to cybersecurity threats and incidents in an organization.
- **SQL Injection**: A cyber attack where malicious code is inserted into a query to manipulate a database, potentially gaining unauthorized access to data.
- **Buffer Overflow**: A security vulnerability that occurs when a program writes more data to a buffer than it can hold, potentially leading to arbitrary code execution or crashes.