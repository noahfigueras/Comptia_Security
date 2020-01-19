# Identity and access Management

## Identification
There is different types of authentications:
1. Something you know.
	* Passwords,pincodes,captcha and security questions.  
2. Something you have.
	* Smart Card (chip with id), rsa key.
3. Something about you.
	* Fingerprints, facial recognition, etc.
4. Something you do.
	* The rythm of your typing style to identify an user.
5. Somewhere you are.
	*  Has to do with geolocalization in order to track an asset like a credit card or cellphone.

**Multifactor authentication:** Using two or more authentication methods in order to gain access to an asset or system.

## Authorization concepts
Once we are authenticated, it is very important to define what tasks can a user do or not do.

**Permissions:** Are applied to resources.
**Rights and privileges:** We tend to assign at system level.

**Least privilege:** It is a concept that gives to a user only the minimal rights and privileges in order to get the job done.
**Separation of duties:**

## Access control List
The access control list or ACL is nothing more than a List with all of the types of rights and permissions for different kind of users.  

### Authorization Models
* Mandatory access control (MAC): Get some kind of resources and put Labels on them. This way, only the users with permissions to the specific labels will be able to access.

* Discretionary Access Control (DAC): The owner of the data decides who has access to it and the different rights and privileges to each user.

* Role-based Access Control (RBAC): Based on the role we apply different rights or permissions.

## Password Security
In order to start choosing save passwords we are going to write a **good Security Policy**, so we can keep it in mind every time we choose a new password. Also, it has to include the following: 

* **Complexity**
	* Length and character requirements
* **Expiration**
	* Reset and time triggers
* **Passwords history**
	* Reusage and retention

**Local Security policy:** These are the set of policies declared on a local OS in order to secure passwords (Change passwords after 120 days, minimum password length, alphanumerical password required, 5 incorrect password attempts before getting locked).

**Group policy objects:** Same as local security policy but it can apply to an entire directory. Therefore we can use it to setup some security policies inside a network of computers.

## Linux File permissions
The first value of the permissions of a linux file or folder it is going to determine wheter it is a directory (d) or file (f).  

The next values are going to be the permissions of that file or directory in order to read, write and execute fot three different types of users: 1.Owner, 2.group, 3.Everyone.

**Ex:** drwxrwxrwx chemistry.pdf

**r** = read (Open a file, view contents)
**w** = write (Edit a file, Add or Delete Files)
**x** = execute (Run a file, CD to a different directory)

The main tool we use in linux to change user permissions it is called **chmod**.

`chmod o= rw- FileName` (Change permissions for other, everyone)

We can use **o** for Everyone, **g** to change group permissions, **u** for owner.

Also, there is an old school way of using chmod based in a binary system:

Decimal | Binary | Permissions
--- | --- | ---
0 | 000 | ---
1 | 001 | --x
2 | 010 | -w-
3 | 011 | -wx
4 | 100 | r--
5 | 101 | r-x
6 | 110 | rw-
7 | 111 | rwx


`chmod 777` (gives everybody read, write and execute permissions).  
`chmod 720` (gives owner all permissions, write for grup and non for others).

In order to change the user ownership of the file we are going to use **chown**.

`sudo chown root *FileName*` (changing the user owner to root)

In order to change user passwords we use **passwd**.

`sudo passwd` (change current user password)

## Windows File Permissions
The best way to implement the permissions in windows is to create users and grups. Then, instead of given different permissions to an individual user. We can activate the permissions we want for the whole group and all the users of that grup will be influenced by those **NTFS permissions**.  

**Concept of Inheritance:** If you create a folder inside a directory with some NTFS permissions. That new folder will inherit all of the permissions from the parent directory.  

**Deny checkbox:** Turns off inheritance  

**NTFS Permissions**  
	* Full Control (you can do anything you want)
	* Modify (Read, write and Delete Files and Subfolders)
	* Read/Execute (See contents and run programs)
	* List Folder contents (See contents of folders and subfolders)
	* Read (View contents and Open data files)
	* Write (Write to files and create new files and folders)

**Copying and Moving NTFS Objects**  
	* Copy from drive B -> C: Will take on the NTSF properties of the destination drive.
	* Move from drive B -> C: Will take on the NTSF permissions of the original drive or directory.

## User account Management
**Continuous access monitoring**    
We should be monitoring every single move our users are doing to have an idea of what is goin on on our infrastructure.
	* Track log on/log off activity.
	* Track file access.

**Shared accounts**  
That is a really bad thing, never do sharing accounts.  

**Multiple accounts**  
	* Use different username and passwords to different accounts.
	* Monitor which users belong to which groups.
	* Use least privilege - enough necessary to acomplish task.
	* Monitor and log activity of users with multiple acounts.  

**Default accounts**
	* Use dedicated service accounts, that way you can know who is doing what.

## AAA
Triple A, means Authentication, Authorization and Accounting. There is two ways to do that:  
	* Remote Authentication Dial-In User Service.
	* Terminal Access Controller Access-Control System Plus.  

**RADIUS:** it is used in wireless authentication.
	* Radius is used for network access mainly.
	* Radius can use up to 4 different ports: 1812,1813,1645,1646.  

**TACACS+:** Decouple the authorization from the authentication.
	* It uses TCP port 49.

**Both TACACS+ AND RADIUS do auditing for log files**

## Authentication Methods

**Password Authentication Protocol (PAP):** The oldest authentication method. PAP sends username and password in the clear to authenticate. Very bad practice we don't use it anymore.  

**Challenge-Handshake Authentication Protocol (CHAP):** It uses hash values to authenticate an user.  

**NT LAN Manager:** It uses hashes and key authentication to challenge the client and the server against each other to verify that both have the same key.

**KERBEROS:** It is used to authenticate windows domain controllers. It listens on port 88 for stuff to happen.  

**SAML - Security Assertion Markup Language** - It is used exclusively for web applications. Very powerful tool.  
**LDAP - Lightweight Directory Access protocol** - Structured language that allows one computer to go inside someone else directory and query, updated, etc. Uses **tcp and udp port 389**.  

## Single Sign-on
You signed in once to one computer and you have access to all of the different computers on the network.  

**Local Area Network (LAN)**  
	* Uses windows Active Directory.
	* We have a windows server which is going to have a window domain, and all the other computers on the network will have to join that domain in order for the admin to monitor all of them (**Federated system**).  

**Security Assertion Markup Language (SAML)**  
	* It is used to manage multiple apps using a single account and interact with other servers or devices like: login webapps, cameras, lights, etc.

