---
description: Create a subnet
---

# 3.4 Subnetting

Subnetting is the process of dividing a large network into smaller networks called subnets. Each subnet provides its own space for devices to communicate, improving network performance, security, and management.

<div data-full-width="true"><figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20251007160034646647/1.jpg" alt="1" width="563"><figcaption><p>Subnetting</p></figcaption></figure></div>

<details>

<summary>Example: Why Subnetting is Important</summary>

In a company, different departments (Sales, HR, IT) can have their own subnets, keeping their traffic separate and organized.

Let's consider the company follows classful addressing, it has a **Class C network (192.168.1.0/24)** with **256 IP addresses**. They have to meet different needs of each department:

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20250731151737177345/192_168_1_0_24.webp" alt="192_168_1_0_24" height="400" width="800"><figcaption><p>Subnetting</p></figcaption></figure>

Without subnetting, all departments share the same network, and all **256 IP addresses** are available to everyone, which leads to:

* **IP Waste:** Only 80 devices used out of 256 addresses i.e 176 wasted.
* **Performance Issues:** All traffic floods the same network, slowing communication.
* **Security Risks:** Devices from different departments can access each other freely.

**With Subnetting**, we split the network into three subnets, allocating just enough IP addresses for each department:

| Department | Devices | IPs Allocated (after subnetting) |
| ---------- | ------- | -------------------------------- |
| Sales      | 20      | 32 (`192.168.1.0/27`)            |
| HR         | 10      | 16 (`192.168.1.32/28`)           |
| IT         | 50      | 64 (`192.168.1.48/26`)           |

{% hint style="warning" %}
By subnetting, we:

* **Efficient IP usage:** Only 112 addresses used, leaving space for growth.
* **Better performance:** Traffic stays within each subnet.
* **Improved security:** Each department is isolated.
{% endhint %}

</details>

### Key Concepts in Subnetting <a href="#key-concepts-in-subnetting" id="key-concepts-in-subnetting"></a>

<table data-view="cards"><thead><tr><th></th><th></th></tr></thead><tbody><tr><td><h4 id="ip-addressing"><a href="../3.3-ip-addressing/">IP Addressing</a></h4></td><td>Network Portion + Host Portion</td></tr><tr><td><a href="../3.3-ip-addressing/3.3.2-classful-addressing.md">Network Classes</a></td><td>Classes A-B-C-D-E</td></tr><tr><td><a href="../3.3-ip-addressing/3.3.1-subnet-mask.md">Subnet Mask usage</a></td><td>Matching (Bitwise AND)</td></tr></tbody></table>

### Subnetting Workflow <a href="#how-subnetting-works" id="how-subnetting-works"></a>

The working of subnets starts in such a way that firstly it divides the subnets into smaller subnets. <mark style="background-color:purple;">For communicating between subnets, routers are used.</mark> Each subnet allows its linked devices to communicate with each other. Subnetting for a network should be done in such a way that it does not affect the network bits.

#### Dividing a net into two subnets

In class C the first 3 octets are network bits so it remains as it is.&#x20;

* **For Subnet-1:** The first bit which is chosen from the host id part is zero and the range will be from (193.1.2.00000000 till you get all 1's in the host ID part i.e, 193.1.2.01111111) except for the first bit which is chosen zero for subnet id part.\
  \
  Thus, the range of subnet 1 is: **`193.1.2.0` to `193.1.2.127`**&#x20;

{% code overflow="wrap" %}
```
Subnet id of Subnet 1 is: 193.1.2.0
The direct Broadcast id of Subnet-1 is: 193.1.2.127
The total number of hosts possible is: 126 (Out of 128, 2 id's are used for Subnet id & Direct Broadcast id)
The subnet mask of Subnet- 1 is: 255.255.255.128
```
{% endcode %}

* **For Subnet-2:** The first bit chosen from the host id part is one and the range will be from (193.1.2.100000000 till you get all 1's in the host ID part i.e, 193.1.2.11111111).\
  \
  Thus, the range of subnet-2 is: **`193.1.2.128` to `193.1.2.255`**&#x20;

<pre data-overflow="wrap"><code><strong>Subnet id of Subnet 2 is : 193.1.2.128
</strong>The direct Broadcast id of Subnet-2 is: 193.1.2.255
The total number of hosts possible is: 126 (Out of 128, 2 id's are used for Subnet id &#x26; Direct Broadcast id)
The subnet mask of Subnet- 2 is: 255.255.255.128
The best way to find out the subnet mask of a subnet is to set the fixed bit of host-id to 1 and the rest to 0.
</code></pre>

Finally, after using the subnetting the total number of usable hosts is reduced from[ 254 to 252](#user-content-fn-1)[^1] .

{% hint style="info" %}
**Note**

1. To divide a network into four (2 <sup>2</sup> ) parts you need to choose two bits from the host id part for each subnet i.e, (00, 01, 10, 11).
2. To divide a network into eight (2 <sup>3</sup> ) parts you need to choose three bits from the host id part for each subnet i.e, (000, 001, 010, 011, 100, 101, 110, 111) and so on.
3. We can say that <mark style="background-color:purple;">if the total number of subnets in a network increases the total number of usable hosts decreases</mark>.
{% endhint %}

**The network can be divided into two parts:** To divide a network into two parts, you need to choose one bit for each Subnet from the host ID part.

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20251007155848317951/nid_193_1_2_0.webp" alt="nid_193_1_2_0" height="400" width="800"><figcaption><p> There are two Subnets as for the initial target</p></figcaption></figure>

{% hint style="info" %}
**Note:** It is a class C IP so, there are 24 bits in the network id part and 8 bits in the host id part.
{% endhint %}

{% columns %}
{% column %}
{% hint style="success" %}
#### Advantages of Subnetting <a href="#advantages-of-subnetting" id="advantages-of-subnetting"></a>

* **Improved Security:** Subnets isolate departments, preventing unauthorized access (e.g., HR data hidden from Sales).
* **Traffic Prioritization:** Critical subnets (e.g., Sales hosting video conferences) can get higher priority.
* **Easier Maintenance:** Smaller, segmented networks are simpler to manage.
* **Reduces Congestion:** Minimizes broadcast traffic, improving network speed.
* **Efficient IP Allocation:** Distributes IPs based on need, preventing wastage.
* **Improved Security:** Isolates subnets so sensitive data (e.g., developer code) stays protected.
* **Departmental Segmentation:** Allows priority handling for specific subnets (e.g., sales video conferencing).
* **Supports Scalability:** Makes it easier to expand networks while keeping them organized.
{% endhint %}


{% endcolumn %}

{% column %}
{% hint style="danger" icon="square-xmark" %}
#### Disadvantages of Subnetting <a href="#disadvantages-of-subnetting" id="disadvantages-of-subnetting"></a>

* **Extra Overhead:** Each subnet wastes 2 IP addresses (network ID and broadcast address).
* **Additional Hardware Costs:** Often requires routers or Layer-3 devices to connect subnets, increasing expenses.
* **More Complexity:** Compared to a single flat network, subnetting adds extra steps in communication and requires careful planning.
* **Compatibility Issues:** Older devices or legacy systems may not fully support subnetting schemes.
{% endhint %}


{% endcolumn %}
{% endcolumns %}

[^1]: 
