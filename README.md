# 🔐 Footprinting & Reconnaissance with Multiple Kali Linux Tools

This is my **Week 2 project** for the Cybersecurity & Ethical Hacking Program at **Networkwalks**.

In this project, I performed basic **footprinting and reconnaissance** using multiple tools available in Kali Linux. The purpose of the lab was to understand what information can be discovered from publicly available sources about a website.


## 🎯 Objectives

The main objectives of this project were to:

- Understand the concept of footprinting and reconnaissance
- Use multiple Kali Linux reconnaissance tools
- Find public domain registration information
- Identify web technologies used by a website
- Resolve a domain name to an IP address
- Inspect HTTP response headers
- Detect a Web Application Firewall (WAF)
- Enumerate publicly available DNS records
- Document the results of each reconnaissance task

## 🎯 Lab Target

The target used for this practical was:

```text
networkwalks.com
```

###  WHOIS


## ⚙️ Reconnaissance Process

### 1. WHOIS — Domain Registration Information

I used `whois` to retrieve publicly available domain registration information.

### Command

```bash
whois networkwalks.com
```
![WHOIS Screenshot](images/whois.png)


###  WhatWeb


### 2. WhatWeb — Web Technology Fingerprinting

I used WhatWeb to identify technologies exposed by the website.

### Command

```bash
whatweb networkwalks.com
```
![WhatWeb Screenshot](images/whatweb.png)

###  NSLookup


### 3. NSLookup — DNS Resolution

I used `nslookup` to resolve the domain name and identify its IP address.

### Command

```bash
nslookup networkwalks.com
```
![NSLookup Screenshot](images/nslookup.png)

###  CURL


### 4. CURL — HTTP Response Headers

I used `curl` to inspect the HTTP response headers returned by the website.

### Command

```bash
curl -I https://networkwalks.com
```
![CURL Screenshot](images/curl.png)

###  WAFW00F


### 5. WAFW00F — Web Application Firewall Detection

I used `wafw00f` to check whether the website was protected by a Web Application Firewall.

### Command

```bash
wafw00f networkwalks.com
```
![WAFW00F Screenshot](images/wafw00f.png)

###  DNSRecon


### 6. DNSRecon — DNS Enumeration

I used `dnsrecon` to gather publicly available DNS information.

### Command

```bash
dnsrecon -d networkwalks.com
```
![DNSRecon Screenshot](images/dnsrecon.png)

###  Problems Encountered


## 🐞 Problems I Encountered & How I Solved Them

### 1. Understanding Different Reconnaissance Tools

At first, the different reconnaissance tools performed similar-looking tasks, but I learned that each tool provides different information.

For example:

- `whois` focuses on domain registration information.
- `whatweb` focuses on web technologies.
- `nslookup` resolves DNS information.
- `curl` displays HTTP response headers.
- `wafw00f` checks for Web Application Firewalls.
- `dnsrecon` provides more detailed DNS enumeration.

### 2. Understanding the Information Returned

Some commands returned a large amount of information. I learned to read the output carefully and identify information that was relevant to the task.

### 3. Recording Evidence

For each task, I saved screenshots and recorded command output so that the reconnaissance process could be documented and reviewed later.


## 💡 What I Learned

Through this project, I learned how reconnaissance and footprinting are used during cybersecurity assessments.

Some of the things I learned include:

- How to use `whois`
- How to fingerprint websites using WhatWeb
- How DNS resolution works
- How to use `nslookup`
- How to inspect HTTP headers using `curl`
- How to detect WAF technologies using `wafw00f`
- How to enumerate DNS records using `dnsrecon`
- How to document cybersecurity practical work
- Why publicly exposed information can be useful during security assessments
- Why organizations should minimize unnecessary information exposure

This project helped me understand that reconnaissance is an important part of cybersecurity because security professionals can identify publicly exposed information before conducting further authorized security testing.


## 🛡️ Ethical & Legal Notice

This project is intended for **education, cybersecurity training, and authorized security testing**.

The reconnaissance techniques demonstrated in this repository should only be used against systems and domains that you own or have **explicit permission** to assess.

Always follow applicable laws, organizational policies, and the defined scope of a security assessment.
