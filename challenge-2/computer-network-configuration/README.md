---
description: INTRODUCTION TO LOGICAL NETWORK INSTALLATION AND ADDRESSING
icon: '3'
cover: ../../.gitbook/assets/3cone.png
coverY: 0
coverHeight: 217
---

# Computer Network Configuration

In the first challenge, we explored the main characteristics of a Local Area Network (LAN), as well as the physical foundation required to set up a network. We began by defining what a LAN is and its purpose—to share information and devices—and analyzed the main network [**topologies**](../../challenge-1/networking-features-and-interconnection-elements/1.2-computer-network-topologies.md): Star topology, Ring topology, and Bus topology. We also examined [**transmission modes**](../../challenge-1/networking-features-and-interconnection-elements/1.5-transmission-modes.md) (Simplex, Half Duplex, and Full Duplex) and covered broader [**network categories**](../../challenge-1/networking-features-and-interconnection-elements/1.1-computer-network-categories.md) (LAN, WAN, WLAN, MAN, PAN, WMAN, WWAN).

Furthermore, we addressed the physical network installation, utilizing the term [**structured cabling**](../../challenge-1/deploying-ethernet-cabling/2.3-structured-cabling.md). We studied the essential components needed to assemble networks, such as cable types (twisted pair/UTP, fiber optic), connectors (RJ-45), and intermediary devices (switches and routers). We established that the primary goals of structured cabling are **flexibility and security**, and outlined the steps necessary for a network installation, including installing outlets, routing cables through conduits, placing connectors (RJ-45 male and female), and setting up the communication cabinet/rack with a **patch panel**.

***

#### **Challenge2: Transitioning to Logical Network Installation**

Now, in the second challenge, we shift from the physical foundation to the **logical network installation**. Simply connecting components physically is not enough to manage a network; devices require a set of rules and protocols to understand each other.

To manage the complexity of communication, tasks are divided into different layers or levels. There are two main models: the **OSI reference model** (7 layers), used primarily as a reference, and the **TCP/IP model** (4 layers), which is the model used in practice.

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20230417045622/OSI-vs-TCP-vs-Hybrid-2.webp" alt=""><figcaption></figcaption></figure>

In this second challenge, <mark style="color:$info;background-color:purple;">we will delve into the methods for identifying network devices and the network models, focusing specifically on the foundational layers, particularly corresponding to the first three layers of the OSI model and their equivalents in the TCP/IP model:</mark>

1.  **Data Link Layer (OSI Layer 2) / Network Access Layer (TCP/IP Layer 1):** [**MAC Addressing**](3.2-mac-addressing/)

    This layer is responsible for ensuring bits are successfully transmitted as blocks (called frames) from one end of the cable to the other, and checking for errors.

    The most critical concept at this level for device identification is the **MAC address** (_Media Access Control_, also known as the **physical address**). The MAC address is a unique identifier consisting of 48 bits, typically expressed in hexadecimal format, which is permanently engraved on each network card by the manufacturer. The **MAC address** is essential for two computers on the **same network** to communicate.
2.  **Network Layer (OSI Layer 3) / Internet Layer (TCP/IP Layer 2):** [**IP Addressing**](3.3-ip-addressing/)

    The main responsibility of the **Network Layer** is determining how information (segmented into packets) should be **routed**. This means managing the path the information must follow across the network. The most commonly used protocol at this layer is the **IP protocol** (Internet Protocol).

    **IP addresses** are used to identify devices residing on **different networks**. Unlike MAC addresses (which are fixed from the factory), the **IP address** must be manually configured (or automatically assigned via DHCP). IPv4 addresses are composed of four numbers ranging between 0 and 255. <mark style="background-color:purple;">To logically locate a device within a network, the</mark> <mark style="background-color:purple;"></mark><mark style="background-color:purple;">**subnet mask**</mark> <mark style="background-color:purple;"></mark><mark style="background-color:purple;">must be specified along with the IP address, which indicates which part of the IP address defines the subnet.</mark> Choosing the size of the net or the number of subnets needed is the key for [**subnetting**](3.4-subnetting/).&#x20;

In summary, having understood the physical bases and cabling systems in the first challenge, this second challenge focuses on the logical network installation and the fundamental addressing systems required for data transfer: **MAC addresses (within the same network) and IP addresses (across different networks)**. We will also examine the need for routing devices (routers) and how [**routing tables**](3.5-routing-tables-and-subnet-matching/) are managed.

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20250503155335598874/tcp_ip-2.webp" alt=""><figcaption><p>TCP/IP</p></figcaption></figure>
