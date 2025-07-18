---
description: >-
  Discover how data travels across the internet through packet switching,
  routing protocols, and network optimisation to ensure efficient and secure
  communication.
---

# 513 How data is routed across the Internet

### TL;DR

When you send data across the internet, it doesn’t travel as a continuous stream but as discrete packets, each following its own path to the destination. This process is managed by routing protocols that determine the most efficient path through a network of interconnected routers. The Internet Protocol (IP) ensures that each packet reaches the correct address, while the Transmission Control Protocol (TCP) or the User Datagram Protocol (UDP) determines how data is handled along the way. Routing strategies such as static, dynamic, and adaptive routing play a crucial role in optimising network performance and reliability.

***

### Targets

In this section, you will learn to

* Explain the concept of data packetisation and its role in internet communication.
* Describe the function of routing protocols in determining the best path for data transmission.
* Compare and contrast TCP and UDP in terms of data reliability and speed.
* Analyse how routers use IP addressing to forward data to its destination.
* Identify factors that influence routing decisions, including congestion and latency.
* Explain the impact of routing on network efficiency and security.

***

### **Internet addresses**

The Internet is a vast network of interconnected routers that forward data packets along the correct route to the intended destination. Each router cannot hold a list with the physical address of every device. This list would be huge, and it would take a lot of memory and processor time to use it and keep it updated. And how would the system cope if a device moved? It just wouldn't work!

**Internet Protocol (IP) addresses**

When IP addresses were invented in the 1970s, they were decided to be 32 bits long. 32 bits allow for 4 billion unique addresses, enough for each person on Earth at the time to have one. We didn't know how big the interconnected network—or internet—we were building would become!

Writing a 32-bit IP address in binary would not be very human-friendly. Instead, the address is split into four 8-bit chunks (bytes), and each chunk is converted to decimal. The address is then written in dotted decimal notation, with the four decimal values separated by dots.

So, the IP address 11000000101010000000111000010111 becomes:

| Binary         | 11000000 | 10101000 | 00001110 | 00010111 |
| -------------- | -------- | -------- | -------- | -------- |
| Dotted decimal | 192      | 168      | 14       | 23       |

**11000000 10101000 00001110 00010111 = 192.168.14.23**

**IPv4 vs IPv6**

So far, all of the information about IP addresses has referred to IP version 4 (IPv4), which uses the 32-bit address structure described and has facilitated the growth of the internet over the last four decades. The 32 bits in IPv4 give 4,294,967,296 addresses, but we are running out. Nobody dreamed that the internet would grow to the size it is today. The possibility of using more than four billion addresses would have seemed ludicrous in the 1970s. However, the growth of the internet has been exponential, and there are now not enough addresses. Techniques have been developed to work around this problem, but the permanent solution is to have more addresses.

Therefore, IP version 6 (IPv6) has been developed, with 128 bits allocated for each address: a colossal 3.4×1038  (340,282,366,920,938,463,463,374,607,431,768,211,456) addresses.

**MAC addresses**

Every device connected to the Internet has a unique identifier called a Media Access Control address (MAC address) and an IP address. The manufacturer assigns MAC addresses, which can’t be changed.

**Subnet masks**

On any network or subnet (subnetwork), the network ID in the IP address for all hosts must be identical. In this context, a host is any device on the subnet with a unique IP address, meaning that the section of the IP address representing the host ID must be different for each host. The subnet mask specifies the number of bits allocated to the network ID.

Subnet masks are written to contain 1s in the position of the network ID and 0s in the position of the host ID. In binary, a subnet mask might look like this:

1 1 1 1 1 1 1 1 . 1 1 1 1 1 1 1 1 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0

This would show that the network ID was 16 bits and the host ID was 16 bits. Because humans are not great at working with long binary numbers, it is more likely to see the mask written as:

255.255.0.0

A subnet mask of 255.255.0.0 means that the first 16 bits of the IP address are the network ID. A subnet mask 255.192.0.0 implies that the first 10 bits are the network ID. Writing this denary subnet mask in binary illustrates how many bits are associated with the network ID:

255.192.0.0

converts to

1 1 1 1 1 1 1 1 . 1 1 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0

A newer notation uses a slash and the number of bits appended to the address. For example, an IP address specified as  172.16.200.12/12 means that the first 12 bits are the network ID.

### **Data packets**

Information is transmitted in 32-bit data packets, which comprise the data being transported, called the payload, and a header. The header of a data packet contains essential routing information, such as source and destination IP addresses, packet sequencing details, and error-checking data.

Data packets carry various payload data types, such as web pages, emails, or audio tracks. The protocol field in the packet header identifies the type of data being transmitted. Internet packets have a maximum size limit to prevent any single transmission from monopolising bandwidth.

<figure><img src="../../../.gitbook/assets/image (24).png" alt=""><figcaption><p><em>The IPv4 packet header structure illustrates the essential fields for routing and managing data across networks. It includes metadata such as the IP version, header length, source and destination addresses, and additional fields for error checking, fragmentation, and routing options. This structure ensures efficient and reliable packet transmission while allowing flexibility for optional enhancements.</em></p></figcaption></figure>

Packets are moved around the Internet using a method called packet switching. This approach utilises relatively small data packets, sharing multiple data paths. As a result, different packets from the same transmission can take different routes to their destination. The internet operates on an end-to-end principle, meaning that the source and destination endpoints ensure that all sent data is correctly received. This communication method is termed connectionless, as it does not rely on a dedicated path. Most internet traffic utilises packet switching, making the internet a connectionless network.

**Routers and packet switching**

Packet switching is a method for efficiently routing data over a network. It involves breaking down data into smaller packets, which are then independently routed through various paths in the network, allowing for more flexible and efficient bandwidth use. Each packet travels separately through the network, potentially taking different routes to reach the same destination, where they are reassembled into the original data.

<figure><img src="../../../.gitbook/assets/image (25).png" alt=""><figcaption><p><em>This diagram illustrates packet switching, dividing data into smaller packets that travel independently through various network paths. Each packet is routed dynamically based on availability and efficiency, allowing optimal bandwidth utilisation. At the destination, packets are reassembled into the original data, demonstrating the flexibility and resilience of packet-switched networks.</em></p></figcaption></figure>

In any packet-switched network, the router is the key device. The router examines the destination address of an incoming packet and decides which of its interfaces the packet should be sent to until it eventually arrives at the destination. On domestic routers, such as those provided within your home, there are only two interfaces: the LAN and the WAN. Here, the decision is simple. All packets not for the local network are directed to the WAN interface. Core Internet backbone routers have many different interfaces. Due to the meshed nature of the internet backbone, it may be possible to get to a specific destination over several different paths.

Each router has a set of rules — a routing table — to decide what to do with an incoming packet. Each packet is treated individually, and a separate routing decision is made for each. Each router-to-router link is called a hop; the router determines the best 'next hop' to allow the packet to reach its final destination. If any part of the communications infrastructure fails, the router chooses a different route, and subsequent packets may be sent over a different path.\
Routers can be configured to select the best route or share data to learn the best routes. This is how the core routers work. The routing table is constantly updated with information about the optimal path for packets.&#x20;

#### Latency and lost packets

Some routers may sometimes receive packets faster than they can route them. These packets are buffered in memory, which introduces delays (known as 'high latency'). For most traffic, this is not an issue; it just means that the web page takes longer to load or a file download takes more time than expected. However, for other network traffic, these delays may have more of an impact, mainly if you are talking over a voice call or playing an online game. If the buffering is severe, the router may run out of memory, and packets can be discarded.

IP packets contain a Type of Service (ToS) field in the packet header; this makes it possible to mark packets with a priority level and thus request special treatment, i.e. to be placed at the front of the queue of packets to be routed. However, routers may choose to implement or ignore these requests.\
A situation can occur where packets are sent to an unreachable destination address. Unaware of this, routers may route such packets towards a default device. This default device may also pass the packet on, causing a loop. In such circumstances, a packet could loop forever between routers. To prevent this, internet packets have a time to live (TTL) counter in their header. This is initially set when the packet is created and reduced by one every time it goes through a router. If the counter reaches zero, the packet is discarded.

***

### Key concepts

> * **Packet switching**\
>   The method of breaking data into packets that travel independently across a network.
> * **Internet Protocol (IP)**\
>   The addressing system that directs packets to the correct destination.
> * **Transmission Control Protocol (TCP)**\
>   A connection-oriented protocol ensuring data is delivered reliably.
> * **User Datagram Protocol (UDP)**\
>   A connectionless protocol prioritising speed over reliability.
> * **Routing protocols**\
>   Algorithms that determine the best path for data, including static, dynamic, and adaptive routing.
> * **Latency and congestion**\
>   Factors that affect the efficiency and performance of data routing.
> * **Network security in routing**\
>   The role of encryption and secure routing strategies in protecting data during transmission.



