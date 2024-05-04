[Objective 3.3] Given a scenario implement secure network designs
##### Load Balancing
Common technique in fault tolerance is load balancing through the use of a load balancer
Load balancing involves the use of devices that move loads across a set of resources in an effort not to overload individual servers.
	Designed to distribute the processing load over two or more systems
Should any one system fail the other can pick up processing it was handling
Often used for systems handling websites, high-bandwidth file transfers, and IRC networks
###### Active/Active
All the load balancers are active, sharing the load-balancing duties
If  a server fails, service interruption or traffic loss may result
###### Active/Passive
Having a single load balancer creates a single point of failure (SPOF)
In an active/passive, the primary load balancer is actively doing the balancing while the secondary load balancer passively observes and is ready to step in any time the primary system fails
`All traffic is sent to the active server in a active/passive configuration. If the active server fails, the passive is active`
##### Scheduling
###### Affinity
Affinity-based scheduling is designed to keep a host connected to the same server across a session. Some applications, such as web applications can benefit from affinity.
The method used by affinity scheduling is to have the load balancer keep track of where it last balanced a particular session and direct all continuing session traffic to the same server.
###### Round-Robin
Involves sending each new request to the next server in rotation.
All requests are sent to server in equal amounts, regardless of server load.
###### Virtual IP
Allows multiple systems to be reflected back as a single IP address
###### Persistence
Condition where a system connects to the same target in a load balanced system
Achieved through affinity scheduling
###### VLAN
Trunking is the process of spanning a single VLAN across multiple switches.
A trunk based connection between switches allows packets from a single VLAN to travel between switches
Trunks enable network administrators to setup VLANs across multiple switches with minimal effort.
##### Screened Subnet (DMZ)
The zone between the untrusted Internet and the internal network
To demarcate the zones and enforce separation, a firewall is used on each side of the screened subnet.
Special attention is required ad you should consider them to always be compromised nu unauthorized users. Machines whose functionality is locked down to preserve security is called hardened operating system.
`Screened subnets act as a buffer zone between unprotected areas, allowing for the monotoring and regulation of traffic between these two zones.`
###### East-West Traffic
Data flowing into and out of a data center or enterprise is called north-south traffic
East-West traffic is the data flow between devices with a portion of the enterprise
###### Extranet
Is a semiprivate network that uses common network technologies to share information and provide resources to business partners
###### Intranet
Referred to as campus or corporate networks with trust from the network security
Private internal  network that uses common network technologies to share information and provide resources to internal organizational users
###### Split Tunnel vs. Full Tunnel
Split tunnel is a form of VPN where not all traffic is routed via the VPN. Split tunneling allows multiple connection paths, some protected whereas other traffic is routed via non-VPN paths.
Advantage is the ability to avoid bottlenecks from all traffic having to be encrypted across the VPN.
*Full tunnel* routes all traffic over the VPN, providing protection to all networking traffic.
###### Remote Access vs. Site-to-Site
Site to site communication links are network connections to two or more networks across an network layer.
To secure the traffic that is going from site to site in the form of VPN or a tunnel can be used.
Remote access is when a user requires access to a network but is not able to make a physical connection. Remote via a tunnel or VPN has the same effect as directly plugging a cable directly into the machine.
###### IPSec
IPSec is a set of protocols developed to securely exchange packets at the network layer
IPSec has two modes - transport and tunnel - that provide different levels of security
	Transport mode encrypts only the data portion, thus enabling an outsider to see source and destination IP address. Transport protects the higher level protocols associated with a packet and protects the data being transmitted.
	Tunnel mode encrypts the source and destination IP addresses, as well as data itself
	Provides greatest security, but can be done only between IPSec servers or routers
<mark style="background: #BBFABBA6;">	Protection of header info is called context protection</mark>
IPSec has three modes of connecting: host to server, server to server, and host to host
##### Layer 2 Tunneling Protocol (LT2P)
Has ability to use IPSec and encryption protocols, providing data security
Also designed to work with AAA services such as RADIUS and TACACS+
##### Port Security
Port security is a capability provided by switches that enables you to control which devices and how many of them are allowed to connect via each port on a switch.
Port security has three variants:
- Static learning - a specific MAC address is assigned to a port. MAC addresses need to be known and programmed in advanced.
- Dynamic learning - Learn MAC addresses when they connect.
- Sticky learning -  Allows multiple devices to a port, but stores the information in memory that persists in reboot.
##### Broadcast Storm Prevention
One form of attack is a flood. Flooding attacks are used as a form of DoS to a network/system
Flood guards manage traffic flows, by monitoring traffic rate and percentage of bandwidth occupied by broadcast, multicast, and unicast traffic, a flood guard can detect when to block traffic to manage flooding.
##### Bridge Protocol Data Unit (BDPU) Guard
To manage the Spanning Tree Protocol, devices and switches can use the BDPU packets.
These are crafted message with frames that contain information about the STP.
An attacker can issue multiple BDPU packets to force recalculations that server as a network DoS attack.
To prevent this, edge devices can be configured with BDPU guards that detect and drop these packets.
##### Loop Prevention
Layer 2 switches do not have a way to kill packets that get caught in a loop
To prevent loops spanning trees is employed.
STP allows for multiple redundant paths to ensure a proper broadcast pattern.
It acts by trimming connections that are not part of the spanning tree connecting all of the nodes.
STP messages are carried in BPDU frames
##### DHCP Snooping
A rogue DHCP can route the client to a different gateway, an attack known as DHCP spoofing
DHCP snooping is a defensive measure against an attacker that attempts to use a rogue DHCP device.
	Prevents malicious DHCP servers from establishing contact by examining DHCP responses at the switch level and not sending those from unauthorized DHCP servers
##### MAC Filtering
Selective admission of packets based on a list of approved MAC addresses
	Can be bypassed by attackers and spoofing allowed MAC addresses for the wireless card
##### Network Appliances
###### Jump Servers
Used to access devices in a separate security zone
For someone outside the network to access protected resources they first connect to the jump host, and their activities to the internal services are performed via the connection.
Level of functionality via a jump host can be controlled, and the activity monitored.
##### Proxy Servers
Can be used to filter out undesirable traffic and prevent employees from accessing potentially hostile websites
A proxy server takes requests from a client system and forwards them to the destination server on behalf of the client
Usually done by setting up the proxy and requiring all client systems to configure their browsers to use the proxy or by deploying an intercepting proxy that actively intercepts all requests without requiring client-side configuration
###### Forward
Proxies can operate in two directions. A forward proxy operates to forward requests to servers based on a variety of parameters.
Can be used to bypass's firewall restrictions, act as a cache server, and change your IP address
Can be deployed by attackers to get users to use them for caching purposes when in fact they actually create a man-in-the-middle attack
###### Reverse
Reverse proxy typically installed on the server side in front of a group of web servers, and intercepts all incoming web requests.
Can perform traffic filtering, SSL/TLS decrypting, and perform load balancing
`A forward proxy is Internet facing and acts on behalf of the client. It protects the client. A reverse proxy is internally facing and acts on behalf of the server, which it protects`
##### NIDS/NIPS
AN IDS will have the following logical components:
- Traffic collector (or sensor) - This collects activity/events for the IDS to examine. On a host based IDS this could be log files, audit logs, or traffic coming to or leaving a system. ON a network IDS, this is typically a mechanism for copying traffic off the network link - functioning as a sniffer. Referred to as a sensor.
- Analysis engine - Examines the collected network traffic and compares it to known patterns of suspicious or malicious activity stored in signature database. The analysis engine is the "brain" of the IDS
- Signature database - this is a collection of patterns and definitions of known suspicious or malicious activity
- User interface and reporting - provides alerts when appropriate and gives the user a means to interact and operate the IDS
###### Signature Based
Relies on a predefined set of patterns (signatures). Signature based works by matching signatures in the network traffic to defined patterns stored in the system. Very fast and precise with low false-positive rates.
###### Heuristic/Behavior
*Behavioral* relies on a collected set of "normal" behavior - what should happen on the network and is considered acceptable traffic. Behavior that does not fit into the activity categories or patterns is considered suspicious or malicious Can potentially detect zero-day or unpublished attacks but carries high false-positive rate because any new traffic pattern can be labeled as suspect.
*Heuristic* uses AI to detect intrusions and malicious traffic. Implemented through algorithms that help an IDS decide whether malicious.
###### Anomaly
IDS is first taught what "normal" traffic looks like and then looks for deviations from the normal patterns.
Anomaly is a deviation from an expected pattern or behavior.
##### HSM
Hardware security module is a device used to manage or store encryption keys. Typically peripheral devices connected via USB or network connection.  Designed to allow the use od the key without exposing it to the range of hoist based threats.
##### Sensors
Devices that capture data and act upon it.
Sensors can be divided into two types based on where they are placed: network and host
	Network based sensors can provide coverage across multiple machines, but are limited by traffic engineering to systems that packets pass them. Issues with encrypted traffic because if encrypted they cannot read it and act upon it.
	Host based sensors provide more specific and accurate information in relation to what the host machine is seeing and doing, but they are limited to just that host.
Sensors have different actions they can take: they can report on what they observe, they can use multiple readings to match a pattern and create an event, and they can act based on proscribed rules. This deployment strategy must consider network traffic engineering, the scope of action and other limitations.
###### Collectors
Collectors are sensors, or concentrators that combine multiple sensors, that collect data for processing by other systems.
###### Aggregators
A device that takes multiple inputs and combines them to a single output. an aggregate switch will reduce this to one connection, while providing faster switching between users than the router would.
##### Firewalls
###### Web Application Firewall (WAF)
A device that performs restrictions based on rules associated with HTTP/HTTPS traffic
WAF can detect and block disclosure of critical data, such as account numbers and credit card numbers. Also used to protect websites from common attacks.
You can configure a web application firewall to examine inside a TLS session.
###### NGFW
Keep track of the state associated with the state of the communication. Stateful packet filtering.
###### Stateful
Can act upon the state condition of a conversation.
Stateful means that the firewall maintains, or knows, the context of a conversation.
Stateful monitoring will enable the system to determine which sets of high port communications are permissible and which should be blocked.
	A disadvantage is that stateful monitoring takes significant resources and processing to perform this type of monitoring, and this reduces efficiency and requires more robust and expensive hardware.
##### Unified Threat Management (UTM)
UTM devices provide a wide range of services, including switching, firewall, IDS/IPS, anti-malware, anti-spam, content filtering and traffic shaping. UTM can also be a single point of failure.
##### NAT Gateway
To compensate for a lack of IP address space, NAT translated private non-routable IP addresses into Public (routable) IP addresses.
- Static NAT - maps an internal private address to an external, public address. The same public address is always used for that private address. 
- Dynamic NAT - maps an internal, private IP address to a Public IP address selected from a pool of registered public IP addresses.
- Port Address Translation (PAT) - allows many different internal, private addresses to share a single external IP address. PAT devices keep a translation table to track which internal hosts are using which ports. When response packets are received, the PAT device reverses the process and forwards the packets to the correct internal host.
##### Quality of Service (QoS)
Is the use of specific technologies to guarantee its ability to manage traffic based on a variety of indicators. QoS technologies are used to manage network conditions such as bandwidth, latency, jitter and error rates.
##### Port Spanning/Port Mirroring
Most switches have the ability to copy activity of one or more ports through a Switch Port Analyzer (SPAN), also known as port mirror
##### Port Taps
A test access point (TAP) is a passive signal copying mechanism installed between two points on the network. The TAP can copy all packets it receives, rebuilding a copy of all messages.
Disadvantage is that TAP is a separate piece of hardware and adds to network costs
Unauthorized TAPs can present a security threat, man in the middle attack.