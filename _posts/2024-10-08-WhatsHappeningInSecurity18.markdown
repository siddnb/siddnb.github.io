---
title: "What's Happening In Security #18: BECs"
layout: post
headerImage: true
image: /assets/images/cyber_blog/week18/sunset.JPG
date: 2024-10-08 16:00
tag:
- Tech
- Cybersecurity
- Scams
category: blog
author: sidd
---
<figure>
        <img class="image" src="/assets/images/cyber_blog/week18/fish.JPG" alt="phishing">
        <figcaption class="caption">A Not So Clever Phishing Attempt</figcaption>
</figure>

*One thing that people often get wrong about cybersecurity, is that many of the issues we face aren’t technical in nature. Humans are as much a part of the security infrastructure as anything and often the part most vulnerable to attack.*

**BEC Scams.** A couple of times a week, I’ll get an email from someone impersonating an executive at my company. The typical email’s subject will be the executive’s name, and the email will ask me to “***URGENTLY***” send them my phone number.

This email is an example of an attempt at Business Email Compromise (BEC). BEC is a type of email scam which targets businesses with the aim of stealing money or information.

While email I got looks like it was thrown together in the 20 seconds it took the scammer to take the elevator, other instances of BEC can be much more well thought out. Let’s take a look at what goes into a BEC and what to look out for to safeguard yourself from them.

**“Better” BECs.** BEC often involves someone impersonating your boss and telling you to move money or buy gift card, and to do so urgently. Another route scammers may choose is to masquerade as a vendor you’re working with and request that their payments be wired to a different account.

The concerning thing about BEC attacks is that the monetary losses can be immense and immediate. Back in 2019, [Facebook and Google were victims of this scam](https://www.cnbc.com/2019/03/27/phishing-email-scam-stole-100-million-from-facebook-and-google.html) and had a combined $100 million stolen from them. Fortunately they were able to recover most of the money.

In contrast to the email I received, more advanced BEC scams will follow one of two processes.

- **Account Takeover:** An actual email compromise is much more dangerous because it means the email will look a lot more authentic. The target email is ideally someone through whom payments are routed. As a results, the attacker will be able to monitor their inbox to figure out behaviours and make an increasingly believable phishing email.
- **Domain Imitation:** On the other hand, creating an imitation domain is a lot easier which allows attackers to target more companies. In the case of Google and Facebook, the scammer imitated a Taiwan-based company called Quanta by creating a domain in Lithuania.
    - e.g. The original domain could look like email@quanta(.)tw versus email@quanta(.)li
    - Through other social engineering means, like impersonating a potential new vendor, the scammer can find out who processes payments and use that information to target the individual.

**Protecting yourself from BECs**

1. Question the sender’s urgency. Creating stress and a sense of urgency can cause us to act irrationally, so just take a beat before acting
2. When faced with an unorthodox request, especially one relating to financial matters, double check with a source you trust. Call up your manager or someone else to confirm the legitimacy of the request
    1. Don’t trust phone numbers in the email because they may be falsified too
3. Configure email rules
    1. As always, properly implemented MFA is crucial to prevent account takeovers
    2. Additionally, enable settings which highlight to your users when an email comes from a suspicious source

If you take away anything from this story it should be this: *Your CEO probably doesn’t actually want your phone number*