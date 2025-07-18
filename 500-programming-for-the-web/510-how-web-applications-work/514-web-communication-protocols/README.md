---
description: >-
  Explore the essential protocols that enable communication over the web, from
  HTTP and HTTPS to TCP/IP, DNS, and secure encryption standards, ensuring
  reliable and secure data exchange.
---

# 514 Web communication protocols

### TL;DR

Web communication protocols define the rules for transmitting and securing data over the internet. HTTP and HTTPS manage web content delivery, while TCP/IP ensures reliable data transfer. DNS translates domain names into IP addresses, and FTP/SFTP handles file transfers. Secure communication is facilitated by SSL/TLS, while SMTP, POP3, and IMAP enable email transmission and retrieval. Understanding these protocols is fundamental to developing and maintaining secure and efficient web applications.

***

### Targets

In this section, you will learn to

* Explain the purpose and function of web communication protocols.
* Compare HTTP and HTTPS, including their impact on security and performance.
* Describe the role of TCP/IP in ensuring reliable data transmission.
* Understand how DNS resolves domain names to IP addresses.
* Differentiate between FTP and SFTP for file transfers.
* Explain the encryption mechanisms of SSL/TLS and their role in securing web traffic.
* Identify the purpose of SMTP, POP3, and IMAP in email communication.
* Evaluate how these protocols interact to support web applications and services.

***

### TCP/IP stack

The appropriate protocols must be implemented within a device that wishes to communicate over a network. The protocols will be used to format the data from the application that needs to send it and transform it into bits encoded as a suitable optical, electrical, or radio frequency signal. This signal is transmitted onto the 'media' (any wired or wireless technology over which data can be transmitted). At the receiving end, the reverse must happen, transforming the bits back into the data to be passed to the receiving application.

This complex set of requirements is achieved by organising the process into a series of functional layers and ensuring the data is sent from layer to layer for processing before being sent to the media for transmission.

These sequential layers can be visualised as a set of processes arranged on top of each other to form a stack. Conceptually, data flowing down the stack as it moves from the application on a device heads out onto the media for transmission. At the receiving end, the data flows from the transmission media up the stack to be delivered to the application on the receiving device.

The TCP/IP is the protocol stack used on the Internet. It is split into four layers, which are:

* Application layer
* Transport layer
* Internet layer (sometimes called the Network Layer)
* Link layer (sometimes called the Data Link Layer)

![TCP/IP four-layer model](https://isaaccomputerscience.org/api/v3.5.0/api/images/content/computer_science/computer_networks/the_internet/figures/isaac_cs_net_internet_layer_overview.svg)

**Application layer**

The application layer sends data from software applications into the protocol stack and passes it to the receiving application at the other end of the communications link.

This layer uses protocols specific to the types of applications being used. For example, a web browser uses HTTP or HTTPS (HTTPS is an encrypted version of HTTP used for secure web transactions). An email client uses SMTP alongside either IMAP or POP3.

The application layer adds the relevant header to the data according to the protocol before sending it to the next layer.

The application layer passes the data down to the transport layer.

**Transport layer**

The transport layer breaks the application data down into data packets. Sequence numbers are allocated, and source and destination Port numbers are added to the header. See more on port numbers and sockets below.

At this layer, there are two options:

1. Data can be sent using TCP, a reliable transport protocol. If the receiving end notices that some data is missing, it requests that it be sent again.
2. The data can be sent using a protocol called UDP. This is an unreliable transport protocol; the receiving end may note that some data is missing and pass this information up to the application layer.

The transport layer passes the data down to the internet layer.

**Internet layer**

The Internet layer prepares the data for the Internet. At this stage, source and destination IP addresses are added in a header. The resultant data is called an IP packet.

For each IP packet to reach its destination, routers use the destination address stored in the header to choose the route through the Internet.

The internet layer passes the data down to the link layer.

**Link layer**

The link layer is responsible for transporting IP packets across each link that connects two communicating computers. These links could be a combination of Ethernet, WiFi, 4G, satellite, or fibre.

An IP packet will travel across many physical and/or wireless links between the source and the final destination. Each type of physical link uses a different technology and has its own protocol. Each protocol adds its own headers to the IP packets to create frames, which are used to carry the IP packets across that particular link.

Ethernet is a common link layer protocol used in local area networks. It governs the way data packets are transmitted on a shared channel.

The link layer at one end of a link communicates with the link layer at the other end by converting the frame into an electrical, electromagnetic (wireless), or light signal and then sending this signal out onto the media.

We call the data structures **frames** at the link layer to distinguish them from 'packets', which is the term used at the internet layer.

We call the data structures **frames** at the link layer to distinguish them from 'packets', the term used at the internet layer. The frames carry, or encapsulate, the packets from the layer above. If the link layer is Ethernet, the frames are called Ethernet frames. The header of an Ethernet frame contains the source and destination MAC addresses. The source MAC address is the device sending the frame, typically your computer. The destination MAC address is the device on the Ethernet LAN receiving the frame, typically your router. The destination device then retrieves the packet and discards the frame before processing it or sending it on its way to the following link, where a new frame will encapsulate it.

### **Web communication protocols**

Web communication protocols define how data is transmitted, received, and processed across the internet. These protocols ensure that web applications function reliably, securely, and efficiently. Below is a summary of key protocols used in web development and data exchange.

<table><thead><tr><th width="89.5625">Protocol</th><th width="121.76953125">Full Name</th><th width="168.69921875">Purpose</th><th width="179.49609375">Key Features</th><th>Common Use Cases</th></tr></thead><tbody><tr><td>HTTP</td><td>Hypertext Transfer Protocol</td><td>Enables communication between web browsers and servers</td><td>Stateless, text-based, operates over TCP, request-response model</td><td>Loading web pages, fetching resources</td></tr><tr><td>HTTPS</td><td>Hypertext Transfer Protocol Secure</td><td>Secure version of HTTP with encryption</td><td>Uses SSL/TLS for encryption, protects data integrity and confidentiality</td><td>Secure web browsing, e-commerce, banking</td></tr><tr><td>TCP/IP</td><td>Transmission Control Protocol / Internet Protocol</td><td>Governs how data is sent and received over networks</td><td>TCP ensures reliable transmission, IP handles addressing and routing</td><td>Sending web traffic, email, streaming services, online gaming</td></tr><tr><td>DNS</td><td>Domain Name System</td><td>Translates domain names into IP addresses</td><td>Hierarchical structure, caches frequent lookups, distributed servers</td><td>Website access, email routing, cloud services</td></tr><tr><td>FTP</td><td>File Transfer Protocol</td><td>Transfers files between a client and a server</td><td>Requires authentication, can be unencrypted, supports file directories</td><td>Uploading/downloading website files, managing remote storage</td></tr><tr><td>SFTP</td><td>Secure File Transfer Protocol</td><td>Secure version of FTP using SSH encryption</td><td>Encrypts commands and data, prevents eavesdropping, requires authentication</td><td>Secure file transfers for web hosting, enterprise data exchange</td></tr><tr><td>SSL/TLS</td><td>Secure Sockets Layer / Transport Layer Security</td><td>Encrypts data to secure internet communications</td><td>TLS is the successor to SSL, protects against data interception, uses certificates</td><td>Securing HTTPS traffic, encrypted email, VPNs</td></tr><tr><td>SMTP</td><td>Simple Mail Transfer Protocol</td><td>Sends email messages between servers</td><td>Push protocol, handles outgoing mail, operates on port 25 (or 587 for authentication)</td><td>Sending emails from mail clients to servers</td></tr><tr><td>POP3</td><td>Post Office Protocol 3</td><td>Retrieves emails from a server for offline access</td><td>Downloads emails to local device, deletes from server by default</td><td>Checking email on single-device setups</td></tr><tr><td>IMAP</td><td>Internet Message Access Protocol</td><td>Manages emails on a remote server</td><td>Syncs emails across multiple devices, allows partial downloads</td><td>Cloud-based email access, multiple-device email syncing</td></tr></tbody></table>

### **Ports**

Computers run many applications, and the transport layer is well-used. Upon receiving a segment or datagram, the transport layer must pass the data to the correct application layer service. For example, if the data comes from a web server, as it arrives at the transport layer on the client computer, it must be passed to the web browser that requested it at the application layer. To deliver the data to the correct application, each request from the application layer is allocated a port number to return the data to the proper place. Client or ephemeral port numbers are randomly assigned from a bank of numbers on the client device.

Server processes also use ports. An application server, e.g., a web server, is said to be 'listening' on a specific port to receive relevant requests. Servers use "well-known port numbers." These numbers are well-known so that the client making the request doesn't need to look them up. The next section has a table of well-known port numbers.

The source and destination port numbers are added to the segment header at the transport layer.

When a request is received at the server, the source and destination ports are swapped. For example, if a web browser sends a message to a web server on port 80 (destination) from port 3302 (source), the reply will come back from the web server on port 80 (source) and be sent to the web browser on port 3302 (destination).

This is essential, as you may have many open sessions accessing the same resource. For example, you may have multiple tabs open in a browser, accessing different pages of the same website. The randomly generated source port becomes the destination port of the reply and thus uniquely identifies the exact process that made the original request.

![Source and destination ports](https://isaaccomputerscience.org/api/v3.5.0/api/images/content/computer_science/computer_networks/the_internet/figures/isaac_cs_net_internet_ports.png)

**Port numbers**

Servers use well-known port numbers, ranging from 0 to 1024, so the client making a request does not need to look them up. The table below shows the numbers for the most common application servers.

Servers can be configured to use different numbers, but these will need to be communicated to the client. Server port numbers are usually configured within the client application software to be readily available to the transport layer.

<table><thead><tr><th width="220.828125" align="center">Port</th><th width="288.7265625" align="center">Protocol</th><th>Use</th></tr></thead><tbody><tr><td align="center">20</td><td align="center">FTP</td><td>File transfer</td></tr><tr><td align="center">22</td><td align="center">SSH</td><td>Secure remote access</td></tr><tr><td align="center">25</td><td align="center">SMTP</td><td>Mail transfer</td></tr><tr><td align="center">80</td><td align="center">HTTP</td><td>Website access</td></tr><tr><td align="center">110</td><td align="center">POP</td><td>Mailbox access</td></tr><tr><td align="center">143</td><td align="center">IMAP</td><td>Mailbox access</td></tr><tr><td align="center">443</td><td align="center">HTTPS</td><td>Secure website access</td></tr></tbody></table>

### **Sockets**

TCP is often referred to as an 'end-to-end' protocol. From the application's point of view (client or server), using the TCP protocol to handle communications is analogous to having a simple serial cable running between the two devices (all of the complex details of how this works are abstracted through the lower layers).

**A TCP endpoint is a combination of an IP address and a port number; this combination is known as a socket. The socket will persist throughout the connection.**

The server needs to be able to handle multiple concurrent sessions as it communicates with many clients. Each session is identified by its socket. Each client uses a unique IP address and 16-bit port number so that the server can track up to 65,534 connections per host.

The sockets facilitate asynchronous communication, which means that only one device (client or server) can communicate at a time. The socket is designated as the source or the destination, depending on which side is transmitting the data.

Let us consider a situation where you are using your laptop and have two browser tabs open. In one tab, you are scrolling through your Twitter feed; in another, you are checking the news on the BBC. Each session has been allocated a port number to communicate with the relevant server. The socket is the combination of your IP address and this port number.

<figure><img src="../../../.gitbook/assets/image (5).png" alt=""><figcaption><p>TCP/IP sockets</p></figcaption></figure>

***

### Key Concepts

> * **Hypertext Transfer Protocol (HTTP/HTTPS)**\
>   The foundation of web communication, with HTTPS adding encryption for security.
> * **Transmission Control Protocol/Internet Protocol (TCP/IP)**\
>   A suite of protocols governing how data is sent and received over networks.
> * **Domain Name System (DNS)**\
>   Converts human-readable domain names into machine-friendly IP addresses
> * **File Transfer Protocols (FTP/SFTP)**\
>   Methods for transferring files over the internet, with SFTP providing encryption.
> * **Secure Sockets Layer (SSL) / Transport Layer Security (TLS)**\
>   Encryption protocols that protect data from interception.
> * **Ports and protocols**\
>   Standardised communication endpoints for different services (e.g., port 80 for HTTP, port 443 for HTTPS).
> * **Email protocols (SMTP, POP3, IMAP)**\
>   Control how email is sent, retrieved, and stored on mail servers.
> * **Interoperability of protocols**\
>   How these communication standards work together to create a functional and secure internet ecosystem.
