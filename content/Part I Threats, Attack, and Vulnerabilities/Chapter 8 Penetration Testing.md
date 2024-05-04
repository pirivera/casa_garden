[Objective 1.8] Explain the techniques used in penetration testing
##### Penetration Testing
Simulates an attack from a malicious outsider
Often the most aggressive form of security testing and can take many forms, depending on what is considered "in" and "out" of scope
A pen test attempts to exploit vulnerabilities to see how much access they allow
Useful in the following ways
- They can show "low-risk" items that can be exploited to gain access to make it "high-risk"
- Can be used to test the training of employees, the effectiveness of your security measures, and the ability of your staff to detect and respond to potential attackers
- Often identifies and test vulnerabilities that are difficult to detect with traditional scanning tools
It is important to mimic real-world attackers if that is what the company wants to test its defenses against
###### Known Environment
Known environment (white box) testing is almost the opposite of unknown environment (black box) testing.
Sometimes called clear box testing, white box techniques test the internal structures and processing within an application for bugs, vulnerabilities and so on.
A white box tester will have detailed knowledge of the application they are examining - they'll develop test cases designed to exercise each path
Sometimes the term white box testing is applied to network assessments where tester  has detailed knowledge of the network.
###### Unknown Environment
Unknown environment (black box) testing is a software-testing technique that consists of finding implementation bugs using malformed data injected in an automated fashion.
Black box testing tests the functionality of the software from an external perspective.
Testers typically do not have any knowledge of the internal working of the software.
No visibility into how data is processed, only the output
Developers can potentially find and correct errors in the development or testing stage
###### Partially Known Environment
Gray box testing, the testers typically have some knowledge of the software, network, or systems they are testing.
This can be efficient and effective because testers can often quickly eliminate entire testing paths, test cases and can rule out things that are not worth trying.
###### Rules of Engagement
Critical for several reasons
	Activities associated with a penetration test are illegal if not authorized, and the rules of engagement specify legal authority that the penetration testers have in performing their duties.
	Rules of engagement also establish the boundaries with the test, what is in scope and what is not
The scope of activities should be nondestructive, but what considers proof of compromise must be determined.
How  testers interact with employees when discovered should also be included, as well as a point of contact whom to call when something that requires immediate enterprise action.
###### Lateral Movement
Sometimes referred to as network lateral movement, refers to the process used by attackers to move deeper into a network to get the target data.
<mark style="background: #FFB86CA6;">Process of moving across a network is referred to as lateral movement and is a common event for advances attackers.</mark>
###### Privilege Escalation
Process of gaining increased privileges for an account.
Some of these paths are easy to block - blocking local admin and limiting the number of users with native admin ability.
There are two types of privilege escalation: horizontal and vertical
	Horizontal, the attacker expands their privilege by taking over another account and misusing the legitimate privileges granted. Frequently done with lateral movement.
	Vertical, the attacker attempts to gain more permissions or access with an existing account they have already compromised.
	Vertical requires more sophistication and is the main technique used by advanced persistent threats (APT's)
###### Persistence
The ability to exist beyond a machine reboot or after disconnection
That means the attacker will come back into the network and it will not be obvious when they reenter
Persistence can be achieved by backdoors, using bots, fake accounts, and manipulating OS items such as DLLs or permissions.
###### Cleanup
Attacking a system can leave a lot of evidence laying around
Testing vulnerabilities and access control systems creates a pile of failed events.
Covering up tracks is an essential step
Clearing logs, blocking remote logging, messing with system history, and using reverse shells and ICMP tunnels to avoid detection and logging are some of the methods employed.
Use of rootkits to modify the OS so that specific account-based activities are not logged is one of the methods used by APT attacks.
As an attacker moves laterally within the network and escalates privileges, covering their tracks behind makes it very difficult for defenders to find the attacker once they have moved to a different account or machine.
###### Bug Bounty
Programs where companies pay hackers for revealing the details of vulnerabilities that they discover. Important aspect is that in order for bug bounty on the company to be legal, the firm must have an established bug bounty program, and the hunting activity must be in accordance with the program. 
The firm that runs the program sets the rule of engagement.
###### Pivoting
Pivoting a is a technique similar to lateral movement. One moves to a new location in a network and begins the attack process over again, performing scans to see machines that were not visible from the outside.
Pivoting is one of the key methods of learning where to move next in a network
To cross a screen subnet (DMZ) takes a couple of pivots.
One of the giveaways of this activity is internal scanning. A scan reveals someone is looking, slowing down the scans can avoid detection.
`Lateral movement is to go where data is, and Pivoting is learning where to move next`

##### Passive and Active Reconnaissance
*Passive reconnaissance* is performed using methods to gain information about targeted computers and networks without actively engaging with the target systems and avoiding detection.
*Active reconnaissance*, the attacker engages with the target system, typically conducting a port scan to find any open ports.
Active reconnaissance involves using packets that can be traced; it involves engaging services that can be logged.
Passive has limits on how much an attacker can learn, but its stealthy.
Active is much informative, but tells machines they are being attacked.
Key is to use passive first, and active when necessary to get job done.
###### Drones
War flying is the name of a drone able to capture network traffic.
###### War Flying
Using a drone to fly over a facility and capture wireless network traffic
###### War Driving
The same as war flying but instead, drives past the point of access.
War shipping is shipping a device with a large battery that collects data as long as phone is on. This bypasses guards and gates.
###### Footprinting
Also called reconnaissance, is first step in gathering active information on a network
A pen tester can gather information on computers and user information as well.
##### OSINT
Open Source Intelligence, is the technique of using publicly available information sources to gather information.
Beginning with zero knowledge, OSINT can increase significantly a unknown environment to a partially known environment.
##### Exercise Types
Red Team- focused on the offense
Blue Team- Focused on the defense
White Team - Are there to ensure that the exercise stays on track
Purple Team - mix of red and blue