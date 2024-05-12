---
title: "This Week in Security #2"
layout: post
headerImage: true
image: /assets/images/hacking-stock.jpg
date: 2024-05-12 16:00
tag:
- Tech
- Cybersecurity
category: blog
author: sidd
---
> Navigating the ever-evolving landscape of cybersecurity can feel like a whirlwind—new threats, innovations, and incidents are constantly reshaping the digital world. This week's post breaks down some of the developments and that took place this past week.

### [“Cybersecurity Incidents” Hit Government Networks, B.C.](https://www.cbc.ca/news/canada/british-columbia/bc-premier-cyberattacks-sophisticated-1.7198501)
Clearly attempting to be as vague as possible, on Wednesday B.C.’s premier said their government networks were involved in “sophisticated cybersecurity incidents”. He says that so far there is no evidence that sensitive information was breached and that they’re working with the Canadian Centre for Cyber Security as well as the Office of the Information and Privacy Commissioner. 
Meanwhile, government employees were told to change their passwords, making them even longer (increased from 10 to 14 characters).

**Further Discussion**: 
- The directive for employees to use longer passwords likely means they believe the cause of the hack was not key-logging but rather just the use of powerful GPUs to crack passwords.
- Using a [passphrase](https://www.okta.com/identity-101/password-vs-passphrase/) is a great way to easily remember longer passwords instead of trying to remember a long password before inevitably just writing it down on a sticky note you keep at your desk (I’m looking at you 😊)

### [New MacOS Information Stealer/Spyware](https://blog.kandji.io/malware-cuckoo-infostealer-spyware)

“Mac’s can’t get viruses”

This commonly held belief likely stems from the fact that relative to malware targeting Windows machines, there haven’t been many for Macs. Combining the 72% marketshare Windows holds with a user demographic consisting of some of the most vulnerable users, it makes sense that cybercriminals would dedicate most of their resources towards Windows computers. \\
However, Macs aren’t immune to all attention and in late April a spyware dubbed “Cuckoo” was discovered. On downloading an application designed to download music off streaming services like Spotify, Kandji (a security company) found the files included malicious code which would steal information relating to everything from hardware details to passwords.

**Further Discussion:** Do not get complacent because you have a Mac. Please please please, don’t download software from suspicious sources… please.

### Scams:
*Phishing, smishing… vishing? Scammers are getting more creative and more able by the day, we'll be covering a fresh set of modern scams each week to keep you informed and vigilant*

Online shopping scams are rampant generally aim to steal payment information, contact information, and of course money. For example, a [large scale scam network](https://www.theguardian.com/money/article/2024/may/08/chinese-network-behind-one-of-worlds-largest-online-scams) that seems to originate in China created many fake retail sites offering large discounts on many clothing brands like Versace and Hugo Boss. 
Most would-be consumers didn’t receive any of the items they ordered, and while some didn’t have any money stolen their data was nonetheless given up. 

**How do we combat this?**
- **Consumers**: All we can do is be wary of deals that look to good to be true and avoid giving out information when possible (e.g. checking out as a guest instead of making an account)
- **Companies**: Many cybercriminals wait for a domain to expire so they can buy it themselves allowing them to more easily impersonate you.
    - Buying your domain means their website link will look legitimate, further confusing your clients

### Rapid-fire:

[Paris 2024](https://www.reuters.com/technology/cybersecurity/paris-2024-gearing-up-face-unprecedented-cybersecurity-threat-2024-05-06/): Any high profile event brings with it plenty of people looking to attack it, few bigger than the summer olympics. The event spans many days and locations, giving prospective attackers many potential entry points.
Organizers are working together with national french agencies and other security companies to combat cyberattacks.
The 2018 winter olympics was hit by the [“Olympic Destroyer”](https://blog.talosintelligence.com/olympic-destroyer/) which took down several bits of infrastructure.

[Russia Disputes Germany’s Hacker Claims](https://www.reuters.com/world/europe/russia-says-germany-using-baseless-hacker-myths-destroy-ties-2024-05-08/): Germany accused Russia of attacking its defence and aerospace firms, recalling their ambassador as a result. Russia in turn claims that this was merely a ploy to worsen other Russian international relations. \\
*The intersection of PR and Cybersecurity muddies the waters even more, how should we deal with these situations?*

[Deepfakes Impact India’s 2024 Election](https://www.reuters.com/world/india/fake-videos-modi-aides-trigger-political-showdown-india-election-2024-05-05/): Fake video clips of high ranking politicians and even Bollywood actors, Aamir Khan and Ranveer Singh, in which they comment on the ongoing election have gone viral prompting police investigations into the source of these videos. \\
*Companies like Meta and OpenAI extol the virtues of advancing this technology at breakneck speeds, how can we ensure the responsible development of generative AI? [Here](https://openai.com/index/our-approach-to-ai-safety/) are some of OpenAI’s guidelines.* 

### Glossary:

- **Passphrase**: Generally 14 characters or more, a passphrase is generally a short phrase which is easier to remember than a complicated password but hard to break because of its length.
- **Spyware**: Malware (malicious software) which collects information without consent.
- **Domain**: Domain or Domain Names refer to a part of a website’s URL which tells your computer which website to go to
    - Domain names generally expire after 10 years and must be renewed. If it’s allowed to expire it is put up on a marketplace for anyone to buy.