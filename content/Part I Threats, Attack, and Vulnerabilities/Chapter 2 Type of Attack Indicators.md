---
draft:
---

[Objective 1.2] Given a scenario, analyze potential indicators to determine the type of attack
##### Malware
Software that has been designed for some nefarious purpose
Can be designed to cause damage, such as delete files, or create a backdoor
Installation of malware is done so it is not obvious
###### Ransomware
Form of malware that performs some action and extracts a ransom from the user
Ransomware typically encrypts files on a system until a ransom is paid
Ransomware is typically a worm. The only repair is to rebuild the system.
###### Trojans
Is a piece of software that appears to do one thing but hides another functionality
A trojan is a standalone program that must be installed by the user
Many trojans communicate to the outside through a port that the trojan opens, and this is one of the ways trojans can be detected
###### Worms
Pieces of code that attempt to penetrate networks and computers. Once a penetration occurs, the worm will create a new copy of itself on the system.
Reproduction of a worm does not reply on the attachment of a virus to another file, that is a virus
`If code has to attach to something like a file it is a virus`
`If it can survive on own this is a worm`

Worms have the ability to spread without human action. They do not need help to spread.
##### Potentially Unwanted Programs (PUP)
A term used by antivirus vendors to identify programs that may have adverse effects on a computer's security or privacy
These involve adware or spyware and used for revenue generation purposes
PUPs are a form of malware
PUPs can slow down your PC, display ads, add toolbars on browser, collect private info
A common source for PUPs is third-party download sites for downloading apps
Anti-malware can catch and stop installation
###### Fileless Viruses
Most antivirus/anti-malware find malware through monitoring the filesystem for writes and known signatures
When a malware operates in memory, never touching the filesystem, it is harder to detect. This is called *fileless virus*
This runs in memory until device is powered down
###### Command and Control
Servers that are used to control malware that has been launched against targets
Multiple malware on various systems with IDs all working to provide a means for a hacker to re-enter the system are commonly found in enterprises.
These are also work to exfiltrate stolen data
###### Bots
Is a piece of software the performs a task, under the control of another program
A series of bots across the network is called a botnet
Some botnets are legal and perform desired action
Illegal botnets work in the same way and controlled from command and control servers
Bots can do many things - from spam, to installing spyware, and more
###### Crypto-malware
Malware that uses a system's resources to mine cryptocurrency
Theft of service attack using someone else CPU cycles to do mining
###### Logic Bombs
Type of malicious software that is deliberately installed by a user
Logic bomb is a piece of code that sits dormant for a period of time until some event or date invokes its malicious payload
An example is a program that is set to load and run automatically, and periodically checks an organizations payroll or database for a specific user. If the employee is not found, the malicious payload executes deleting corporate files.
If event is specific date or time, often referred to as a time bomb
Logic bombs are difficult to detect because they are often installed by authorized users and by administrators.
This demonstrates the need for separation of duties and a periodic review of programs and services running.
###### Spyware
Software that spies on users, recording and reporting their activity
Typically installed without the users knowledge
It can record keystrokes, known as *keylogging*
Legislations banned unapproved installation of software, but spyware can be in confusing end-user license agreements
###### Keyloggers
Software that logs keystrokes
Keyloggers are not evil, Word can be considered one
What makes a keylogger malicious is when its operation is unknown to the user and not under the users control
Malicious keyloggers are hidden from view, even in Task Manager
###### Remote-Access Trojans (RATs)
Is a toolkit designed to provide the capability of cover surveillance and unauthorized access to a target system
RATs often mimic the behavior of keyloggers and packet sniffers using the automated collection of keystrokes, usernames, password, screenshots, and more.
RATs can also employ malware to infect a system with code that can be used to exploit.
Involves the use of specially configured communication protocols that are setup upon initial infection of a target.
RAT has a operator behind it, guiding it do do more damage
RATs can be delivered via phishing e-mails. watering holes, or many other ways.
Vulnerable to modern anti-malware programs
Major families of RAT packages
###### Rootkit
Form of malware that is designed to modify the operation of the OS to nonstandard function
Rootkits modify the operating systems kernel and supporting functions, changing the nature
Rootkits are designed to avoid the security functions to avoid detection
Rootkits are a form of malware that can change thread priorities to boost an application's performance, perform keylogging, act as a sniffer, or create backdoors
	The use of rootkit to hide other processes and files enables an attacker to use a portion of the computer without the user knowing what is happening
	This hides exploit code from antivirus acting as invincibility
Rootkits can load before the operating system loads
Rootkits can exist in firmware such as video and expansion cards
`Five types of rootkits: firmware, virtual, kernel, library and application level`
It is easier to use a previous clean image and reimage the machine than to attempt to fix
###### Backdoors
Originally used by software developers to get access to an application even if something were to happen i future that prevents normal access method
Sometimes referred as trapdoor, this is hard-coded and cannot be removed. Should an attacker learn this, all systems running this software would be vulnerable
Backdoor is used to refer to programs that attackers install to ensure they continue to have unrestricted access to the system
#### Password Attacks
###### Spraying
Uses a limited number of commonly used password and applies them to a large number of accounts
Spraying uses a limited number of password and tries them against all the accounts
Useful when you don't care which account you get and is fairly successful
###### Dictionary
Using a password-cracking program that uses a list of dictionary words to try and guess
Words can be combines to form a single word
Rules can be created to replace letters for specific characters or numbers
A dictionary attack involves the use of a lookup table to try and find the answer
###### Brute Force
Password-racking attempts all possible password combinations
With increased computer speed now it cracks much fast
A brute force attack on a password can take place at two levels: it can attack a system, where the attacker is attempting to guess a password at a login prompt, or it can attack the list of password hashes contained in a password file.
###### Offline
Brute force attacks can be used to perform hash comparisons against a stolen password file
Possible to use high-performance GPU-based parallel machines to try passwords at high rates
###### Online
Occurs in real time against a system
Online brute force attacks tend to be noisy and easy to see by network monitoring
Limited by system response time and bandwidth
###### Rainbow Tables
Precomputed tables or hash values associated with passwords
Best defense against rainbow attacks are *salted hashes*, which increases the complexity of a problem by making the precomputing process not replicable between systems
A *salt* is merely a random set of characters designed to increase the length of the item being hashed, effectively making rainbow tables too big to compute
###### Plaintext/Unencrypted
Passwords that are stored
Security tool's can extract Kerberos tickets from memory and extract plaintext passwords from process dumps and harvest plain text passwords
#### Physical Attacks
###### Malicious USB Cable
USBs can have embedded electronics in it.
"Poisoned cables" can deliver malware to machines
Cables have even been embedded with Wi-Fi devices enabling attacks against a Wi-Fi network from the cable itself
###### Malicious Flash Drives
USB dropping for people to pick up and use. Once plugged in attack is automated
AutoRun and Auto Play is a security issue and disabled post Windows XP
###### Card Cloning
Possible to copy information on a magnetic strip
Smart cards made it hard as the chip itself cannot be cloned
Contactless IDs can be cloned
NFC chip can be read, copied, and clone implemented
###### Skimming
Physical devices built to intercept credit cards
Placed on credit card readers to skim the data while passing the magnetic strip as well as PIN being entered, enabling a clone to me created
Can be discovered by tugging on the physical interface to reveal the skimmer
##### Adversarial Artificial Intelligence
Used in anti-malware to find new threats based on analysis and programmatic behaviors
Attackers can use adversarial AI to evade defenses
###### Tainted Training Data for Machine Learning
Machine Learning is one of the techniques used in AI
ML works by using a training data set to calibrate the detection model to enable detection on sample data
A good training set data can build a solid detection model
A deficient training data set can have holes
Maintaining security around the parameters of an ML algorithm is essential
##### Supply-Chain Attacks
Network of suppliers that provide the materials for something to be built.
Can be library module for a software, or a physical hard drive that can be tainted
Manufacturers have shipped PCs with preinstalled malware
##### Cloud-Based vs. On-Premise Attacks
Moving computing or storage to the cloud does not change security
The objective and methods are the same
Not all vendors have the same level of protection
#### Cryptographic Attacks
###### Birthday
Special type of brute force attack that gets its name from something known as the birthday paradox, which states that in a group of 23 people, the chance that two individuals will have the same birthday is greater than 50 percent.
This applies to passwords
###### Collision
Two different inputs yield the same output of a hash function
Through manipulation of data, subtle changes are made that are not visible to the user yet create different versions of a digital file
With the creation of many different versions and the use of birthday attack to find a collision between any two of the many versions, an attacker has the chance to create a file with changed visible content but identical hashes
###### Downgrade
The attacker takes advantage of a commonly employed principle to support backward compatibility to downgrade the security to a lower or nonexistent state
