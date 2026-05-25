# 3.3 IP Addressing

An IP Address (Internet Protocol Address) is a unique numerical label assigned to each device connected to a computer network that uses the Internet Protocol for communication. It serves two main purposes:

1. Identifying a device on the network.
2. Locating the device to enable communication with other devices over a network like the Internet.

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20250930173418973038/ip_addresses.webp" alt="ip_addresses" height="400" width="800"><figcaption><p>IP Address</p></figcaption></figure>

{% hint style="info" %}
In simple terms, an IP address acts like a digital home address, allowing data to be sent and received between devices correctly.
{% endhint %}

### Components of an IP Address <a href="#components-of-an-ip-address" id="components-of-an-ip-address"></a>

1. **Network Portion:** Identifies the network to which the device belongs.
2. **Host Portion:** Identifies the individual device on the network.
3. **Subnet Mask (for IPv4):** Defines which part of the IP is network and which part is host.

{% hint style="success" %}
**Example:**&#x20;

IP <kbd>192.168.1.10</kbd> with subnet mask <kbd>255.255.255.0</kbd>\
**Network ID:** 192.168.1.0\
**Host ID**: 10
{% endhint %}

### Types of IP Address <a href="#types-of-ip-address" id="types-of-ip-address"></a>

IP addresses can be classified in several ways based on their structure, purpose, and the type of network they are used in. Here's a breakdown of the different classifications of IP addresses:

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20250930173504982495/types_of_ip_address.webp" alt="types_of_ip_address" height="400" width="800"><figcaption><p>Types of IP Address</p></figcaption></figure>

### 1. Based on Addressing Scope (IPv4 vs. IPv6) <a href="#id-1-based-on-addressing-scheme-ipv4-vs-ipv6" id="id-1-based-on-addressing-scheme-ipv4-vs-ipv6"></a>

#### 1.1 Public IP Addresses <a href="#public-ip-addresses-1" id="public-ip-addresses-1"></a>

A Public IP address is assigned to every device that directly accesses the internet. This address is unique across the entire internet. Uniqueness & Accessibility are its key characteristics & are assigned by Internet Service Providers. When you connect to the internet through an ISP, your device or router receives a public IP address. These addresses can be static or dynamic.

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20241217170342121691/Private-_-Public-Address.webp" alt="Private-_-Public-Address" height="400" width="800"><figcaption><p>Public v/s Private IP Address</p></figcaption></figure>

{% hint style="success" %}
**Example Use:**&#x20;

If you host a website on your own server at home, your ISP must assign a public IP address to your server so users around the world can access your site.
{% endhint %}

#### 1.2 Private IP Addresses <a href="#private-ip-addresses" id="private-ip-addresses"></a>

Private IP addresses are used within private networks and are not routable on the internet. This means that devices with private IP addresses cannot directly communicate with devices on the internet without a translating mechanism like a router performing Network Address Translation (NAT). These are only required to be unique within their own network & are used for communication between devices within the same network

* **Defined ranges for IPv4:** 10.0.0.0 to 10.255.255.255, 172.16.0.0 to 172.31.255.255, 192.168.0.0 to 192.168.255.255
* **Defined ranges for IPv6:** Addresses starting with FD or FC

{% hint style="success" %}
**Example Use:**

In a typical home network, the router assigns private IP addresses to each device (like smartphones, laptops, smart TVs) from the reserved ranges. These devices use their private IPs to communicate with each other and with the router. The router uses NAT to allow these devices to access the internet using its public IP address.
{% endhint %}

### 2. Based on IP Version <a href="#id-2-based-on-ip-version" id="id-2-based-on-ip-version"></a>

#### 2.1 IPv4 <a href="#ipv4-1" id="ipv4-1"></a>

This is the most common form of IP Address. It consists of four sets of numbers(octets) separated by dots. This format can support over 4 billion unique addresses. Each octet represents eight bits, or a byte, and can take a value from 0 to 255. This range is derived from the possible combinations of eight bits (2<sup>8</sup> = 256 combinations).

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20241217170153436945/IPv4-address-format.webp" alt="IPv4-address-format" height="350" width="800"><figcaption><p>IPv4 Address Format</p></figcaption></figure>

{% hint style="success" %}
**Example of IPv4 Address**: <kbd>192.168.1.1</kbd>

* 192 is the first octet
* 168 is the second octet
* 1 is the third octet
* 1 is the fourth octet
{% endhint %}

{% hint style="info" %}
Each part of the IP address can indicate various aspects of the network configuration, from the network itself to the specific device within that network.
{% endhint %}

#### 2.2 IPv6: <a href="#id-22-ipv6" id="id-22-ipv6"></a>

IPv6 addresses were created to deal with the shortage of IPv4 addresses. They use 128 bits instead of 32, offering a vastly greater number of possible addresses. These addresses are expressed as eight groups of four hexadecimal digits, each group representing 16 bits. The groups are separated by colons.

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20241125171150513292/ipv6---------address.webp" alt="ipv6---------address" height="400" width="800"><figcaption><p>IPv6 Address Format</p></figcaption></figure>

{% hint style="success" %}
**Example of IPv6 Address**: <kbd>2001:0db8:85a3:0000:0000:8a2e:0370:7334</kbd>&#x20;

Each group (like 2001, 0db8, 85a3, etc.) represents a 16-bit block of the address.
{% endhint %}

### 3. Based on Assignment <a href="#id-3-based-on-assignment" id="id-3-based-on-assignment"></a>

#### 3.1 Static IP Addresses <a href="#static-ip-addresses" id="static-ip-addresses"></a>

* Static IP Addresses are permanently assigned to a device, typically important for servers or devices that need a constant address.
* Reliable for network services that require regular access such as websites, remote management.

#### 3.2 Dynamic IP Addresses: <a href="#dynamic-ip-addresses" id="dynamic-ip-addresses"></a>

* Temporarily assigned from a pool of available addresses by the Dynamic Host Configuration Protocol (DHCP).
* Cost-effective and efficient for providers, perfect for consumer devices that do not require permanent addresses.

### 4. Based on Function <a href="#id-4-based-on-function" id="id-4-based-on-function"></a>

#### **4.1. Unicast Address** <a href="#id-1-unicast-address" id="id-1-unicast-address"></a>

In unicast, data is sent from one sender to one specific receiver identified by a unique IP address. It is the most common type of communication used in networks. Its Purpose is One-to-one communication.

{% hint style="success" %}
**Example:**&#x20;

Sending an email or loading a webpage - your computer directly communicates with a specific server.

**Use Case:** Regular web browsing, file transfers (FTP), email (SMTP), etc.
{% endhint %}

#### 4. 2. Broadcast Address <a href="#id-2-broadcast-address" id="id-2-broadcast-address"></a>

In broadcast, a message is sent from one device to all devices in the same network segment. Every device in the network receives and processes the broadcast message. Its Purpose is One-to-all communication within a network.

{% hint style="success" %}
**Example:**&#x20;

An ARP (Address Resolution Protocol) request uses broadcasting to find a device’s MAC address on the local network.

**Use Case:** Network discovery, DHCP requests, ARP queries
{% endhint %}

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20241015172245941827/Difference-Between-Unicast-Multicast-and-Broadcast.png" alt="Difference-Between-Unicast-Multicast-and-Broadcast" height="400" width="800"><figcaption><p>Unicast v/s Multicast v/s Broadcast</p></figcaption></figure>

{% hint style="info" %}
Broadcast communication is supported in IPv4, but not in IPv6 (IPv6 replaces it with multicast).
{% endhint %}

#### 4. 3. Multicast Address <a href="#id-3-multicast-address" id="id-3-multicast-address"></a>

In multicast, data is sent from one source to multiple selected receivers that are part of a multicast group. Only devices that have joined the group will receive the data, making it more efficient than broadcasting. Its Purpose is One-to-many (selected group) communication.

{% hint style="success" %}
**Example:**&#x20;

Streaming live video or online conferencing to a group of users.

**Use Case:** IPTV, video conferencing, live streaming

**IPv4 Range:**<kbd>224.0.0.0</kbd> to <kbd>239.255.255.255</kbd>

**IPv6 Prefix:** <kbd>FF00::/8</kbd>
{% endhint %}

#### 4.4. Anycast Address <a href="#id-44-anycast-address" id="id-44-anycast-address"></a>

In anycast, data is sent from one sender to the nearest receiver (in terms of network distance) among a group of devices sharing the same IP address. Routers determine the closest destination dynamically. Its Purpose is One-to-nearest communication (based on routing distance).

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20231024103350/Anycast.png" alt="Anycast" height="395" width="430"><figcaption><p>Anycast</p></figcaption></figure>

{% hint style="success" %}
**Example:**&#x20;

Content Delivery Networks (CDNs) use anycast to route user requests to the nearest data center.

**Use Case:** DNS servers, CDN routing, load balancing
{% endhint %}

{% hint style="info" %}
_Anycast_ is primarily used in IPv6, but it can also be implemented in IPv4.
{% endhint %}

### Special IP Addresses <a href="#special-ip-addresses" id="special-ip-addresses"></a>

There are also some special-purpose IP addresses that don't follow the usual structure:

* **Loopback Address**: The loopback address `127.0.0.1` is used to test network connectivity within the same device (i.e., sending data to yourself). Often called "`localhost`."
* **Broadcast Address**: The broadcast address allows data to be sent to all devices in a network. For a typical network with the IP range `192.168.1.0/24`, the broadcast address would be `192.168.1.255`.
* **Multicast Address**: Used to send data to a group of devices (multicast). For example, `233.0.0.1` is a multicast address.

{% hint style="info" %}
### IP Networking Summary <a href="#how-do-ip-addresses-work" id="how-do-ip-addresses-work"></a>

An IP address (Internet Protocol address) serves as a unique identifier for every device connected to a network, enabling communication and data exchange across local and global networks. The Internet Protocol governs how data is packaged, addressed, transmitted, routed, and received.

#### 1. Unique Identification <a href="#id-1-unique-identification" id="id-1-unique-identification"></a>

* Every device-such as a computer, smartphone, or server-connected to a network is assigned an IP address.
* This address acts like a digital home address, allowing the device to be uniquely identified within the network.
* Without an IP address, a device cannot send or receive data on the network.

#### 2. Communication Protocol <a href="#id-2-communication-protocol" id="id-2-communication-protocol"></a>

The Internet Protocol (IP) defines how data is transmitted between devices. When data is sent over a network, it is divided into smaller units called packets. Each packet contains:

* The source IP address (the sender’s device)
* The destination IP address (the receiver’s device)

{% hint style="warning" %}
Routers and switches use these addresses to ensure that each packet reaches its correct destination.
{% endhint %}

#### 3. [Data Routing](../3.5-routing-tables-and-subnet-matching/) <a href="#id-3-data-routing" id="id-3-data-routing"></a>

When a device sends data to another device on the internet, the following steps occur:

1. The data is divided into packets.
2. Each packet includes the IP address of its destination.
3. Routers examine the destination IP on each packet and determine the best route to forward it.
4. Routers communicate with each other to update routing tables and maintain the most efficient paths for data transmission.

{% hint style="warning" %}
This process ensures that packets may take different routes but ultimately arrive at the correct destination, where they are reassembled.
{% endhint %}

#### 4. LAN and WAN Communication <a href="#id-4-lan-and-wan-communication" id="id-4-lan-and-wan-communication"></a>

* **Local Area Network (LAN):** Within a local network, IP addresses can be assigned statically (manually) or dynamically using DHCP (Dynamic Host Configuration Protocol). Devices within the same LAN can communicate directly using private IP addresses.
* **Wide Area Network (WAN):** When communicating across different networks, data travels through multiple routers over the internet. Each router independently decides the next hop based on the destination IP address to ensure optimal routing.

#### 5. Network Address Translation (NAT) <a href="#id-5-network-address-translation-nat" id="id-5-network-address-translation-nat"></a>

* NAT (Network Address Translation) allows multiple devices in a private network to share a single public IP address when accessing the internet.
* Inside the local network, devices use private IPs (e.g., 192.168.x.x).
* The router translates these private IPs into a public IP for outbound communication.

{% hint style="warning" %}
NAT helps conserve the limited number of public IPs and provides an additional security layer by hiding internal network structures from the outside world.
{% endhint %}
{% endhint %}

<details>

<summary>IP Address Security Threats</summary>

IP addresses are essential for connecting devices on the internet, but they also come with various security risks. Understanding these threats can help you protect your network and personal information more effectively. Some common IP address security threats are:

1. **IP Spoofing:** Attackers fake a trusted IP address to bypass security and gain unauthorized access.
2. **DDoS Attacks:** Multiple infected systems flood a target with traffic, causing slowdowns or crashes.
3. **Man-in-the-Middle (MitM):** Hackers intercept or alter data between two parties to steal sensitive information.
4. **Port Scanning:** Attackers scan for open ports to find vulnerabilities and exploit system weaknesses.

{% hint style="info" %}
Protecting against these threats requires strong network security, monitoring, and regular system updates.
{% endhint %}

</details>

<details>

<summary>How to Protect and Hide Your IP Address</summary>



* **Use a VPN (Virtual Private Network)**: A VPN hides your real IP address by routing your internet traffic through a secure VPN server. This masks your identity, encrypts your data, and prevents websites or attackers from tracking your location or online activities.
* **Use a Proxy Server**: A proxy server acts as an intermediary between your device and the internet. When you send a request, it goes through the proxy, which substitutes its own IP address for yours, helping to conceal your real identity.
* **Use the Tor Browser**: The Tor network routes your data through multiple volunteer-run servers (nodes), encrypting it at every layer. This makes it extremely difficult for anyone to trace your IP address or monitor your browsing activity.
* **Enable a Firewall**: A firewall monitors and filters incoming and outgoing network traffic. It blocks suspicious or unauthorized connections, reducing the risk of hackers targeting your device via your IP address.

</details>

