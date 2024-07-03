---
title: "This Week in Security #9"
layout: post
headerImage: true
image: /assets/images/cyber_blog/week9/laduree.JPG
date: 2024-07-01 16:00
tag:
- Tech
- Cybersecurity
category: blog
author: sidd
---
> Navigating the ever-evolving landscape of cybersecurity can feel like a whirlwind—new threats, innovations, and incidents that are constantly reshaping the digital world. This week's post breaks down some of the developments and that took place last week.

<h4 style="font-weight:bold;">Rapid-fire:</h4>

- LockBit alleged that they had US Federal Reserve data, [turns out they lied](https://www.cyberdaily.au/security/10745-lockbit-lies-about-us-federal-reserve-data-publishes-alleged-evolve-bank-data)
- Cybersecurity company [Blackberry beats revenue estimates](https://finance.yahoo.com/video/blackberry-stock-pops-q1-earnings-195020534.html?guccounter=1&guce_referrer=aHR0cHM6Ly93d3cuZ29vZ2xlLmNvbS8&guce_referrer_sig=AQAAAGpoq9-cM3Ho6_pTJE4Dy9QzHI5fCZhiTN4MrlToTsEiXhlXlG3qDxiLuD0T00jMN6W_fG02jIlP_93z_otgrnv1bQwpYTAgNwUe6U3hEkrZE22sCxdpg-3wB2W1R8Xs4S7lSnFTzMuE44X2qUo7s6MV0blZCZhgsWt4nd-jBuhL)… but is still not profitable yet
- Popular open-source browser support project, Polyfill.js is the root of a supply chain attack [affecting over 100 thousand websites](https://securityboulevard.com/2024/07/more-than-100k-sites-impacted-by-polyfill-supply-chain-attack/)

### Cybersecurity and the Bottom Line

In good times, insurance might seem like a luxury rather than a necessity, but it's invaluable when trouble strikes. Unfortunately, many corporations have adopted a similar mindset toward their security culture, viewing it as an unnecessary expense rather than a crucial investment.

As trends have shown that cybersecurity incidents will continue to occur at increasing rates, the cost of not having a dependable security solution has become too high to ignore. The only issue? There aren’t enough professionals to fill the growing need…

In 2013 there were an estimated 1 million job openings in the security industry, this number has [since ballooned to 3.5 million in 2023](https://apnews.com/press-release/ein-presswire-newsmatics/technology-steve-morgan-ein-presswire-newsmatics-2c99c00b8673966bde5eca81f6535320). Why the employment gap?

- Graduates of security programs are often not seen as employable because of how quickly the cybersecurity landscape evolves
    - Today’s threats are vastly different than the ones we faced ten years ago and will be different than what we may face only a few years from now
- Moreover, it is exceedingly rare to find entry level positions in the industry and employers
- Lastly, employers are unable or unwilling to compete with salaries offered by other companies

**So now what?** There needs to be a major mindset shift. While increasing salaries is the “easiest” first step, mentorship and up-skilling through employment may be even more important for the long term success of this industry.

<figure>
        <img class="image" src="/assets/images/cyber_blog/week9/dogs.JPG" alt="dog walking is hard">
        <figcaption class="caption">Dog Walking is Hard</figcaption>
</figure>

### Security Fundamentals
**Buffer Overflow:** A buffer overflow occurs when data is written to unallocated memory due to the absence of bounds checking. These bugs are commonly associated with programs written in languages like C or C++ where there is no built-in protection against accessing out-of-bounds memory.
- Attackers will often exploit this kind of vulnerability to run their own malicious code instead of the original program