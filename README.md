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

### 5️⃣ WHOIS


## ⚙️ Reconnaissance Process

### 1. WHOIS — Domain Registration Information

I used `whois` to retrieve publicly available domain registration information.

### Command

```bash
whois networkwalks.com
```
![WHOIS Screenshot](images/whois.png)


### 6️⃣ WhatWeb


### 2. WhatWeb — Web Technology Fingerprinting

I used WhatWeb to identify technologies exposed by the website.

### Command

```bash
whatweb networkwalks.com
```

### 7️⃣ NSLookup


### 3. NSLookup — DNS Resolution

I used `nslookup` to resolve the domain name and identify its IP address.

### Command

```bash
nslookup networkwalks.com
```


### 8️⃣ CURL


### 4. CURL — HTTP Response Headers

I used `curl` to inspect the HTTP response headers returned by the website.

### Command

```bash
curl -I https://networkwalks.com
```


### 9️⃣ WAFW00F


### 5. WAFW00F — Web Application Firewall Detection

I used `wafw00f` to check whether the website was protected by a Web Application Firewall.

### Command

```bash
wafw00f networkwalks.com
```
