---
description: >-
  How distributed web applications function through communication between client
  devices and centralised servers
---

# 512 Client-server model

### TL;DR

The **client-server model** is the foundation of web applications, where a **client** (e.g., a web browser or mobile app) requests resources from a **server** that processes and responds to those requests. This interaction follows the **request-response cycle**, typically using **HTTP** or **HTTPS** protocols. Web servers handle client requests, often working with **database servers** to retrieve and store data. The model can be **centralised** (single server) or **distributed** (multiple servers for scalability). Security measures, such as **authentication, encryption, and access control**, are essential to protect data and maintain secure communication between clients and servers.

***

### Targets

In this section, you will learn to

* Explain the **client-server architecture** and its role in web applications.
* Differentiate between **clients** (browsers, mobile apps) and **servers** (web, database, application servers).
* Describe the process of **request-response communication** using **HTTP** and **HTTPS**.
* Identify different types of **servers** and their functions, including web servers, database servers, and caching servers.
* Compare **centralised vs. distributed architectures**, including cloud-based solutions.
* Recognise security considerations in **client-server interactions**, such as authentication and encryption.

***

### How the client-server model works

The client-server model is a distributed application structure that partitions tasks or workloads between the providers of a resource or service, called servers, and service requesters, called clients. In the client-server architecture, when the client computer sends a request for data to the server through the internet, the server accepts the requested process and delivers the data packets requested back to the client. Clients do not share any of their resources. Examples of the client-server model are email,the  World Wide Web, and cloud computing.

The most common application of the client-server model is delivered through the Internet via web browsers and servers.

* **Client**\
  When we say the word Client, we mean a person or organisation using a particular service. Similarly, in the digital world, a client is a computer (host) capable of receiving information or initiating a request for a particular service from the service providers (servers).
* **Servers**\
  Similarly, when we talk about servers, we mean a person or medium that serves something. In this digital world, a server is a remote computer that provides information (data) or access to particular services.

So, the client requests something, and the server serves it as long as it is in the database.

![](https://media.geeksforgeeks.org/wp-content/uploads/20240419170238/Client-Server-Model.webp)

_Client-server model_

### **How the browser interacts with the servers?**

A few steps exist to interact with a client's servers.

1. The user enters the website or file's URL (Uniform Resource Locator). The browser then requests the DNS (Domain Name System) server.
2. The DNS server looks up the IP address of the web server.
3. The DNS server responds with the IP address of the web Server.
4. The browser sends over an HTTP/HTTPS request to the web server’s IP address (provided by the DNS server).
5. The server with the necessary files for the website.
6. The browser then renders the files, and the website is displayed. This rendering is done with the help of a DOM (Document Object Model) interpreter, CSS interpreter, and JS Engine, collectively known as the JIT or (Just in Time) compilers.

![](https://media.geeksforgeeks.org/wp-content/uploads/20231128175510/Client-Server-Model-2.png)

_Client-server request and response_

#### **Advantages of the client-server model**

* A centralised system with all data in a single place.
* It is cost-efficient and requires less maintenance cost, and data recovery is possible.
* The capacity of the client and servers can be changed separately.

#### **Disadvantages of the client-server model**

* Clients are prone to viruses, Trojans, worms, and malware that may also be present on the server.
* Servers are prone to denial-of-service attacks.
* Data packets may be spoofed or modified during transmission.
* Phishing or capturing user login credentials or other useful information is common, as are MITM(Man in the Middle) attacks.

The client-server architecture consolidates resources on servers for greater control and security, allows for flexible client options, and relies on a robust network for scalability and efficiency. While there are cost implications, the client-server model remains fundamental and has been shaped by trends such as cloud computing.Text

***

### Key Concepts

> * **Client-Server Model**: A network structure where a client (e.g., a browser) requests resources or services from a central server.
> * **Client**: A device or application that sends requests to a server, such as web browsers, mobile apps, and IoT devices.
> * **Server**: A system that processes client requests and returns responses, including web servers (e.g., Apache, Nginx) and database servers (e.g., MySQL, MongoDB).
> * **Request-Response Cycle**: The process where a client sends an **HTTP request**, and the server responds with a **resource** (HTML, JSON, etc.).
> * **Stateless Communication**: HTTP is a stateless protocol, meaning each request is independent unless session management techniques (cookies, tokens) are used.
> * **Centralised vs. Distributed Systems**: Centralised architectures rely on a single server, while distributed systems use multiple servers for scalability and redundancy (e.g., cloud computing).
> * **Security Considerations**: Authentication methods (OAuth, JWT), encryption protocols (SSL/TLS), and access controls ensure secure client-server communication.



