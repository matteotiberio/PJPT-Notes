# Passive

Before actually touching the machine, we perform research with tools to gather everything that could be useful; this is called passive reconnaissance.

## Physical/Social

- Physically gathering useful information (gates, badges...) or using satellites (Google Maps...).
- Also understanding who works there by checking social media for any photos.

## Web/Host

- **Target Validation**: WHOIS, nslookup, dnsrecon — used to verify if the provided target is correct.
- **Finding Subdomains**: Google Fu, dig, nmap, sublist3r, bluto, curl, crt.sh...
- **Fingerprinting**: nmap, wappalyzer, whatweb, builtwith, netcat...
- **Data Breaches**: haveibeenpwned, breach-parse, weleakinfo

---

# Identifying our Targets

We used **Bugcrowd**, which is a Bug Bounty platform, to perform information gathering on in-scope targets.

---

# Discovering Email Addresses

- Tools like **hunter.io** allow discovering email domains of targets.
- Another useful tool is **phonebook.cz**.
- One way to validate emails is directly on Gmail or Outlook by entering the email in the login field to see if it exists.
- Alternatively, use tools like **email checker** and **email hippo**.

---

# Hunting Breached Credentials

There are several ways to find breached credentials, such as using a list like **BreachCompilation** and some tool to read it.  
Or websites like **DeHashed**.

---

# Hunting Subdomains

When we put `*` before a domain, like `*.example.com`, the `*` symbol represents a *wildcard* that searches all available subdomains for that domain.

- Useful tools for finding subdomains include **sublist3r** and **theHarvester**.  
- A useful website is **crt.sh**.

**OWASP Amass** is a very useful tool but requires a long loading time.

---

# Identifying Websites

Knowing what a website is built with is very useful. A tool like BuiltWith can be very helpful, for example:

![alt text](/Images/IW.png)

It tells you all the tools used on a specific site, useful to gain more information.

Another extension tool is **Wappalyzer**.

It is very helpful to know what a site is built with, especially its framework, because it can help identify specific vulnerabilities related to programming languages, web servers, etc.

Another tool for Information Gathering on a site is **WhatWeb**.

---

# Information Gathering with Burp Suite

A very useful tool for web-level information gathering is **Burp Suite**.

Burp Suite acts as a *proxy*, intercepting connections between you and a website.

## Setting up Burp Suite

To set up Burp Suite, go to browser settings > proxy > set `127.0.0.1` (for both HTTP and HTTPS).

Then go to https://burp and download the certificate by clicking on **CA Certificate**.  
Go to browser settings > privacy & security > certificates and import the previously downloaded certificate.

## Intercepting Traffic with Burp Suite

Burp Suite is very useful for information gathering on a website because it allows you to capture many details by intercepting API requests.  
You can also interact with the API requests.
