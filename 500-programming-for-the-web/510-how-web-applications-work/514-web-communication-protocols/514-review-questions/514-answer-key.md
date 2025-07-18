---
hidden: true
---

# 514 / Answer key

### Question 1

The primary purpose of HTTP in web communication is

* [ ] A. encrypting web content before it is displayed.
* [ ] B. converting domain names to IP addresses.
* [x] C. transferring data between a web client and a web server.
* [ ] D. managing user authentication and authorisation.&#x20;

### **Question 2**

The key difference between HTTP and HTTPS is that

* [ ] A. HTTPS does not use a web server.
* [ ] B. HTTP uses TCP, but HTTPS uses FTP.
* [x] C. HTTPS encrypts data using SSL/TLS, while HTTP does not.
* [ ] D. HTTP supports media streaming, while HTTPS does not.

### Question 3

Which protocol is typically used to secure communication between web clients and servers?

* [ ] A. FTP
* [ ] B. HTTP
* [ ] C. TCP
* [x] D. HTTPS

### Question 4

What role does TCP play in web communication?

* [ ] A. It identifies the location of the requested resource.
* [x] B. It establishes a reliable connection and ensures data arrives in order.
* [ ] C. It encrypts content at the application layer.
* [ ] D. It hosts websites and serves files to users.&#x20;

### Question 5

Port 443 typically indicates that

* [ ] A. the server is hosting FTP content.
* [x] B. HTTPS is being used for secure communication.
* [ ] C. the website is down or unavailable.
* [ ] D. the DNS lookup failed.

### Question 6 (3 marks)

Define the role of SSL/TLS in web communication.

<details>

<summary>See answer</summary>

SSL (Secure Sockets Layer) and TLS (Transport Layer Security) are cryptographic protocols used to encrypt data sent between a client and server. They ensure that information such as login credentials or payment details is secure from eavesdropping or tampering during transmission. TLS is the modern, more secure successor to SSL.

</details>

### Question 7 (3 marks)

What are protocols and why are they essential in web communication? Provide two examples relevant to web development.

<details>

<summary>See answer</summary>

Protocols are agreed-upon rules that define how data is formatted, transmitted, and received over networks. They ensure that devices and software can communicate reliably and consistently, regardless of differences in hardware or location.

Examples:

* **HTTP/HTTPS**\
  Used to request and deliver web content between browsers and servers.
* **TCP/IP**\
  Ensures reliable delivery and routing of data packets across the internet.

</details>

### Question 9 (4 marks)

Describe how a typical HTTP request is processed from the time a user enters a URL in the browser.

<details>

<summary>See answer</summary>

1. The browser sends a DNS request to resolve the domain name into an IP address.
2. It initiates a TCP connection with the web server over port 80, which is the default for HTTP.
3. Once connected, the browser sends a plain-text HTTP request (e.g., a GET request for a webpage or resource).
4. The server processes the request and sends back an HTTP response, which includes a status code, headers, and the requested content (such as HTML, CSS, or JavaScript).
5. The browser receives the response and renders the webpage for the user.

</details>
