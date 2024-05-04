[Objective 1.4] Given a scenario, analyze potential indicators associated with network attacks
##### Wireless
Wireless networking is a target for hackers, the wireless removes the physical barrier
###### Evil Twin
Attack against the wireless protocol via substitute hardware
This attack uses an AP owned by the attacker that usually has been enhances with higher power and higher gain antennas to look like a better connection to the users and computers
By getting users to connect through the evil access point, attackers can easily analyze traffic and perform man in the middle attacks
###### Rogue Access Point
An attacker can attempt to get client to connect to it as if it were authorized and then simply authenticate to the real AP
Rogue AP's can act as a man in the middle and easily steal user credentials
You should routinely scan for and remove rogue APs

`A rogue AP is an AP that is usually placed on an internal network either by accident or nefarious reasons. It is not administered by the network owner or admin
`An evil twin is an AP that appears to be legitimate but isn't and is often used to eavesdrop on wireless communications`
###### Bluesnarfing
Similar to bluejacking in that it uses the same contact transmission protocol
The difference is that instead of sending unsolicited message to the victim's phone, the attacker copies off the victim's information, which can include emails, contact lists, calendars, and anything else.
Bluesnarfing used to require a laptop with a Bluetooth adapter but nor applications are available on mobile device

`Bluejacking is the sending of unauthorized data via Bluetooth , whereass bluesnarfing is the unauthorized taking of data over a Bluetooth channel`
###### Bluejacking
Term used for the sending of unauthorized messages to another Bluetooth device
This involves sending a message as a phonebook contact: The attacker then sends the message to the possible recipient via Bluetooth
	More recent phones can send images and audio as well
The victim and attacker must be within 10 yards of each other and victim phone must also have Bluetooth enabled and discoverable
###### Disassociation
Designed to disassociate a host from the wireless access point and from the wireless network
Disassociation attacks stem from the de-authentication frame that is 802.11 standard
	It is designed to remove unauthorized stations from a Wi-Fi access point
The attacker only needs to have the MAC address of the intended victim, which enables them to send a spoofed message to the access point, specifically the victim machine, making this attack a form of denial of service.

Disassociation attacks are not typically used alone but rather in concert with another attack objective.
###### Jamming
A form of denial of service that targets the radio spectrum aspect of wireless
This can be used to connect to a rogue AP instead
##### Radio Frequency Identification (RFID)
RFID tags are used in a wide range of cases. Such as tracking keys or devices.
RFID comes in active or passive
- Active tags have a power source
- Passive tags utilize the RF energy transmitted to them for power
RFID tags are used as a means of identification, and have advantage of barcode in that they do not need to be visible, just within radio wave range
Several attack types can be performed:
- Against the RFID devices themselves (chip and readers)
- Against communication channel between device and reader
- Against the reader and back-end system

Secured with ISO/IEC standards with securing RFID data flow. ISO/IEC 18000 and ISO/IEC 29167 for cryptography methods to support confidentiality, untraceability, tag and reader authentication, and over-the-air privacy
ISO/IEC 20248 specifies a digital signature data structure for use in RFID systems

The last type is more of a standard IT/IS attack.
Attacks against the communication channel are relatively easy because the radio frequencies are known and devices exist to interface with tags.
In a replay attack, the RFID information is recorded and then replayed later
In eavesdropping, the data can be collected, monitoring the movement of tags for whatever purpose needed by an attacker.

Both these attacks can be defeated using ISO/IEC standards

RFID can be cloned if information is not protected via a cryptographic component
###### Near Field Communication (NFC)
Enables smartphones and other devices to establish radio communication over a short distance
It is not being used more and even linked to financial information

`RFID is a process that communicates with a reader using radio waves and NFC is a high-frequency subset of RFID that acts over a shorter distance`

##### Initialization Vector (IV)
Used in wireless systems as the randomization element at the beginning of  a connection
Attacks are aimed at determining the IV, thus finding the repeating key sequence
The IV is the primary reason for the weaknesses in WEP
The IV is sent in the plaintext part of the message, and because the total key space is 16 million keys, the same key will be reused
Once they key has been repeated, an attacker has two ciphertexts encrypted with the same key stream. This allows attacker to examine the ciphertext and retrieve the key
This attack can be improved by examining only packets that have weak IVs, reducing the number of packets needed to crack the key.
The biggest weakness of WEP is that the IV problem exists regardless of key length because the IV always remains at 24 bits
##### On-path attack
Man in the middle attack (MITM) occurs when an attacker is able to place himself in the middle of two other hosts that are communicating.
This is done by ensuring that all communication going to or from the target host is routed through the attackers host
The attacker can then observe all traffic before relaying it and can actually modify or block traffic
The common method is via session hijacking, which can occur when information such as a cookie is stolen, allowing attacker to impersonate the legitimate session
This can be done as a result of cross-site scripting

Man in the browser attack (MITB) is a variant of MITM
In an MITB attack the first element is a malware attack that places a trojan element that can act as a proxy on the target machine
This malware changes browser behavior through browser helped objects or extensions
The malware can intercepts users keystrokes for example
#### Layer 2 Attacks
Layer 2 is where local addressing decisions operate
This is switches or MAC addresses
There are many ways of tampering, Security+ identifies three
- ARP poisoning
- MAC flooding
- MAC cloning
###### ARP Poisoning
ARP knows where to send a packet using MAC  or layer 2 address
These messages are used in conjunction with a devices ARP table, where a form of short-term memory associated with these data elements reside.
When a machine sends an ARP request to the network, the reply is received and entered into all devices that hear the reply.
This makes address lookups efficient but prone to attacks

When the ARP table gets a reply, it automatically trusts the reply and updates the table
Some OS's will even accept the ARP reply data  even if they never heard the original request
An attacker can send messages, corrupt the ARP table, and cause packets to be misrouted.
This is *ARP Poisoning* and results in malicious address redirection
This can inject an attacker into a man in the middle attack
###### MAC Flooding
Attack where an attacker floods the table with addresses, making the switch unable to find the correct address for a packet.
The switch responds by sending the packet to all addresses, acting as a hub.
The switch also asks for the correct address. thus setting up the switch for ARP poisoning
###### MAC Cloning
Act of changing a MAC address to bypass security checks based on the MAC address
This can work when the return packets are being routed by IP address and can be properly linked to the correct MAC address
Not all MAC cloning is an attack, firewall routers commonly have a MAC clone function to make it seem transparent to other devices
##### DNS
DNS provides the correct address to get to the packets destination
If you can corrupt DNS, you can control where all the packets go
###### Domain Hijacking
Act of changing the registration of a domain name without permission of its original owner
Can have consequences because the DNS system will spread the false domain location far and wide automatically.
The original owner can request it to be corrected, but this can take time.
###### Domain Poisoning
To examine a DNS query for a specific address, you can use nslook up command
The changing of where DNS is resolved can be  a DNS poisoning attack
The challenge is detecting when it changes unauthorized
VPN can change DNS source, but unauthorized change can be attacks

At time nslookup will return a nonauthoritative answer, this typically means the result is from a cache as opposed to a server that has an authoritative answer (current)

There are other commands you can use to examine and manipulate the DNS cache on a system
ipconfig /displaydns will show the current DNS cache on a machine

DNS poisoning is a variant of a larger attack referred to as *DNS spoofing*
	In DNS spoofing an attacker changes a DNS record through any of a multitude of means
	Such as compromising a DNS server, a Kaminsky attack, and the use of a false network node advertising a false DNS address
An attacker can even user DNS cache poisoning to result in DNS spoofing
BY poisoning an upstream DNS cache, all of the downstream users will get spoofed DNS records

Project has begun to secure name DNSSEC, by digitally signing records
This can be assured that the information received is correct
##### Universal Resource Locator (URL) Redirection
Telling browser where to go and the DNS process that converts it to a machine-readable address
Social engineers use psychology to trick users into doing things
Such as a slight difference in the name displayed in an e-mail or link
This is a man in the middle attack where all of your traffic is being read and redirected
How to defend? Security and email vendors have support that looks for differences and alerts a user before going to a site
###### Domain Reputation
IP addresses have reputation as well. Security companies track where spam comes from, and if your IP address becomes associated with spam, botnets, or other behaviors, your domain reputation will suffer.
Many services will stop working if your score gets low enough
To stop, make sure others are not piggybacking on your address
Open mail relays can lead to spamming
Bots can abuse API's
To prevent, make certain others are not piggybacking on your address
Open mail relays can lead to spamming
##### Distributed Denial-of-Service (DDoS)
The attacker attempts to deny authorized users access either to specific information or to a computer system or network itself
This can be done by crashing the system, taking it offline, or by sending so many requests that the machine is overwhelmed
A DoS attack employing multiple attacking systems is known as a *distributed denial-of-service* attack

The attacking systems are not willing agents - they are systems that have been compromised and on which the DDoS attack software has been installed.
It is a multi step process that involves unauthorized access or tricking end users to install the software. Once the network had been created, the agents (zombies) wait for instructions that will include data on the specific target

A defensive approach involves changing the time-out option for TCP connections so that attacks such as SYN flooding attack are more difficult to perform
Much has been written about distributing your own workload across several systems to that any attack against your system would have to target several hosts to be successful. This can be an attempt to mitigate the attack rather than preventing. If large enough zombies are created it can still be successfully attacked.

To prevent a DDoS attack, you must be able to either intercept or block the attack messages or to keep the DDoS network from being established in the first place. Tools have been developed to scan your systems, searching for sleeping zombies.
Many antivirus/anti-malware security tools will detect known zombie-infections.
You have to rely on the community of network administrators to test their own systems to prevent attacks on yours.
###### Network
If the attack network is large enough even ordinary web traffic can quickly overwhelm the largest of sites.
The purpose of DDoS/Dos is to prevent access to the target system and blocking network connections will do this.
One method, a SYN flooding attack, can be used to prevent service to a system temporarily in order to take advantage of a trusted relationship that exists between the system and another.
In a SYN flooding attack, the attacker sends fake communication requests to the target.
Each are answered by the target system, which then waits for the third part of the handshake
Since the requests are fake the target will wait for responses that never come.
the system drops these connections after a period of time, but if the attacker sends requests faster than the time out, the system will quickly be filled with requests.
The number of connections a system can support is finite, so when more requests come in than can be  processed, the system will soon be reserving all its connections for fake requests.
Any further requests are simply dropped and legitimate users who want to connect to the target system will not be able to do so because the system has been denied to them.

Another simple DoS attack is the ping of death (POD), targeted at a specific application or operating system, as opposed to SYN flooding which targets a protocol.
In the POD attack, the attacker sends an ICMP ping packet  equal to or exceeding 64 KB
Certain system are not able to handle this size of a packet, and the system will hang or crash

A newer form of reflection attack, uses the Connectionless Lightweight Directory Access Protocol
The attacker asks for all the information on all accounts in the Active Directory, pointing all the information to the victim machine
Because the attack is spoofed, the data is sent to the victim machine
Preventable, as the UDP port 389 will have a source IP. Blocking this port on the inbound firewalls will block this attack.
###### Application
Applications are subject to DDoS as well
The object of an application level DDoS is to consume all the resources or to put the system into a failed state.
One of the most common targets is HTTP
Because the requesters to the application are typically outside of the local network, the packets are not spoofed, and detection of attack packets versus legitimate ones is challenging.
Advanced next-gen web application firewalls have some resiliency built to in to detect this type of attack, but in severe cases, the issue of DoS is just moved to the firewall
These types of attacks also work against API interfaces as well
The principles behind the attack come from the disparity between the level of resources it takes to attack versus the level of resources it takes to mitigate this action.
The resource being attacked is typically processing power not bandwidth
###### Operational Technology (OT)
OT is the name given to networks of industrial devices in cyber physical systems
These devices use computers to control physical processes - from traffic lights, to refineries, to manufacturing plants, and more.
OT systems have OT-specific protocols that are used to perform the communications of equipment control.
The systems do not perform correctly when communications are interrupted, so DoS/DDoS attacks can result in significant problems.
For these reasons, OT systems are not directly connected to the Internet and have barriers preventing outside packets from getting into these networks.
##### Malicious Code and Script Execution
Attackers have a wide range of technologies to choose from when automating attacks
###### PowerShell
PowerShell is fully integrated with the Windows environment, allowing admins to program any function that can be done with the OS
A wide range of toolsets built to leverage the power of PowerShell can be used to attack a system.
A common used tool is PowerSploit
###### Python
Effective scripting tool that is easy to learn, and good at automating tasks and data analysis.
Very useful for cybersecurity and attackers alike.
###### Bash
Interpreter that processes shell commands on Linux
Bash takes commands in plain text and calls OS services to perform the specified tasks
One of the strengths is the ease of programming complex scripts to automate significant system changes and data manipulation
Hackers use bash to search through systems and perform tasks on Linux systems
###### Macros
Macros are recorded sets of instructions, typically presented to an application to automate their function.
The term macro is used for scripting applications
With this functionality comes risk in the form of unwanted macros calling the system and performing system activities
Restricting macros in these and other applications is an important part of managing the cybersecurity of a workstation
###### Visual Basic for Applications (VBA)
Older technology from Microsoft
Used to automate many internal processes in applications
You should protect systems by disabling macros or VBA from running in applications unless you are sure that the source of the document containing the code can be trusted