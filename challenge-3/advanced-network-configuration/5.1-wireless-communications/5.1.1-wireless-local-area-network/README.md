# 5.1.1 Wireless Local Area Network

**WLAN** stands for **Wireless Local Area Network.** WLAN is a local area network that uses radio communication to provide mobility to the network users while maintaining the connectivity to the wired network. <mark style="background-color:purple;">A WLAN basically, extends a wired local area network.</mark> <mark style="background-color:purple;">WLAN's are built by attaching a device called the access point (AP) to the edge of the wired network. Clients communicate with the AP using a wireless network adapter which is similar in function to an Ethernet adapter (NIC).</mark> It is also called a LAWN is a Local area wireless network. \
\
The performance of WLAN is high compared to other wireless networks (Bluetooth, Zigbee, etc). The coverage of WLAN is within a campus or building or that tech park. It is used in the mobile propagation of wired networks.&#x20;

### WLAN Standards

The standards of WLAN are HiperLAN, Wi-Fi, and [IEEE 802.11](ieee-802.11.md). It offers service to the desktop laptop, mobile application, and all the devices that work on the Internet. WLAN is an affordable method and can be set up in 24 hours. WLAN gives users the mobility to move around within a local coverage area and still be connected to the network. Most latest brands are based on IEE 802.11 standards, which are the WI-FI brand name.&#x20;

### WLAN Architecture

Components in Wireless LAN architecture as per IEEE standards are as follows:

1. **Stations:** Stations (STA) consist of all the equipment that is used to connect all wireless LANs. Each station has a wireless network controller: either Wireless [**Access Point (WAP)**](/broken/pages/hQbJCnTvadw96dhTCUHK) or final **Clients** (examples include computers, laptops, printers, and smartphones). Flatly any device able to send or receive data. &#x20;
2. [**Base Service Set(BSS)**](basic-service-set.md)**:** It is a group of stations communicating at the physical layer. It allows stations to remain in the same network while moving between WAPs, sort of roaming thing. While it keeps the same SSID to the user, internally it may be changing many antennas.&#x20;
3. [**Extended Service Set(ESS)**](extended-service-set-and-distribution-system.md)**:** It is a group of connected Base Service Set(BSS).
4. **Distribution Service (DS):** It connects all Extended Service Set (ESS) linking closer BSS. Usually a wired connection (Ethernet) between WAP devices or repeaters. Provided a station is moving physically from one BSS to the next, DS issues where has to be send the data-packets.  &#x20;

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20240424114752/WLAN-768.png" alt="WLAN" height="547" width="768"><figcaption><p>WLAN Architecture</p></figcaption></figure>

### Types of WLANs

As per IEEE standard WLAN is categorized into two basic modes, which are as follows:

1. **Infrastructure:** In Infrastructure mode, all the endpoints are connected to a base station and communicate through that; and this can also enable internet access. A WLAN infrastructure can be set up with: a wireless router (base station) and an endpoint (computer, mobile phone, etc). An office or home WiFi connection is an example of Infrastructure mode.
2. **Ad Hoc:** In Ad Hoc mode WLAN connects devices without a base station, like a computer workstation. An Ad Hoc WLAN is easy to set up it provides peer-to-peer communication. It requires two or more endpoints with built-in radio transmission.

### Working of WLAN

WLAN transmits data over radio signals and the data is sent in the form of a packet. Each packet consists of layers, labels, and instructions with unique MAC addresses assigned to endpoints. This enables routing data packets to correct locations.

### How is a WLAN Created ?

A WLAN is a collection of nodes interconnected with each other for the purpose of data sharing, transmitting messages over the internet, connecting for peer-2-peer connectiob etc. As discussed above in types, it can be created in following 2 ways :

1. Connecting through one base station and that could be the router that acts as a doorway to the internet, and every other nodes (devices like computer, smartphones) can connect to the internet and to each other through it.
2. Peer-2-Peer connection using the wifi direct technology. This is more suitable for situations when we require to connect two or more devices without internet and only for purpose of data exchange, connecting over a same local network.

### Is a WLAN Secure ?

Whether or not WLAN is secure depends on multiple factors of implementation configured by the network administrator. However, by default it has multiple security vulnerabilities. So the security team should consider all the factor and configure accordingly.

Following are 3 ways to ensure best security practices :

1. **Encryption:** Ensure that the network is using highest level of encryption
2. **Authentication:** There are multiple authentication mechanism, its good to use protocols that rely on 802.1x standards like WPA-EAP (Wireless Protected Acess-Extensible Authentication Protocol) for organisation as this method ONLY gives access when correct username and passwords are inputed. And usernames and passwords are not shared and are individual specific only.
3. **Monitor Rougue APs:** The Rougue APs (Access Points) are similar set of networks that user can unknowingly connect to where all the activities of the user will be tracked and monitored by the bad actor who set up the network. Hence the security team can be on the lookout for such configured networks occasionally.

### Characteristics of WLAN

1. Seamless operation.
2. Low power for battery use.
3. Simple management, easy to use for everyone.
4. Protection of investment in wired networks.
5. Robust transmission technology.



{% columns %}
{% column %}
{% hint style="success" %}
#### Advantages of WLAN

1. Installation speed and simplicity.
2. Installation flexibility.
3. Reduced cost of ownership.
4. Reliability.
5. Mobility.
6. Robustness.
{% endhint %}
{% endcolumn %}

{% column %}
{% hint style="danger" icon="square-xmark" %}
#### **Disadvantages** of WLAN

1. Slower bandwidth.
2. Security for wireless LANs is the prime concern.
3. Less capacity.
4. Wireless networks cost four times more than wired network cards.
5. Wireless devices emit low levels of RF which can be harmful to our health.
{% endhint %}
{% endcolumn %}
{% endcolumns %}
