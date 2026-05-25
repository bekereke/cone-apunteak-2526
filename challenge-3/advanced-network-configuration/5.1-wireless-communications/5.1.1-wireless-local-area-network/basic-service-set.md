---
description: Wireless Communication
---

# Basic Service Set

**Basic Service Set (BSS)**, as the name suggests, is basically a network topology that allows all wireless devices to communicate with each other through a common medium i.e., AP (Access point). It also manages these wireless devices or clients. It basically provides a building block to all wireless LAN (Local Area Network). BSS basically contains only one AP that is connected to all stations i.e., all wireless devices within the network. Here, an AP is a common access point that acts as a medium and creates a WLAN (Wireless Local Area Network). &#x20;

AP allows all wireless devices to get connected to a wired network and start communicating with each other. Therefore, an AP is considered a master that controls all wireless devices or stations with BSS or WLAN. BSS contains only one AP, but it may contain one or more stations. BBS is generally considered simplest if it contains one AP and one station. Before connecting to a wireless network, wireless device or station need to send an association request to AP and then AP checks whether the client fit any of the following criteria or not –&#x20;

* Matching SSID (Service Set Identifier).&#x20;
* Compatible wireless data rate i.e., transmission speed or speed at which data is transferred between stations.&#x20;
* Authentication credentials i.e., verification of the client’s identity.&#x20;

AP then either denies or permits requests. In BSS, stations or devices do not communicate directly with each other. AP is required that acts as a medium. All stations communicate or transfer data frames to AP that they want to transfer or share to the destination station, then AP forward received data frames to destination stations. BSS usually provides short-range wireless communication and such an area is known as BSA (Basic Service Area).&#x20;

Each BSS is uniquely identifying using an ID called BSSID (Basic service set identifier). BSSID is the mac address of AP being associated with BSS and this mac address of AP is used to identify BSS. It is mostly used at small offices or homes because of its low range of the network.&#x20;

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20201105114401/fffd.png" alt=""><figcaption></figcaption></figure>

{% columns %}
{% column %}
{% hint style="success" %}
#### Advantages

1. BSS is a small range network therefore it is more secure.
2. Devices or computers communicate easily with each other without any problem.
3. AP also manages all stations within this network and thereby making the network more portable and manageable.&#x20;
{% endhint %}


{% endcolumn %}

{% column %}
{% hint style="danger" %}
#### Disadvantages

1. BSS only contains one AP therefore it does not support mobility i.e., clients cannot move freely from one place to another.
2. It only provides short-range wireless communication.&#x20;
3. As BSS includes only one AP and many devices or clients or stations, every station or client shares or communicates through the same medium. This can create some issues or problems while transmission. Therefore, it is recommended that BSS should include only a limited number of devices.
{% endhint %}
{% endcolumn %}
{% endcolumns %}

### Applications and Use-Cases of Basic Service Set

* **Networking in Homes and Offices:** BSS is frequently utilized in homes and workplaces to provide wireless connectivity for gadgets like laptops, tablets and smartphones.
* **Public Wi-Fi Hotspots:** BSS is frequently used in public spaces like airports, cafes and libraries to give patrons wireless internet access, resulting in the creation of Wi-Fi hotspots.
* **Enterprise Networks**: BSS is used by big businesses to set up wireless networks in their office buildings so that workers and their gadgets may connect seamlessly.
* **Education Institutions:** BSS is used to provide wireless connectivity for workers, instructors, and students in educational institutions including schools and universities.
* **Smart Homes:** By enabling wireless connectivity, BSS plays a crucial role in the deployment of IoT (Internet of Things) and smart home gadgets.

### Future Trends and Developments in Basic Service Set Technology

* **5G Integration:** As 5G networks grow, there might be a greater degree of coordination and integration between 5G and BSS technologies, enabling smooth connectivity changes and enhanced performance.
* **Edge Computing**: By enabling more processing to take place closer to the network edge, edge computing's rise may have an impact on BSS. Applications that rely on BSS may run better and experience lower latency as a result.
* **IoT Integration:** As Internet of Things (IoT) devices proliferate, BSS technology may advance to better accommodate their varied communication patterns and high bandwidth needs.
* **AI Optimization:** By incorporating AI algorithms into BSS management, network parameters may be dynamically optimized, improving user experience and maximizing resource efficiency.
* **Multi-Access Edge Computing (MEC):** By combining MEC and BSS, processing power at the network edge may be increased, allowing for a low-late applications and services.
