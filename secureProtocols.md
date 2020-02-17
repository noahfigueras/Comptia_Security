# Secure Protocols
## Secure Applications and Protocols
1. **SSH:** It's an encrypted application and it's used to log in into different servers and it exhanging a public and private key in order to authenticate.  
2. **TLS (Transport Layer Security):** It is a protocol that creates an encryption layer between the servers and the client requesting to visit the website, fixing the non-encrypted HTTP.    

## Network Models
**OSI Model**  
1. Physical Layer.
  * Ex: Types of Cables to use.
2. Data Link Layer.
  * Everything that works with a MAC adress.
3. Network Layer.
  * IP Adressees. Ex: Routers.
4. Transport Layer.
  * Assembles and disassembles packets. 
5. Session Layer.
  * Actual conexion between two systems like TCP.
6. Presentation Layer.
  * Used to convert data into a format that your applications can read.  
7. Application.  

**TCP/IP Model**  
1. Network Interface.
  * Covers all the physical cabling, MAC adresses, network cards, pretty much everything in terms of hardware.  
2. Internet.
  * This Layer is for anything it has to do with an IP adress, for example a router.  
3. Transport.
4. Application.  

## Know your Protocols
**IP adresses**  
* IPV-4 -> **EX.** 172.16.254.1
* IPV-6 -> **EX.** 2001:0DB8:85A3:0000:8A2E:0370:7334 (128 bits)  

**Private IP adress**  
1. Any IP adress that starts with the number **10**.  
2. Any IP adress that ranges from **172.16 - 172.31**.
3. Any IP adress that starts with **192.168**.  

**Transport Protocols**  
* **TCP:**  Connexion oriented type of protocol (client sends request to server and server sends response), can send a lot of packages and it is how the internet works. 
* **UDP:** Connectionless (sends one packet to the server with no response).  
* **ICMP:** supports TCP and UDP protocols, handles ARP and ping.  

## Know your Protocols - Applications
**Internet Protocols**  
* **HTTP:** Using TCP port 80, it is for unsecure websites.  
* **HTTPS:** Using TCP port 443, secure websites.  

**Remote Shell**  
* **Telnet:** Using TCP port 23, very insecure.  
* **SSH:** Using TCP port 22, secure shell.  

**File Transfer** 
* **FTP:** File transfer protocol using ports 20-21, completely insecure.  
* **FTP/SSH:** Using FTP over a SSH conexion using port 22.  
* **FTPS:** Using ports 20-21, using TLS encryption and it is very secure.  
* **SFTP:** SSH File Transfer Protocol uses port 22. 
* **SCP:** Secure Copy moves files across systems uses port 22. 
* **TFTP:** Trivial FTP uses UDP port 69.  
* **NETbios:** Using port 137,138,139 but more modern ones use SMB(running on port 445).  

**Mail**  
* **SMTP:** Simple Mail Transfer Protocol, uses port 25 (sends mail to other people).   
* **IMAP:** Internet Message Access Protocol (recieves mail), uses port 143.  
* **POP:** Older protocol but quite popular, uses port 110.  

**Others**
* **DNS:** Domain Name System, uses port 53.  
* **DHCP:** Dynamic Host Configuration Protocol, uses UDP port 67/68.
* **SNMP:** Simple Network Management Protocol, uses UDP ports 161/162.  
* **LDAP:** Light Weight Directory Access Protocol, uses port 389.  
* **RDP:** Remote Desktop Protocol, uses tcp port 3389.  

## Transport Layer Security
**SSL:** Secure Sockets Layer was developed to establish secure conexions between two points.  
**SSL/TLS are used in HTTPS**  

## Internet Service Hardening

**DNS**: Runs in port 53 and is a nonsecure protocol.  
**DNSSEC:** Use public and private key to connect and prevent the spoofing of packets from an evil person.  

**Always use secure protocols**  

## Protecting your servers 
Because encrypting&decrypting consumes a lot of cpu usage and can easily burn one, we are going to need to take some measures in order to prevent that.  

**SSL Accelerator Card:**  These cards instantly encrypts & decrypts asymmetric encryption.  
**Load Balancer:** Distributes all the requests coming from a website to different web servers to improve the performance.  
**DDOS Mitigator:** will send out an alert to emergency response services which assist in traffic flow to the site under attack.  

## Secure Code Development 
**Waterfall Model**  
1. Requirements.
2. Design.
3. Implementation.
4. Verification.
5. Maintenance. 

**Agile Methodology**  



