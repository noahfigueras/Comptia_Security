# Tools Of The Trade

## OS Utilities
**ping:** We use ping to send a request to another server to see if everything is working right (recieves and responds to request). **Ex:** `ping www.google.com`. Sometimes if we get an ipv6, we can force it to connect on ipv4 with `ping www.google.com -4`.  

**netstat:** Prints information about the linux networking subsystem. If we need to know what sessions a particular host is running at  every given moment this is our tool.  
	`netstat -n` (check which network connections my system is establishing)  
	`netstat -a` (show me all opening ports including the ones not connected)  

**traceroute:** The traceroute command maps the journey that a packet of information undertakes from its source to its destination. One use for traceroute is to locate when data loss occurs throughout a network, which could signify a node that's down. `traceroute www.google.com`  

**arp:** manipulates the System’s ARP cache. It also allows a complete dump of the ARP cache. ARP stands for Address Resolution Protocol. The primary function of this protocol is to resolve the IP address of a system to its mac address, and hence it works between level 2(Data link layer) and level 3(Network layer). `arp -a` (hostname).  

**ip or ifconfig:** Take a look at your network system `ip addr`.  

**nslookup or dig:** command allows you to display information that you can use to diagnose Domain Name System (DNS) infrastructure.  

**netcat:** can open and listen to ports, and can be an aggressive tool for reconnaissance.

## Network Scanners

**nmap:** is a free and open-source network scanner used to discover hosts and services on a computer network by sending packets and analyzing the responses. 
Example -> `nmap --top-ports 20 192.168.1.106`

## Protocol Analyzers
The tools that we use to analyze the network traffic coming in and out of a specific host computer.  

**wireshark:** Allows us to filter the data by services and protocols and there are two seperate pieces for every protocol analyzer:  

	* Sniffer (captures all data coming in/out of a particular interface).
	* Analyzer (analyzing the data)

Looking at a network analyzer we can look closely at an activity taking place with that session.

## SNMP - Simple Network Management Protocol
In an SNMP Network, there is a Managed Device which has an agent (software from the factory) that allows us to connect with the SNMP Manager to controll it. That is called a **Network Management Station**. The connections are made via UDP port 161 or TLS 10161 if encrypted.  

**Management Information Based (MIB):** It is a database that has the Managed Device in order to know the functions that can do when told.

**Network communications**  
	* Get: We send some information to the device and it provides a response.
	* Trap: It is setup in the Manage device itself and if the action happens, the device will send information to the NMS.
	* SNMPWalk: Send a lot of get requests in a big batch.  

**SNMP Version 1 does not support encryption**  
**SNMP Version 2 added basic encryption**  
**SNMP Version 3 added TLS encryption**  

## LOGS
**Non-Network Events**  
	* Events that happen on a host even though it's not connected to a network. Mainly OS events or Apps running on the system.

**Network Event**  
	* Events that deals with the communication between the host and something on the network.
	

