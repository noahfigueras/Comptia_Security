# The Basic LAN

## LAN Review
LAN = Local Area Network.  

### Switches
Switches filter and forward data based on MAC addresses (Layer 2). And we are going to review some of it's most important concepts.  
1. **VLAN:** provides layer 2 separation of networks and we can have multiple VLAN in a switch and specify which ports we want to use for that specific Network. With VLAN we can create separate networks from a single switch.  

2. **STP (Spanning Tree Protocol):** We enable STP or RSTP in a switch in order to prevent loop floods. 

### Routers
Routers filter and forward information based on IP adresses (Layer 3) and they are going to act as the gateway or interface between different network IDs.  

## Network Topologies Review
A network topology is the organization of a network in terms of how is the data moving around that network.  
**LAN:** A bunch of computers connected to a Broadcast Domain or Switch.  
**WAN (Wide Area Network):** At least two LANs connected together and at least one router.  
**MAN (Metropolitan Area Network):** A bunch of WANs that are connected together throughout a city.  
**TCP/IP:** Protocol that runs the internet.  
**Intranet:** Private network which still runs on TCP/IP.

## Network Zone Review
**DMZ (Demilitarized zone):** It is a secure way to structure all of our systems in a organization and the structure is the following:                              
LOCAL AREA NETWORK -> ROUTER + (FW) -> WEB,FILE,VPN SERVERS -> GATEWAY ROUTER + (FW)-> INTERNET  
**FW** = FIREWALL  
**Wireless Networks:** Plugin a ethernet cable from our main switch in a LAN to a Wireless access point (WAP), is going to provide us with a zone with access to that LAN wirelessly.  
**Guest Network:** It is always going to run in a separate VLAN and it is designed and protected for guests to not be able to access any information of the network.  
**Virtualization:** Creating a LAN network with virtual computers.  
**Airgap:** Disconnection between networks to provide full isolation.  

## Network Access Controls
**Point to Point Protocol (PPP):** The first internet protocol with very weak authentication.  
**EAP Extensive Authentication Protocol:** A framework which was developed as an extension to improve the authentication of PPP. It has different methods: *EAP-MD5, EAP-PSK, EAP-TLS, EAP-TTLS*.  

## The Network Firewall

**Stateless Firewall:** It is going to block connections for a specific address, ip, port, conexion, etc. And it is going to be specified in a file called Access Control List.  
**Stateful Firewall:** Looks at what is going on and then makes a decision of what is going to do. It is based on behavior more than rules.  
**Application-based firewall:** Usually used to protect servers (designed to protect single applications).  

## Proxy Servers
A Proxy is a box/piece of software running on a computer which acts as an intermediary between two different devices having a session. Proxy is application specific, so there is Web proxy, FTP proxy, Vo1p proxy, etc. There is two kinds of proxy servers: *Forward proxy servers* and *Reverse proxy servers*:  

* **Forward proxy:** In this case the client speaks to the proxy and the last one establishes communication with another server.  
**Ex:** CLIENT -> **PROXY** -> FIREWALL -> INTERNET -> SERVER  
There is also a **modern forward proxy** that is used for people who want to be more anonymous and it connects to a proxy through the internet (that proxy can be in another state or country).  
**Ex:** CLIENT -> INTERNET -> **PROXY** -> FIREWALL -> SERVER (in this case if we want it even more secure, we can encrypt our communication from the client to the proxy with a **VPN**).  

* **Reverse proxy:** This server is specific for web servers or servers in general, and the proxy protects the main server from possible DOS attacks, it is also used for load balancing (if you have more than one server will balance the information through all of those), Catching, encryption acceleration.  
**Ex:** SERVER -> **PROXY** -> FIREWALL -> INTERNET -> CLIENT

## Virtual Private Network 
VPN directly connects into the network from a remote location, fully functional.  
**Connection Options for VPN**  
* Leased Line (cable) and it is very expensive.
* Via public network, virtualized (internet). 

**VPN Tunnel:** Connection between two VPN endpoints.  

* There is two types of VPNs: **remote access** and **site to site**.

## IPSEC
Internet Protocol Security is a secure network protocol that authenticates and encrypts the packets of data to provide secure encrypted communication between two computers over an Internet Protocol network. It is used in VPNs.  

Ipsec runs in two very different modes: 
1. **Authentication headers:** It only provides integrity, it adds an Authetication header to the packet before sending it (HMAC). 
2. **Encapsulating Security Payload:** It encrypts the packet before sending them and also adds the authentication header.  

* If we keep the original IP adresses, we are using **transport mode** and does not work very well in the real world that is why we use **Tunnel mode**.  
**Tunnel mode:** we replace the original IP for a new one in the packet. It is commonly used with ESP as well, injecting the new IP adress as a header in the encrypted packet.  

**IPSec Protocol Suite**  
* Uses negotiation protocol **ISAKMP**.
 * Initial authentication.
  * Certificates.
  * Preshared keys.
  * Key Exchange.
  
**IPSEC is commonly used in VPNs and there's used in two ways: Pure IPSEC and IPSEC with L2TP**  

## NIDS/NIPS
This means Network Intrusion Detection/Prevention System. Detection means that it alerts somehow of an intrusion. Prevention instead, detects if something is happening but also tries to stop it one way or another.  

### NIPS Detection
* Active.
 * Blocks from router.
* Detection methods.
 * Behavioral/anomaly.
 * Signature-based (Pre-made instructions).
 * Rule-based.
 * Heuristic.
  * Combines anomaly and signature.
  
## SIEM 
Security Information and Event Management, it is a type of software that is going to help us monitor all of our network to check the performance.  


  
 



