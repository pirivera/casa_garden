[Objective 3.1] Given a scenario, implement secure protocols
##### Protocols
Secure protocols are those that have built-in security mechanism so that by default , scurity can be enforced via the protocol.
###### Domain Name System Security Extensions (DNSSEC)
DNSSEC is a set of extensions to the DNS protocol that, through the use of cryptography, enables origin authentication of DNS data, authenticated denial of existence, and data integrity but does not extend to availability or confidentiality
DNSSEC records are signed so all DNS responses are authenticated but not encrypted
DNSSEC typically uses TCP port 53
`DNSSEC validates DNS data, providing integrity but it does not provide availability or confidentiallity`
###### SSH
SSH uses asymmetric encryption but generally requires an independent source of trust with a server. such as receiving a server key to operate.
###### Secure/Multipurpose Internet Mail Extension (S/MIME)
S/MIME is a standard for transmitting binary data via e-mail
E-mails are sent as plain text files, and any attachments need to be encoded to fit the plaintext format. There is no security.
S/MIME is designed to provide cryptographic protections to e-mails and is built into the majority of modern e-mail software to facilitate interoperability.
`S/MIME is standard for e-mail encryption`
###### Secure Realtime Transport Protocol (SRTP)
Network protocol to securely deliver audio and video over IP networks
Uses cryptography to provide encryption, message authentication and integrity, and replay protection to the RTDP data
###### LDAPS
LDAP over SSL/TLS over TCP port 636
LDAPS communication to a global catalog server occurs over TCP port 3269
###### FTPS
FTP over SSL/TLS over TCP port 989 (data connection port)
FTP over SSL/TLS over TCP port 990 (control connection port)
<mark style="background: #FFB86CA6;">SSL deprecated, now only TLS is used in FTPS</mark>
###### SFTP
FTP over SSH channel on TCP port 22
###### Simple Network Management Protocol v3 (SNMPv3)
Standard for managing devices on an IP network
Can be used to manage and monitor devices including network devices, computers, and others
SNMP requires ports 161 and 162
###### HTTPS
SSL deprecated and TLS replaces it
port 80 HTTP and port 443 for HTTPS
###### IPSec
Set of protocols to securely exchange packets at network layer 3 of the OSI model
It is possible to tunnel across other networks at lower levels of the OSI model
IPSec provides connectionless integrity, data security, data origin authentication
IPSec has two modes - transport and tunnel that provide different levels of security
Also three modes of connection: host-to-server, server-to-server, and host-to-host
IPSec uses the term *security association (SA)* to describe a unidirectional combination of algorithm and key selection to provide a protected channel.
	 Two protocols to provide traffic security:
	 - Authentication Header (AH)
	 - Encapsulating Security Payload (ESP)
`IPSec AH protects integroty but does not provide privacy because only header is secured. IPSec ESP provides confidentiality, but does not protect integrity of packet. To provide both, both headers can be used at same time`
###### Tunnel/Transport
Transport mode encrypts only the data portion of a packet, thus enables an outsider to see source and destination IP addresses.
	Protects higher level protocols and protects data being transmitted but allows knowledge of the transmission itself
Tunnel mode provides encryption of source and destination IP addresses as well as of the data itself.
	It can only be done between IPSec servers (or routers) because the final destination needs to be known for delivery
`In transport mode (end-to-end), security of the packet is provided by endpoint computers. In tunnel mode (portal-to-portal), security of packet traffic is provided between endpoint node machines in each network`
###### POP/IMAP
IMAP uses port 143. Secure IMAP4 uses port 993
POP3 uses port 110. Secure POP3 uses port 995
SMTP between servers is TCP port 25, but when clients are involved it is port 587
If encrypted TCP port 465
