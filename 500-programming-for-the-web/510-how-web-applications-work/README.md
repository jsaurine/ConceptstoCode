---
description: Understanding the foundation of web-based systems and data exchange
---

# 510 How web applications work

This chapter explores the fundamental principles of web applications, focusing on how they function, communicate, and deliver content to users. It introduces the client-server model, the role of web browsers, and how data is transmitted across the internet. Understanding these concepts provides the groundwork for developing and optimising modern web applications.

{% tabs %}
{% tab title="TARGETS" %}
By the end of this chapter, students will be able to:

• Explain how web applications operate within a client-server model.

• Describe how web browsers interpret and display web content.

• Understand the process of data exchange between clients and servers.

• Identify key components of web communication, including HTTP, protocols, and APIs.

• Recognise how different web architectures impact performance and scalability.
{% endtab %}

{% tab title="SYLLABUS" %}
New South Wales Education Standards Authority. (2022). _Software Engineering 11–12 Syllabus_. NSW Curriculum. [https://curriculum.nsw.edu.au/learning-areas/tas/software-engineering-11-12-2022](https://curriculum.nsw.edu.au/learning-areas/tas/software-engineering-11-12-2022/overview)

### [**Programming for the web / Designing web applications**](https://curriculum.nsw.edu.au/learning-areas/tas/software-engineering-11-12-2022/content/year-12/fa6aab137e#cg-b41eaf65-d44a-4db3-916a-99bd3594651c)

* Investigate and explain the role of the World Wide Web Consortium (W3C) in the development of applications for the web, including:
  * Web Accessibility Initiative (WAI)
  * internationalisation
  * web security
  * privacy
  * machine-readable data
* Model elements that form a web development system Including:
  * client-side (front-end) web programming
  * server-side (back-end) web programming
  * interfacing with databases that are based on Structured Query Language (SQL) or non-SQL
* Explore and explain the influence of a web browser on web development, including the use of developer (dev) tools
*   Investigate cascading style sheets (CSS) and its impact on the design of a web application

    Including:

    * consistency of appearance
    * flexibility with browsers or display devices
    * CSS maintenance tools
* Investigate the reasons for version control and apply it when developing web application
*   Explore the types and significance of code libraries for front-end web development

    Including:

    * frameworks that control complex web applications
    * template engines
    * predesigned CSS classes
* Explain the use and development of open-source software in relation to web development
* Investigate methods to support and manage the load times of web pages/applications
{% endtab %}

{% tab title="GLOSSARY" %}
* **Client-Server Model**\
  A distributed system where clients request services or resources from a central server.
* **Web Browser**\
  A software application that interprets HTML, CSS, and JavaScript to display web content.
* **HTTP (Hypertext Transfer Protocol)**\
  A protocol used for transmitting web pages and data between clients and servers.
* **API (Application Programming Interface)**\
  A set of rules that allows web applications to communicate with external services.
* **Web Hosting**\
  The service of storing and serving web pages on internet-connected servers.
* **Frontend and Backend**\
  The front-end refers to the visible user interface, while the backend handles data processing and server logic.
{% endtab %}

{% tab title="RESOURCES" %}
TBA
{% endtab %}
{% endtabs %}

### Overview

Web applications function by enabling communication between clients and servers over the internet. A typical web application consists of a front-end, which users interact with through a web browser, and a back-end, which processes requests, manages data, and delivers responses. This interaction follows the client-server model, where the browser (client) requests web pages, data, or resources from a web server, which then processes the request and returns the appropriate content. This exchange relies on protocols such as HTTP and HTTPS, ensuring secure and structured communication between systems.

Beyond basic page rendering, web applications rely on APIs to fetch and exchange data dynamically, allowing them to integrate with external services like databases, authentication systems, and cloud storage. Different architectures, such as monolithic and microservices-based designs, influence how scalable and maintainable a web application is. Understanding the mechanics of web applications—from how a request flows through a network to how a browser interprets and renders content—is essential for building efficient, interactive, and reliable digital experiences.



