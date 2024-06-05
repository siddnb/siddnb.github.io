---
title: "This Week in Security #1"
layout: post
projects: false
date: 2024-05-05 17:00
tag:
- Tech
- Cybersecurity
category: blog
author: sidd
---
> Navigating the ever-evolving landscape of cybersecurity can feel like a whirlwind—new threats, innovations, and incidents are constantly reshaping the digital world. This week's post breaks down some of the developments and that took place this past week.

### [**UK bans default passwords on IoT devices**](https://therecord.media/united-kingdom-bans-defalt-passwords-iot-devices)
In 2016, a small group of hackers created the botnet “Mirai” and infected approximately 300,000 IoT devices to launch a DDoS attack on a DNS service provider, Dyn. Years later, the UK has become the first country to ban manufacturers from providing weak default passwords (e.g. “1234” or “admin”). The US doesn’t have any similar rules, but as noted by Bruce Schneier, manufacturers aren’t going to make different versions of this device for the UK and the rest of the world, which means this law should effectively change this globally.
**Further Discussion:** While this is a step in the right direction, a lot of the real concerns people in the field revolve around the possibility of manufacturers inserting backdoors into these simple products. Back in 2017 [Trustwave found a backdoor in DblTek devices](https://www.trustwave.com/en-us/resources/blogs/spiderlabs-blog/undocumented-backdoor-account-in-dbltek-goip/), allowing the manufacturer to access the hardware. This of course could be used by other malicious parties as well.

### [**London Drugs Cyberattack**](https://www.cbc.ca/news/canada/british-columbia/london-drugs-closure-western-canada-1.7187615)
Closer to home, last week London Drugs said it was the “victim of a cybersecurity incident”. As a result they shuttered all of their ~80 stores across western Canada, and they are currently trying to figure out whether any data breaches occurred. For those who don’t know, the store functions as a pharmacy but also sells consumer goods. [Chester Wisniewski from Sophos](https://globalnews.ca/video/10461455/london-drugs-investigates-cyberattack-and-possible-impact-on-personal-information), mentioned it’s likely a ransomware attack but paying the ransom or not typically doesn’t affect how long it takes for the company (in this case London Drugs) to recover. David Gray followed up saying that retail companies now treat these attacks as a “normalized cost of business”.
**Further Discussion:** With the increasing ubiquity of the use of digital records, companies need to have security built into the fabric of their infrastructure rather than treating it as an add-on. Moreover, individuals should be more cautious with what websites and services they are willing to give their information to. Encrypting data, restricting access to it, and logging/monitoring usage are all ways to help reduce the chances of your data being leaked but it’s not perfect.

### Rapidfire:
[**Dropbox Sign Breach**](https://thehackernews.com/2024/05/dropbox-discloses-breach-of-digital.html): Dropbox Sign (formerly HelloSign) is Dropbox’s e-signature solution. On April 24th, the company became aware of a data breach affecting a segment of clients. This breach gave access to users’ phone numbers, API keys, multi-factor authentication, etc. Possibly more concerning, parties who signed documents but don’t have a DropBox Sign account still had names and email addresses exposed. While they investigate further, the DropBox Sign team has reset passwords, logged users out of accounts on all devices, and are trying to “[coordinate] the rotation of all API keys and OAuth tokens.

[**Cuttlefish Malware**](https://blog.lumen.com/eight-arms-to-hold-you-the-cuttlefish-malware/): Discovered by Lumen Technologies, this malware (which targets networking equipment) has two goals. The first is that it attempts to steal authentication information from web requests which go through the router. A secondary objective of this malware is DNS and HTTP hijacking. Given the wide-spread adoption of TLS making the first goal very difficult to achieve, the latter is probably the main objective.

### Glossary:

- **Botnet**: A botnet is a network of machines infected by a malicious user to be used for their own purposes. By agglomerating many machines, the malicious party has access to much more compute and can launch more powerful attacks.
- **DDoS**: Distributed-Denial-of-Service attacks make use of many different machines to repeatedly access a certain resource, making it so that the victim is unable to serve other clients.
- **Trustwave**: A Managed Detection and Response company
- **DNS hijacking**: Domain Name System (DNS) hijacking is where the user is directed to a malicious website rather than the one they meant to access. This can be achieved by installing malware on the user’s machine, router (like with Cuttlefish), or even hacking a DNS server. In some rare cases, this can be done by your ISP itself such as when [Dutch ISPs were forced to redirect from the Pirate Bay](https://torrentfreak.com/dutch-isps-must-block-the-pirate-bay-despite-fierce-protest-court-rules-200602/) by the Amsterdam Court.

