---
title: "What's Happening In Security #13"
layout: post
headerImage: true
image: /assets/images/cyber_blog/week13/fireworks.JPG
date: 2024-07-30 16:00
tag:
- Tech
- Cybersecurity
category: blog
author: sidd
---
<h4 style="font-weight:bold;">Rapid-fire:</h4>

- [North Korean IT worker scam](https://www.axios.com/2024/07/26/knowbe4-north-korea-it-worker-scam) works again on a US based cybersecurity firm
- Financial institution in the Middle East was [DDoSed for 6 days](https://therecord.media/middle-east-financial-institution-6-day-ddos-attack)

## [Millions of Computers Compromised by Secure Boot Issue](https://www.binarly.io/blog/pkfail-untrusted-platform-keys-undermine-secure-boot-on-uefi-ecosystem)

Many machines use a process called “Secure Boot” to ensure that software used while the machine boots up is trusted by the Original Equipment Manufacturer (OEM). This ensures that malware can’t take control of the computer during the boot process. The Unified Extensible Firmware Interface firmware (UEFI) contains a database of trusted keys which it uses to check the firmware, bootloader, and other important pieces of software to ensure they haven’t been tampered with. If a discrepancy is found, the firmware halts the processes!

If a malicious party were able to insert malware at such a low level of the computer’s processes they would be able to wreak havoc and likely go undetected while doing so. Residing in this area of the computer, the malware would be able to influence important software like the operating system which means it would easily be able to hide itself. In 2011 a malware called [Mebromi](https://www.theregister.com/2011/09/14/bios_rootkit_discovered/) did just that. In response to this, security architects came up with Secure Boot. Through the use of public key cryptography, we would be able to set up a chain of trust and sleep better as a result.

> But what if someone working at a device manufacturing company *accidentally* published the private portion of their company’s platform key to github…

Essentially for machines running certain versions of the UEFI firmware, Secure Boot no longer matters. If any software can be signed using the correct key, verification doesn’t mean much.

Unfortunately this wasn’t the end. An additional 21 platform keys were found in various Certificates containing keys labeled “**DO NOT TRUST**” made their way into production.

<figure>
        <img class="image" src="/assets/images/cyber_blog/week13/do-not-trust-certificate.JPG" alt="A sample test certificate">
        <figcaption class="caption">A Test Certificate from AMI</figcaption>
</figure>

**How did this happen?**
1. Security is not always the number one priority. [Talking about their own experiences](https://www.schneier.com/blog/archives/2024/07/compromising-the-secure-boot-process.html/#comment-439620) at their workplace, a poster on Bruce Schneier’s blog said, “Where marketing staff call the shots, quality control is impossible”
    1. Sometimes company’s can be pressured to hand out keys earlier than they’d want for testing purposes, and sometimes these keys end up being irresponsibly used in production
2. Poor key management
3. There are alternatives to Secure Boot that would involve embedding the public key portion of they key directly into the hardware which could remove some of these issues

**How do we do better?**

The last point I raised about alternative techniques to Secure Boot is likely not the best solution. I believe that new technology isn’t the solution, because Secure Boot itself isn’t necessarily the issue here. It may have some flaws, but that’s not what brought us to this place. The mistakes that compromised these computers were human ones.

My takeaways from this are:
1. Limit access to important credentials. Whether it’s passwords or keys, limit their distribution as much as possible so there are fewer opportunities for a leak *a la* committing to github
2. Have processes in place to ensure that critical information is kept track of in code and that it is never shipped
3. Refresh your keys relatively frequently. If your credentials are leaked

While creating 100% foolproof solutions is impossible, staying vigilant and proactive can help us minimize risks and protect our systems effectively.

*Here are some resources if you want to go further into the details and get some more opinions on the matter:*
1. Shout out to Dave who has a [great video explaining the issue](https://www.youtube.com/watch?v=7sYzwb6eUgQ)
2. [Reddit](https://new.reddit.com/r/hardware/comments/1ec1t2x/secure_boot_is_completely_broken_on_200_models/ )
3. [DarkReading](https://www.darkreading.com/endpoint-security/millions-of-devices-vulnerable-to-pkfail-secure-boot-bypass-issue)
4. [The Original Report from Binarly](https://www.binarly.io/blog/pkfail-untrusted-platform-keys-undermine-secure-boot-on-uefi-ecosystem)
5. [ArsTechnica](https://arstechnica.com/security/2024/07/secure-boot-is-completely-compromised-on-200-models-from-5-big-device-makers/)