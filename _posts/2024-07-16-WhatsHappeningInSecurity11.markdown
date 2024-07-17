---
title: "What's Happening In Security #11"
layout: post
headerImage: true
image: /assets/images/cyber_blog/week11/flag.JPG
date: 2024-07-16 16:00
tag:
- Tech
- Cybersecurity
category: blog
author: sidd
---
> Navigating the ever-evolving landscape of cybersecurity can feel like a whirlwind—new threats, innovations, and incidents that are constantly reshaping the digital world. This week's post breaks down some of the developments and that took place last week.

<h4 style="font-weight:bold;">Rapid-fire:</h4>

- [Dozens of Squarespace domains hijacked](https://krebsonsecurity.com/2024/07/researchers-weak-security-defaults-enabled-squarespace-domains-hijacks/#more-68067) amidst poorly thought out domain migration
- Hoping to combat common scams, [Singapore banks are phasing out SMS OTPs](https://thehackernews.com/2024/07/singapore-banks-to-phase-out-otps-for.html) in favor of a “Digital Token” OTP.
- Github Token for integral [Python repositories was leaked](https://thehackernews.com/2024/07/github-token-leak-exposes-pythons-core.html); fortunately it seems like it wasn’t exploited

<figure>
        <img class="image" src="/assets/images/cyber_blog/week11/roses.JPG" alt="A family taking pictures in a garden">
        <figcaption class="caption">Summer Happiness</figcaption>
</figure>

### [AT&T Data Breach Affects Most Customers](https://thehackernews.com/2024/07/at-confirms-data-breach-affecting.html)

Another company suffers at the hands of the Snowflake related breaches.

The attackers bought stolen Snowflake credentials to gain access to data like call records and “cell cite identification numbers” which can be used to triangulate the location where a call was made. 

- AT&T made it clear that personal information like names, date of birth and SSNs weren’t accessed
- However, they also noted that “there are often ways, using publicly available online tools, to find the name associated with a specific telephone number”

AT&T reportedly paid a ransom of $370,000 to have the hackers delete the stolen data. Amusingly, as proof of deletion the hacker sent a video of them deleting their copy. 

- A while ago I mentioned that Change Healthcare was threatened by a second ransomware group after they paid their initial ransom
- This case, however, is rare as ransomware groups seem to have a “code” of some sort where they keep their word apropos deleting data
    - Cybercriminals need to appear honest in this respect so victims will actually have a reason to pay their ransom

*A lack of 2FA on user accounts seemed to be the root cause of these breaches. In hopes of limiting further breaches, Snowflake has allowed admins to force MFA for their users.*

<figure>
        <img class="image" src="/assets/images/cyber_blog/week11/buildings.JPG" alt="Some interesting buildings">
        <figcaption class="caption">Beautiful Beige</figcaption>
</figure>

### Security Fundamentals
As I’ve begun my journey in the cybersecurity industry I have come across certain core processes that are common practice. Here’s an important one, the Incident Response Process.

**The Incident Response Process in 6 steps:**
1. **Prepare:** The organization needs to define roles and responsibilities so everyone is ready in case of an incident
2. **Identification:** Detecting threats is the first step towards remediation. There are many tools such as security information management (SIM) solutions.
3. **Containment:** Isolate the threat and stop it from spreading. In the short term this means quarantining the malicious processes or even the infected machine.
4. **Eradication:** After assessing the attack surface (we learnt about attack surfaces in the [8th edition](https://siddnb.github.io/WeeklySecurity8/)) find the root cause. Harden the system as needed which could include patching bugs or removing backdoors.
5. **Recovery:** Restore your systems to a desired state and resume normal operations. To achieve this you may restore from back ups and reconfigure compromised accounts. At this point it is important to test your systems to ensure everything is as it should be.
6. **Lessons Learned:** How did we get to this point? What went wrong? Did we react well? Share lessons learned and figure out how you can improve for next time.