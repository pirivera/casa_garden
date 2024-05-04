##### Authentication Management
###### TPM
Trusted Platform Module is a hardware solution on the mother board, one that assists with key generation and storage as well as random number generation.
When encryption keys are stored in the TPM they are not accessible via normal software channels and are physically separated from the hard drive
`TPM acts as a secure cryptoprocessor, its a hardware solution that assists with key generation and secure , encrypted storage`
###### HSM
Hardware security module, is a device used to manage or store encryption keys
Can also assist in cryptographic operations such as encryption, hashing, or the application of digital signatures
HSMs are peripheral devices connected via USB or a network connection
HSMS have tamper protection and mechanisms to prevent physical accesses to the secrets they protect
##### Authentication
###### EAP
Is a protocol for wireless networks that expands on authentication methods used by PPP
	PPP is a protocol that was commonly used o directly connect devices to each other
EAP is designed o support multiple authentication mechanisms, including tokens, smart cards, certificates. OTP, and public key encryption authentication
PEAP is encapsulated with TLS
EAP-FAST offers lightweight tunneling protocol to enable authentication EAP-TTLS server authenticates to the client with a certificate, allows the use of legacy authentication
###### CHAP
Provide authentication across a point to point link using PPP
CHAP is designed to provide authentication periodically through the use of challenge/response system
###### PAP
Does not provide any protection
Deprecated
###### SAML
Single sign on capability for web applications 
SAML is an XML based protocol that uses security tokens
By following identity providers to pass on credentials to service providers, SAML allows you log in to many different websites using one set of credentials
###### OAUth OpenID
OpenID and OAuth are typically used together, yet have different purposes
<mark style="background: #FF5582A6;">OpenID is used for authentication, whereas OAuth is used for authorization</mark>
###### Kerberos
Network authentication protocol designed for a client/server environment
Built around the idea of a trusted third party, termed a *key distribution center (KDC)*, which consists of an authentication server and a ticket granting server
Kerberos communicates via tickets that serve to prove the identity of users
Kerberos contains user IDs and passwords for all users
##### Access Control Schemes
###### Attribute-Based Access Control (ABAC)
Access control based on attributes associates with a subject or object
More complicated and costly to implement
###### Role-Based Access Control
Each user is assigned a set of roles that he or she may perform
Thus will be granted permissions in terms of specific duties
###### Rule-Based Access Control
Uses objects such as ACLs to help determine whether or not access should be granted
A series of rules is contained in the ACL, and whether to grant access will be based on these rules
###### MAC
Mandatory Access Control
A means of restricting access to objects based on the sensitivity of the information of such sensitivity
In MAC, the security mechanism controls access to all objects, and individual subjects cannot change that access
It is up to the access control mechanism to ensure than an individual with only permissions cannot access a Top Secret access
###### Discretionary Access Control (DAC)
Means of restricting access to objects based on the identity of subjects or groups to which they belong