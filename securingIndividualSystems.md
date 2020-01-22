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
    
