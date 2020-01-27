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
	 The ip_forward file is set to 0 by default and we have to change it to 1.  
	`echo 1 > /proc/sys/net/ipv4/ip_forward`  
2. Know our default gateway or ip address of our router.  
	`ip route`
3. Know the interface on which we are going to perform this attack.  
	`if config` (in our case is wlo1)  
4. Start the attack with arpspoof.  
	`arpspoof -i [interface] -t [ipTarget] -r [defaultGateway]`  
5. Sniff information with Wireshark.  

[See More complex example](https://www.youtube.com/watch?v=7PqMPhItKPM)  

## System Resiliency
It is the ability to defend a system from a possible incident that may happen.  
**Scalability and Elasticity:** If the webserver starts to get a lot of requests, we are going to need more servers ready in order to prevent a crash. Also, if we know that a particular day we are going to have a lot of traffic coming through our website is good to have the ability to scale and reduce servers as we need.  

**Redundancy:** Is a form of distributive allocation. Ex: Distributing servers around different places in the US.  

**Non-persistence:** Data that is collected but will not be saved on restart.  
**Examples:** Backups, Systems Snapshots, updates removal ... 

## RAID - Redundant Array of Independent Disks
* RAID arrays enable you to speed up data access, protect data, or both.  
* The most common RAID styles includes 0,1,5, & 10.  
* RAID 1 & RAID 0 requires at least 2 drives, RAID 5 requires 3 or more drives, & RAID 10 requires 4 drives.  

## NAS AND SAN
Those two technologies are designed to store data. They have dedicated systems that only share data.  

**Network attached storage:** File-level computer data storage server connected to a computer network providing data access to a heterogeneous group of clients. NAS is specialized for serving files either by its hardware, software, or configuration.  

**Storage area network:** A Storage Area Network (SAN) is a specialized, high-speed network that provides block-level network access to storage. SANs are typically composed of hosts, switches, storage elements, and storage devices that are interconnected using a variety of technologies, topologies, and protocols. SANs may also span multiple sites.

A SAN presents storage devices to a host such that the storage appears to be locally attached. This simplified presentation of storage to a host is accomplished through the use of different types of virtualization.

## Physical Hardening
### Removable media control
Optical media can be very dangerous as someone could insert some evil CD into your computer and load some malicious software into the system. Fortunately for us, we can configure our systems to control what the optical media system can and can't do. There is different ways to set this up on different OS and we can set it up to not work for the whole OS or just banned some particular users.  

### Data Execution Prevention (DEP)
DEP is a security feature that can help prevent damage to your computer from viruses and other security threats. Harmful programs can try to attack Windows by attempting to run code from system memory locations reserved for Windows and other authorized programs.  

### Disabling ports
In order to do that we are going to disable the ports through the UFI BIOS of the computer. In the peripherals window we can disable the USB ports and almost every port in our computer.

## RFI, EMI and ESD 
### Radio Frequency Interference & Electromagnetic Interference 
Radio radiation and Electromagnetic signals can cause some interference on our systems. That's why we should always connect them in different circuits or separate them so there is no interference at all.

### Electrostatic Discharge 
We can suffer from a Discharge if there is an over power circuit. So always use wrist band circuits and materials in order to prevent that to happen. Also, it is very important to use the right voltagees to power electronic equipments.  

## Host Hardening
### Disabling Services
Disabling unnecessary services that we don't use on our system is one of the good practices of a good system administrator. As, some malicious people can get into your system through those open services.  

### Default passwords
It is very important to not use default passwords as bruteforcing cracking lists can discover those very quickly. Not only on the OS, change all default passwords on routers, ip cameras, devices...  

### Disabling unecessary accounts 
If we don't use an account anymore just delete it and it will avoid one more way for people to hack into it.  

### Patch Management 
1. Monitor: Always keep up to date for the new patches that are coming out for OS, software, hardware ...
	* Might not get reminders.
2. Test
	* Deploy the system in sandbox environment to test if the patch works good first.
3. Evaluate 
4. Deploy patch
	* Watch for scheduling issues.
5. Document
	* Always document all of the changes that we are going to make in all of the computers we manage.

### Anti-malware 
Always make sure we have an alti malware installed on our computer and up to date with all the possible attacks that might happen.  
* Training for our users
* Procedures 
	* Teach best practices for users and they have to learn how to detect malware if it happens.
* Monitoring
	* Watching our security logs, dns, IDS (Intrusion Detection System can help detect threats to the hosts).
	* But if we want to get serious about it is better to get a Third-party anti-malwere.

### Firewall
Every computer in our network should have a firewall. Many corporations have a whitelist and a blacklist of applications you can and can't install and use for security reasons.  

## Data and System Security 
1. Always make sure we have data integrity, like backups so if something happens to our system we don't lose that data.
2. Speed/quick access.
3. High availability.

**RAID** it is a grate way to secure data and it is fairly cheap. The only disadvantage is that if the OS blows up we are going to lose the data.  

**Clustering** you have a lot of computers sharing the data and if one dies, you don't lose the data because another computer will have it.  

**Virtualize a server** is a really good option to secure data because we can save a snapshot of the system and if something goes wrong we can always go back to the previous update.

## Disk Encryption
Encrypt the data that is stored in our massed storage, but this is going to slow down your system.  
**Recommended on:**  
* Mobile and portable devices (Laptops, smartphones,tablets).
* Desktop systems with limited security.  

Disk encryption can be broken into two groups: *TPM & NON-TPM*.  
Two examples of disk encryption programs are *BitLocker* and *FileVault*.  

## Hardware and Firmware Security

### Full Disk Encryption (FDE)
It is a methodology to encrypt all our mass storage to secure our Data. *BitLocker* is a software that we can use in a Windows OS to encrypt a full Disk.  

### Secure Boot
Checks the performance of every hardware, software and firmware every time we log in to a system to check performance and possible errors in order to boot up.  

### Hardware security module
It is a piece of hardware that takes care of the sign in on your system.

## Secure OS Types
1. Server OS.
	* Bulit-in functionality.
	* Connections.
2. Workstation.
	* Desktop version (Windows 10, Ubuntu, MacOS).
	* Workhorse.
3. Embedded systems.
	* Appliance.
	* Own OS.
4. Kiosk.
	* Limited function (Small versions of linux most of the time).
5. Mobile OS.
	* Apple.
	* Android.
	* Mobile devices Operating Systems.

**In order to choose one of those types of Operating Systems always go with the one who has the least amount of functionality but enough to perform their job.**  

## Securing peripherals

### Wired vs Wireless peripherals
**Bluetooth**  
* *Bluejacking* is the idea of connecting into a Bluetoth device.
* *Bluesnarfing* means connecting in to a bluetooth device to steal data.  
In order to prevent that if you don't use bluetooth simply don't enable it in your device.  

**WPS**  
It is a technology that allows to connect to the router pressing a single button using wpa2 encryption.  

**Hidden Wi-fi**  
Sometimes printers and other devices have SD slots to store information. But there are different types of SD cards an not all of them are used to store data. There is SD wifi cards which are perfectly fine for someone to use it as a normal connection and steal data from all the new user who connect to it.  

**Displays**  
USB ports in displays can become a big problem as some evil person can plug a *Rubber Ducky* and steal a lot of information displaying on the screen.  

**Turn off non necessary ports for security and make sure always keep up to new updates and patches**  

## Malware 
Malicious software that is running on the background of your system without you knowing about it.  
**Virus:** Piece of software that gets into your computer through hardwere or internet.
* It will attach to other files.
* Will propagate.
* Spread to other devices.
* Activate.  
**Adware:** Programs that try to put adds on your computer like: pop-ups, links, etc.  
**Spyware:** Some form of malware that is hidden from you (we don't see it), but it is spying your system one way or another. Ex: seeing connections, what you type, camera, files, etc.  
**Trojan Horse & RATs:** Software running on your system that is doing something nice, but is running a malicious piece of code on the background.  
**Remote Access Trojans (RATs):** Trojan but it is controlled remotely and the evil person can turn it on and off.  
**Ransomware/Cryptomalware:** Type of malware that locks your system in some way that you can't get into it until you pay the evil people some money and they unlock it for you.  
**Logic Bomb:** Program that is sitting on a computer until is triggered by an event.  
**Rootkit:** Software that escalates privilages to execute other things on computer.  
**Backdoor:** Software that allows you to log in to the system remotely.
**Polymorphic malware, Keylogger & Armored Viruses:** Polymorphic malware changes itself, armored viruses are hard for anti-malware to detect, Keylogger collects information of the keys entered in a computer.  



	
	
