##### Network Reconnaissance and Discovery
###### tracert/traceroute
tracert is a Windows command for tracing the route packets take over the network
	Provides a list of hosts, switches and routers
On Linux and macOS the command is traceroute
###### nslookup/dig
Is used to convert a domain name into an IP address
You can use nslookup on Windows
The command dig works on Linux
###### ipconfig/ifconfig
ipconfig for Windows
ifconfig for Linux
###### nmap
open source port scanning tool
Works on Linux, Windows, macOS
###### ping/pathping
ping sends echo requests
pathping provides data beyond ping as if you were using tracert or traceroute  then calculates loss information
###### hping
A packet creation tool that allows a user to craft raw IP,TCP,UDP and ICMP packets from scratch
###### netstat
Monitors network connections to and from a system
###### netcat
Is the network utility designed for Linux
Been ported to Windows but not regularly used in Windows
##### IP Scanners
###### arp
Designed to interface with the OS's ARP caches on a system
Arp allows to see and manipulate the ARP cache on a system
###### route
Route works in Linux and Windows to provide information on current routing parameters
Lists the current routing table
###### curl
Tool designed to transfer data to or from a server without user interaction
###### theHarvester
Python based program designed to assist penetration testers in the gathering of information during the reconnaissance portion of a penetration test
Designed for Linux and part of Kali
###### sn1per
Linux based tool used by penetration testers
Designed to collect a large amount of information while scanning for vulnerabilities
Runs scripts to enumerate servers, open ports, and vulnerabilities, and it's designed to integrate with the penetration testing tool Metasploit.
It can also brute force open ports, subdomains and DNS systems and run targeted nmap scripts against open ports
###### scanless
Command line utility to interface with websites that can perform port scans as part of a penetration test
###### dnsenum
Perl script to enumerate DNS information
`DNS enumeration can be used to collect info such as usernames and IP addresses of targeted systems`
###### Nessus
Vulnerability scanner
Used to audit systems for compliance
###### Cuckoo
Sandbox used for malware analysis
Can run on Windows and Linux
##### Forensics
###### dd 
Data dump is a Linux command line utility used to convert and copy files
dd can be used to backup the boot sector of a hard drive, obtaining a fixed amount of random data or backing up entire disks
###### memdump
Linux has a utility program called memdump
Dumps system memory to the standard output stream, skipping over any holes in memory maps
Output is in the form of a raw dump
###### WinHex
Hexadecimal file editor
Useful in forensics
###### FTK Imager
Designed to capture an image of a hard drive in a forensic fashion
Retains the file system metadata and creates a log of the files copied
This process does not change file access attributes
###### Autopsy
MD5 creation and lookup, deleted file carving, email message extractions, on hard drives, smart phones, and removable devices.
