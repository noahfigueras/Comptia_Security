# Securing Individual Systems
We are going to learn different attacks hackers can use to penetrate your system and how to defend them.  

## Denial of Service 
The whole idea behind this attack is to deny a service, in order to do that we try to connect as many people as we can to a server until it collapses and can't handle anybody else.  
### DOS Attack types  
* **Volume attack**
	* We try to overwhelm the machine sending a lot of requests.  
	* **Ex:** Ping flood, UDP flood.

* **Protocol attack**
	* It is performed by sending a lot of SYN packets to the server until the last one doesn't respond anymore and it is the most common DOS attack we have today.

* **Application attack**
	* We take advantage of some problem happening inside an application.
	* *Slow Loris Attack* is an example in which we keep sending requests to a server but not responding them. 

* **Amplification attack**
	* *Smurf attack*, sending an ICMP packet to server is going to do a lot of other systems connected to the network communicate with the original server to see what is going on (we amplify a request).  

* **DDOS - Diistributed Denial of Service Attack**
	* A lot of computers infected by Malware, *Zombies*, send a lot of requests at the same time to a Server. These are called *BotNets* and they are controlled by a single computer.  

## Host Threats
**Spam:** Unsolicited email from third party services.  
**Phishing & Spear fishing:** Unsolicited email from individuals with malicious intent in order to get some kind of private information from a person.  
**Spim:** Using instant messaging to spam.  
**Vishing:** Spam trying to get private information via phone calls.  
**Clickjacking:** Malicious clickbait links on the internet.  
**Domain Hijacking:** People steal your domains and they ask a lot of money from you to get it back.  
**Privilege Escalation:** Get more privileges in a system in order to do evil or malicious stuff.   

## Man in the Middle
A man in the middle (MITM) attack is one where the attacker (in our example, Mallory) secretly captures and relays communication between two parties who believe they are directly communicating with each other (in our example, Alice and Bob).  

![alt text](https://witestlab.poly.edu/blog/content/images/2016/03/mitm-illustration.svg)  

### How to perform an MITM attack with ARP spoofing over a wireless network  

1. Setup ip forwarding on KALI Machine.
	* The ip_forward file is set to 0 by default and we have to change it to 1.  
	`echo 1 > /proc/sys/net/ipv4/ip_forward`  
2. Know our default gateway or ip address of our router.  
	`ip route`
3. Know the interface on which we are going to perform this attack.  
	`if config` (in our case is wlo1)  
4. Start the attack with arpspoof.  
	`arpspoof -i [interface] -t [ipTarget] -r [defaultGateway]`  
5. Sniff information with Wireshark.  

[See More complex example](https://www.youtube.com/watch?v=7PqMPhItKPM)  



