---
title: "What's Happening In Security #16"
layout: post
headerImage: true
image: /assets/images/cyber_blog/week16/towers.JPG
date: 2024-08-20 16:00
tag:
- Tech
- Cybersecurity
category: blog
author: sidd
---
<h3 style="text-align:center"><a href="https://www.troyhunt.com/inside-the-3-billion-people-national-public-data-breach/">Data Brokerage; Somehow Legal</a></h3>
_Guys Guys Guys, big news! A data breach just occurred! What do you mean you don’t care? Oh, it’s the millionth one this year? **What if I told you this data breach isn’t like other data breaches?**_

Earlier this month, a class action lawsuit was filed against the data brokerage company, National Public Data (NPD) for an [alleged data breach](https://nypost.com/2024/08/19/business/national-public-data-admits-hackers-stole-social-security-numbers/). This incident differs from many of the other ones we’ve heard about in the past few months in a couple of ways:

1. **NPD is a data broker**
    1. Whereas companies like AT&T, Ticketmaster, and Snowflake are parties that we provide our information to as a part of our contract with them, NPD isn’t
    2. *“[Data brokers](https://www.mcafee.com/blogs/tips-tricks/how-data-brokers-sell-your-identity/) aggregate user info from various sources on the internet. They collect, collate, package, and sometimes even analyze this data to create a holistic and coherent version of you online. This data then gets put up for sale to nearly anyone who’ll buy it.”*
2. **The size of the breach**
    1. 2.9 billion *records* were leaked (not information on 2.9 billion people as was [reported frequently](https://www.cnbc.com/2024/08/15/billions-people-social-security-numbers-and-data-stolen-allegedly.html))
    2. The thinnest of silver linings is that [researchers](https://www.troyhunt.com/inside-the-3-billion-people-national-public-data-breach/) have gone through many of these records and found that a lot of the data was incomplete or incorrect (at least 100 million email addresses and many SSNs were still present though)

When we do business with companies there’s an understanding that they’ll store our data. When there’s a data breach, it sucks but at least it makes sense that it’s in the realm of possibility. What about a company like NPD?! Although most of us have never even heard about them, due to their negligence a lot of sensitive data has been leaked. If we’re not giving them this data, how do they get a hold of it?

Data brokers collect information through a [few main ways](https://tomkemp00.medium.com/a-closer-look-at-data-brokers-sources-of-data-ded248f8d760):

1. Web/Mobile Tracking: Third party cookies have come under scrutiny over the last couple of years, but they are still alive and well. Moreover, phones each have a unique advertising ID which gives companies a way to track user behaviour through their phones.
2. Publicly Available Data: Governments publish lots of data about censuses, court proceedings, etc. Aside from government sources, social media is another treasure trove of personal information which is publicly available.
    1. Several Python libraries like BeautifulSoup and Scrapy make scraping data relatively easy.
3. Buying Data: Nielsen, a data broker, claims they collect 80% of all credit card transactions. They buy this information from other organizations such as credit card companies.

<figure>
        <img class="image" src="/assets/images/cyber_blog/week16/cplace.JPG" alt="Canada Place">
        <figcaption class="caption">Canada Place</figcaption>
</figure>

[**How is this legal?**](https://clearcode.cc/blog/what-is-data-broker/#toc-label-9)\\
*"Data brokers often operate either on the brink of the law, or in full accordance with the law”*

Data privacy laws aren’t very robust around the world. Even in the EU where the GDPR has been around for more than 6 years now, firms are able to skirt the rules due to vague language. For example, companies are said to have a “legitimate interest” if they have a use for your data and you don’t object

**All is not lost**\\
As society adjusts to the ever changing realities advances in technology bring to us, slowly but surely companies and governments are adjusting as well. Obviously it’s never fast enough, but here are some glimmers of hope for you.

We have seen many instances of gross negligence when it comes to data loss prevention (DLP) but we haven’t seen companies face major repercussions. Recently however, a company providing IT services to the NHS has found themselves facing a £6 million fine for failings over the way they handled a ransomware incident in 2022.

Meanwhile, around the same time in 2022, Apple introduced their “App tracking transparency” feature which allowed users to opt out of providing their unique advertising ID to third party apps. Fingerprinting, the process of creating a profile of a user from combining indicators like browser version and phone model, is a pretty good workaround for companies but Apple’s commitment to privacy is a step in the right direction.

Finally, there are a lot of great resources out there like the blog “What’s Happening in Security” which help educate people on security and privacy. Here are some ideas on what you can do to help reduce the amount of information you companies have on you.

1. Think before you post on social media. If you don’t want to do that, at the very least, tighten your privacy settings - whether it’s setting your Instagram page to private or even just obfuscating your last name on LinkedIn.
2. Opt out of data collection when possible. Sometimes I’ll even create a throwaway account for services I’ll only use once using temporary email services like https://temp-mail (.) org/en[/](https://temp-mail.org/en/) 
3. You can reach out to various data brokers to request the removal of your information. However, this process can be quite challenging due to the sheer number of brokers and the fact that some make it difficult to locate and contact them.