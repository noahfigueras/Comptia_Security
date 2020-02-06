# BEYOND THE BASIC LAN 
**SSID** is associated to the MAC address on a wireless access point and is know as a **BSSID**.
## Wireless Review
These are the main Wirless Infrastructure modes sorted by oldest methods to more modern ones:  
1. **802.11 Infrastructure mode**
  * It has no authorization and no encryption.
2. **Wired equivalent privacy (WEP)**
  * Provides basic authentication and encryption.
  * Based on RC4 streaming protocol.
  * Generates and Shares key of 64bit or 128bit to connect with clients.
  * WEP can easily be **hacked**.
3. **Wireless Protected Access (WPA)**.
  * In order to create a strong authentication they created **802.11i** standard.  
  * It incorporates the **802.1X** authentication.
  * Connection with username and password.
  * They use a very strong and robust **AES encryption**.
  * We can always use PSK or pre-shared keys.  
4. **WPA2**
 * It is going to be completely 802.11i standard which uses 802.1.X and AES encryption.

## Living in open Networks
Open networks are very practical because they provide us quick access to the internet, but they are very dangerous because they are also insecure. They are a big problem because evil people can capture and steal data and information. **Ex:** stealing cookies (SSL Stripping), sniffing packets.  

**What do we do to prevent that ??**  
* Use **secure protocol** on unsecure wireless networks.
* Use **https** on Web sites that collect information.
* Use VPN in non-secure web environments.  

**HTTP strict transport security (HSTS):** Servers automatically redirect you to their Secured website instead of http.  

## Vulnerabilities with Wireless Access Points
**Rogue access points:** It is an unauthorized access point.  
**Evil Twin:** Creating another access point with the same SSID of the AP we want to attack and then get the credentials from the user who wants to log in with a false authentication pop up.  
**Deauthentication attack:** We can see all the clients connected to an Access Point and with these tecnique we can deauthenticate a client from a specific Network in order to get them connected to our Evil Twin network.  

## Cracking 802.11 (WEP)
Cracking WEP, WPA, WPA2 and WPS:  
**Cracking WEP**  
WEP initialization vector is vulnerable to cracking and we can crack it with an **IV attack**. What these attack does is getting the password by analyzing a lot of packets. We are going to use Aircrak tool to grab WEP keys.  

1. `airmon-ng`
 * Check what kind of network cards I have.
2. `airmon-ng start [interface]`
 * Start the network card.
3. `airodump-ng [interface]`
 * Start monitoring the wireless networks around the area.
 * Grab the wireless AP we want to attack.
4. `airodump-ng -w dumpfile -c 6 --bssid [BSSID] [interface]`
 * Grab the specific packets that we asked about and dump it on that file.
 * Let it run about 5 to 10 minutes.
 * We can see systems that are making connections with the AP.
5. `aircrack-ng [dumpfile.cap]`
 * HACKING DONE and hopefully you Decrypt the key correctly.  
 
## Cracking 802.11 (WPA)
WPA is very difficult to crack because it has a very strong encryption and it is very difficult to decrypt. There is other methods to crack WEP and a very famous one is a **dictionary attack**. WPA/WPA2 can be cracked at the initial connection between the WPA/WPA2 client and the access point during the 4-way handshake.  

1. `airodump-ng [interface]`
2. `airodump-ng -w wpafile -c [channel] --bssid [BSSID] [interface]`
 * Monitor for people to connect to the AP to get Handshakes.
3. `aircrack-ng -a2 -w dictionaryFile wpafile-01.cap`
 * -a2 is WPA2 cracking mode.
 * dictionaryFile contains a bunch of possible passwords.
 * wpafile-01.cap is the file which has the handshake that we want to crack.  
 
 **Always use long, complex private shared keys when dealing with WPA and WPA2 in order to prevent bad people to easily discover your password**  
 
## Cracking 802.11 (WPS)
WPS is a push button configuration and it has several weaknesses:  
* 8 digit key is actually only 7 digits 2^7.
* Key exchange is the first processed in 4-bit and 3-bit.
* The key or pin used in WPS is very weak.

1.`reaver -i [interface] -b [BSSID]`
 * Cracking wps  

**WPA Attack Prevention**  
* Get rid of older routers.
* Firmware updates. 
* Upgrade to newer wireless router.  

## Wireless Hardening
**Hardening 802.11 Networks**  
1. **Survey installation issues.**
 * Survey tools are going to help us to setup and install our network.  
2. **Maintaining existing wireless networks.**  
 * Keep a good Documentation.
  * SSIDs.
  * MAC addresses associated to: WAPS, AP locations, Heatmaps.
  * Disable Wireless SSID Broadcast.
  * AP Isolation.
  * Make Long Passwowrds.
  * Periodic Scanning.
3. **Monitor wireless networks**
 * WIDS - Wireless Instruction System (very important to have).
  * Monitor wireless radios.
  * Watches for rogue access points.
  * Knows MAC address of authorized equipment.
4. **Define how to defend wireless clients.**
 * Trained clients are an essential part of good wireless security.  

## Wireless Access Points
There's different kinds of access points and we want to make sure we pick the right one for every different situation:  

**Thick client:** Big powerful WAP for corporations mostly and we have to configure every client individually.  
**Thin client:** Are configured through a controller and make it easier to configure multiple units.  

**WAP Antenna Types**  
* **omni:** The signal goes to every possible direction (installed outdoors).
* **dipole:** They are useful to cover floors or spaces at the same level  \|/ .
* **directionals:** There is yagi and parabollics.
* **patch:** Patches are usually mounted on a wall and they only shoot one direction.   
**Band Selection**  
The 802.11 standard has two different bands: 2.4 or 5 GHz band.  




