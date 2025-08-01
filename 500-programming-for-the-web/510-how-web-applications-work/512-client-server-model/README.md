---
description: >-
  Understand how the client-server model enables interactive communication
  between browsers and web servers.
---

# 512 Client-server model

### 512 Client-server model

Understand how the client-server model enables interactive communication between browsers and web servers.

### Overview

In this topic, we explore how web applications use the client-server model to process requests and deliver dynamic content. This model defines the relationship between the user's device (client) and a remote server, enabling them to exchange information over the internet using web protocols. Understanding this model is fundamental to designing, debugging, and securing web-based systems.

### Targets

In this topic, students learn to:

* Define the client-server model and identify its components
* Describe the flow of requests and responses in a web application
* Understand the role of protocols such as HTTP and IP in managing communication
* Explain how sessions and state are managed across multiple interactions
* Recognise how separating client and server logic improves security and design

### Syllabus references

<details>

<summary><a href="https://curriculum.nsw.edu.au/learning-areas/tas/software-engineering-11-12-2022/content/year-12/fa6aab137e"><strong>Programming for the web</strong></a></summary>

**Data transmission using the web**

*   Investigate and practise how data is transferred on the internet

    data packets

    internet protocol (IP) addresses, including IPv4

    domain name systems (DNS)

</details>

### What is the client-server model?

The **client-server model** describes a relationship in which a **client**, such as a web browser, requests resources from a **server**, which processes the request and returns a response.

This model is used by nearly all web applications. The client handles user interaction and presentation, while the server manages business logic, data storage, and security. This separation allows each part to be developed, scaled, and secured independently.

### The request-response cycle

1. The client (browser) sends an HTTP request to a server.
2. The server processes the request—possibly querying a database or performing a calculation.
3. The server sends an HTTP response back to the client.
4. The browser receives the response and displays the content or data to the user.

This cycle repeats with each interaction—clicking links, submitting forms, or navigating to new pages.

**Image placeholder:**\
&#xNAN;_&#x41; labelled diagram showing the request-response cycle between client and server, including arrows for requests and responses, and optional components like DNS lookup or database query._

**Caption:**\
The client sends a request to the server using HTTP. The server processes the request and returns a response, such as a webpage, data, or confirmation message.

### Benefits of the client-server model

#### Security

Sensitive operations such as login verification or data access are handled on the server side, reducing exposure to malicious activity on the client.

#### Modularity

Front-end and back-end development can be handled by separate teams using different tools and languages. This improves maintainability and scalability.

#### Scalability

Servers can handle multiple simultaneous requests from clients, and can be scaled vertically (more resources) or horizontally (more servers) as needed.

### Real-world example

A student logs into their school portal:

* The client (browser) sends a login request to the server.
* The server checks the credentials and creates a session.
* The server sends back a personalised dashboard page.
* The client renders the dashboard for the student to use.

### Summary

The client-server model is the foundation of all interactive web systems. It allows user devices to send requests to servers, which respond with content or actions. Understanding how this model works is essential for building secure, efficient, and responsive web applications.
