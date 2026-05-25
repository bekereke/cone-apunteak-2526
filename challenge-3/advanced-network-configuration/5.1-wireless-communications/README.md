# 5.1 Wireless Communications

> Wireless Communication is a method of transmitting data or information between two or more devices without the use of physical wires or cables. Instead of using cables, it uses radio waves (RF - Radio Frequency) or other types of electromagnetic waves to send signals through the air or free space.

### Wired vs Wireless Medium <a href="#wired-vs-wireless-medium" id="wired-vs-wireless-medium"></a>

A wired network is a bounded medium, where data travels along a predefined path such as cables or wires. While reliable, wired networks impose several restrictions in a modern environment where a large number of devices need to connect simultaneously.

* **Example:** If you wish to connect 10 or more devices around you, each device would require its own physical port - a highly impractical solution.
* This is where the wireless network shines.
* By eliminating the need for physical wiring, wireless communication offers mobility, convenience, and easy scalability.
* Multiple devices can connect to the network easily and simultaneously, simply by being within the wireless coverage area.

### Important Standards to Know <a href="#important-standards-to-know" id="important-standards-to-know"></a>

* Wired network comes under IEEE standard 802.3
* wireless network comes under IEEE standard 802.11

{% hint style="info" %}
The IEEE (Institute of Electrical and Electronics Engineers) is the organization responsible for developing and managing these standards.
{% endhint %}

### Basics of Wireless Communication <a href="#basics-of-wireless-communication" id="basics-of-wireless-communication"></a>

Wireless communication works by transmitting signals through free space using Radio Frequency (RF) waves. Here’s how it works:

* One device acts as the Transmitter, sending RF signals through an antenna.
* Another device serves as the Receiver, capturing the transmitted signals.
* Both devices must use the same frequency (or channel) for effective communication.

#### Key Constraint <a href="#key-constraint" id="key-constraint"></a>

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20250929110527657822/2.webp" alt="2" height="315" width="661"><figcaption><p>Unidirectional Communication</p></figcaption></figure>

{% hint style="info" %}
As the number of devices increases, the chances of interference rise significantly.&#x20;
{% endhint %}

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20250929110610523300/4.webp" alt="4" height="315" width="661"><figcaption><p>Bidirectional Communication</p></figcaption></figure>

When many wireless devices communicate simultaneously, their radio frequencies may interfere with each other, degrading performance.

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20250929110657996684/3.webp" alt="3" height="268" width="661"><figcaption><p>Interference from other devices</p></figcaption></figure>

### Shared Medium and Half-Duplex Operation <a href="#shared-medium-and-halfduplex-operation" id="shared-medium-and-halfduplex-operation"></a>

Much like wired devices share a common communication medium, wireless devices share airtime and bandwidth.\
To avoid signal collisions and interference:

* Wireless devices operate in half-duplex mode (cannot send and receive data at the same time).
* Before transmitting, devices follow the IEEE 802.11 standard procedure to check if the channel is free and available.

{% hint style="info" %}
While full duplex is theoretically possible (using separate frequencies for sending and receiving), typical wireless communication remains half duplex due to the use of the same channel.
{% endhint %}

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20250929110732527787/5.webp" alt="5" height="315" width="527"><figcaption><p>Half Duplex Operation</p></figcaption></figure>

### Understanding Radio Frequency (RF) <a href="#understanding-radio-frequency-rf" id="understanding-radio-frequency-rf"></a>

Wireless communication in free space relies on the generation of electromagnetic waves:

1. The Transmitter sends an alternating current into an antenna, generating moving electric and magnetic fields.
2. These fields propagate as travelling waves, with the electric and magnetic fields moving at right angles to one another.
3. To sustain the wave propagation, the current must alternate cyclically.

The Frequency of a wave refers to the number of cycles the wave completes in one second, calculated as: `Frequency (Hz) = Number of cycles per second`

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20250929110805981426/1.webp" alt="1" height="400" width="661"><figcaption><p>Wave Propagation with an Antenna</p></figcaption></figure>

{% hint style="info" %}
Antennas in our daily lives send out Electromagnetic waves in all directions, like the waves travelling in water when a stone is dropped in a water body.&#x20;
{% endhint %}

#### Frequency Unit Names <a href="#frequency-unit-names" id="frequency-unit-names"></a>

| Unit      | Abbreviation | Meaning             |
| --------- | ------------ | ------------------- |
| Hertz     | Hz           | Cycles per second   |
| Kilohertz | kHz          | 1000 Hz             |
| Megahertz | MHz          | 1, 000, 000 Hz      |
| Gigahertz | GHz          | 1, 000, 000, 000 Hz |

{% hint style="info" %}
Everyday devices like WiFi routers and Bluetooth gadgets operate in the MHz and GHz frequency ranges.
{% endhint %}
