---
description: CHALLENGE#3
---

# III CLI commands cheatsheed

{% hint style="info" %}
#### Command format

<kbd>order no. ROUTER# short command (long command)</kbd>

The original command precept is in parentheses, although the short lefter version is usually used. Choose one, not both!\
On the other hand, any modification will be visible in the summary of the router settings:

<kbd>ROUTER# show running\_conf</kbd><br>
{% endhint %}

1. ### DHCP Relay (DHCP service not in router)

TO DISTRIBUTE THE IP POOL ON THE DESIRED INTERFACE (SUCH AS ETH, VLAN OR BRIDGE)

```powershell
ROUTER> en (enable)
ROUTER# conf t (configure terminal)
ROUTER(config)# int g0/1.10
ROUTER(config-if)# ip helper-address 172.16.0.2
```

{% columns %}
{% column %}
<figure><img src="../../.gitbook/assets/irudia (6).png" alt=""><figcaption></figcaption></figure>


{% endcolumn %}

{% column %}
{% hint style="success" %}
## Issue

Indicate the address from which the POOL or DHCP IP beam corresponding to each of the subinterfaces included in the router will be distributed.
{% endhint %}

{% hint style="danger" %}
Remember to remove the STATIC on the computer in the IP configuration section and choose DHCP option instead.
{% endhint %}

{% hint style="danger" %}
Remember the server also needs its own IP in the network (i.e. `192.168.1.253/24`).
{% endhint %}


{% endcolumn %}
{% endcolumns %}

2. ### DHCP service on Router

TO DISTRIBUTE THE IP POOL ON THE DESIRED INTERFACE (SUCH AS ETH, VLAN OR BRIDGE)

```
ROUTER> en (enable)
ROUTER# conf t (configure terminal)
ROUTER(config)# ip dhcp pool VLAN10
ROUTER(config)# network 192.168.10.0 255.255.255.0 
ROUTER(config)# default-router 192.168.10.1
(ROUTER(config)#dns-server 1.1.1.1)
ROUTER(config)# ip dhcp excluded-address 192.168.10.1
```

{% columns %}
{% column %}
<figure><img src="../../.gitbook/assets/irudia (4).png" alt=""><figcaption></figcaption></figure>
{% endcolumn %}

{% column %}
{% hint style="success" %}
Indicate the address from which the POOL or DHCP IP beam corresponding to each of the subinterfaces included in the router will be distributed.
{% endhint %}

{% hint style="danger" %}
Remember to remove the STATIC on the computer in the IP configuration section and choose DHCP option instead.
{% endhint %}
{% endcolumn %}
{% endcolumns %}

3. ### Filling Routing tables

A JUMP FROM THE ROUTER TO ROUTE PACKETS TO NETWORKS BEYOND IT (NEXT HOP)

```
ROUTER> en (enable)
ROUTER# conf t (configure terminal)
ROUTER(config)# ip route 192.168.25.0 255.255.255.0 192.168.21.1
```

{% hint style="success" %}
Any <kbd>192.168.25.0/24</kbd> network request not recognized by the router is addressed to the issued interface (NEXT HOP).
{% endhint %}

4. ### Router on-a-stick (sub-interfaces)

A SINGLE ROUTER INTERFACE DIVIDED INTO SOME VLAN NETWORKS

{% hint style="danger" %}
This is the only configuration that is mandatory to be done on CLI!
{% endhint %}

```
ROUTER> en (enable)
ROUTER# conf t (configure terminal)
Router(config)# interface f2
Router(config-if)# no ip address
Router(config-if)# exit 
Router(config)# interface f2.1
Router(config-if)# encapsulation dot1q 10
Router(config-if)# ip address 172.16.10.1 255.255.255.0
Router(config-if)# exit 
Router(config)# interface f2.2
Router(config-if)# encapsulation dot1q 202
Router(config-if)# ip address 172.16.20.1 255.255.255.0
Router(config-if)# exit
```

{% hint style="success" %}
The `FastEthernet2` or `f2` interface has been split into two to have a connection to two subnets through a single interface or cable. Each of them has subsequently been assigned an IP in the range of that vlan.
{% endhint %}

5. ### VLAN creation and assignation to intended interfaces

```
Switch1> en (enable)
Switch1# conf t (configure terminal)
Switch-1(config)# interface range f0/0 -15
Switch-1(config-if-range)# switchport
Switch-1(config-if-range)# switchport mode access
Switch-1(config-if-range)# switchport  access vlan 10
Switch-1(config-if-range)# exit
Switch-1(config)# interface range f0/16 -31
Switch-1(config-if-range)# switchport
Switch-1(config-if-range)# switchport mode access
Switch-1(config-if-range)# switchport  access vlan 20
Switch-1(config-if-range)# exit
Switch-1(config)# interface range f0/32 -47
Switch-1(config-if-range)# switchport
Switch-1(config-if-range)# switchport mode trunk
Switch-1(config-if-range)# switchport  trunk native vlan 30
Switch-1(config-if-range)# switchport  trunk allowed vlan 10,20,30
Switch-1(config-if-range)# exit

```

{% hint style="success" %}
Interfaces are set as **access (single)** or **trunk (any)** depending in the VLANs they will manage.&#x20;
{% endhint %}

6. ### Bridge-group

Cut the connection to a network (or VLAN) using its IP/interface/range

```
Router> enable
Router# configure terminal

! IRB zerbitzua eta zubiaren protokoloa aktibatu
Router(config)# bridge irb
Router(config)# bridge 1 protocol ieee
Router(config)# bridge 1 route ip

! EZKERREKO ALDEA: PC0 eta PC1 dauden switch-era doan portua
Router(config)# interface gigabitEthernet 0/1
Router(config-if)# no shutdown
Router(config-if)# bridge-group 1
Router3(config-if)# exit

! ESKUINEKO ALDEA: Switch0-ra doan VLAN 10eko azpi-interfazea
Router(config)# interface gigabitEthernet 0/0.10
Router(config-subif)# encapsulation dot1Q 10
Router(config-subif)# bridge-group 1
Router(config-subif)# exit

! BVI interfazea konfiguratu
Router(config)# interface bvi 1
Router(config-if)# ip address 192.168.10.1 255.255.255.0
Router(config-if)# no shutdown
Router(config-if)# end

! Konfigurazioa memorian gorde
Router# write memory

Router# show bridge
```

{% hint style="success" %}
Cisco bideratzaile batean (Router) bi interfaze fisikok (edo azpi-interfazek) zubi baten moduan jokatu dezaten eta IP rango bera partekatu dezaten, IRB (Integrated Routing and Bridging) protokoloa aktibatu behar da.
{% endhint %}

{% hint style="danger" %}
Interfaze fisikoak zubi-taldean daudenez, ezin zaie IP helbiderik jarri. Horren ordez, BVI (Bridge Virtual Interface) izeneko interfaze birtual bat sortzen da. Interfaze honen IPa izango da VLAN 10eko ordenagailu guztien Gateway (Atebidea).
{% endhint %}

6. ### Access Lists (ACL)

Cut the connection to a network (or VLAN) using its IP/interface/range

```
ROUTER> en (enable)
ROUTER# conf t (configure terminal)
Router(config)# ip access-list extended EXAMPLE_NAME
Router(config)# deny ip 172.16.20.0 0.0.0.255 192.168.25.0 0.0.0.255 
Router(config)# int g0/1.20 (interface gig0/1.20)
Router(config-subif)# ip access-group EXAMPLE_NAME in
```

{% hint style="success" %}
Azalpena: Sarbide zerrenda arruntak 1-99 bitartekoak dira. Norberak definitzekoak 100etik aurrerakoak lirateke. Kasu honetan trafiko guztia ukatzen zaio ezarpen hau jasotzen duena azpisareari.&#x20;



Hirugarren pausoa exekutatzean erantzun hau espero behar da: &#x20;

<kbd>%sys-5-CONFIGI: Configured from coshow access-lists …</kbd>&#x20;

<kbd>Extended IP access-list 101</kbd>

<kbd>10 eny ip any any</kbd>
{% endhint %}
