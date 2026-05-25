# 3.2 MAC Addressing

> To communicate or transfer data from one computer to another, we need an address. In computer networks, various types of addresses are introduced; each works at a different layer. A MAC address, which stands for _Media Access Control Address_, is a physical address that works at the Data Link Layer. In this article, we will discuss addressing a DLL, which is the MAC Address.&#x20;

<mark style="background-color:purple;">**MAC Addresses**</mark> <mark style="background-color:purple;"></mark><mark style="background-color:purple;">are unique</mark> <mark style="background-color:purple;"></mark><mark style="background-color:purple;">**48-bit**</mark> <mark style="background-color:purple;"></mark><mark style="background-color:purple;">hardware numbers of a computer that are embedded into a network card (known as a</mark> <mark style="background-color:purple;"></mark><mark style="background-color:purple;">**Network Interface Card**</mark><mark style="background-color:purple;">) during manufacturing.</mark> The MAC Address is also known as the **Physical Address** of a network device. In the IEEE 802 standard, the data link layer is divided into two sublayers:

1. Logical Link Control (LLC) Sublayer
2. Media Access Control (MAC) Sublayer

**The MAC** address is used by the Media Access Control (MAC) sublayer of the Data-Link Layer. MAC Address is worldwide unique since millions of network devices exist and we need to uniquely identify each.&#x20;

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/mac.jpg" alt=""><figcaption></figcaption></figure>

### Format of MAC Address <a href="#format-of-mac-address" id="format-of-mac-address"></a>

To understand what is MAC address is, it is very important that first you understand the format of the MAC Address. So a <mark style="background-color:purple;">MAC Address is a 12-digit hexadecimal number (48-bit binary number)</mark>, which is mostly represented by Colon-Hexadecimal notation.

The First 6 digits (say 00:40:96) of the MAC Address identify the manufacturer, called the OUI (**Organizational Unique Identifier**). IEEE Registration Authority Committee assigns these MAC prefixes to its registered vendors.&#x20;

Here are some OUI of well-known manufacturers:

<pre><code><strong>CC:46:D6 - Cisco 
</strong><strong>3C:5A:B4 - Google, Inc.
</strong><strong>3C:D9:2B - Hewlett Packard
</strong><strong>00:9A:CD - HUAWEI TECHNOLOGIES CO.,LTD
</strong></code></pre>

The rightmost six digits represent **Network Interface Controller**, which is assigned by the manufacturer.&#x20;

As discussed above, the MAC address is represented by Colon-Hexadecimal notation. But this is just a conversion, not mandatory. MAC address can be represented using any of the following formats:

![Format of MAC Address](https://media.geeksforgeeks.org/wp-content/uploads/mac-notation.jpg)

{% hint style="info" %}
Colon-Hexadecimal notation is used by _Linux OS_ and Period-separated Hexadecimal notation is used by _Cisco Systems_. &#x20;
{% endhint %}

{% hint style="warning" %}
A **hyphen** joins two or more words together while a **dash** separates words into parenthetical statements. The two are sometimes confused because they look so similar, but their usage is different. While dashes are longer (—), so they are used between phrases or clauses (groups of words); Hyphens are shorter (-), so they are only used between prefixes and words to make compound words such as _self-esteem_.
{% endhint %}

### Types of MAC Address <a href="#types-of-mac-address" id="types-of-mac-address"></a>

**1. Unicast:** A Unicast-addressed frame is only sent out to the interface leading to a specific NIC. If the LSB (least significant bit) of the first octet of an address is set to zero, the frame is meant to reach only one receiving NIC. The MAC Address of the source machine is always Unicast.&#x20;

![Unicast](https://media.geeksforgeeks.org/wp-content/uploads/unicast.jpg)

**2. Multicast:** The multicast address allows the source to send a frame to a group of devices. In Layer-2 (Ethernet) Multicast address, the LSB (least significant bit) of the first octet of an address is set to one. IEEE has allocated the address block 01-80-C2-xx-xx-xx (01-80-C2-00-00-00 to 01-80-C2-FF-FF-FF) for group addresses for use by standard protocols.&#x20;

![Multicast](https://media.geeksforgeeks.org/wp-content/uploads/MULTICAST.jpg)

**3. Broadcast:** Similar to Network Layer, Broadcast is also possible on the underlying layer( Data Link Layer). Ethernet frames with ones in all bits of the destination address (FF-FF-FF-FF-FF-FF) are referred to as the broadcast addresses. Frames that are destined with MAC address FF-FF-FF-FF-FF-FF will reach every computer belonging to that LAN segment.&#x20;

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/broadcast.jpg" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
### Reason to Have Both IP and MAC Addresses <a href="#reason-to-have-both-ip-and-mac-addresses" id="reason-to-have-both-ip-and-mac-addresses"></a>

The reason for having both IP and MAC addresses lies in the way the Internet works, specifically in the structure of the OSI Model. This model is a conceptual framework that describes how data is sent and received over a network. It's divided into seven layers, each performing specific functions.

* **Layer 2** uses **MAC addresses** and is responsible for packet delivery from [**hop to hop**](../3.5-routing-tables-and-subnet-matching/#how-does-ip-routing-work) .
* **Layer 3** uses **IP addresses** and is responsible for packet delivery from **end to end** .

Layer 2 **(Data Link Layer)** uses a **MAC (Media Access Control) address**. These are unique identifiers assigned to network interfaces for communications at the data link layer. The primary function of MAC addresses is to manage how data is transported from one network node to another on a direct, physical basis - this is also referred to as "hop to hop" delivery.

On the other hand, Layer 3 **( Network Layer )** uses an **IP (Internet Protocol) address**. These IP addresses are used to identify devices on a network and to route traffic between networks. The IP addresses ensure that the data gets from its original source reaches its final destination and it is also called "end-to-end" delivery of data.

When a computer sends data, it first wraps it in an IP header, which includes the source and destination IP addresses. This IP header, along with the data, is then encapsulated in a MAC header, which includes the source and destination MAC addresses for the current "hop" in the path.

As the data travels from one router to the next, the MAC address header is stripped off and a new one is generated for the next hop. However, the IP header, which was generated by the original computer, remains intact until it reaches the final destination. This process illustrates how the IP header manages the "end to end" delivery, while the MAC headers handle the "hop to hop" delivery.

So, Both IP and MAC addresses are essential for the functioning of the Internet. While MAC addresses facilitate the direct, physical transfer of data between network nodes, IP addresses ensure that the data reaches its final destination.
{% endhint %}

{% hint style="danger" %}
### Why Should the MAC Address Be Unique in the LAN Network? <a href="#why-should-the-mac-address-be-unique-in-the-lan-network" id="why-should-the-mac-address-be-unique-in-the-lan-network"></a>

Consider a **LAN (Local Area Network)** as a large gathering where everyone is engaged in conversations. Now, let's suppose that there are two individuals at this gathering who coincidentally share the same name. This scenario would inevitably create confusion, right? If someone calls out that name, both individuals would respond, making it challenging to discern the intended recipient of the message.

In a similar manner, within a network, each device possesses a distinct identifier referred to as a MAC (Media Access Control) address. Think of it as a unique name assigned to the device. When information is transmitted across the network, it is directed to a specific MAC address, much like a letter being addressed to a specific individual.

However, if multiple devices within the same network were to have identical MAC addresses, it would result in confusion and disrupt the network's functioning. The network would struggle to ascertain which device should receive the transmitted information. To prevent this confusion and ensure the accurate delivery of information, it is vital for each device on a network to possess a unique MAC address.
{% endhint %}

<details>

<summary>MAC address on Windows</summary>

Here is the Step-by-Step guide to finding MAC addresses on Windows.

**Command:**

```
ipconfig /all 
```

**Step 1 -** Press **Window Start** or Click on Windows Key.

![windows-ss-1](https://media.geeksforgeeks.org/wp-content/uploads/20230714134143/windows-ss-1.jpg)

**Step 2 -** In the search box, type **cmd,** and the command prompt will get open.

<img src="https://media.geeksforgeeks.org/wp-content/uploads/20230714134632/cmd-ss-2.jpg" alt="cmd-ss-2" height="706" width="1000">

**Step 3 -** Click on cmd, the command prompt window will display,<br>

<img src="https://media.geeksforgeeks.org/wp-content/uploads/20230714135228/ss-cmd-new.jpg" alt="ss-cmd-new" height="548" width="1000">

**Step 4 -** In the command prompt type **ipconfig/all** command and then press enter.

<img src="https://media.geeksforgeeks.org/wp-content/uploads/20230714135555/ipmg.jpg" alt="ipmg" height="534" width="1000">

**Step 5 -** As you will scroll down, each physical address is the MAC address of your device.

<img src="https://media.geeksforgeeks.org/wp-content/uploads/20230714145918/ipmg-(1).jpg" alt="ipmg-(1)" height="534" width="1000">

</details>

<details>

<summary>MAC Address on Unix/Linux</summary>

Here is a step-by-step guide to finding MAC addresses on a Unix/Linux operating system.

**Command For MAC Address in Unix/Linux:**

```
ifconfig -a
ip link list 
ip address show
```

</details>
