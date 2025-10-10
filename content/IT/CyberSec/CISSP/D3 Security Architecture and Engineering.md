#it/cybersecurity/CISSP

## Concepts of secure design principles, incorporating new technologies
## Updated security models fundamental principles
## Security capabilities of information systems, including IoT and mobile devices
## Advanced vulnerabilities and countermeasures in web-based systems and mobile systems
## Expanded cryptography section covering concepts, methodologies, and emerging practices
## Physical security integrated with smart technologies
## Secure protocol and design components, with a focus on new and emerging threats
## Management of the information system lifecycle



---
## Cryptographic foundation
Main Goals of cryptography:
- <mark style="background: #FFB8EBA6;">Confidentiality</mark> - data remains <mark style="background: #FFF3A3A6;">private</mark>
	- in <mark style="background: #BBFABBA6;">rest</mark> - hard drives, backups, USB devices...
	- in transit/<mark style="background: #BBFABBA6;">motion</mark> (data on the wire) - network, wireless 
	- in <mark style="background: #BBFABBA6;">use</mark> - stored on active memory (computer, phone,...)
- <mark style="background: #FFB8EBA6;">Integrity</mark> - <mark style="background: #FFF3A3A6;">not altered</mark> without authorization 
- <mark style="background: #FFB8EBA6;">Authentication</mark> - <mark style="background: #FFF3A3A6;">verifies</mark> claimed identity
- <mark style="background: #FFB8EBA6;">Nonrepudiation</mark> - Provides <mark style="background: #FFF3A3A6;">assurance</mark> to recipient + <mark style="background: #FFF3A3A6;">prevents claiming they never</mark> sent a msg (Only asymmetric) 

Integrity keywords:
- Message digest - digital signature
- 


Cryptosystems
- Symmetric - One key
- Asymmetric - Two (Public & Private)



#### Terminology

Cryptology
- Cryptography - Creating and implementing secret codes
- Cryptoanalysis - Defeat codes and ciphers.

P - Plain text
C - Ciphertext - Encrypted plain text

```bash
ეს ვერ გავიგე
```
Key space - range of values valid for use as a key
Bit size - number of binary bits in the key

Cryptographic key = Cryptovariables


Kerckhoffs's principle
Cryptographic system should be secure even if everything about the system, except the key, is public knowledge. 
In short: <mark style="background: #FFF3A3A6;">The enemy knows the system</mark>
Additions: `Security through obscurity` - hide both key and algorithm


