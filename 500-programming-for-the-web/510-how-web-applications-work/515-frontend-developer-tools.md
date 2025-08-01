---
description: >-
  Explore the browser developer tools used by front-end developers to build,
  debug, and optimise web applications
---

# 515 Frontend developer tools

### TL;DR

Front-end developer tools streamline the process of designing, developing, debugging, and optimising web applications. Modern web development relies on browsers’ built-in developer tools, version control systems, code editors, and frameworks that enhance productivity. Debugging tools help identify and resolve performance issues, while package managers and build tools automate workflows. Understanding how to effectively use these tools is essential for creating efficient, scalable, and maintainable front-end applications.

***

### Targets

In this section, you will learn to

* Identify key front-end development tools and their purpose.
* Use browser developer tools to inspect and debug web applications.
* Understand the role of version control systems such as Git.
* Explain the benefits of code editors and Integrated Development Environments (IDEs).
* Evaluate the role of front-end frameworks and libraries in modern web development.

***

### Developer tools

Web browsers provide built-in tools that allow developers to inspect and troubleshoot how web pages are loaded and displayed. These developer tools (DevTools) provide insights into network requests, page elements, scripts, and performance metrics. Using these tools, we can observe how a browser (client) interacts with a server, analyze the flow of HTTP requests and responses, and diagnose potential issues in web applications.

One of the most valuable features in developer tools is the Network tab, which logs all requests made when loading a webpage. By inspecting these requests, we can see how files are fetched, how long they take to load, and whether any errors occur. Understanding how to use these tools is essential for debugging and optimising websites.

Once you have opened DevTools, go to the Network tab. Here, you will see a list of requests the browser makes when loading a webpage. Each request contains valuable resource type, status, and load time information.

**Understanding the Network tab**

Key components in the Network tab:

* **Name**\
  The requested resource (e.g., HTML, CSS, JavaScript, images, fonts).
* **Status**\
  The HTTP status code (e.g., 200 OK, 404 Not Found, 500 Server Error).
* **Type**\
  The kind of file requested (e.g., document, script, stylesheet, image).
* **Initiator**\
  The script or file that triggered the request.
* **Size**\
  The amount of data transferred for the request.
* **Time**\
  How long did the request take to complete?

**Inspecting a web request**

To see how a webpage is loaded, follow these steps:

1. Open Developer Tools in your browser and select the Network tab.
2. Refresh the page (or press Ctrl + R / Cmd + R). This reloads the website and logs all requests made.
3. Look for the main HTML request (usually the first request in the list). Click on it.
4. In the Headers tab, examine the following:\
   Request URL – The web address of the request.\
   Request Method – The HTTP method (GET, POST, etc.).\
   Response Headers – Information from the server about the request.
5. In the Response tab, view the content returned by the server. If it's an HTML page, you can see the actual page structure.

**Monitoring Real-Time Requests**

Some web pages continue making requests after the page loads. These requests might be for:

* Fetching new data (e.g., live scores, stock prices, chat messages).
* Loading additional resources dynamically (e.g., images, scripts).
* Sending form data to a server (POST requests).

To monitor real-time requests:

* Keep the Network tab open.
* Perform an action on the page (e.g., click a button or submit a form).
* Observe any new network activity and inspect what data was sent and received.

**Common HTTP status codes in DevTools**

When analysing network requests, it is helpful to understand HTTP status codes:

<table><thead><tr><th width="164.2578125">Status code</th><th>Meaning</th></tr></thead><tbody><tr><td>200 OK</td><td>The request was successful, and the server retruned the requested resource.</td></tr><tr><td><strong>301 Moved Permanently</strong></td><td>The requested resource has been permanently removed.</td></tr><tr><td><strong>404 Not Found</strong></td><td>The requested resource does not exist on the server</td></tr><tr><td><strong>500 Internal Server Error</strong></td><td>The server encountered an error and could not process the request.</td></tr></tbody></table>

***

### Key Concepts

> * **Browser developer tools**\
>   Built-in tools for debugging, inspecting, and optimising web pages (e.g., Chrome DevTools).
> * **Version Control Systems (VCS)**\
>   Tools like Git for managing code changes, collaboration, and tracking history.
> * **Code editors and IDEs**\
>   Environments like VS Code and WebStorm that provide enhanced development features.
