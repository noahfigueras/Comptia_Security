# Cryptography
It is the science of taking data and make it invisible from the outside to bring it back later on. The main purpuse of cryptography is confidentiality.

**Obfuscation:** We take some data that makes sense and we hide it, for the purpose of not showing it to an outsider.

**Encryption/Decryption:** The two processes of cryptography.

Example: The Ceasar Cipher (It uses substitution in order to encrypt data).
**Viegenere Cypher:** A more complex cryptography method than the Ceasar.
**XOR Encryption:** Another method used with binary encryption.
**Cryptanalysis:** The science of decrypting encrypted data.
**Kerckhoff's principle:** Even if you understand the algorithm of an encryption, if you don't have the key ther's going to be any way to decrypt it.

## Cryptography methods
### Symetric encryption 
They only use one key to encrypt and decrypt the data and it is called a **Session key**. This form of encryption has two ways to send the key:
**In-band:** Send the key with the encrypted data (very risky).
**Out-of-band:** Send the key physically out of the internet (Anne goes to Bob's house and gives him the key on a piece of paper).

**Symetric encryption is the primary way we encrypt data**.
**Ephemeral key:** It is a temporary session key.

### Asymmetric Encryption
It uses two keys in order to exchange a session key in a secure way. The host generates a key pair with a **Public key** and **Private key**.

## Symmetric Cryptosystems
### Symetric key algorithm 
One way are the symetric **block** algorithms, that get a certain amount of data in blocks and encrypt them. The first type of encryption in blocks is called **Data Encryption Standard (DES)** (56-bit keys).  

DES can be hacked in some situations, especially if it has a short key and two alternatives to that are **Blow fish** (variable key size 32-448-bits) and **Triple DES** (168-bit keys).  

**Advanced Encryption Standard(AES)**  
After a while, Computer scientists created a modern symetric block encryption way more secure and that is the most up to date standard. Has key sizes of 128, 192 or 256-bits.

**Streaming cyphers:** Instead of encrypt blocks of bits, it will encrypt one bit at a time as it comes through the wire in a sudo-random manner. One method of streaming encryption is **RC4**(Rivest Cipher 4).

## Symmetric Block Modes
**Electronic Code Book:** Was the first generation of AES encryption and it uses the same key every time to generate the output. Therefore, ECB blocks will always output the same result that is why it is a problem sometimes to use it.  
Therefore, people have come with other much better solutions. All the following block modes use an initialization vector, which ensures the output block is uniquely different:  
**Cipher Block Chaining:** In this mode we encrypt the new data with the previous encrypted result.
**Cipher Feedback:** This mode is very similar to CBC, but it encrypts the inizialization value first and after that it generates a key which we are going to use to encrypt the final result. After that, that output is used for the next encryption packet.
**Output feedback:** Output feedback only uses the same Initialization vector every time to encrypt the data and then performs a final XOR on it.
**Counter (CTR):** It uses a NONCE + COUNTER(changes incremental) to encrypt the data to generate a new key every block and then perform the final XOR on the data to generate output.

## RSA Cryptosystems
Symetrics algorithms have a big problem, it uses the same key to encryt and decrypt. This, in the real world that can cause some serious issues.  
That is why we are also in need of **Asymetric Encription** which uses two keys one to encrypt (Public key) and another to decrypt(Private key).

### RSA
Asymetric algorithm that specifies how a host generates an individual key pair and how we send public keys to different parties.

### ECC (Eliptic Curve Cryptography)
It can provide very small keys that we can use and move around with the same robustness as RSA with increased performance.

## Diffie-Hellman (key exchange protocol)
Asymetric algorithm that provides a methodology for two parties to come up to the same session key. 

## PGP/GPG
Was originally invented for sending encrypted emails so other people couldn't read them. Today it has multiple uses as: encrypt files, partitions, drives ...

## HASH
It takes a large amount of data and converted in a certain unreadable format.

**Message Digest 5 (MD5)**  
Invented in 1992 by Ron Rivest and uses an 128 bit hash. It has the ability to generate collisions.  
A collision means that two different pieces of data will generate the exact same hash.
**Secure Hash Algorithm**  
Developed by NIS, and there is different types of it.  
* SHA-1: Have the ability to generate collisions and has 160 bit hash.  
**Collision based hashes are not used that often anymore because they can be hacked.**
Most commonly used and advance hashes:
* SHA-2: It is based on the length of the hash (SHA-256, SHA-512).
* RIPEMD: Not very common, but it is an open standard and it comes in 128, 160, 256, 320 bit digests.

**For the exam make sure we know the size of the hashes**  

## HMAC
HMAC (hash-based message authentication code) requires each side of the conversation to hace the same key and it is based on standards hashes (MD5,SHA-1,etc.).  
HMAC uses two passes of hash computation. The secret key is first used to derive two keys – inner and outer. The first pass of the algorithm produces an internal hash derived from the message and the inner key. The second pass produces the final HMAC code derived from the inner hash result and the outer key.

## Steganography
Is the process of taking data and hiding it within other types of data. Usually we take data and we hide it within images. There is different programs that can help us do that.

## Certificates and trust
A digital certificate is a document with a public key and a digital signature of the host and a digital signature of a trusted third party. That third party will generate a certificate to generate trust to other people that wants to connect to our website.

## Public Key Infrastructure
Is the real infrastructure that we use for every real world application that uses public key. 

## Cryptographic Attacks
**Password cracking:** All of the passwords in a Server, Database, Webserver, etc. Are stored in a form of a hash. So, if we want to start hacking passwords what we are typically trying to hack is a hash.  

1. First of all we need to get to those hashes and it is really the most big and important part. Once we hack the server and get all the list of username and passwords then we can start cracking passwords.  
2. We can't reverse a hash, therefore we will have to generate our own hashes until one matches with a hash on the list. Hashing attacks, are comparitive attacks, generated hashes vs sotred hashes.  

This attacks are done by **brute force** and the longer the password the longer is going to take the machine to crack it. **That is why we use always long and complex passwords**.

**Dictionary attacks:** A dictionary attack is performed when we assume that the password we want to crack might have some words in combination with other numbers or characters. Then, we write in a file (Dictionary) those possible words we think the password might have and we try them along with different other patterns or just by themselves (it still is a bruteforce but with some assumptions).  

**Rainbow-table attack:** If we need to crack some very complex passwords and we need to improve our timing issues we are going to use this type of attack. Those are nothing more than a pack of a lot of hash tables in order to compare against the hashed password we want to crack and try to discover it.

**Key stretching:** It is more powerful than a hash and a salted hash, and it is pretty much uncrackable nowadays if everything is well done. One key stretching technque is called **bcrypt**. 

