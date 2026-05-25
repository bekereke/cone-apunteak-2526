---
description: INTRODUCTION TO NETWORKING AND ITS COMPONENTS
icon: '1'
cover: ../../.gitbook/assets/computer_networking_header_1.png
coverY: 0
---

# Networking Features and Interconnection Elements

> Thank goodness for computer networks! If they'd never been invented, you wouldn't be reading this now (using the Internet) and I wouldn't be writing it either (using a wireless home network to link up my computer equipment). There's no doubt that computer networking is extremely complex when you delve into it deeply, but the basic concept of linking up computers so they can talk to one another is pretty simple. Let's take a closer look at how it works!

Networks and communication involve connecting different systems and devices to share data and information. This setup includes hardware like computers, routers, switches, and modems, as well as software protocols that manage how data flows between these devices.

Protocols such as TCP/IP and HTTP are essential for communication between devices. They set the rules for how data is exchanged, ensuring a common connection.

Advancements in technology have led to the creation of complex communication networks, like the Internet. The Internet has transformed how we communicate and access information. It has made it easier for people to connect, work more efficiently, and find information and resources quickly.

### What is A Network?

You can do lots of things with a computer but, connect it up to other computers and peripherals (the general name given to add-on bits of computer equipment such as modems, inkjet and laser printers, and scanners) and you can do an awful lot more. <mark style="background-color:purple;">A computer network is simply a collection of computer equipment that's connected with wires, optical fibers, or wireless links so the various separate devices</mark> (known as nodes) can "talk" to one another and swap data (computerized information).

<details>

<summary>Basic Terminologies of Computer Networks</summary>

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20250730125206711694/network.webp" alt=""><figcaption></figcaption></figure>

* **Network:** A group of connected computers and devices that can communicate and share data with each other.
* **Node:** Any device that can send, receive, or forward data in a network. This includes laptops, mobiles, printers, earbuds, servers, etc.
* **Networking Devices:** Devices that manage and support networking functions. This includes routers, switches, hubs, and access points.
* **Transmission Media:** The physical or wireless medium through which data travels between devices.
* **Wired media:** Ethernet cables, optical fibe&#x72;**.**
* **Wireless media:** Wi-Fi, Bluetooth, infrared
* **Service Provider Networks:** Networks offered by external providers that allow users or organizations to lease network access and capabilities. This includes internet providers, mobile carriers, etc.

</details>

#### Characteristics of Computer Networks <a href="#characteristics-of-computer-networks" id="characteristics-of-computer-networks"></a>

Computer networks are systems that connect multiple devices to facilitate communication, resource sharing, and data transfer. They possess several key characteristics that ensure efficient and secure operations. These characteristics include Security, Reliability, Scalability, Performance, Fault Tolerance, and hardware and software support.

<details>

<summary>Keys</summary>

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20240604163259/Characteristic-of-CN.png" alt="characteristics of Computer Networks" height="488" width="692"><figcaption><p>characteristics of Computer Networks</p></figcaption></figure>

### 1. **Security** <a href="#id-1-security" id="id-1-security"></a>

**Security** is one of the most important characteristics of a computer network. Most businesses nowadays depend on computers, which are accessed by using network. If computer network technology is not secure, then any one can able to access companies data and this in not good for any company, because those who unautharize data can missuse of the data . However, nowadays, computer networking tools primarily provide the highest level of security and prevent any unauthorized access.

Computer networks are vulnerable to [security threats](https://www.geeksforgeeks.org/computer-science-fundamentals/computer-security-threats/) such as hacking, viruses, and data breaches. Security measures such as firewalls, encryption, and user authentication are essential to protect network resources and data.&#x20;

### &#x20;2. **Reliability** <a href="#id-2-reliability" id="id-2-reliability"></a>

Computer networks must be reliable to ensure that data and resources are always available when needed. Redundancy and [backup](https://www.geeksforgeeks.org/dbms/difference-between-backup-and-recovery/) systems can help to ensure that the network remains operational in the event of a failure.

### &#x20;3. **Scalability** <a href="#id-3scalability" id="id-3scalability"></a>

Scalability means a network can grow and handle more users or devices without losing performance. The internet is a great example of this: even as millions of new users connect and communicate with other devices, the network continues to work well.

Computer networks must be scalable to accommodate growth and changing needs. As the number of devices and users on the network increases, the network must be able to handle the additional traffic and data.

### 4. Flow of Data <a href="#id-4-flow-of-data" id="id-4-flow-of-data"></a>

Computer networks let users access and share data like files and documents between devices. This feature is essential because it enables data to move smoothly from one device to another.

### **5. High Performance** <a href="#id-5-high-performance" id="id-5-high-performance"></a>

Performance is measured by how quickly a command is executed. If data transfers fast and responses are quick, it benefits users by making data sharing and resource usage more efficient. Using multiple processors can further enhance performance.

The performance of a computer network is determined by factors such as bandwidth, latency, and throughput. These factors affect the speed and responsiveness of the network and can impact the user experience.

### 6. Fault Tolerance <a href="#id-6-fault-tolerance" id="id-6-fault-tolerance"></a>

Fault tolerance is a valuable feature of computer networks. For example, if two devices are connected by both wired and wireless means, and the wireless connection fails, the data can still be sent through the wired connection. This ensures that communication continues smoothly even if part of the network is down or damaged.

### 7. Quality of Service (QoS) <a href="#id-7-quality-of-service-qos" id="id-7-quality-of-service-qos"></a>

It means people can choose what data gets sent first and how it's sent, making sure it goes fast. If some data doesn't make it through, the system can handle that too. This makes sure users get a good experience when using the network.

### 8. Compatible With Hardware and Software Components <a href="#id-8-compatible-with-hardware-and-software-components" id="id-8-compatible-with-hardware-and-software-components"></a>

Another important characteristics of computer network is that it lets lots of devices use the same software. This means you can use the same program on different hardware. This makes things work better together and makes software easier to use. Plus, it helps make the most out of the stuff you have.

</details>

### Types of networks

Not all computer networks are the same. The network I'm using to link this laptop to my wireless router, printer, and other equipment is the smallest imaginable. It's an example of what's sometimes called a PAN (personal area network)—essentially a convenient, one-person network. If you work in an office, you probably use a **LAN (local area network)**, which is typically a few separate computers linked to one or two printers, a scanner, and maybe a single, shared connection to the Internet. LAN is restricted in size and has ownership. In LAN networks internet speed is from 10 Mbps to 100 Mbps (But now much higher speeds can be achieved). The most common topologies used in LAN networks are bus, ring, and star.

Imagine your home Wi-Fi network. All the devices connected to it, like your computer, phone, or smart TV, form a LAN. They can share files, printers, and internet access, making it easy to work and play together.

LANs are convenient because they allow devices to communicate quickly and efficiently, without needing to go through the internet. It's like having your own private neighborhood of connected gadgets.

Networks can be much bigger than this. At the opposite end of the scale, we talk about MANs (metropolitan area networks), which cover a whole town or city, and WANs (wide area networks), which can cover any geographical area. The Internet is a WAN that covers the entire world but, in practice, it's a network of networks as well as individual computers: many of the machines linked to the Net connect up through LANs operated by schools and businesses.

The big difference between the <mark style="background-color:purple;">**Internet**</mark> <mark style="background-color:purple;"></mark><mark style="background-color:purple;">and many other PANs, LANs, and WANs is that</mark> <mark style="background-color:purple;"></mark><mark style="background-color:purple;">**it's open to the public**</mark>, so that's another way of differentiating networks: are they public or private? If you work for a big corporation, you're probably used to the idea that much of the information you share with your colleagues is accessible only over internal machines; if it's accessed in a web-like way, what you have there is called an Intranet (a kind of private, internal Internet/Web not accessible over the public Internet). But what if you're working from home and you need to access the private bits of your corporate network over the public Internet? Then you can use something called a VPN (virtual private network), which is a secure way of accessing a private network over a public one. Sometimes the difference between public and private networks gets a little blurred. For example, using the World Wide Web, you may come across password-protected files or subscription-only websites. So even on a completely public network, it's possible to create a degree of selective, private access.

{% hint style="danger" %}
Internet is a network, so why it won't be a LAN?
{% endhint %}

### Rules

Computers are all about logic—and logic is all about following rules. Computer networks are a bit like the army: everything in a network has to be arranged with almost military precision and it has to behave according to very clearly defined rules. In a LAN, for example, you can't connect things together any old how: all the nodes (computers and other devices) in the network have to be connected in an orderly pattern known as the network topology.

You can connect nodes in a simple line (also called a daisy chain or bus), with each connected to the next in line. You can connect them in a star shape with the various machines radiating out from a central controller known as the network server. Or you can link them into a loop (generally known as a ring). Other topologies include meshes (where each machine is directly connected to some of the others or all of them—which is called a full mesh) and trees (where small star networks are connected together in a line or bus).

All the devices on a network also have to follow clearly defined rules (called protocols) when they communicate to ensure they understand one another—for example, so they don't all try to send messages at exactly the same time, which causes confusion.

<figure><img src="https://cdn4.explainthatstuff.com/computer-network-topologies.png" alt="Network Topology"><figcaption><p>Network Topology</p></figcaption></figure>

### Permissions and security

Just because a machine is on a network, it doesn't automatically follow that every other machine and device has access to it (or can be accessed by it). The Internet is an obvious example. If you're online, you get access to billions of Web pages, which are simply files stored on other machines (servers) dotted all over the network. But you can't access every single file on every single computer hooked up to the Internet: you can't read my personal files and I can't read yours, unless we specifically choose for that to happen.

<img src="https://cdn4.explainthatstuff.com/website-permissions-example.png" alt="Granting permissions to a file on a web server" height="390" width="480">

Permissions and security are central to the idea of networking: you can access files and share resources only if someone gives you permission to do so. Most personal computers that connect to the Internet allow outgoing connections (so you can, theoretically, link to any other computer), but block most incoming connections or prohibit them completely. Servers (the machines on the Internet that hold and serve up Web pages and other files) operate a more relaxed policy to incoming connections. You've probably heard of hacking, which, in one sense of the word, means gaining unauthorized access to a computer network by cracking passwords or defeating other security checks. To make a network more secure, you can add a firewall (either a physical device or a piece of software running on your machine, or both) at the point where your network joints onto another network or the Internet to monitor and prohibit any unauthorized, incoming access attempts.

#### Network Security <a href="#network-security" id="network-security"></a>

Ensuring the security of a network is crucial to protect data and resources from unauthorized access and attacks. Key aspects of network security include:

* **Firewalls:** Devices or software that monitor and control incoming and outgoing network traffic based on security rules.
* **Encryption:** The process of encoding data to prevent unauthorized access. Commonly used in VPNs, HTTPS, and secure email.
* **Intrusion Detection Systems (IDS):** Tools that monitor network traffic for suspicious activity and potential threats.
* **Access Control:** Mechanisms that restrict access to network resources based on user identity and role.
* **Regular Updates and Patching:** Keeping software and hardware up to date to protect against vulnerabilities.

### What makes a network?

To make a network, you need nodes and connections (sometimes called links) between them. Linking up the nodes means making some sort of a temporary or permanent connection between them. In the last decade or so, wireless connections have become one of the most popular ways of doing this, especially in homes. In offices, wired connections are still more commonplace—not least because they are generally faster and more secure and because many newer offices have network cabling already in place.

Apart from computers, peripherals, and the connections between them, what else do you need? Each node on a network needs a special circuit known as a network card (or, more formally, a network interface card or NIC) to tell it how to interact with the network. Most new computers have network cards built in as standard. If you have an older computer or laptop, you may have to fit a separate plug-in circuit board (or, in a laptop, add a PCMCIA card) to make your machine talk to a network. Each network card has its own separate numeric identifier, known as a MAC (media access control) code or LAN MAC address. A MAC code is a bit like a phone number: any machine on the network can communicate with another one by sending a message quoting its MAC code. In a similar way, MAC codes can be used to control which machines on a network can access files and other shared resources. For example, I've set up my wireless link to the Internet so that only two MAC codes can ever gain access to it (restricting access to the network cards built into my two computers). That helps to stop other people in nearby buildings (or in the street) hacking into my connection or using it by mistake.

<img src="https://cdn4.explainthatstuff.com/wireless-lan-card-large.jpg" alt="Inside a TP-Link PCMCIA laptop wireless card with Ralink RT2560/RT2525 chipset" height="450" width="600">



The bigger you make a network, the more extra parts you need to add to make it function efficiently. Signals can travel only so far down cables or over wireless links so, if you want to make a big network, you have to add in devices called repeaters—effectively signal boosters. You might also need bridges, switches, and routers—devices that help to link together networks (or the parts of networks, which are known as segments), regulate the traffic between them, and forward traffic from one part of a network to another part.

### How Does a Computer Network Work <a href="#how-does-a-computer-network-work" id="how-does-a-computer-network-work"></a>

Basics building blocks of a Computer network are Nodes and Links.

* A Network Node can be illustrated as Equipment for Data Communication like a Modem, Router, etc., or Equipment of a Data Terminal like connecting two computers or more.
* Link in Computer Networks can be defined as wires or cables or free space of wireless networks (as shown in the below diagram)
* The working of Computer Networks can be simply defined as rules or protocols which help in sending and receiving data via the links which allow Computer networks to communicate.
* Each device has an IP Address, that helps in identifying the device.
* A firewall is a network security device either hardware or software-based which monitors all incoming and outgoing traffic and based on a defined set of security rules it accepts, rejects, or drops that specific traffic .

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20250726184452563578/frame_25.webp" alt=""><figcaption></figcaption></figure>

### Types of Computer Network Architecture <a href="#types-of-computer-network-architecture" id="types-of-computer-network-architecture"></a>

Depending on what they share, devices or information, LANs are categorized under these broad choices:

* **Client-Server Architecture:** Client-Server Architecture is a type of Computer Network Architecture in which Nodes can be Servers or Clients. Here, the server node can manage the Client Node Behaviour.
* **Peer-to-Peer Architecture:** In P2P (Peer-to-Peer) Architecture, there is not any concept of a Central Server. Each device is free for working as either client or server.

### Network Devices <a href="#network-devices" id="network-devices"></a>

An interconnection of multiple devices, also known as hosts, that are connected using multiple paths for the purpose of sending/receiving data or media. Computer networks can also include multiple devices/mediums which help in the communication between two different devices; these are known as [Network devices](./#network-devices) and include things such as routers, switches, hubs, and bridges.&#x20;

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20230406173121/router-hub.jpg" alt="Network Devices" width="334"><figcaption><p>Network Devices</p></figcaption></figure>

### Understanding computer networks with layers

Computers are general-purpose machines that mean different things to different people. Some of us just want to do basic tasks like word processing or chatting to friends on Meta and we couldn't care less how that happens under the covers—or even that we're using a computer to do it (if we're using a smartphone, we probably don't even think what we're doing is "computing"—or that installing a new app is effectively computer programming). At the opposite end of the spectrum, some of us like modifying our computers to run faster, fitting quicker processors or more memory, or whatever it might be; for geeks, poking around inside computers is an end in itself. Somewhere in between these extremes, there are moderately tech-savvy people who use computers to do everyday jobs with a reasonable understanding of how their machines work.

Because computers mean different things to different people, it can help us to understand them by thinking of a stack of layers: hardware at the bottom, the operating system somewhere on top of that, then applications running at the highest level. You can "engage" with a computer at any of these levels without necessarily thinking about any of the other layers. Nevertheless, each layer is made possible by things happening at lower levels, whether you're aware of that or not. Things that happen at the higher levels could be carried out in many different ways at the lower levels; for example, you can use a web browser like Firefox (an application) on many different operating systems, and you can run various operating systems on a particular laptop, even though the hardware doesn't change at all.

<div align="center"><img src="https://cdn4.explainthatstuff.com/computer-architecture.webp" alt="A typical computer architecture linking the hardware to the applications via the BIOS and the operating system." height="400" width="350"></div>

Computer networks are similar: we all have different ideas about them and care more or less about what they're doing and why. If you work in a small office with your computer hooked up to other people's machines and shared printers, probably all you care about is that you can send emails to your colleagues and print out your stuff; you're not bothered how that actually happens. But if you're charged with setting up the network in the first place, you have to consider things like how it's physically linked together, what sort of cables you're using and how long they can be, what the MAC addresses are, and all kinds of other nitty gritty. Again, just like with computers, we can think about a network in terms of its different layers—and there are two popular ways of doing that.

#### The OSI model

Perhaps the best-known way is with what's called the OSI (Open Systems Interconnect) model, based on an internationally agreed set of standards devised by a committee of computer experts and first published in 1984. It describes a computer network as a stack of seven layers. The lower layers are closest to the computer hardware; the higher levels are closer to human users; and each layer makes possible things that happen at the higher layers:

1. **Physical**: The basic hardware of the network, including cables and connections, and how devices are hooked up into a certain network topology (ring, bus, or whatever). The physical layer isn't concerned in any way with the data the network carries and, as far as most human users of a network are concerned, is uninteresting and irrelevant.
2. **Data link**: This covers things like how data is packaged and how errors are detected and corrected.
3. **Network**: This layer is concerned with how data is addressed and routed from one device to another.
4. **Transport**: This manages the way in which data is efficiently and reliably moved back and forth across the network, ensuring all the bits of a given message are correctly delivered.
5. **Session**: This controls how different devices on the network establish temporary "conversations" (sessions) so they can exchange information.
6. **Presentation**: This effectively translates data produced by user-friendly applications into computer-friendly formats that are sent over the network. For example, it can include things like compression (to reduce the number of bits and bytes that need transmitting), [encryption](https://www.explainthatstuff.com/encryption.html) (to keep data secure), or converting data between different character sets (so you can read emoticons ("smileys") or emojis in your emails).
7. **Application**: The top level of the model and the one closest to the user. This covers things like email programs, which use the network in a way that's meaningful to human users and the things they're trying to achieve.

<img src="https://cdn4.explainthatstuff.com/osi-networking-model.png" alt="The seven layers of the OSI model of networking." height="300" width="400">

OSI was conceived as a way of making all kinds of different computers and networks talk to one another, which was a major problem back in the 1960s, 1970s, and 1980s, when virtually all computing hardware was proprietary and one manufacturer's equipment seldom worked with anyone else's.

#### TCP/IP (Darpa) model

The Internet is based on a two-part networking system called TCP/IP in which computers hook up over networks (using what's called TCP, Transmission Control Protocol) to exchange information in packets (using the Internet Protocol, IP). We can understand TCP/IP using four slightly simpler layers, sometimes known as the TCP/IP model.

While the OSI model is quite an abstract and academic concept, rarely encountered outside books and articles about computer networking, the TCP/IP model is a simpler, easier-to-understand, and more practical proposition: it's the bedrock of the Internet—and the very technology you're using to read these words now.

### **Network Protocols** <a href="#network-protocols" id="network-protocols"></a>

A protocol is a set of rules or algorithms which define the way how two entities can communicate across the network and there exists a different protocol defined at each layer of the OSI model. A few such protocols are TCP, IP, UDP, ARP, DHCP, FTP, and so on.&#x20;

* **Transmission Control Protocol/Internet Protocol (TCP/IP):** TCP/IP is the foundational protocol suite of the internet, enabling reliable communication. TCP Ensures data is delivered reliably and in order and IP routes data packets to their destination based on IP addresses.
* **Hypertext Transfer Protocol (HTTP) and HTTPS:** HTTP and HTTPS protocols used for transmitting web pages. **In HTTP** communication is unsecured and in **HTTPS** secured communication using SSL/TLS encryption.
* **Simple Mail Transfer Protocol (SMTP):** SMTP protocol used to send email. SMTP protocol works with other protocols like POP3 and IMAP for email retrieval.
* **File Transfer Protocol (FTP):** FTP protocol used for transferring files between computers. Includes commands for uploading, downloading, and managing files on a remote server.
* **Dynamic Host Configuration Protocol (DHCP):** DHCP protocol automatically assigns IP addresses to devices on a network. Reduces manual configuration and IP address conflicts.
* **Domain Name System (DNS):** DNSTranslates human-friendly domain names into IP addresses. Ensures seamless navigation on the internet.

<details>

<summary>Vocabulary: Unique Identifiers of Networks</summary>

**Hostname:** Each device in the network is associated with a unique device name known as Hostname. Type “hostname” in the command prompt(Administrator Mode) and press ‘Enter’, this displays the hostname of your machine.&#x20;

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/hostname.png" alt="HostName"><figcaption><p>HostName</p></figcaption></figure>

**IP Address (Internet Protocol address):**  Also known as the Logical Address, the IP Address is the network address of the system across the network. To identify each device in the world-wide-web, the Internet Assigned Numbers Authority (IANA) assigns an IPV4 (Version 4) address as a unique identifier to each device on the Internet. The length of an IPv4 address is 32 bits, hence, we have 2<sup>32</sup> IP addresses available. The length of an IPv6 address is 128 bits.

In **Windows** Type “ipconfig” in the command prompt and press ‘Enter’, this gives us the IP address of the device. For **Linux,** Type “ifconfig” in the terminal and press ‘Enter’ this gives us the IP address of the device.\
\
**MAC Address (Media Access Control address):** Also known as physical address, the MAC Address is the unique identifier of each host and is associated with its NIC (Network Interface Card). A MAC address is assigned to the NIC at the time of manufacturing. The length of the MAC address is: 12-nibble/ 6 bytes/ 48 bits Type “ipconfig/all” in the command prompt and press ‘Enter’, this gives us the MAC address.&#x20;

{% hint style="danger" %}
### What is the difference between a MAC address and an IP address?

Network switches refer to MAC addresses in order to send Internet traffic to the right devices, not IP addresses.

Every device that connects to the Internet has an IP address. An IP address is a series of alphanumeric characters, like 192.0.2.255 or 2001:0db8:85a3:0000:0000:8a2e:0370:7334. IP addresses act like a mailing address, enabling Internet communications directed at that address to reach that device. IP addresses often change: because there is a limited number of IPv4 addresses, user devices are typically assigned new ones when they form a new connection with a network.

IP addresses are used at layer 3, which means computers and devices all over the Internet use IP addresses for sending and receiving data, no matter which network they are connected to. All IP packets include their source and destination IP addresses in their headers, just as a piece of mail has a destination address and a return address.

In contrast, a MAC address is a permanent identifier for each piece of hardware, somewhat like a serial number. Unlike IP addresses, MAC addresses do not change. MAC addresses are used at layer 2, not layer 3 — which means they are not included in IP packet headers. In other words, MAC addresses are not part of Internet traffic. They are only used inside a given network.
{% endhint %}

**Port:** A port can be referred to as a logical channel through which data can be sent/received to an application. Any host may have multiple applications running, and each of these applications is identified using the port number on which they are running.&#x20;

A port number is a 16-bit integer, hence, we have 2<sup>16</sup> ports available which are categorized as shown below:&#x20;

| **Port Types**   | **Range**     |
| ---------------- | ------------- |
| Well known Ports | 0 – 1023      |
| Registered Ports | 1024 – 49151  |
| Ephemeral Ports  | 49152 - 65535 |

Number of ports: 65,536 \
Range: 0 – 65535 \
Type “**netstat -a**” in the command prompt and press ‘Enter’, this lists all the ports being used.&#x20;

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/ports.png" alt="List of Ports"><figcaption><p>List of Ports</p></figcaption></figure>

**Socket:** The unique combination of IP address and Port number together is termed a Socket.&#x20;

**DNS Server:** DNS stands for **Domain Name System**. DNS is basically a server that translates web addresses or URLs (ex: www.google.com) into their corresponding IP addresses. We don’t have to remember all the IP addresses of each and every website. The command ‘**nslookup**’ gives you the IP address of the domain you are looking for. This also provides information on our DNS Server. \\

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/nslookup.png" alt="Domain IP Address"><figcaption><p>Domain IP Address</p></figcaption></figure>

**ARP:** ARP stands for **Address Resolution Protocol**. It is used to convert an IP address to its corresponding physical address(i.e., MAC Address). ARP is used by the Data Link Layer to identify the MAC address of the Receiver’s machine. \
\
**RARP:** RARP stands for **Reverse Address Resolution Protocol**. As the name suggests, it provides the IP address of the device given a physical address as input. But RARP has become obsolete since the time DHCP has come into the picture.





</details>

