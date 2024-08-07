---
title: "What's Happening In Security #14"
layout: post
headerImage: true
image: /assets/images/cyber_blog/week14/plants.JPG
date: 2024-08-06 16:00
tag:
- Tech
- Cybersecurity
category: blog
author: sidd
---
<h4 style="font-weight:bold;">Rapid-fire:</h4>

- Official Olympics Android app [asks for many invasive permissions](https://cybernews.com/security/paris-2024-olympic-apps-eavesdropping-on-users/)
- Record [$75 million ransomware payment](https://krebsonsecurity.com/2024/08/low-drama-dark-angels-reap-record-ransoms/) made

### [Domain Buyer’s Remorse](https://krebsonsecurity.com/2024/07/dont-let-your-domain-name-become-a-sitting-duck/)

When setting up a website, one of the most important decisions you can make is what your domain name will be. To “buy”<sup>1</sup> a domain, you have to procure services from a Domain Registrar. They will allow you to pick a domain name and link it to the IP address of the server your website is hosted on. \\
This linking process is important because computers can’t find a website based on a name, rather it requires an IP address to find it. The Domain Name System (DNS) translates domain names to IP addresses which your machine will then use to find the website you’re looking for.

*“Sidd, thanks for the quick lesson on DNS but what’s the issue? I just bought my kick-ass domain name, I’m all good.”*

Unfortunately the DNS is complicated and requires a few different parties and servers to work. As we know, where there are complications there’s room for oversight and issues. \\
When you lease a domain, you have to pick a domain from a Domain Registrar, AND tell it which domain name servers will be the authoritative servers for the domain.
- Domain Name Resolution is a process which distributes the task of resolving a domain name to an IP address
    - The last step of this process involves an “authoritative server”<sup>2</sup> which holds the IP address mapping

While oftentimes the two services (leasing a domain and domain hosting) are provided by the same company, there are companies like DNSMadeEasy that only host domain records (DNS provider). When there’s a miscommunication between these two kinds of companies, domains can become duds but the *DNS provider may not know about it.* \\
This brings us to the issue at hand. A domain takeover can occur when a domain is registered with a registrar, but before you can set up your DNS provider to point towards your website’s server an attacker could set *their* server up with the same DNS provider and use your domain name. 

This is also called a “sitting duck” vulnerability because a similar issue can occur when  deprovisioning your website. If you only take down your host from your DNS provider but don’t remove the DNS entry which points machines towards the DNS provider, at any time a malicious party can swoop in and host their content under the domain. In 2016 Matthew Bryan, a security researcher, demonstrated this vulnerability affected [approximately 120,000 domains](https://thehackerblog.com/the-orphaned-internet-taking-over-120k-domains-via-a-dns-vulnerability-in-aws-google-cloud-rackspace-and-digital-ocean/). Today, [Eclypsium estimates this number to be around one million](https://eclypsium.com/blog/ducks-now-sitting-dns-internet-infrastructure-insecurity/).

**Why is this a problem?** It allows bad actors to pose as trusted parties which makes detecting things like phishing attacks that much harder

**How do we fix it?** This is a harder question to answer. 
- According to Steve Job (yes, that’s his name) the founder of DNSMadeEasy, it’s not their problem to solve.
    - He claims the onus is on the domain registrants themselves (which I partially agree with) to ensure the records are set up properly.
- Some form of verification before setting up your server with a DNS provider would go a long way towards fixing the issue
    - DNS provider and registrar Hostinger says they are working on a feature to introduce verification on whether a “domain truly belongs to the customer”. Hopefully others will follow suit

Either because of complacency in your organization or lack of checks by DNS providers, the issue rages on. This has been a known issue for about eight years now and so far there haven’t been major changes so some skepticism towards industry giants is warranted. 

**What should we do going forward?** 
- Here are some tips from [Mozilla](https://developer.mozilla.org/en-US/docs/Web/Security/Subdomain_takeovers)
    - Standardize steps for provisioning and deprovisioning hosts
        - Create DNS records last when creating and remove them first when deprovisioning
    - Create an inventory of your domains and the hosting providers to keep track of them
- [This](https://github.com/indianajson/can-i-take-over-dns?tab=readme-ov-file) github repo keeps track of many domains which may be vulnerable, check it out
- While it might be comforting to trust that large tech providers have foolproof systems, they are not immune to vulnerabilities. Stay proactive and vigilant in monitoring and maintaining your DNS security to safeguard your site effectively.

#### Glossary/Clarifications
1. You don’t buy a domain, you can only lease it up to a maximum of 10 years at a time. However, you do have the right to renew the lease when it’s up.
2. Here’s an explanation on how [Domain Name Resolution works](https://www.cloudflare.com/learning/dns/dns-server-types/)
3. Domain Registrar vs DNS Provider: 
    1. DNS Provider (also DNS Host among other names) owns the authoritative server which will tell computers trying to find your website where it is
    2. Domain Registrars allow you to pick a domain name and link it to an IP address

**Further Reading:**
- <https://developer.mozilla.org/en-US/docs/Web/Security/Subdomain_takeovers>
- Other recent domain related issues
    - [Squarespace domains hijacked](https://krebsonsecurity.com/2024/07/researchers-weak-security-defaults-enabled-squarespace-domains-hijacks/)
    - [Google Workspace accounts created by third parties](https://krebsonsecurity.com/2024/07/crooks-bypassed-googles-email-verification-to-create-workspace-accounts-access-3rd-party-services/)