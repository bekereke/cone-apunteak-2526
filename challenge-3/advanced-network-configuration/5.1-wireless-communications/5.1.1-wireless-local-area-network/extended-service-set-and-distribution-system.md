# Extended Service Set and Distribution System

ESS connects multiple BSSs and consists of several BSS cells, which can be interlinked through wired or wireless backbones known as a distributed system. Multiple cells use the same channel to boost aggregate throughput to network. The equipment outside of the ESS, the ESS and all of its mobile stations comprise a single MAC layer network where all stations are virtually stationary. Thus, all stations within the ESS appear stationary from an outsider's perspective.

Other components include:

* **Distribution System (DS):** Links APs within the ESS.
* **Portal:** Serves as a gateway to other networks.

<figure><img src="https://media.geeksforgeeks.org/wp-content/uploads/20231018194111/Blank-diagram-(3).png" alt="Architecture for IEEE 802.11 Configuration" height="776" width="1040"><figcaption><p>Architecture for IEEE 802.11 Configuration</p></figcaption></figure>

* **Roaming:** In an environment with multiple access points (like a large office building or campus), a device can move from the range of one AP to another and still maintain its connection. This is possible due to the underlying architecture of the IEEE 802.11 standard which allows for roaming between APs.<br>
* **Authentication and Association:** Before a station can send or receive data frames on a WLAN, it needs to establish its identity with an AP. This process is called authentication. After authentication, the station then establishes a data link-layer connection with the AP through a process called association.

