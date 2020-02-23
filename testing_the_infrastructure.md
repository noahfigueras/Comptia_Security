# Testing your Infrastructure
## Vulnerability Scanning Tools 
Vulnerability assessment is an action we do and we use vulnerability assessment tools to actually go about that process.  

**Tracert:** It is a simple tool but it's going to give us a lot of information about the network and we can use that as a tool to be part of our assesment.  
**nmap:** Port scanner and network analyzer tool.  
**Microsoft Baseline Security Analyzer:** Microsoft tool that will help us to see if we are up to date in our system and it's going to perform a vulnerability assessment.  
**Vulnerability assesment tools for entire infrastructure:** Nessus, Nexpos, OpenVAS.
* Management determines when vulnerability scanning is done.  
* Misconfigurations often are vulnerabilities.  
* Vulnerability scanners can be configured to scan against different databases or rule sets.  

## Social Engineering Principles 
Social engineering principles are focused more on people's behavior as apposed to their physical actions.  
1. **Authority:** To impersonate or imply a position of authority.  
2. **Intimidation:** To frighten by threat.  
3. **Consensus:** To convince of a general group agreement.  
4. **Scarcity:** To describe a lack of something.  
5. **Trust:** To assure reliance on their honesty and integrity.  
6. **Urgency:** To call for immediate action.  

**Never give to anyone private information**  

## Social Engineering Attacks 
**Phishing:** Emails that are used to steal personal information.  
**Spear-fishing:** Phishing that is directed to a specific person or company.  
**Whaling:** Spear phishing that targets senior management and executives.  
**Vishing:** Uses the telephone system to get private information.  
**Hoax:** Warns someone that something bad is happening when its not.  
**Watering hole attack:** An attempt to infect websites that a group of end users would normally go to gain access to their information or network.  

## Attacking Websites
**CLF:** Common Log Files are the standard types of logs that every single type of web server generates and they all generate it in the same format.  
**EX:** 127.0.0.1 -- [10/0ct/2017:10:05:24 - 0600] "GET /CompTIA09_small.gif HTTP/1.0" 200 *42213(Bytes in the object returned to client).*  
**Web application attacks**  
1. Cross-site scripting XSS.  
 * Client-side script injected into trusted web sites. **Ex:** `<script>source=http://evilsite</script>`
2. XML injections.  
 * Inserts XML information that should be there altering the logic of the program.
 **Ex:** http://www.example.com/Newuser.php?user=mike&password=12345&PRODUCT=VoucherGeneric&price=50.00&email-mike@totalsem.com  

## Attacking Applications
**Injection Attacks**  
Injecting extra stuff into an application through an input in order to brake it.  
* **Code injection:** Add extra code to the application to make it do something that it shouldn't be doing.  
* **Command injection:** Uses the application to get to the underlying operating system.  
* **SQL injection:** Type SQL commands through input in order to communicate and retrieve information from the database.  
* **LDAP injection:** LDAP it's used in order to authenticate user and it can be modified to get some information. It is based on X.500 protocol.  

**Buffer Overflow**  
Every time we enter data into an application it goes into a buffer. A buffer is just a part of memory that is set aside to store the data before it actually gets put into the application itself. A *buffer overflow* simply means that we insert so much data into the buffer that the buffer blows up.  

**Integer Overflow:** Bit Overflow with a defined integer value.  

## Exploiting a Target 
**Penetration Testing Steps**  
1. Get Authorization.
  * Define targets.
  * Attack model.
2. Discover Vulnerabilities.
  * Reconaissance.
  * Try to get information.
3. Exploit vulnerabilities.
  * Grab user names and passwords.
  * Take data from a database.
  * Corrupt webpage. 
  
**Attack Model**  
**White box:** Attackers have extensive knowledge about the target.  
**black box:** Attackers know nothing about the target, more like strangers (external hacking).  
**gray box:** Attackers know some information but not a lot.  
  
**Types of discoveries**
* Passive discovery (whois lookup), Semi-passive discovery(Looking a Website) , Active discovery (Attacking the server).  

**Exploiting the target**  
* We are going to use Kali Linux and Metasploit Framework.  

## Vulnerability impact 
**Embedded systems:** It is simply an immutable system that never changes.  
**Lack of vendor support:** if a company is not selling more a specific product we are not going to be able to patch it and keep it up to date.  
**Weak configurations:** it is very important for us to change the default config from a hardware or software and provide the best possible configurations we can.  
**Misconfiguration:** We have a configuration but we have done something incorrectly.  
**Improperly configured accounts:** we have an user account with incorrect rights,privileges and permissions active.  
**Vulnerable business processes:**  
**Memory/buffer vulnerabilities:** resource exhaustion, memory leak, integer overflow, buffer overflow, pointer difference, DSL injection.  

