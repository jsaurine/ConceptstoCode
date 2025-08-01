---
description: >-
  Understand how data packets, IP addresses and DNS work together to deliver
  information to and from web servers.
---

# 513 Routing data across the Internet

### Overview

In this topic, we explore how data travels across the internet when a user accesses a website. Behind every web request is a process of **routing**, where data is split into packets, assigned addresses, and passed through multiple networks to reach its destination. Students learn how systems like **DNS** and **IP addressing** make this possible, and how these concepts relate to real-world web application performance and reliability.

### Targets

In this topic, students learn to:

* Describe how data is split into packets and routed across the internet
* Explain the role of IP addresses (including IPv4) in identifying devices
* Understand how DNS translates domain names into IP addresses
* Trace the journey of a web request from client to server
* Recognise how routing influences speed, reliability and security

### Syllabus references

<details>

<summary><a href="https://curriculum.nsw.edu.au/learning-areas/tas/software-engineering-11-12-2022/content/year-12/fa6aab137e"><strong>Programming for the web</strong></a></summary>

**Data transmission using the web**

* Investigate and practise how data is transferred on the internet\
  – data packets\
  – internet protocol (IP) addresses, including IPv4\
  – domain name systems (DNS)

</details>

### How is data sent across the internet?

#### Data packets

When a large message (such as a webpage or file) is sent over the internet, it is broken into **small pieces called packets**. Each packet includes:

* A **payload** (the actual data)
* A **header** (routing information, such as source and destination IP addresses)

These packets may take different paths through the network and are reassembled at the destination.

<figure><img src="../../.gitbook/assets/image (24).png" alt=""><figcaption><p><em>The IPv4 packet header structure illustrates the essential fields for routing and managing data across networks. It includes metadata such as the IP version, header length, source and destination addresses, and additional fields for error checking, fragmentation, and routing options. This structure ensures efficient and reliable packet transmission while allowing flexibility for optional enhancements.</em></p></figcaption></figure>

#### IP addressing

Every device connected to the internet has a unique **IP address**, which works like a postal address for digital communication.

* **IPv4** uses four sets of numbers (e.g. 203.14.53.1)
* Newer systems may also use **IPv6** to accommodate more devices

Packets use these addresses to determine where they are going and where they came from.

#### Domain Name System (DNS)

Humans use domain names (like `www.example.com`), but computers route information using IP addresses. DNS acts like a **phonebook for the internet**, translating domain names into IP addresses.

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption><p>A browser sends a request to <code>www.example.com</code>. The DNS server translates this into an IP address, which is used to route packets to the correct web server.</p></figcaption></figure>

### Data packets and routing

When information is sent over the internet, it is broken into **small units called packets**. Each packet contains:

* a **payload** (the actual data, such as part of a webpage or video), and
* a **header** (which includes source and destination IP addresses, sequencing, and error-checking data).

Packets allow data to be transferred efficiently, even over busy or unreliable networks. This method of transfer is known as **packet switching**.

#### How packet switching works

Packets are sent independently across the network and may take different routes to reach the same destination. Once they arrive, they are reassembled into the original message. This flexible approach helps balance network traffic and avoids reliance on a single fixed path.

The internet uses a **connectionless** approach—there is no permanent connection between sender and receiver. Each packet is handled individually, and it's the responsibility of the source and destination systems to ensure everything is received correctly.

#### The role of routers

Routers are devices that guide packets through the internet. Each router examines the destination address and decides where to send the packet next using a **routing table**. This is known as a **hop**, and most packets pass through many routers on their journey.

If one path becomes unavailable, routers automatically choose another route. Large internet backbone routers have many interfaces and constantly update their routing tables to select the most efficient path.

<figure><img src="../../.gitbook/assets/image (25).png" alt=""><figcaption><p><em>This diagram illustrates packet switching, dividing data into smaller packets that travel independently through various network paths. Each packet is routed dynamically based on availability and efficiency, allowing optimal bandwidth utilisation. At the destination, packets are reassembled into the original data, demonstrating the flexibility and resilience of packet-switched networks.</em></p></figcaption></figure>

### The journey of a web request

1. The user types a URL into the browser.
2. The browser checks the DNS cache or queries a DNS server.
3. The domain name is resolved to an IP address.
4. The browser sends an HTTP request to that address.
5. Routers direct the data packets across multiple networks to reach the destination server.
6. The server responds, and packets are sent back using the same process.

### Why routing matters

Understanding routing helps explain:

* Why some websites load faster than others
* How content delivery networks (CDNs) improve speed
* How attackers can intercept, block, or spoof traffic
* Why secure communication protocols (like HTTPS) are important

### Summary

Every web interaction relies on routing systems that break up data, label it with addresses, and deliver it through networks using DNS and IP. These foundational concepts are essential for understanding how the web works and for troubleshooting issues in web development.



