[Objective 1.7] Summarize the techniques used in security assessments
##### Threat Hunting
Practice of proactively searching for cyber threats that are inside a network, yet remain undetected.
Most defensive elements are outward facing and are on or near the network perimeter, as this is where you are most likely to catch an unauthorized user.
Threat hunting uses tools and techniques to detect users who hide in a network.
Indicators of compromise are artifacts left behind by the activities of an attacker.
###### Intelligence Fusion
Threat intelligence fusion enables a defender to identify and contextualize the threats they face in the environment, using information from threat intelligence.
`Intelligence fusion is a process involving cllecting and analyzing threat feeds from both internal and external sources on a large scale`
###### Threat Feeds
Sources of information concerning adversaries.
Threat feeds can come from internal and external sources.
By leveraging threat data from your own network, it is possible to find other locations of the same threat in your environment.
###### Advisories and Bulletins
Published sets of information from partners , such as security vendors, government, and other "trusted" information.
These are external sources of threat feeds and need to be processed by security personnel to determine their applicability and how to use them to improve defenses for the enterprise.
###### Maneuver
Refers to the ability to move within a network, a tactic used by advanced adversaries as they move towards their objectives.
Threat hunting can counter an attacker maneuvering via a couple ways.
First, the threat hunter can watch for traffic where the unauthorized entity must pass (chokepoint)
Second, the threat hunter can analyze the company's own network infrastructure, through the eyes of an attacker and provide insight into how the network can be connected to provide better defenses against lateral movement, both in terms of connection and logging.
`Maneuvering is also a part of security professionals as a defense tactic to disrupt or prevent an attacket from moving laterally`
##### Vulnerability Scans
Process of examining services on computer systems for known vulnerabilities in a software.
Process of determining software program version and looking up known vulnerabilities.
###### False Positives
If you test for something, get a positive indication, but the indication is wrong, that is a false positive.
External factors can introduce errors, in turn these errors can influence a measurement.
The possibility of errors and their influence must be a part of the decision process.
Example: Nmap tests an OS like Windows 10. If this is incorrect, this is a false positive.
###### False Negatives
Opposite of false positives.
If you test something that comes back negative but it was in fact positive, this result is false negative.
Example: IDS does not generate a alert from a malware attack. This is false negative.
###### Log Reviews
The key is in proper configuration so that you can capture the events to want without adding extraneous data.
A log system is also a treasure for someone attacking a system.
Log reviews can provide information as to security incidents, policy violations, and other conditions.
###### Credentialed vs. Non-Credentialed
Vulnerability scans can be preformed with and without credentials.
Performing a scan without credentials can provide some information as to the state of a service and whether or not it might be vulnerable.
However, without credentials it is not possible to see the detail that a login provides.
*Credentialed vulnerability scans* can look deeper into a host and return more accurate and critical risk information.
Both can be used together, first a non-credentialed scan then based on preliminary results, more detailed credentialed scans are run on machines with the most promise for vulnerabilities.
###### Intrusive vs. Non-Intrusive
A non-intrusive scan is a simple scan of ports and services
An intrusive scan attempts to leverage potential vulnerabilities through an exploit to demonstrate the vulnerabilities. This intrusion can result in system crashes therefore referred to as intrusive.
###### Application
Vulnerability scans asses the strength of a deployed application against the desired performance of the system when being attacked.
Application vulnerabilities represent some of the riskier problems because the applications are necessary.
###### Web Application
Accessible from across the web.
Brings greater potential exposure to unauthorized activity.
Standard applications still apply, but the placing of the system on the web adds additional burdens to prevent unauthorized access and keep web based risks under control.
###### Network
The network can also be used in vulnerability scans to access connected systems. 
Most commons vulnerability scans are performed across the network in a sweep where all systems are scanned, mapped, and enumerated.
###### Common Vulnerabilities and Exposures (CVE)/Common Vulnerability Scoring System (CVSS)
CVS is a list of known vulnerabilities in software systems.
Each vulnerability has an identification number, description, and reference.
This is the basis for most vulnerability scanner systems, as the scanner determines software version and look up known reported vulnerabilities.

The CVSS is s scoring system to determine how risky a vulnerability can be to a system
Score ranges from 0-10, where if the score increases so does the severity of the risk.
Although CVSS can't take into account where the vulnerability is in an enterprise, it can help determine severity using metrics.
`CVE is a list of known vulnerbilities, CVS determines how risky a vulnerability can be to a system.`
###### Configuration Review
Configuration reviews are important enough that they should be automated and performed on a regular basis.
There are protocols and standards for measuring and validating configurations.
##### Syslog/Security Information and Event Management (SIEM)
Syslog is a standard protocol used in Linux to send system log or event messages to a specific server.
The information in a syslog server is just tables of raw data
To make this info easier to use, SIEM is employed to collect, aggregate, and apply pattern patching to the volumes of data.

###### Review Reports
Primary means of providing output from a SIEM is either a trap ort a alert
Reports can then be reviewed to determine whether an incident exists or is a false alarm
###### Packet Capture
More recently, concept of continuous packet captures to monitor a segment of network has become a tool in the security professionals toolbox.
Most security alerts occur after the attack, the packets are then long gone.
A continuous collection of the packets can provide that opportunity
Using a SIEM, coupled with next gen-firewalls, when a rule is fired, the network capture appliance can automatically collect and ship off a predetermined amount of traffic for later analysis.
###### Data Inputs
While a modern network can generate extremely large quantities of log data, what is important i a SIEM is to determine what information is needed to support what decisions.
What is important is to define the outputs desired from the SIEM and trace the necessary inputs from firewalls, servers, and so on to support those determinations.
###### User Behavior Analysis
Correlating events between systems can show patterns of activity  that are either normal and expected or abnormal and require investigation.
Many SIEMS have modules that analyze end-user behaviors, looking for anomalous patterns that indicate a need for analysis.
###### Sentiment Analysis
Used to identify and track patterns in human emotions, opinions, or aptitudes that may be present in data.
###### Security Monitoring
Process of collecting and analyzing information to detect suspicious behavior or unauthorized changed on your network and connected systems.
Complexity of modern IT systems makes it not possible without automated systems like SIEM
###### Log Aggregation
Process of combining logs together
Log aggregation works to allow multiple sources of information to be connected together in a more comprehensive picture
The goal is to take multiple data sources and condition the data into a form more searchable and usable 
##### Security Orchestration, Automation, and Response (SOAR)
SOAR takes SIEM data as well as data from other sources and assist in the creation of runbooks and playbooks, to examine an enterprise as an attacker would
Then using the information a threat hunter can narrow where they look for attackers
Information is also useful to security assessors as it lays out the security defenses in an understandable format
