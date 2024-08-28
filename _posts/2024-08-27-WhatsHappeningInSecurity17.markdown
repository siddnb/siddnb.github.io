---
title: "What's Happening In Security #17"
layout: post
headerImage: true
image: /assets/images/cyber_blog/week17/ship.JPG
date: 2024-08-27 16:00
tag:
- Tech
- Cybersecurity
category: blog
author: sidd
---
<h2 style="text-align:center"><a href="https://abc7news.com/telegram-ceo-pavel-durov-arrested-in-paris-amid-investigation-into-/15235678/#:~:text=Telegram%20says%20nearly%20a%20billion,or%20was%20organized%20on%20Telegram.">Telegram’s Founder Arrested: Let's Talk About Encryption</a></h2>
Most of what we do on our devices is tracked in one way or the other. Whether it’s the posts we interact with on Instagram, or the amount of time we scroll on youtube, it’s all tracked. While that’s something most of us can live with, I think I speak for everyone when I say that we draw the line at our personal messages. Thankfully, modern day encryption is used to hide our messages from onlookers, even from the messaging service providers themselves. 

Encrypting text (you can encrypt other forms of media too) transforms the subject into a new and ideally unrecognizable set of characters. To decrypt this new text, the observer has to have a key of some sort which allows them to revert the encrypted text.  Encryption in one form or the other has been around since around [2000 BC](https://tresorit.com/blog/the-history-of-encryption-the-roots-of-modern-day-cyber-security/) in ancient Egypt, and has been the basis for securing communications from prying eyes and ears for centuries. Examples of well known encryption methods include the [Caesar cipher](https://en.wikipedia.org/wiki/Caesar_cipher) and cipher machines like Enigma, the machine used by the Germans during WW2. Nowadays to keep our data secure we have a couple of standard encryption methods. 

- **Symmetric encryption:** Aka private key cryptography, symmetric encryptions involve using the same key to encrypt and decrypt the data.
- **Asymmetric encryption:** Aka public key cryptography, this involves two different keys. A public key to encrypt the data and a private key to decrypt it.

Symmetric is faster but is harder to use because you have to figure out how to share the key with the other party. On the other hand, asymmetric encryption takes more time but is great for use cases where exchanging keys securely would be difficult. 

> **Side note on hashing:** Hashing is another method of obfuscating data, but unlike encryption it is a one way process. Essentially what this means is that if you hash something, you can’t undo it (or this is the case for good hashing algorithms anyway). “Decrypting” is a valid process, but undoing a hash really isn’t (this was a pet peeve of my cyber prof’s). Hashing is useful if two parties want to compare two pieces of data to see if they’re the same, but they don’t want to reveal the contents to each other. For example, companies store a hashed version of your password so hackers can’t learn your password, but they can still check if your submitted password is correct by hashing it and comparing it to their records to check its validity. 
<div class="breaker"></div>
Now that we’ve covered the basics of encryption, I know you have a burning question inside you. 
<p style="text-align:center"><i>“Sidd, how does my friend read my encrypted messages? I don’t remember telling them that the key I used to encrypt it is ABD9920D0188BCD17848E1!”</i></p>

The more keen-eyed among you might have noticed something before. With asymmetric cryptography, you can tell the whole world your public key which they can use to encrypt messages they send to you. This way, even if someone “stumbles” upon their message on its way to you, no one would be able to read it. Using your private key, you can safely decrypt the message and rest assured that nobody else saw what was going on. This case, where the message is encrypted once at your device and then decrypted only one other time, at your friend’s device is called end-to-end encryption (e2ee). As of 2016 WhatsApp rolled this out to all their users, and it’s become standard among most messaging apps. An interesting point to note is that many companies including WhatsApp use the Signal Protocol which is an open source protocol that often has you changing your keys almost every message, which makes the communications all the more secure.

Transport Layer Security (TLS), which is used to encrypt the majority of other internet communication, used to also be the foundation of cryptography for most messaging apps before 2016. This meant that the messaging service’s servers were a middleman between you and your friend, so messages were decrypted and encrypted again on the server before going to the final destination. This meant that companies were able to read your data, but with the adoption of e2ee it’s rarely still the case. 

> What the hell Sidd, I read all this way because you said someone got arrested. Let’s get to it already!

Fair enough. Let’s get to the juicy stuff.\\
Wiretapping is the process of monitoring someone’s telephone communications. Back in the day, wiretapping literally involved using another physical wire to connect to the wires used to route someone’s phone calls. Governments or even more shady individuals didn’t need to deal with finicky things like radio signals or even worse, encryption.

The advent of advanced cryptographic techniques allowed for lots of shady stuff to pop up on the dark web since people were able to hide their web traffic. One of the most infamous websites which came out of all of this was known as the [Silk Road](https://en.wikipedia.org/wiki/Silk_Road_(marketplace)#), which launched in 2011. This website was the OG online marketplace on the dark web where all sorts of illicit substances and services were for sale. After a few years, the FBI arrested the founder, and in 2013 the website was shut down.

These days, one of the more public homes these transactions and discussions have found, is Telegram. Tools like disposable phone numbers and cryptocurrencies provided by Telegram enabled the distribution of child sexual abuse material, drugs, and stolen information. This, in conjunction with allegedly loose moderation and a lack of cooperation with authorities lead to Pavel Durov, the founder of Telegram, to be arrested last week in France.

Putting Telegram to the side, e2ee has still been a thorn in the side for law enforcement ever since it came about. Since decrypted messages don’t exist on company servers, governments are unable to get the conversations they want of suspected criminals. Debates on our rights to privacy versus ramifications on public safety continue to rage on. In 2015, the UK government proposed [a ban on e2ee](https://en.wikipedia.org/wiki/Encryption_ban_proposal_in_the_United_Kingdom) or that companies would need to provide a backdoor for the government. This latter part would essentially be a way for the government to easily break the encryption, but the issue with that is it would allow anyone who could figure it out, to do so as well. 

This is why governments now tend to focus on endpoints. Rather than trying to crack messages on servers or as they travel across networks, governments have turned to the device itself. Once they have access to someone’s phone, if they are able to unlock it they’ll have access to the unencrypted messages they wanted in the first place.

### What Should You Think?

I don’t know, but I hope you’ll tell me. I for one, am torn on how I feel about this decision to arrest Pavel Durov. On one hand, his platform has been used for some truly awful things and he should be held responsible to an extent. However, if there’s an issue with his company, shouldn’t governments try to regulate the company itself? Many people around the world depend on Telegram for private communication, and this kind of precedent doesn’t sit well with me.

All I know is that I’m glad e2ee is around and hopefully it doesn’t go anywhere soon.

**Further Reading**\\
[Here’s](https://en.wikipedia.org/wiki/Key_distribution#:~:text=In%20public%20key%20cryptography%2C%20the,a%20private%2C%20encrypted%2C%20message.) how public keys are shared