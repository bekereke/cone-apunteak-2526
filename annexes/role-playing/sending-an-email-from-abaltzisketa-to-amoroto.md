# Sending an Email from Abaltzisketa to Amoroto

> Let's explore how IP addresses work through a real-world example that involves sending an email from one person to another across the globe:

#### Step 1: Assigning IP Addresses <a href="#step-1-assigning-ip-addresses" id="step-1-assigning-ip-addresses"></a>

* Alice in Abaltzisketa has a laptop with a private IP, e.g., 192.168.1.5, assigned by her home router.
* Bob in Amoroto has a computer with a private IP, e.g., 192.168.2.4, assigned by his office router

#### Step 2: Connecting to the Internet <a href="#step-2-connecting-to-the-internet" id="step-2-connecting-to-the-internet"></a>

* Both routers have public IP addresses provided by their ISPs (Internet Service Providers).
* These public IPs are used for all communications over the internet.

#### Step 3: Sending the Email <a href="#step-3-sending-the-email" id="step-3-sending-the-email"></a>

* Alice composes an email and clicks "Send."
* Her email client (e.g., Gmail or Outlook) converts the email into data packets that contain: Source IP -> Alice’s public IP (her router’s address) & Destination IP -> Bob’s mail server’s public IP

#### Step 4: Routing the Packets <a href="#step-4-routing-the-packets" id="step-4-routing-the-packets"></a>

* The packets move from Alice’s laptop to her router.
* The router detects that the destination IP is external and forwards the packets to Alice’s ISP.
* The ISP’s routers analyze the destination IP and determine the optimal route.
* Packets travel across several intermediate routers -perhaps through data centers in North America, Europe, and Asia -before reaching Viscay.

#### Step 5: Reaching Bob <a href="#step-5-reaching-bob" id="step-5-reaching-bob"></a>

* The packets arrive at Bob’s email server’s ISP in Amoroto.
* The server’s router forwards them to Bob’s email server.
* The server reassembles the packets into the original email message.

#### Step 6: Email Retrieval <a href="#step-6-email-retrieval" id="step-6-email-retrieval"></a>

* Bob’s computer requests the email from the server using his local IP.
* The server sends the email to Bob’s device, completing the communication.

{% hint style="danger" %}
**Note:**&#x20;

This illustrates the fundamental role of IP addresses and the complex network of routers involved in even the simplest internet activities like sending an email. Each part of the process depends on the IP address to ensure that data finds its way correctly from sender to receiver, no matter where they are in the world.
{% endhint %}
