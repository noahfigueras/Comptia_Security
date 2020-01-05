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

### Framework
It is a methodolgy that helps you deal with risk managment.  
* [NIST Risk Management Framework Special Publication 800-37](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-37r2.pdf)  
* [ISACA Risk IT Framework](http://www.isaca.org/Knowledge-Center/Research/Documents/Risk-IT-Framework-Excerpt_fmk_Eng_0109.pdf)  

## Using Guides for Risk Assesments
Using up to date guides to configure different OS systems or network infrastructure devices is very beneficial in order to make sure to set them up as a secure device. Therefore, we should always follow these directions coming from the different companies that manufacture them.

## Security Controls
It is a mechanism or action exexuted in order to protect our IT infrastructure and it is going to help us remediate problems. Security IT specialist uses security controls in order to prevent bad things to happen to our assets. For example: teaching employees to prevent social engineering attacks, setting up a firewall...

An IT specialist understand security controls and they can apply, monitor and adjust them based of the needs of the infastructure. There is different types of security controls:
1. **Administrative Control:** Control actions towards IT security and includes Laws, Policies, Guidelines, Best practices.  
2. **Technical Control:** Control actions IT systems towards IT security as computer staff, Firewalls, Password links, Authentication.
3. **Physical Control:** Control actions in the real world as Gates, Guards, Keys, Man traps.

### Security control Functions
* **Deterrent:** Stops the actor from even attempting the threat.
* **Preventative:** Stops the actor from performing the threat.
* **Detective:** Recognizes an actor's threat.
* **Corrective:** Mitigates the impact of a manifested threat.
* **Compensating:** provides alternative or temporary fixes to any of the above functions. 

### Interesitng Security Controls
* **Mandatory vacation:** It is used to detect fraud and unauthorized activity.
* **Job Rotation:** Enhances employees to know all different task in case the main guy is sick and can't do his job and also avoids people of being jealous of performing particular tasks.
* **Multi-person control:** Avoids a single person to take a bad action on a specific task and allows multiple people to make sure that something is done the right way.
* **Separation of Duties:** A single individual should not perform all critical or privilege duties across the board (Administrative control).
* **Principle of least privilege:** Users are granted only the level of privilege necessary for them to perform their jobs.

## Defense in depth 
There is to particular terms we have to get familiar with in order to start:  
* **Diversity:** Using a variety of controls in a random pattern.
* **Redundancy:** We have applied some kind of security control over and over. We use a bunch of layers to secure a system.

## IT Security Governance
It influences how the organization conducts IT security and there are different kind of sources:

* **Laws and Regulations**
* **Standards (Governamental or Industrial)**
* **Best practices**
* **Common sense**

Once we take a look at all of these different sources, our job will be to create two different documents:  

1. **Policies:** It is a document that defines how are we going to do something.  
... Usually broad in nature.
... Used as directives.
... Define roles and responsabilities.

2. **Organization standards:** Define the acceptable level of performance of a policy (much more detailed than a policy).

Governance has the ultimate goal to make the right security controls  and precedures for our organization.

## Security Policies
### Acceptable use Policy
Defines what a person can and can't do in a company asset.
### Data Sensitivity and Classification Policies
We have to define how important types of data are. Ex: Highly confidential data...
### Access Control Policy
Defines how people can access to data. Ex: How employees authenticate, which data can a person access and how ...
### Password Policy
Defines how people have to deal with passwords. Ex: Long and complex passwords, how to get back a password, deal with multiple logins...
### Care and use of equipment
Explains how you borrow or maintain an equipment.
### Privacy Policies
Those are often for customers and define what private information the company gets from them and what are they going to do with that information.
### Personel Policy
If it has to do with a person and a personel.

## Quantitative Risk Calculation
How much is a particular incident going to affect a specifi asset.

* **Exposure Factor:** Percentage of an asset that's lost as the result of an incident.(Being 1 a total loss of the complete euipment).  

**Single Loss Expectancy =** Asset value * Exposure Factor  

**ARO(Annualized Rate of Ocurrence):** What is the chances of something happen in one year.  

SLE * ARO = **Anual Loss Expectancy** (It is going to tell you the cost of a particular incident annualy).  

## Business Impact Analysis
The study and analysis of the impact on your organization if you have a disruption in your business.

* **Determine mission process** Ex: make sure the servers are running.
* **Identify critical systems**
* **Single point-of-failure**
* **Identify resource requirements**
* **Identify recovery priorities**

The Impact of something that go wrong can come in form of people, finance or reputation.

