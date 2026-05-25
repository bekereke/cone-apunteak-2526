# 5.2 Virtual LAN

> A Virtual Local Area Network (VLAN) is a logical segmentation of a Layer 2 (Data Link Layer) network that enables devices to be grouped together regardless of their physical location. Unlike traditional LANs that rely on physical topology, VLANs are implemented in switches using IEEE 802.1Q VLAN tagging.

<details>

<summary>Practical example (use Packet Tracer)</summary>

As we have seen in previous sections, devices connected to a switch are in the same physical network, as shown in the following figure:

<figure><img src="../../../.gitbook/assets/irudia (22).png" alt=""><figcaption></figcaption></figure>

<mark style="background-color:purple;">But that doesn't mean they belong in the same logical network.</mark> Because to be in the same logical network, you have to consider the IP address. For example, the computers shown in the following figure are in the same physical network (because they are connected to the same switch) and in the same logical network (because their IP addresses and sub-masks are in the same subnetwork, specifically in subsection <kbd>192.168.1.0/24</kbd>):

<figure><img src="../../../.gitbook/assets/irudia (23).png" alt=""><figcaption><p>All computers have a connection between them because they're in the same physical network and logical network.</p></figcaption></figure>

However, the computers that appear in the following figure are in the same physical network (because they are connected to the same switch), but they are not in the same logical network (seeing IP addresses and sub-masks, because they are in different subnetworks, some computers in the <kbd>192.168.1.0/24</kbd> subdivision and others in <kbd>192.168.2.0/24</kbd>):

<figure><img src="../../../.gitbook/assets/irudia (24).png" alt=""><figcaption></figcaption></figure>

As shown above, we can divide a physical network into different subdivisions and thus, among other things, increase network security. For example, the same physical network in a school can be divided into two parts, one for students and the other for teachers (so that students cannot access teachers' computers). So as:

<figure><img src="../../../.gitbook/assets/irudia (25).png" alt=""><figcaption></figcaption></figure>

Even if we are in different logical networks, we can easily pass the security measure, but just put an IP address on a student's computer from the teachers' subdivision.

To solve this problem, imaginary local networks or VLAN (Virtual Local Area Network) were created. To create these types of networks, you need special switches or switches called switches or switches level 3. Because, as we've seen in previous exercises, to assemble our networks, we've had to configure a number of devices, including computers and routers; however, in switches we haven't changed anything within its configuration, all we've done is connect the wires. Well, the switches needed to assemble VLAN are configurable.

For example, in the previous network we can specify 2 VLANs: students VLANs and teachers VLANs. Once this is done, we need to determine which VLAN each switch port or connector corresponds to. So, some switch connectors will be in a VLAN (for example, students), and only the computers of that VLAN will be connected, and other connectors will be in another VLAN (for example, teachers), and only the computers of that VLAN will be connected.

</details>

By partitioning a single physical network into multiple broadcast domains, VLANs improve security, performance, flexibility, and manageability. Traditionally, routers (Layer 3 devices) were used to break up broadcast domains. However, VLANs enable switches to perform this segmentation at Layer 2.

* **Same VLAN:** Devices can communicate directly within the VLAN.
* **Different VLANs:** Communication requires Inter-VLAN Routing (using a router or Layer 3 switch).

{% hint style="info" %}
In a normal LAN, all devices connected to the same switch are part of the same broadcast domain. Any broadcast frame sent by one device is received by all other devices, leading to unnecessary traffic and potential security risks
{% endhint %}

### VLAN Ranges (Cisco Standard) <a href="#vlan-ranges-cisco-standard" id="vlan-ranges-cisco-standard"></a>

* **VLAN 0 & 4095:** Reserved, not usable.
* **VLAN 1:** Default VLAN; all switch ports belong here initially. Cannot be deleted.
* **VLAN 2–1001:** Normal VLAN range (configurable, editable, deletable).
* **VLAN 1002–1005:** Reserved for legacy Token Ring and FDDI.
* **VLAN 1006–4094:** Extended VLAN range.

### VLAN Configuration Example <a href="#vlan-configuration-example" id="vlan-configuration-example"></a>

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20250925112809444690/vlan.webp" alt="vlan" height="400" width="800"><figcaption><p>VLAN Configuration</p></figcaption></figure>

```bat
# Create VLANs
Switch(config)# vlan 2
Switch(config-vlan)# name Accounts

Switch(config)# vlan 3
Switch(config-vlan)# name HR

# Assign switch ports to VLANs
Switch(config)# interface fa0/0
Switch(config-if)# switchport mode access
Switch(config-if)# switchport access vlan 2

Switch(config)# interface fa0/1
Switch(config-if)# switchport mode access
Switch(config-if)# switchport access vlan 3
Here, port fa0/0 belongs to VLAN 2 and port fa0/1 belongs to VLAN 3. Devices in different VLANs need Inter-VLAN Routing to communicate.

```

### Types of VLAN Links <a href="#types-of-vlan-links" id="types-of-vlan-links"></a>

* Access Link: Connects a VLAN-unaware device to a VLAN-aware switch (frames untagged).
* Trunk Link: Connects VLAN-aware devices (switch-to-switch, switch-to-router) carrying multiple VLANs with 802.1Q tagging.
* Hybrid Link: Supports both tagged and untagged traffic.

### VLAN Features <a href="#vlan-features" id="vlan-features"></a>

* **VLAN Tagging (802.1Q):** Inserts a 4-byte VLAN tag into Ethernet frames.
* **VLAN Membership:** Devices grouped by port, MAC address, or protocol.
* **VLAN Trunking:** Enables multiple VLANs over one physical link.
* **Dynamic VLANs:** Membership assigned automatically based on policies.

### Real-Time Applications of VLANs <a href="#realtime-applications-of-vlans" id="realtime-applications-of-vlans"></a>

* **VoIP (Voice over IP):** Dedicated VLAN for voice traffic ensures QoS.
* **Video Conferencing:** Prioritized VLAN reduces latency and jitter.
* **Cloud & Data Centers:** VLANs isolate tenant workloads.
* **IoT Networks:** Devices segmented for security.
* **Gaming Networks:** VLANs prioritize gaming traffic.
* **Remote Access:** Secure VLANs for VPN and external users.



{% columns %}
{% column %}
{% hint style="success" %}
#### Advantages

* **Improved Security:** Sensitive traffic isolated within VLANs.
* **Enhanced Performance:** Reduces broadcast and multicast overhead.
* **Simplified Management:** Logical grouping of departments (e.g., HR, Finance).
* **Flexibility:** Devices can be reallocated without physical rewiring.
* **Cost Savings:** Eliminates need for excessive routers.
* **Scalability:** Networks can be segmented into manageable subnets.
{% endhint %}
{% endcolumn %}

{% column %}
{% hint style="danger" icon="square-xmark" %}
#### Disadvantages <a href="#disadvantages-of-vlans" id="disadvantages-of-vlans"></a>

* Increased configuration complexity.
* Scalability limitations due to VLAN ID restrictions.
* Security risks if VLAN hopping attacks are exploited.
* Interoperability issues with non-standard devices.
* Troubleshooting challenges due to isolated traffic flows.
{% endhint %}
{% endcolumn %}
{% endcolumns %}
