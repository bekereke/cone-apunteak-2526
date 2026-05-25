---
description: Next-hop
---

# 3.5 Routing Tables and Subnet Matching

IP routing is the process that defines the shortest path through which data travels to reach from source to destination. It determines the shortest path to send the data from one computer to another computer in the same or different network. Routing uses different protocols for the different networks to find the path that data follows. <mark style="background-color:purple;">It defines the path through which</mark> <mark style="background-color:purple;"></mark><mark style="background-color:purple;">**data travel across multiple networks**</mark> <mark style="background-color:purple;"></mark><mark style="background-color:purple;">from one computer to others.</mark> Forwarding the packets from source to destination via different routers is called routing. The routing decision is taken by the routers.&#x20;

{% hint style="info" %}
**Subnet Matching**  is essential to ensure packets traveling through the network get to the right place. Each IP address class has a matching “subnet mask,” which is an easy way of identifying which part of the IP address relates to the network and which part relates to the host. So, a destination host address arrives to the router on its packet and first thing to do is to calculate its network ID (address): that is subnet matching!
{% endhint %}

For taking routing decisions router needs various routing protocols and a [routing table](./#routing-tables).

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20250130101048547375/IP-Routing.webp" alt="IP-Routing" height="401" width="801"><figcaption><p>IP Routing</p></figcaption></figure>

{% hint style="warning" %}
_Clarification on Metaphor:_ Routing tables function like a city’s map guide, but specifically for postal carriers (packets). They look up the destination city (network ID), find the optimal highway (next hop IP), and know which ramp (interface) to take, ensuring the mail reaches the correct region, even if the final street address (host ID) is too specific for the map itself.
{% endhint %}

### Importance of IP Routing

IP routing is important because it helps data travel from one device to another across different networks, like from your home network to the internet. It makes sure the data takes the quickest and most efficient route, which helps everything work faster. If one path stops working, IP routing automatically finds another way to send the data, keeping things running smoothly. It also helps manage network traffic so things don't get too crowded, and it prioritizes important data like voice or video calls to keep them clear.

### Types of Routing

There are three different types of routing:

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20250130101626137701/Types-of-Routing.jpg" alt="Types-of-Routing" height="190" width="541"><figcaption><p>Types of Routing</p></figcaption></figure>

1. **Static Routing:** It is also known as **nonadaptive routing.** In this type of routing the routing table is updated by the network administrator manually and routing decisions are not based on topology or condition of network.
2. **Dynamic Routing:** It is also known as **adaptive routing**. In this type of routing the routing table is automatically updated using routing protocols. In response to changes in condition or topology of network, router adds a new route in the routing table.
3. **Default Routing:** In this type of routing the router is configured to send all the data towards a specific router. The default route is chosen only when specific route is not mentioned in the routing table. This routing is generally used with the stub routers. &#x20;

### How does IP Routing Work

When the data is sent from the source to the destination the TCP and other protocols of the source work and form an IP packet that is sent to the network. When an IP packet is sent to the network from the source it has to pass through multiple routers to reach the destination. The router in the network gets the destination address from the packet and through its routing table identifies the next router information to which the data packet has to be passed. The routing table of the router includes various information about the next router, its cost, and other necessary information. The router takes the routing decision with the help of routing protocols and a routing table to which next router the packet has to be sent to find the best route to reach the destination. Different packets can be sent through different paths but all the packets reach their intended destination. When the packets reach the destination through different routers it sends them to the TCP for further processing.

{% hint style="info" %}
### What is "**next-hop" in CISCO routers**?&#x20;

The next-hop mechanism works through a series of technical steps that ensure efficient packet delivery.&#x20;

**Destination IP Address Lookup**&#x20;

When a packet arrives at a router, the router examines the packet’s header to read the destination IP address. This is the starting point for determining where to forward the packet.&#x20;

**Routing Table Match**&#x20;

The router consults its routing table to find an entry that matches the destination IP address. The table entry includes vital information such as the next-hop IP address and the interface through which the packet should be forwarded.&#x20;

**Identifying the Next-Hop IP Address**&#x20;

Using the matched routing table entry, the router identifies the next-hop IP address. This is the address of the router or gateway closer to the destination network.&#x20;

**Forwarding the Packet**&#x20;

Once the next-hop IP address is determined, the router forwards the packet to the appropriate network interface connected to the next-hop device.&#x20;

**Layer 2 Forwarding to the Next Hop**&#x20;

At Layer 2 of the OSI model, the data link layer, the packet is encapsulated in a frame. The router updates the frame’s MAC address to the next-hop device’s MAC address for transmission. The frame is then sent to the next-hop router for further processing.
{% endhint %}

{% hint style="danger" %}
Next-hop feature is belong to either Static Routing or Dynamic Routing?&#x20;
{% endhint %}

### Routing Tables

A Router is a networking device that forwards data packets between computer networks. This device is usually connected to two or more different networks. When a packet arrives at a router, it examines destination IP address of the received packet and makes routing decisions accordingly. Routers use _Routing Tables_ to determine which interface the packet will be sent out. A routing table lists all networks for which routes are known. Each router’s routing table is unique and stored in the RAM of the device.

A routing table is a set of rules, often viewed in table format, that is used to determine where data packets traveling over an Internet Protocol (IP) network will be directed. All IP-enabled devices, including routers and switches, use routing tables. See below a Routing Table:

| **Destination** | Subnet Mask     | Interface |
| --------------- | --------------- | --------- |
| 128.75.43.0     | 255.255.255.0   | Eth0      |
| 128.75.43.0     | 255.255.255.128 | Eth1      |
| 192.12.17.5     | 255.255.255.255 | Eth3      |
| Default         | 0.0.0.0         | Eth2      |

The entry corresponding to the _default_ gateway configuration is a network destination of 0.0.0.0 with a network mask (netmask) of 0.0.0.0. The Subnet Mask of default route is always 0.0.0.0 .

#### **Entries of an IP Routing Table**

A routing table contains the information necessary to forward a packet along the best path toward its destination. Each packet contains information about its origin and destination. Routing Table provides the device with instructions for sending the packet to the next hop on its route across the network. Each entry in the routing table consists of the following entries:

1. **Network ID:** The network ID or destination corresponding to the route.
2. **Subnet Mask:** The mask that is used to match a destination IP address to the network ID.
3. **Next Hop:** The IP address to which the packet is forwarded
4. **Outgoing Interface:** Outgoing interface the packet should go out to reach the destination network.
5. **Metric:** A common use of the metric is to indicate the _minimum number of hops_ (routers crossed) to the network ID.

Routing table entries can be used to store the following types of routes:

* Directly Attached Network IDs
* Remote Network IDs
* Host Routes
* Default Route
* Destination

When a router receives a packet, it examines the destination IP address and looks up into its **Routing Table** to figure out which interface packet will be sent out.

#### **How are Routing Tables Populated?**

There are 3 ways to maintain Routing Table:

* Directly connected networks are added automatically
* Using Static Routing
* Using Dynamic Routing

These Routing tables can be maintained manually or dynamically. In _dynamic routing_, devices build and maintain their routing tables automatically by using routing protocols to exchange information about the surrounding network topology. Dynamic routing tables allow devices to "listen" to the network and respond to occurrences like device failures and network congestion. Tables for _static network devices_ do not change unless a network administrator manually changes them.

### **Route Determination Process (Finding Subnet ID using Routing Table)**

Consider a network is subnetted into 4 subnets as shown in the above picture. The IP Address of the 4 subnets are:

`200.1.2.0 (Subnet a) 200.1.2.64 (Subnet b) 200.1.2.128 (Subnet c) 200.1.2.192 (Subnet d)`

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20190304143543/121121.png" alt=""><figcaption></figcaption></figure>

Then, Routing table maintained by the internal router looks like:

| Destination | Subnet Mask     | Interface |
| ----------- | --------------- | --------- |
| 200.1.2.0   | 255.255.255.192 | a         |
| 200.1.2.64  | 255.255.255.192 | b         |
| 200.1.2.128 | 255.255.255.192 | c         |
| 200.1.2.192 | 255.255.255.192 | d         |
| Default     | 0.0.0.0         | e         |

To find its correct subnet (subnet ID), the router performs the bitwise ANDing of destination IP Address mentioned on the data packet and all the subnet masks one by one.

* If only one match occurs, the router forwards the data packet on the corresponding interface.
* If there are multiple matches, the router forwards the data packet on the interface corresponding to the longest subnet mask.
* If no match occurs, the router forwards the data packet to the interface corresponding to the default entry.
