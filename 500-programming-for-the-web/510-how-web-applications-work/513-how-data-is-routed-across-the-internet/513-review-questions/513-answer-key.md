# 513 / Answer key

### Question 1

The primary role of a router in Internet data transmission is

* [ ] A. storing frequently accessed web wages for faster loading.
* [x] B. directing packets between different networks to their destination.
* [ ] C. converting domain names into IP addresses.
* [ ] D. managing encryption for secure communication.

### Question 2

Which protocol determines the best path for data packets across the Internet?

* [ ] A. HTTP
* [ ] B. FTP
* [x] C. TCP/IP
* [ ] D. DNS

### Question 3

If a data packet cannot reach its destination, it is

* [ ] A. automatically stored in the router’s nearest cache.
* [ ] B. redirected back to the sender immediately.
* [x] C. discarded, and an error message is sent back to the sender.
* [ ] D. converted into a broadcast signal for other networks to pick up.

### Question 4

What information is contained in the header of a data packet?

* [ ] A. the full contents of the transmitted file
* [x] B. the sender and receiver IP addresses and packet sequence number
* [ ] C. the domain name of the website being accessed
* [ ] D. a log of all previous network hops the packet has taken&#x20;

### Question 5

Which device assigns a local IP address to home or business network devices?

* [x] A. DHCP server
* [ ] B. modem
* [ ] C. DNS server
* [ ] D. firewall

### Question 6 (3 marks)

Describe the function of IP addresses in Internet data transfer.

<details>

<summary>See answer</summary>

* An IP address is a unique identifier assigned to each device on a network. It allows data packets to be correctly routed from the sender to the recipient across the internet.&#x20;
* The source IP address indicates where the packet originated, while the destination IP address ensures it reaches the correct device.

</details>

### Question 7 (3 marks)

What is DNS's purpose in routing data across the internet, and how does it function?

<details>

<summary>See answer</summary>

* The DNS (Domain Name System) translates human-readable domain names (e.g., example.com) into IP addresses that computers use to route data.
* When a user enters a web address, the browser sends a DNS query to a DNS server, which returns the corresponding IP address.
* This allows the request to be routed to the correct web server, enabling access to the requested website or online service.

</details>

### Question 9 (4 marks)

Describe how data packets travel from a sender to a recipient using routers, IP addresses, and packet switching.

<details>

<summary>See answer</summary>

* The sender’s device breaks the data into packets containing a destination IP address and a packet sequence number.
* The packets travel through a router, which forwards them based on the best available network path determined by routing protocols.
* The packets may take different paths to the destination (packet switching), passing through multiple routers and network nodes.
* At the recipient’s device, the packets are reassembled in the correct order using their sequence numbers to reconstruct the original data.

</details>
