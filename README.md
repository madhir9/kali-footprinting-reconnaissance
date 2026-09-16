# Footprinting & Reconnaissance with Multiple Kali Linux Tools

## Overview

This project is a Week 2 cybersecurity and ethical hacking practical
focused on **footprinting and reconnaissance** using Kali Linux.

The lab demonstrates how publicly available information about a website
can be collected using several built-in reconnaissance tools. The
objective is educational: understand what information an organization
exposes publicly and how defenders can reduce unnecessary exposure.

> **Educational use only:** Perform reconnaissance only on systems and
> domains you own or have explicit permission to test.

## Tools Used

  -----------------------------------------------------------------------
  Tool                                Purpose
  ----------------------------------- -----------------------------------
  `whois`                             Find public domain registration
                                      information

  `whatweb`                           Identify web technologies, CMS,
                                      plugins, and related information

  `nslookup`                          Resolve a domain name to its IP
                                      address

  `curl -I`                           Inspect HTTP response headers

  `wafw00f`                           Detect whether a Web Application
                                      Firewall (WAF) is present

  `dnsrecon`                          Enumerate publicly available DNS
                                      records
  -----------------------------------------------------------------------

## Lab Target

The practical uses:

``` text
networkwalks.com
```

The project material identifies this as a footprinting exercise and asks
the learner to record the output of each command for a final report.

## Tasks

### Task 1 --- WHOIS

Command:

``` bash
whois networkwalks.com
```

Purpose:

-   View public domain registration details
-   Identify registrar information
-   Review registration and expiry information
-   Identify name servers

### Task 2 --- WhatWeb

Command:

``` bash
whatweb networkwalks.com
```

Purpose:

-   Fingerprint web technologies
-   Identify the CMS and plugins
-   Identify web-server information where exposed

### Task 3 --- DNS Lookup

Command:

``` bash
nslookup networkwalks.com
```

Purpose:

-   Resolve the domain name
-   Identify the IP address associated with the domain

### Task 4 --- HTTP Headers

Command:

``` bash
curl -I https://networkwalks.com
```

Purpose:

-   Inspect HTTP response headers
-   Review server information
-   Observe status codes, redirects, cookies, and other exposed headers

### Task 5 --- WAF Detection

Command:

``` bash
wafw00f networkwalks.com
```

Purpose:

-   Determine whether a Web Application Firewall is detected
-   Understand what defensive layer may be protecting the web
    application

### Task 6 --- DNS Reconnaissance

Command:

``` bash
dnsrecon -d networkwalks.com
```

Purpose:

-   Enumerate publicly available DNS information
-   Review name servers
-   Identify mail servers
-   Review SPF/TXT information
-   Identify available service records

## Learning Objectives

After completing this practical, the learner should be able to:

1.  Explain what reconnaissance/footprinting means.
2.  Use common Kali Linux reconnaissance tools.
3.  Collect publicly available domain and DNS information.
4.  Identify technologies exposed by a web application.
5.  Inspect HTTP response headers.
6.  Understand the purpose of WAF detection.
7.  Recognize why organizations should minimize unnecessary public
    information exposure.

## Evidence

For each task, save:

-   A screenshot of the command and output.
-   The command output in a text file.
-   Notes explaining what information was discovered.

## Example Workflow

``` bash
# 1. Domain registration information
whois networkwalks.com

# 2. Web technology fingerprinting
whatweb networkwalks.com

# 3. DNS lookup
nslookup networkwalks.com

# 4. HTTP response headers
curl -I https://networkwalks.com

# 5. WAF detection
wafw00f networkwalks.com

# 6. DNS enumeration
dnsrecon -d networkwalks.com
```

## Why Footprinting Matters

Reconnaissance is an important first phase of security testing because
it helps a security professional understand what information is publicly
exposed before conducting further testing.

Defenders can also use the same techniques against their own
infrastructure to identify information that could unnecessarily assist
an attacker.

## Ethical & Legal Notice

This repository is for **education, cybersecurity training, and
authorized security testing**.

Do not use these commands against systems you do not own or do not have
explicit permission to assess. Always follow applicable laws,
organizational policies, and the scope of the security assessment.

## Reference

Practical source material: **Networkwalks --- Week 2 \| Project Module
1: Footprinting & Reconnaissance Attacks with Multiple Kali Tools.**
