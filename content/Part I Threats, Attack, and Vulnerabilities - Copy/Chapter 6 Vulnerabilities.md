[Objective 1.6] Explain the security concerns associated with various types of vulnerabilities
##### Cloud-based vs. On-premises Vulnerabilities
With on-premise vulnerabilities, the enterprise has unfettered access to the infrastructure elements, making the discovery and remediation of vulnerabilities a problem defined by scope and resources.
With the cloud, the economies of scale and standardized environments give cloud providers an advantage in the scope and resource side of the equation.
##### Zero Day
Term used to define vulnerabilities that are newly discovered and not yet addressed by a patch.
If a researcher or developer discovers a vulnerability but does not share the information, then this vulnerability can be exploited without the vendor's ability to fix it, because all the practical knowledge is unknown except to the person who found it.
<mark style="background: #ABF7F7A6;">From the time of discovery until a fix or patch is made available, the vulnerability goes by the name "zero day", indicating it has not been addressed yet.</mark>
Although there are no patches for zero-day vulnerabilities, you can use compensating controls to mitigate the risk.
##### Weak Configurations
Most systems have significant configuration options that administrators can adjust to enable or disable functionality based on usage.
Configuring a database server to build a complete replica  of all actions as a backup system can result in a system that is bogged down and not capable of proper responses when usage is high.
Old options, such as support for legacy protocols, can lead to vulnerabilities.
Default credentials can lead to vulnerabilities.
###### Open Permissions
Having properly configured permissions is one of the best defenses that can be employed in an enterprise.
Managing permissions can be tedious and as the enterprise grows, the scale of permissions requires automation to manage.
When permissions are not properly set, the condition of *open permissions* exists.
The risk is context dependent, for some items, unauthorized access leads to little or no risk, whereas in other systems it can be catastrophic.
###### Unsecure Root Accounts
Root accounts have access to everything and the ability to do virtually any activity on a network.
All root accounts should be monitored and all accesses should be verified as correct.
<mark style="background: #D2B3FFA6;">One method of protecting high-value accounts such as root accounts is through access control vaults, where credentials are checked out before use.</mark>
`Strong configurations include secure root (Linux) and Administrator (Windows) accounts.`
###### Errors
The key to manage this condition is establishing error trapping and responses
One of the biggest weaknesses exploited by attackers is improper input validations
Errors should be trapped by the program and appropriate log files generated.
##### Weak Encryption
Cryptographic algorithms become trusted only after years of scrutiny and repelling attacks, so any new algorithms would take years to join the trusted set.
Errors in coding implementations are common and lead to weak implementations of secure algorithms that are vulnerable to bypass.
Deprecated and weak cryptographic algorithms is a weakness.
Example is SSL, now considered deprecated and should switch to TLS solutions.
##### Unsecure Protocols
Improperly secured communication protocols and services and unsecure credentials increase the risk of unauthorized access to the enterprise Network infrastructure devices.
When infrastructure systems are deployed, these devices remain online for years, and many of them are rarely rebooted, patched or upgraded.
###### Default Settings
Older operating systems used to have everything enabled by default.
Old versions of some systems had hidden administrator accounts, and Microsoft SQL used to have a blank admin password by default.
You should create settings as the default configuration baseline.
This way, the settings and the security implications are understood.
###### Open Ports and Services
For a service to respond to its request, its port must be open for communication
Having excess open services leads to pathways into your systems that must be protected.
Disabling unnecessary services, closing ports, and using firewalls to prevent communications except on approved channels creates a barrier to entry by unauthorized users.
Many services runs with elevated privileges by default and malware takes advantage of this.
Security professionals should make every effort to audit services and disable any that aren't required.
###### Third-Party Risks
The enterprise computing environment is full of third parties, and their risks become enterprise risks.
Common third-party risks that are overlooked are issues of vendor management, system integration, and lack of vendor support.
What was once a good fit might not be at a future point in time.
It is important to have an inventory of what the software is, by version, and where it is used.
This assists the security in monitoring sources for vulnerabilities through sources.
This list will also help in determining risk levels as software reaches its end of life or end of service life.
`Remember that supply chain concerns and lack of vendor support are concerns directly related to third-party risks and management`
###### Vendor Management
The challenge of vendor management is one of determining one's own needs and then finding the vendor that offer the best value proposition against those needs.
Support, system lifetime, and maintenance all play a role in long term value of a vendor.
###### System Integration
The connecting of these components, each representing a portion of the system into a complete functioning unit.
System integration is an are where vulnerabilities can exist, as the pieces can have gaps in their integration or capabilities that do not manifest per their desired specification.
System integration is coupled with configuration management.
###### Lack of Vendor Support
When an item reaches its end of life (EOL), this signifies the finality if its life under almost all circumstances.
An organizations that continues to use the product assumes all of the risk associated with issues uncovered after the product has entered EOL status.
###### Supply Chain
Supply chain risk is caused by vulnerabilities that lie within the supply chain
Whether from the actual supply chain itself or a product from a third party, the results are the same - a level of risk is increased.
`A supply chain typically occurs at the weakest security link or even in the product delivery phase`
###### Outsourced Code Development
Code can be one of the greatest sources of vulnerabilities and risk in an enterprise.
However, code developed by a third party, often using third-party code fragments, the chain of risk becomes long and difficult to manage.
The risk isn't in the fact that the code is outsourced, but the visibility and control over these risks becomes harder to manage with every step away from the source.
It is important to have conditions in contracts requiring appropriate development measures be in place for third-party code, including the rights to inspect and verify security functionality.
Ensuring third-party developers have appropriately secure coding practices and having their code reviewed by independent testers and placed in escrow for safekeeping are considered best practices.
###### Data Storage
Data storage is typically distributed throughout the enterprise in different capacities and configurations.
As data is distributed across into multiple enclaves and different requirements and criticalities, the management of data becomes more difficult.
Ensuring the correct access controls and security protections such as backups is important for al data stores, any gap creates vulnerabilities.
<mark style="background: #FFB86CA6;">To ensure all data is protected from becoming a vulnerability to the system, having standardized data storage policy and checklist is good practice.</mark>
##### Improper or Weak Patch Management
One of the important takes away from patching is that once a supplier patches their software, hackers can reverse engineer the vulnerability from the patch.
Therefore, once the patch is released attackers learn where to attack.
To manage with risk associated with patch management vulnerabilities, it is important to establish a strong patch management program that covers all systems and all software.
This makes patch management one of the most essential security controls and where there should be no excuses to why it was not implemented.
<mark style="background: #ADCCFFA6;">It is important to have defined periods of time when patches must be installed as well as an automated means of determining what patches are needed</mark>
###### Firmware
Firmware is another form of software with one distinction: it is stored in hardware to be present when the system boots up.
With firmware being a part of the system itself, it is frequently missed when considering how to keep software up to date.
The vulnerabilities and maintenance associated with firmware mirror those of software.
Patching firmware is often neglected.
###### Operating System (OS)
Today many operating systems can patch themselves, and automation is easy.
First, have a patch management policy. and male it patch everything and track all patches.
Second, follow up on that policy.
Patch on system, test to see if it works, and then patch the rest.
###### Applications
Applications require updating and patching to fix bugs and vulnerabilities.
The challenge is the tracking of all applications used.
The enterprise has to keep track o what apps and when they require updating.
Some companies make it easy to know when to update and others a challenge.
There are applications designed to manage this aspect and is recommended.
##### Legacy Platforms
Term used to describe systems that are no longer being marketed or supported
They are considered old, which can be a little as a few years.
Being in the legacy category means they are no longer supported.
Having systems that can't be patched is a risk
###### Impacts
Impacts are the resulting effects of a risk that is realized.
Impacts are the items an organization is attempting to avoid with a security incident.
###### Data Loss
Data loss is when an organization loses information.
Strong access controls, encryption of data, and data loss prevention (DLP) can lessen the impact.
<mark style="background: #ABF7F7A6;">Encryption is the strongest control because a breach of encrypted data isn't actually a breach.</mark>
###### Data Exfiltration
Data can be copied and then stolen, without affecting the original data.
The theft only occurs when they escape with the item.
Data exfiltration is the exporting of stolen data from an enterprise.
###### Identity Theft
When someone uses information on another party to impersonate them.
Secondary impact once data is exfiltrated.
The impact of PII being exfiltrated can be significant in terms of costs.
###### Financial
Risk is measured in financial terms, and the impact of vulnerabilities can be expressed in financial terms as well.
List of items that can contribute to financial costs:
- Costs with investigation and fixing
- Lost orders/revenue due to downtime
- Attorney fees from lawsuits
- Ransom payments
- Losses due to stolen intellectual property
- Share price decline and market capitalization loss
##### Reputation
Reputation as a result of  of a cyber attack comes in two forms: loss of customer confidence and a competitive field loss of key employees.
If your customer base questions ability to fulfill orders and mange their information or confidence in company management, customers may o a competitor.
Companies that have high skilled workforce members may be concerned about their reputation.
###### Availability Loss
CIA triad is confidentiality, integrity, and availability
Downtime can lead to loss of revenue if ling enough and SLAs being broken