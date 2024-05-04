[Objective 2.1] Explain the importance of security concepts in an enterprise environment
##### Configuration Management
Proper configurations are essential in the enterprise. Monitoring and protecting a system from unauthorized configuration changes is important for security.
###### Diagrams
Commonly used in architectural specification to communicate how enterprise is configured
###### Baseline Configuration
Representation of how the system is supposed to be configured.
This will require updating as time goes on and updates are applied; making it current with the desired system configuration.
A baseline deviation is a change from the original baseline value. This change can be positive lowering the risk or negative increasing the risk.
###### Standard Naming Conventions
Having properly named file, folders, computers, devices that facilitates clear communication eliminates errors.
###### Internet Protocol (IP) Schema
`Configuration management includes developing physical and logical diagrams, establishing secure baselines, creating understandable naming convenctions and implementing secure IP schemas`
##### Data Sovereignty
New legislation that data stored within their borders is subject to their laws, and in some cases that data originating there must be stored there.
Several high end companies have changed their business strategies in order to comply
Data sovereignty can drive architectural decisions in enterprises that are multinational
##### Data Protection
Is the set of policies, procedures, tools. and architectures used to ensure proper control over the data in the enterprise.
Data is the most important element to protect in the enterprise.
Equipment can be replaced information has value.
Data security refers to the action taken in the enterprise to secure data, wherever it resides
###### Data Loss Prevention
Serves to prevent sensitive data from leaving the network without notice
DLP solutions are designed to protect data in transit/motion, at rest or processing from unauthorized use or exfiltration
###### Masking
Data masking involves the hiding of data by substituting altered values.
Data masking makes reverse engineering or detection impossible
###### Encryption
Data encryption continues to be the best solution for data security
Developing policies and procedures to ensure that the correct data fields are properly encrypted and that the business applications that need to use the data are configured to read the data is part of overall enterprise architecture scheme.
##### At Rest
Data at rest refers to data being stored, regardless of what media is stored on
Encryption is the best means of protection
###### In Transit/Motion
Data has value in the enterprise. Whenever data is in transit/motion, being moved from one system to another, it needs to be protected.
Most common method is encryption
###### In Processing
Data can be risked in memory or even in processing.
Data in processing is data that is actively being used, either in a processor or other computational element.
Protected memory schemes and address space layout randomization are two tools that can be used to prevent data security failures during processing.
Secure data principles, including the definitive wiping of critical data elements once they are no longer needed, can assist in protecting data that is processing.
##### Tokenization
<mark style="background: #FFF3A3A6;">The use of a random value to take place of a data element that has traceable meaning.</mark>
Tokens are used all the time in data transmission systems to protect sensitive information from being used or shared.
Tokenization is not an encryption step because encrypted data can be decrypted.
###### Rights Management
The systematic establishment of rules and order to the various rights that users can invoke over digital objects
Digital rights management is the term used to describe rights scenarios associated with various types of media files including playing them, copying and editing them.
Developing corporate-level set of policies and procedures to manage rights is essential.
##### Geographical Considerations
There are a wide range of laws and regulations that do not stop at physical borders
There data protection laws may mandate certain data elements are stored on servers within their national borders.
##### Response and Recovery Controls
Disaster recovery and Business continuity 
Having mechanisms in place to restore data from backups and resume normal operation are elements that need to be designed into the enterprise
##### Secure Sockets Layer (SSL)/Transport Layer Security (TLS) Inspection
To perform the task of SSL/TLS inspection, the appliance must receive a set of proper keys to the encryption
The appliance can then receive, decrypt data, re-encrypt using the same keys and send data.
It is common for next-gen firewalls to have TLS inspection built in, providing protection for inbound and outbound data.
TLS inspection consists of two connections: server and client protection
To perform TLS inspection requires two separate secure connections: one from client to firewall and one from firewall to server
###### Hashing
Hashing is a means of enabling data protection while still enabling the user of the underlying data
###### API Considerations
Designing in the correct set of authentication and authorization protocols is essential to enable this technology
APIs are like doors and windows of modern application
##### Site Resiliency
Restoration sites and their availability
Sites referred to as recovery sites
- Hot Sites
- Cold Sites
- Warm Sites
###### Deception and Disruption
Deception adds a fake layer to your enterprise by placing decoy assets, fake data in your enterprise.
This is not part of enterprises configuration so no system or person should ever touch something fake unless they are actively seeking something or there is a misconfiguration
###### Honeypots
Possesses fake data to attract hackers
###### Honeynets
Network designed to look like a corporate network
Makes it easy to characterize the attackers traffic and where attacks come from
###### Fake Telemetry
Synthetic network traffic that resembles genuine comms, delivered at an appropiate volume to make honeynets and honeypots look real
###### DNS Sinkhole
DNS provider that returns specific DNS requests with fake results
A standard DNS server that has been configured to return nonroutable addresses for all domains