# Risk and Management
---
## The CIA triad of Security 
1. **Confidentiality:** Is the goal of keeping data secret from anyone who has the need or the right to access that data.
2. **Integrity:** Ensures that the data and systems, everything stays in an unaltered state (_non modified_) when stored, transimeted and recieved.
3. **Availability:** We have to ensure that systems and data are available to authorized users when needed.

Following these, we also need to keep in mind a couple of other factors:
**Auditing & Accountability:** We want to keep track of things that are happening on systems like: logs, data access, modified data...
**Non-Repudiation:** Ensures that a user can't deny about having made certain modifications or communications.

## Threat Actors
These are the kind of people or organizations that are going to be performing atacks to systems. It is good to identify these threads as:

1. **internal:** Threads coming from people inside of the organization.
2. **external:** Threads coming from the outside of an organization.
3. **level of sophistication:** The amount of evil a person or organization can do measured by their funding, resources and skills.
4. **intent:** What is their intention, goal or motivation to perform these attacks.

### Types of Threat Actors
**Script-kiddies:** Those are the kind of individuals that usually we are going to get rid of with an up to date system.  
**Hacktivists:** All of the attacks they perform are supporting a cause. They try to do bad things in order to prevent certain organizations to continue with their intentions.  
**Organized crime:** The main motivation for these people is making money.  
**Nation states:** Atacks in order to get premium data and information(gather intelligence). Their big goal is an APT(advanced persistent thread), which means hacking a system and staying there to get and monitor the information and intel.  
**Insider threats:** Any person (employee, contractor, subcontractor) who can access an asset.  

**OSINT:** Means open-source intelligence and provides a wide information to intrigue a threat actor. Examples might be any kind of social media platform and obviously the internet.

## What is Risk?
The potential to harm organizations, people, IT equipment...

**Assets:** Provide benefits to an organization, and are all of the parts of an infrastructured that we might be worried about getting harmed.  
**Vulnerabilities:** Weakness to an asset that it is open for a possible exploit.  
**Thread:** Exploit of a vulnerability. The person who performs the attack is called a _thread Agent_.  
**Likelihood:** The chance of something happening at any time and it is usually measured as a percentage. We can measure it regarding the quality _Qualitative likelihood_ or quantity _Quantitive likelihood_.  
**Impact:** Total harm caused by the thread. We also can look at it qualitative or quantitative.

It is very important to deal first with the risks that have a higher percentatge of likelihood and impact to an infrastructure.

We can found a Risk Assesment guide on a document called [SP 800-30](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-30r1.pdf) by NIST.

## Managing Risk
In order to manage the risk we are going need to perform a vulnerability and a threat assesment.

### Vulnerability Assesment
The first step is to find the possible vulnerabilities we may have. In order to find those we can use the common vulnerabilities and exposure database on [cve.mitre.org](cve.mitre.org).  
Once we get a list of the vulnerabilities we want to test we can use more active tools like _Nessus_. This program runs in localhost and it is going to provide us with a document with all the vulnerabilities that have found in the local area network. However, if we want to go more into detail about those vulnerabilities we are going to need a team of pentesters to test our network or systems.

### Threat Assesment
There is going to be different type of threads:
1. Adversarial (Hacker)
2. Incidental (User accidentally types another url and enters database)
3. Structural (equipment failure)
4. Enviromental (Fire in organization)

### Risk Response
Once we find a risk, we have to do something in order to prevent them and we do it several ways:    
1. **Mitigation** (effort to reduce impact the risk)
2. Risk transference (we contract a specific third party service to do a certain task Ex. cloud servers)
3. Risk acceptance (accept the risks in certain situation because it is very expensive to prevent and it is very unlikely to happen)
4. Risk avoidance (avoiding risks Ex. not holding id information because someon may steal it and I don't want to be involve with it)

###Framework
It is a methodolgy that helps you deal with risk managment.  
* [NIST Risk Management Framework Special Publication 800-37](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-37r2.pdf)  
* [ISACA Risk IT Framework](http://www.isaca.org/Knowledge-Center/Research/Documents/Risk-IT-Framework-Excerpt_fmk_Eng_0109.pdf)  





