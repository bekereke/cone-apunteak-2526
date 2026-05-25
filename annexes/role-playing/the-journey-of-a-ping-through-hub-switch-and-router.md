# The Journey of a Ping through Hub, Switch and Router

### 🎯 Objective

> You will simulate how a **ping** travels through a local network that includes **hubs, switches, and a router**, so you can understand the differences in how each device handles traffic.

***

### 🚀 Dynamic

A device will be assigned to each team member. From the source provided by the teacher, or through your own search, you will obtain information about the device and individually investigate how to perform its role. Then the "expert meeting" will be conducted and the corresponding device expert from each group will meet with equals from the rest of the groups. You will combine the information you have at your disposal and agree on the most important features. Each member of the group will return to the group and explain to the rest of the group the device they expertise and each will make their own annotations in their digital notebook.

Then, you will be ready to become the classroom a network!

***

### 👥 Roles

* **PC1** (192.168.1.10) – Initiates the ping.
* **Hub1** – Forwards all traffic to every connected device.
* **Switch1** – Learns MAC addresses and forwards packets intelligently.
* **Router** (Gateway 192.168.1.1 / 192.168.2.1) – Forwards packets between two different networks.
* **Switch2** – Same as Switch1, but on the destination network.
* **Hub2** – Same as Hub1, but on the destination network.
* **PC2** (192.168.2.20) – Destination of the ping.
* **Packets** – Students carrying signs that say **ARP Request**, **ARP Reply**, **ICMP Echo Request**, **ICMP Echo Reply**.

***

### 📂 Simplified schema

```
PC1 ---- Hub ---- Switch ---- Router ---- Switch ---- Hub ---- PC2
```

* **PC1** and **PC2**: computers that will make the ping.
* **Hub**: commits _flooding_, since it sends all the packets to every port available.
* **Switch**: learns MAC table, so forwards straight to the correct port.
* **Router**: forwards using IP (in case of different subnets).

***

### 🧰 Materials

* Signs for each role: **PC1, PC2, Hub1, Hub2, Switch1, Switch2, Router, ARP, ICMP Request, ICMP Reply**
* MAC address labels (students wear them on their chest)
* Cards with sentences like **“Flooding”** or **“Learned the MAC address”** for switches/hubs to hold up
* A small box or envelope to symbolize the **packet**

***

### 🧩Possible questions for an AI

* I'm asked to play an object as a character in role playing game at class. Mine is \_\_\_\_\_\_\_\_\_\_\_.&#x20;
* What should I know about the device?&#x20;
* Which is its input, process and the output?&#x20;
* What I'm supposed to do?
* What is it? What is it used for?&#x20;
* How could I disguise? Which material should I use?
* Does the device assigned to me have a symbol?&#x20;

<details>

<summary>Printables</summary>

## 🖨️ **Role Play Cards – Local Network Simulation**

#### 💻 Computers

**PC1**

```
💻 PC1
IP: 192.168.1.10
MAC: 0A:1B:2C:3D:4E:01
```

**PC2**

```
💻 PC2
IP: 192.168.2.20
MAC: 0A:1B:2C:3D:4E:02
```

#### 🔌 Hubs

**Hub1**

```css
🔌 HUB 1
"I send packets to ALL ports"
(Flooding)
```

**Hub2**

```
🔌 HUB 2
"I send packets to ALL ports"
(Flooding)
```

#### 🔀 Switches

**Switch1**

```
🔀 SWITCH 1
"I learn MAC addresses"
"I forward packets only to the right destination"
```

**Switch2**

```
🔀 SWITCH 2
"I learn MAC addresses"
"I forward packets only to the right destination"
```

#### 🌐 Router

**Router**

```
🌐 ROUTER
Gateway: 192.168.1.1 / 192.168.2.1
"I look at IP addresses and
forward packets between networks"
```

#### 📡 ARP

```
📡 ARP MESSAGE
"Who has 192.168.2.20?
Tell 192.168.1.10"
```

#### 📦 Packets (Ping)

**ICMP Request**

```
📦 ICMP REQUEST
"Ping: Are you there?"
```

**ICMP Reply**

```
📦 ICMP REPLY
"Pong: Yes, I’m here!"
```

***

👉 Recommendation:

* Print on A4 or A3.
* Use **different colors**: Blue (PCs), Yellow (Hubs), Green (Switches), Red (Router), Orange (Packets).
* Attach with string or lanyard so students can wear them.

</details>

<details>

<summary>Script</summary>

### 🎬 Process

#### 1. Introduction

* The teacher explains:\
  “You are all parts of a local network. Each one of you has a role: computer, hub, switch, or router. We’re going to simulate what happens when PC1 pings PC2.”

***

#### 2. ARP Discovery

* **PC1**: “I want to ping PC2, but I don’t know its MAC address. I’ll send an ARP request!”
* **Hub1**: “I’m a hub, I send this message to EVERYONE.”
* **Switch1**: “I don’t know the address yet, so I’ll flood all my ports.”
* **Router**: “I know where PC2 is. Here’s my MAC address!”
* **Switch1**: “I’ve learned that the Router is connected to this port.”

***

#### 3. Sending the Ping Request

* **PC1**: “Now I can send the ICMP Echo Request!”
* **Packet (ICMP Echo Request)** walks across the network.
* **Hub1**: “I flood it to everyone.”
* **Switch1**: “I know the Router’s port, so I’ll send it directly.”
* **Router**: “I’ve received the packet. The destination IP is 192.168.2.20. That’s on another network, so I’ll forward it to Switch2.”

***

#### 4. Packet Reaches the Destination

* **Switch2**: “First time seeing this packet, I’ll flood it.”
* **Hub2**: “I flood it to all devices connected to me.”
* **PC2**: “This one is for me! I’ll respond with an ICMP Echo Reply.”
* **Packet (ICMP Echo Reply)** is created.

***

#### 5. Returning the Reply

* **Hub2**: “I flood the reply to everyone.”
* **Switch2**: “Now I’ve learned where PC2 is, so I’ll forward directly to the Router.”
* **Router**: “I’ll send this reply back through Switch1.”
* **Switch1**: “I know PC1’s port, I’ll send it directly.”
* **Hub1**: “I flood it to everyone, but PC1 receives it.”
* **PC1**: “Ping successful! I got the reply.”

</details>

<details>

<summary>Abbreviated process</summary>

#### Ping process (PC1 → PC2)

1. **PC1**: "Ping egin nahi dut PC2-ra (192.168.2.20)".
2. **ARP**: PC1-ek ez daki PC2-ren MAC, broadcast egiten du.
3. **Hub1**: broadcast jaso eta **denei** bidaltzen die.
4. **Switch1**: flooding egiten du, baina gero ikasten du zein portutik erantzuten duen router-ak.
5. **Router**: "Ni naiz PC2 dagoen sarearen gateway-a. Hona hemen nire MAC helbidea".
6. **Switch1**: orain badaki router MAC hori zein portutik bidali behar duen.
7. **PC1**: ICMP request sortzen du.
8. **Hub1**: paketea berriz denei bidaltzen die.
9. **Switch1**: paketea zuzenean router-era bidaltzen du.
10. **Router**: jasotzen du ICMP request eta IP helbidea begiratzen du. Bidali behar du bigarren switch-era.
11. **Switch2**: flooding egiten du lehen aldiz, gero ikasten du.
12. **Hub2**: jasotzen du paketea eta denei bidaltzen die, PC2 barne.
13. **PC2**: jasotzen du ICMP request → erantzuna prestatu: ICMP reply.
14. Bidea alderantziz egiten du (PC2 → Hub2 → Switch2 → Router → Switch1 → Hub1 → PC1).
15. **PC1**: "Ping arrakastatsua!"

</details>

{% hint style="success" %}
### Debriefing

* What is the difference between a **hub** and a **switch**?
* Why do we need a **router**?
* What does a switch do when it doesn’t know the destination MAC address?
{% endhint %}
