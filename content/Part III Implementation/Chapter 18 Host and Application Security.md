[Objective 3.2] Given a scenario, implement host or application security solutions
##### Endpoint Protection
Is the concept of extending the security perimeter to devices that are connecting to the network.
Variety can be implemented such as antivirus, endpoint detection and response solutions, and firewalls.
###### Antivirus
Antivirus (AV) products attempt to identify, neutralize, or remove malicious programs, macros and files.
Provide protection against viruses, trojans, and other malware.
Up to date package is essential.
Most antivirus combine :
- Signature based scanning: like an IDS the antivirus scans programs, files macros, and other data for known worms, viruses and malware. Contains a dictionary of known virus signatures, what it does not known it cant catch.
- Heuristic scanning (analysis): does not rely on virus dictionary, instead it looks for suspicious behavior. Anything that does not fit into a normal pattern for the OS and apps running on the system being protected.
Most antivirus use a weight based system or a rule based system.
	Weight-based rates every suspicious behavior based on the degree of threat associated with that behavior. The set threshold is passed it will treat the process, app , or macro as a threat.
	 Rule-based compares activity to a set of rules meant to detect and identify malicious software. If part of a software matches a rule, or if a process app, macro performs a behavior it will threat it as a threat.
###### Anti-Malware
Name of a product designed to protect your machine from malicious software or malware.
Now combined with antivirus solutions into a single product.
One of most dangerous is ransomware, it spreads.
###### Endpoint Detection and Response (EDR)
Integrated solutions that combine individual endpoint security functions into a complete package.
These products are designed to integrate into an enterprise-solution with a neutralized management platform.
Unified endpoint management (UEM) is a newer security model that focuses on managing and securing devices in an enterprise such as desktops, phones and other devices.
###### DLP
DLP monitoring where file activity is reported to centralized systems, and to specialized DLP offerings such as the content DLP being rolled out by Microsoft across 365.
###### Next-Gen Firewalls (NGFW)
NGFW act by inspecting the actual traffic crossing the firewall - not by looking at source and destination but also the actual content being sent.
The challenge is maintaining appropriate rulesets that catch the desired bad traffic.
###### Host-based Intrusion Detection System (HIDS)
Act to detect undesired elements in network traffic to and from the host. It can be very specific with respect to threats to the OS and ignore those that would have no effect. Being deployed at a specific endpoint it can be tuned to the specific of the endpoint and applications, providing greater levels of specific detection.
Disadvantage is that it only detects the issues; it must rely on another component, typically through some logging or reporting mechanism, to act on the threat.
###### Host-based Intrusion Prevention System (HIPS)
Is an HIDS with additional components to permit it t respond automatically to a threat condition.
The response is as simple as dropping a packet up to killing a connection.
###### Host-based Firewall
Monitor and control traffic passing in to and out of a single system.
Included within software or the OS itself such as Windows Defender
##### Boot Integrity
Boot integrity is the characteristic of the intended hardware/firmware/software load for the system in compliance the the expected state.
###### Boot Security/UEFI
Secure Boot which is a mode that only allow signed drivers and OS loaders to be invoked.
Secure Boot enables the attestation that the drivers and OS loaders being used have not changed since they were approved for use.
###### Measured Boot
Hashed the subsequent processes and compares the hash values to known good values.
###### Boot Attestation
IS the reporting o the state of a system with respect to components and their relationship to the Root of Trust
This information can be used remotely by a server to determine if the OS is correct and has the correct patch level before allowing admission to a corporate VPN
`Attestation means verifying the authenticity of a platform or device based on a trusted record of evidence`
##### Database
###### Tokenization
Is the process of substituting a surrogate value, called a token, for a sensitive data element.
This allows processing of the data including referential integrity without disclosing the sensitive value.
###### Salting
Is the process of adding a random element to a value before performing a mathematical operation like hashing. This is done to add randomization and to also prevent original values from being hashed into an identical hash.
###### Hashing
Is a mathematical method of reducing a data element to a short form that is not reversible to the original form.

`Tokenization is the substituting of a surrogate value for a sensitive data element`
`Salting is the process of adding random element to a value before performing a mathematical operation`
`Hashing is a mathematical method of redicing a data element to a short form that is not reversible`
##### Application Security
###### Input Validations
Having a stringent and comprehensive validation of inputs prior to processing them is essential to filter out specific attacks.
Check everything before user. Ensuring that input is properly formulated.
###### Secure Cookies
Secure attribute instructs the browser and server to only transport the cookie over HTTPS channels
###### Code Signing
Involves applying a digital signature to code, providing a mechanism where the end user can verify the code integrity.