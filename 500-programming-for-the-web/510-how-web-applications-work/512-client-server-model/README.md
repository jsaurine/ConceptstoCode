---
description: >-
  Understand how the client-server model enables interactive communication
  between browsers and web servers.
---

# 512 Client-server model

### Overview

In this topic, we explore how web applications use the client-server model to manage interactions between users and the systems that process their requests. This model separates concerns between the front-end (client) and back-end (server), enabling efficient, scalable, and secure application development. A deep understanding of this model is essential to design reliable systems that respond to user input in real time.

### Targets

In this topic, students learn to:

* Describe the components and roles of the client-server model
* Explain how requests and responses are exchanged across a network
* Identify the benefits of separation between front-end and back-end
* Understand how session data is maintained between interactions
* Prepare for full-stack development by recognising system responsibilities

### Syllabus references

<details>

<summary><a href="https://curriculum.nsw.edu.au/learning-areas/tas/software-engineering-11-12-2022/content/year-12/fa6aab137e"><strong>Programming for the web</strong></a></summary>

**Designing web applications**

* Model elements that form a web development system\
  – client-side (front-end) web programming\
  – server-side (back-end) web programming
* Describe how collaborative work practices between front-end and back-end developers improve the development of a web solution

</details>

### What is the client-server model?

The **client-server model** is a network architecture where a client (such as a web browser) sends requests for information or services, and a server responds with the appropriate data or functionality. This model enables multiple clients to interact with a centralised server, making it ideal for web applications.

### How the request-response cycle works

When you load a website or interact with a form, a series of actions take place:

1. The **client** sends an HTTP request (e.g. to fetch a webpage).
2. The **server** receives the request, processes it (often by querying a database), and generates a response.
3. The **client** receives and renders the response, such as displaying a webpage or JSON data.

Each request is treated independently unless session management strategies are used.

<figure><img src="../../../.gitbook/assets/image (40).png" alt=""><figcaption><p>Clients sends requests to the server. The server processes the requests and returns a response, often involving business logic or database access.</p></figcaption></figure>

### Key features and benefits

#### Separation of concerns

* **Client-side**: Manages user interface and interactivity.
* **Server-side**: Handles business logic, data access, and authentication.\
  This separation allows developers to work independently on each part, improving maintainability and scalability.

#### Security

Sensitive operations such as login authentication, payment processing, or database queries occur on the server, which is not exposed to the client.

#### Scalability

Multiple clients can interact with the same server simultaneously. Load balancers and replicated servers can help manage growing demand.

### Real-world example

A student logs into an online learning platform:

* The browser sends a login request with the student’s credentials.
* The server checks the credentials and creates a session.
* The server returns a personalised dashboard page.
* The client renders the dashboard in the browser.

Each step is part of the request-response cycle defined by the client-server model.

### Summary

The client-server model is the cornerstone of web architecture. It allows clients to request resources and services from servers, which respond with content, actions, or data. This model promotes modularity, scalability, and security, and forms the foundation for full-stack development in both front-end and back-end roles.
