[Objective 1.5] Explain different threat actors, vectors, and intelligence sources

A <mark style="background: #FF5582A6;">threat actor is the source </mark>of the threat on the system
<mark style="background: #BBFABBA6;">Vectors are the methods</mark> that the threat actors use to attack a vulnerability in a system
<mark style="background: #FFB86CA6;">Threat intelligence is a knowledge</mark> that allows you to prevent or mitigate cyber threats

##### Actors and Threats
The act of deliberately accessing computers and networks without authorization is referred to as hacking, with the individuals called hackers.
<mark style="background: #FF5582A6;">Attacks by an individual or even a small group of attackers fall into the *unstructured threat* category</mark>
Attacks at this level generally are conducted over short periods of time, do not involve a large number of individuals.
##### Advanced Persistent Threats (APTs)
A major advance in cyberattacks is the development of advanced persistent threats
An APT is characterized by using toolkits to achieve a presence on a target network, and then focusing on the long game by maintaining admin access and avoid detection.
##### Insider Threats
Insiders are more dangerous than outside intruders
The reason is insiders have the access and knowledge necessary to cause immediate damage to an organization.
They also may know security systems in place and are better to avoid detection
An attack may also be an accident and not intended at all.

Separation of duties, where function requires more than one person to affect changes, is a way to prevent any individual from performing critical duties.
##### State Actors
Elite hackers employed by major cybersecurity firms in an effort to combat criminal activity
Others are employed by nation-states and other international organizations, to train and run large groups of skilled hackers to conduct nation-state attacks.
As nations have become dependent on computer systems, essential elements in society might be targeted by organizations or other nations.
Many nations have developed capabilities to conduct *informational warfare*
	Warfare conducted against the information and information-processing equipment used by an adversary
<mark style="background: #FFB8EBA6;">Information warfare falls into the *highly structured threat* category</mark>
Characterized by longer preparation and a large group of attackers
##### Hacktivists
Account for 8 to 12 percent of malicious Internet activity
When hackers work together for a collective effort
They may include script kiddies but in general they do not have the skills to participate in a meaningful manner, they may be enlists as ground troops to add volume to an attack
###### Script Kiddies
Low end of the spectrum
Individuals who do not have the technical expertise to develop scripts or discover new vulnerabilities, but have enough understanding of computer systems to be able to download and run scripts that others have developed
Not interested in attacking specific targets, but instead want to find any organization that hasn't patched a newly discovered vulnerability with a script to exploit.
Fastest growing group
###### Criminal Syndicates
One of the major changes over the past decade in cybersecurity has been the ability for hackers to monetize their efforts.
Part of this is due to the rise of cryptocurrency, but an entire marketplace exists for stolen, identities, financial data.
Attacks by criminal organizations usually fall into the *structured threat* category
##### Hackers
Describes anyone using computers improperly. This has led to the descriptors authorized, unauthorized, and semi-authorized
###### Authorized
Use their computer skills for good purpose. The common name "white" hackers.
They can be security consultants or penetration testers.
The white hat hacker uses same tools and techniques as threat actors, but doing with permission so a firm can learn it's weaknesses.
###### Unauthorized
Black hats rather use their skills for illegal and criminal activities
There are many motivation behind black hat hackers, but all illegal
###### Semi-authorized
Grey hat hackers may use their skills for good at their job as a white hacker
But at other times they use the same skills illegally acting as a black hat hacker
Works in both realms.
##### Shadow IT
Name given to the parts of an organization that perform their own IT functions
Rises from a desire "to get things done" when central IT does not respond in what they consider a reasonable time frame.
Might seem helpful but if outside of the central IT it can lead to a risk for outside threats and infrastructure.
###### Competitors
Competitors have been known to attack other firms IT processes
This includes stealing intellectual property or customer lists as well as DoS attacks
#### Attribute of Actors
There are ways to differentiate the threat actors: by location (internal/external), level of sophistication, level of resources, and intent.
###### Internal/External
Internal threat actors have access to the system
Although access may be limited to user level, it still provides the threat actor the ability to pursue the attack.
External actors need additional steps to take: establish access to the target system
###### Level of Sophistication/Capability
Within a group of threat actors , the skill the level of individual members of the group may be mixed, with a few high level skilled and less skilled participants.
Greater the skill, the more an individual will be expected to lead and design the attacks.
As skill level goes up, so do the use of minimal methods.
Zero-day vulnerabilities are rarely used, they are reserved for the few cases where there are no other options.
###### Resources/Funding
Criminal organizations and nation-states have larger budgets, bigger teams, and the ability to pursue campaigns for longer periods of time, some lasting years.
###### Intent/Motivation
At the top of the intent pyramid is the APT threat actor, whose intent is at least threefold
First is the drive to maintain continual access. Second is to remain undetected. Third is the goal of stealing something of value on the network.
APT's do not go to all the trouble of maintaining access and remain invisible  just to crash a system or force a rebuild.
##### Vectors
Vectors is the term for the various methods that an attacker can use to get in.
If there is a way to move data into your system this can be a potential vector for attackers to use.
###### Direct Access
This can be an insider attack or perhaps outsiders are given the ability to interact directly with systems.
Direct access is why we need to use the principle of least privilege, only giving necessary permissions and blocking all others.
###### Wireless
Wireless networks brings simplicity and with that it also brings security issues.
No longer does the attacker have to have direct physical access to the network.
###### Supply Chain
Involves using a company's supply chain as an agent in the attack.
An attack finds a mean by which they can get their attack code into the supply chain for a product or an update.
###### Social Media
Can be used for social engineering attacks, and for security checks and other communication channels.
Redirection in URLs is commonly used in order to trick a user
###### Removable Media
This type of storage is small and takes no skill to attach to a PC
This becomes a threat driven by social engineering
The trick is to get someone to interact with the file.
Placing a USB in a location prone to discovery is called a  "USB drop attack"
You can employ USB blockers and disable AutoPlay
###### Cloud
If your cloud agreement does not include antivirus protection on files, then it is really no different from any other internet-connected source.
##### Threat Intelligence Sources
Threat intelligence is the gathering of information from a variety of sources, including nonpublic sources.
Threat intelligence sources are the places where one can get this information from open source, proprietary, to specialized sources.
###### Open Source Intelligence (OSINT)
Refers to data collected from public sources.
The challenge is collating the information into a usable format
The importance is where its information comes from, how reliable the information is, and how up to date.
###### Closed/Proprietary
Threat intelligence marketplace is filled with security firms offering threat intelligence products.
One of the offerings is access to their closed or proprietary database.
One of the key factors is the number and diversity of data feeds.
Common formats include CSV, JSON, XML, and STIX.
STIX is the **Structured Threat Information Expression** format
###### Vulnerability Databases
The weakness in software that allow an attacker a means of entry
You need to know what is vulnerable and either patch the vulnerability or provide a defensive solution to prevent the vulnerability from being exposed to an attacker.
*Vulnerability databases* is a database of vulnerabilities that is cataloged and maintained
NVD is a repository of vulnerabilities and information such as checklist references
###### Public/Private Information Sharing Centers
There are Information Sharing and Analysis Centers and Information Sharing and Analysis Organizations
ISAOs vary greatly in capability but include any organization, that is sharing cyber related information for the purpose of enhancing the members cybersecurity posture
ISAC's are privately run, but government approved, industry based cyber security.
Both share what is happening and learn together.
The sharing is anonymized, the analysis is performed by highly skilled workers in a security operations center, and the resulting information is fed back to the members in real time.
###### Dark Web
Subset if the worldwide content on the Internet, that has access restricted via obfuscation methods
Dark web sites require Tor - a open source software that enables anonymous communication
The web sites end in .onion
###### Indicators of Compromise
Indications that a system has been compromised and left behind on the system
Common set of IoC's include
- Unusual outbound traffic
- Anomalies in privileged user account activity
- geographical irregularities in network traffic
- Account login red flags
- increase in database read volumes
- HTML response sized
- Large number of requests for the same files
- Suspicious registry changes
- Unusual DNS requests
- Unexpected patching of systems
- Signs of DDoS activity, even temporary
###### Automated Indicator Sharing (AIS)
Automated, bidirectional cyber-threat indicator that's used for reporting.
<mark style="background: #FFB86CA6;">A key element of AIS is that it operates at machine speed, permitting real time reporting and response.</mark>
Firms must sign up to join this effort, and once they agree to anonymized information sharing , their connection is established.
The goal of AIS is to commoditize collection of threat intelligence information to enable everyone access to feeds of cyber threats.
<mark style="background: #FFF3A3A6;">AIS uses Structured Threat Information Expression (STIX) and Trusted Automated Exchange of Intelligence Information specifications to enable machint-to-machine communication at machine speed
</mark>
Participants in AIS must be able to produce and consume these protocols
##### Structured Threat Intelligence Expression (STIX)/Trusted Automated Exchange of Intelligence Information (TAXII)
Both STIX and TAXII provide a set of community-driven standards that enable the automated exchange of information associated with cyber threats, network defense, and threat analysis
STIX is  a standardized, machine-readable structured language to represent cyber-threat information.
TAXII defines a set of services and message exchanges that enable the automated sharing of actionable cyber-threat information across organizational, product line, and service boundaries.
<mark style="background: #FFB8EBA6;">TAXII represents the transport method, and STIX represents the cyber-threat information</mark>
###### Predictive Analysis
The use of threat intelligence information to anticipate the next move of a threat
This is done by using a large quantity of data and finding the key pieces that are necessary to make a hypothesis about what threats there are and determine how to find them.
Works best when tailored to specifics of an industry.
It can also be useful to examine new threats that emerge because of some specific factor.
###### Threat Maps
Geographical representation of attacks showing where packets are coming from and going to.
Just because an attack comes from an IP in a certain city does not mean the attack originated from there.
The machine attacking may be a victim, with attacker working from somewhere else.
###### File/Code Repositories
Growth in software development has been file/code repositories. Where people can work together on projects and develop software.
This can be used in two roles in threat intelligence. First, source code can give them a chance to examine for vulnerabilities. Second, you can use same sources to examine the capabilities of some of the tools your adversaries will use against you.
They are a source for both sides.
##### Research Sources
Each has strengths and weaknesses
###### Vendor Websites
Vendor websites appear to be teeming with information used for marketing.
You need to find out what their sources are, how they are curated, and what standards they use.
###### Vulnerability Feeds
It is important to vet your feeds for a variety of issues, including what the source of the data is and what specific characteristics are presented as part of the feed.
Using multiple feeds, with different sources and characteristics, consolidated to a single database is the path to better coverage.
###### Conferences
Timelines for conference submissions are much shorter than journals
The presentation of the material at the conference is a good way to get multiple points of view in the form of feedback in a quicker fashion
Downside is until the feedback is vetted, most conference papers have little serious peer review, so they need to be treated with an open eye toward accuracy and applicability.
###### Academic Journals
Research that has been peer reviewed and is published in academic journals
Publishing a paper in an academic journal can take from a year to 18 months at the minimum - after the work is done.
Delay is due to peer reviews and editing
This means academic research in journals are outdated by the time it is printed
###### Requests for Comments (RFCs)
Sets of standards used to define how the internet and protocols involved in the world wide web are established and managed
There are fixed in time when written
Changes to these documents are formal and noted, and if an Internet standard requires updating, a new RFC is drafted and approved
Useful as source documents because they list the details by which the protocols operate
###### Local Industry Groups
They are a good source of practical information concerning threats, threat actors, and what can be done to defend networks
They are  a solid networking source of information that enables one to get answers to questions that have been vetted by others in similar positions.
###### Social Media
The key is vetting the sources of information
Share ideas with like-minded people
###### Threat Feeds
Very much like vulnerability feeds
Understanding where information comes from, how it has been vetted and how it applies to your industry are important elements.
###### Adversary Tactics, Techniques, and Procedures (TTPs)
Used to describe how threat agents organize and orchestrate their efforts
TTPs, or the patterns used by adversaries, are key elements of a threat intelligence program
These methods can be cataloged and understood as attack patterns
