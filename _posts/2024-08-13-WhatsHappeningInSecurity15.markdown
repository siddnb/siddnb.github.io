---
title: "What's Happening In Security #15"
layout: post
headerImage: true
image: /assets/images/cyber_blog/week15/tea.JPG
date: 2024-08-13 16:00
tag:
- Tech
- Cybersecurity
- Fundamentals
category: blog
author: sidd
---
<h3 style="text-align:center">Best Left in the Past: Knowledge Based Authentication</h3>

*What was the name of your first pet? What’s your favourite hobby? What was the last thing you ate which made your throw up?*

Riddles that are supposed to thwart any would be attacker, and they work with varying degrees of success. [Knowledge Based Authentication](https://www.incognia.com/the-authentication-reference/knowledge-based-authentication-kba-meaning-and-examples) (KBA) is the classic authentication method we are used to where one or more questions are used to verify your identity. Back in the days when our personal information wasn’t accessible to everyone (whether through data brokers or even social media) the answers to these personal questions were a pretty useful form of security.

Say you’re traveling abroad and your credit card keeps getting declined, so you decide to call the bank to iron the issue out. After waiting the requisite 30 minutes to get a hold of a service rep, they ask you some questions to verify your identity before getting started. 

*Could you please tell me the last 4 digits of your debit card, your birthday, etc.*

After flawlessly reciting the answers to these questions, you are verified and they quickly get you sorted out and you’re on your way. **What if instead, someone had stolen your card and tried the same thing?** Would they have been able to overcome the hurdles? Through some light social media stalking, someone could easily find out your birthday and your mom’s maiden name. This highlights the issue with *static* KBA. In contrast with *dynamic* KBA, the answers to these questions don’t change. Dynamic KBA is a bit more secure since the answers can change with time (e.g. where did you use your credit card last?).

#### Multi-Factor Authentication (MFA)
What if we want to ditch KBA altogether? In security we generally talk about three factors of authentication: 

1. Something you know (e.g. password)
2. Something you have (e.g. physical key card)
3. Something you are (e.g. biometrics or location)

KBA obviously falls under the first one and so do passwords.

When designing your MFA, you don’t want to double dip from the same category. I was told that having a password and a pin is just like having a longer password, and the same would be true of using KBA along with a password. Instead, by combining two of them (e.g., requiring a thumbprint and a password), you create a more secure MFA system that leverages different types of security factors, reducing the risk of compromise by making it harder for attackers to gain access using a single method.

**A Better Way**\\
With all we now know, here’s a better way the customer service rep from our first example could have performed their authentication checks.\\
When the customer rep receives your call they do a few things:

1. They ask you where you last used your card (*Dynamic KBA, Something you know)*
2. They send you a One-Time Password (OTP) to your phone number (*Something you have,* while your phone number can be spoofed, only you could receive the text*)*
3. They lean on technology to compare the profile they have of you against recent banking transactions (*Something you are)*

Once they are satisfied that everything looks right, they go ahead and ask how they can help you.

Recently I listened to a [podcast about a social engineer](https://darknetdiaries.com/episode/144/) who managed to break into people’s bank accounts through phone calls with customer reps. Funnily enough, as skilled as she is, I believe that good MFA would have prevented her from succeeding. Implementing well-designed MFA, whether for personal or organizational use, doesn’t make you invincible, but it significantly reduces the chances of someone successfully impersonating you online.