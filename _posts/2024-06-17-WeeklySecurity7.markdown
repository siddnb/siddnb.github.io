---
title: "This Week in Security #7"
layout: post
headerImage: true
image: /assets/images/cyber_blog/week7/cranes.JPG
date: 2024-06-17 16:00
tag:
- Tech
- Cybersecurity
category: blog
author: sidd
---
> Navigating the ever-evolving landscape of cybersecurity can feel like a whirlwind—new threats, innovations, and incidents that are constantly reshaping the digital world. This week's post breaks down some of the developments and that took place last week.

<h4 style="font-weight:bold;">Rapid-fire:</h4>

- Ransomware attack in the UK leaves hospitals [unable to match blood types](https://www.cbc.ca/news/business/nhs-ransomware-attack-blood-donors-1.7230601)
- [Top-10 commercial bank in the US confirms breach](https://www.bleepingcomputer.com/news/security/truist-bank-confirms-data-breach-after-stolen-data-shows-up-on-hacking-forum/) that occurred back in October

### [The Fallout From Change Healthcare’s Ransom payment](https://www.axios.com/2024/06/13/ransomware-cyberattack-change-healthcare)
Malicious actors tend to target information which would give them the most monetary value, and generally this means they target confidential and personal information. Following that train of thought, it makes sense that many attacks are targeted towards medical related companies. 
- In March, Change Healthcare [paid out a $22 million ransom](https://www.wired.com/story/alphv-change-healthcare-ransomware-payment/) making it one of the largest payments in history
- At the time, U.S. officials and cybersecurity researchers echoed the same sentiment that paying out ransoms sets a dangerous precedent
    - On top of funding further criminal activity, such payments also signal that these companies are good prospective targets
- After the payment went through, [a different group attempted to extort Change Healthcare](https://www.wired.com/story/change-healthcare-ransomhub-threat/) with the same sensitive information

Since then, there has been an uptick in ransomware attacks targeting the medical industry. Not only did April have the highest number of such attacks recorded, it was the largest month over month jump recorded as well.

The US government is partnering with Microsoft and Google to provide better security resources for healthcare companies.

<figure>
        <img class="image" src="/assets/images/cyber_blog/week7/windows.JPG" alt="Reflections">
        <figcaption class="caption">Reflections</figcaption>
</figure>

### [Deepfakes and the Indian Election](https://theconversation.com/indian-election-was-awash-in-deepfakes-but-ai-was-a-net-positive-for-democracy-231795)
Early on in during the election cycle in India, we briefly mentioned that deepfakes of various public figures were being circulated to sway public opinion theorizing the ramifications they would have on the world’s largest democratic election. 

Although this isn’t directly related to security, not only is tackling misinformation always something worth doing, staying aware of these technologies is important when considering how to deal with more advanced phishing campaigns.

So, what are a couple of ways parties spent approximately $50 million on AI generated content?
- A deepfake of Tamil Nadu’s late chief minister was created with the party’s consent
    - Other beloved figures who had passed away were “brought back” through the use of generative AI to play on constituents’ emotions
- AI was used to translate speeches live to increase the reach of party members
    - India is home to 22 official languages and many many more others, live translations helped reach more minority populations

While there’s obviously some good that’s come from these use cases, it raises many more questions and issues for me. It brings to mind issues like misinformation, the creation of toxic content, and getting consent.

With social media platforms like _X_ removing many guardrails against misinformation, how do we ensure wide-spread education on these topics? Moreover, as I noted above, for one of the deepfakes, consent was given by the party but does that on its own make creating a deepfake okay?

<figure>
        <img class="image" src="/assets/images/cyber_blog/week7/stairs.JPG" alt="Onwards and upwards">
        <figcaption class="caption">Onwards and upwards</figcaption>
</figure>

### Security Fundamentals
**Attack Signatures**: Attack signatures are a crucial resource used in identifying known threats to your machine. 
- Signature-based malware detection scans a machine and by checking files, commands or traffic for these signatures they can detect known attacks
- The downside of this approach is that it can’t detect unknown attacks or even variants of a known attack
To complement signature-based detection there are other methods such as behavioural detection.