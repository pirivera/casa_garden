---
draft:
---

[Objective 1.3] Analyze potential indicators associated with application attacks
##### Privilege Escalation
Most attacks begin at a privilege level with an ordinary user
The attacker then exploits vulnerabilities that enable them to achieve root or admin access
This step is called privilege escalation
One way is to use existing privileges to perform an action that steals a better set of credentials
Another method is exploiting vulnerabilities in processes that are running with escalated privileges. Injecting malicious code achieves escalated privilege.
###### Cross-Site Scripting
Cause of vulnerability is weak user input validation
An attacker can include a script in their input and have it rendered as part of the web process
Different types of XSS:
- Non-persistent XSS attack - the injected script is not persisted or stored but rather is immediately executed and passed back via the web server
- Persistent XSS attack - The script is permanently stored on the web server or some back-end storage. This allows the script to be used against others who log in to the system.
- DOM- based XSS attack - The script is executed in the browser via the Document Object Model (DOM) process as opposed to the web server
XSS can be used for session hijacking, impersonation, phishing, theft of authentication

Well designed Anti-XSS input libraries have proven as best defense
XSS should be tested as part of plan for every application
Various other ways to mitigate attacks include limiting the type of uploads, screening the size of uploads, and whitelisting inputs
`Input validation is helpful at preventing XSS attacks`
###### Injection Attacks
User input without input validation results in opportunity for the attacker to craft input to create specific events that occur when the input is parsed and used by an application

SQL injection attacks involve the manipulation of input, resulting in an SQL statement that is different from the statement the designer intended

Extensible Markup Language (XML) injection attacks and Lightweight Directory Access Protocol injection (LDAP) attacks  are performed in the same way.
Because SQL, XML, and LDAP are used to store date, this can give an attacker access to data.
Command injection attacks occur when input allows command-line manipulation.
###### Structured Query Language (SQL)
SQL injection is a form of code injection aimed at any SQL-based database regardless of vendor.
An example is substituting user provided inputs and puts them in  a **where** clause into which it gives a false answer. Such as putting a username and password *where* it is a correct one, into 1=1 - to list all that equals a true statement
*Stored procedures* are precompiled methods implemented within a database engine.
Stored procedures act as a secure coding mechanism because they isolate user input from the actual SQL statements being executed; separation of user input from SQL statements.
`Stored procedures are the gold standard for preventing SQL injection attacks and are specifically mentioned in the objectives`
###### Dynamic-Link Library (DLL)
A piece of code that can add functionality to a program through inclusion of library routines linked at runtime.
A DLL that has a specific function vulnerability can be capitalized by the attacker.
Adding a evil DLL in correct directory via a registry key can result in functionality being incurred.
###### Lightweight Directory Access Protocol (LDAP)
An LDAP request based on user input, can lead to a bad LDAP request if there's a failure
LDAP injection can be done in a directory system
Such a a wildcard * in a search card can be beyond the scope of a query.
Proper input validation is important.
###### Extensible Markup Language (XML)
XML injections can be used to manipulate an XML-based system
XML can alter changes in configurations, changes in data streams, change in outputs
###### Pointer/Object Dereference
A pointer is a construct that refers to the memory location that holds the variable
To get the value at the memory locations denoted by a pointer variable, one must dereference the pointer.
The act of dereferencing a pointer now changes the meaning of the object to the contents of the memory location, not the memory location as identified by the pointer.
Mistakes in input validation can lead to errors in the pointer dereference, which may trigger an error, as the location will contain data and it will be returned.
###### Directory Traversal
When an attacker uses special inputs to circumvent the directory filesystem
Classified as input validation errors, these can be difficult to detect without doing code walkthroughs and specifically looking for them.
Directory traversals can be masked by using the encoding of input streams
	If the security check is done before the string is decoded by the system parser, the recognition of the attack may be impaired
Parsers are used to render the canonical form for the OS such as "Rose is a r%6fse"
###### Buffer Overflow
Nearly half of all exploits of computer programs for from some form of buffer overflow
The generic classification of buffer overflow includes many variants, such as static buffer overruns, indexing errors, format string bugs, Unicode and ANSI buffer size mismatches, and heap overruns.

The input buffer that is used to hold program input is overwritten with data that is larger than the buffer can hold.
The root cause is poor programming and programming language weakness.
Many programs will provide error checking to ensure that too many characters will not cause a problem. Some programs however cannot handle this error and the extra characters continue to fill memory, overwriting portions of the programs.
This can cause program to abort or system crash.
Some programs can execute a command supplied by the attacker.
Buffer overflows typically inherit the level of privilege of the program exploited, this is why programs with root level access are so dangerous with a buffer overflow, as code executed will be run as root level privilege as well.
Buffer overflow are input validation attacks that are designed to take advantage of input that foes not validate the length of inputs.
Solution is the validation of input lengths prior to writing to memory.
This can be done such as the use of safe library functions for inputs.
###### Race Condition
An error condition that occurs when the output of a function is dependent on the sequence of timing of the inputs.
It becomes a bug when the inputs do not happen in the order the programmer intended.
Race conditions can occur in multithreaded or distributed programs when the sequence or timing of processes or threads is important for the program to operate properly.
These conditions can be difficult to predict and find.
Race conditions are defined by race windows, a period of opportunity when concurrent threads can compete in attempting to alter the same object.

First step to avoid is to identify the race windows. Once identified, the system can be designed so that they are not called concurrently. This is called *mutual exclusion*.
Race conditions can be combated with reference counters, kernel locks, and thread synchronization.

The impact of a race condition is usually the failure of a system in the form of a crash.

Race counters are structures in the kernel that detail where or not a resource is actively being used at the current moment.

Another timing issue is the infinite loop. When program logic becomes complex care should be taken to ensure that all conditions are covered and that errors and other loop breaking mechanisms to not allow the program to enter a state where the loop control fails.
Such as date processing on leap years, if the sequence is not satisfied causing a loop and crashing.

`Race conditions can be used for privilege escalation and DoS attacks`
###### Time of Check/Time of Use
It is possible for different systems to attempt to interact with the same object at the same time
It is also possible for events to occur out of sequence based on timing differences between different threads of a program
Understanding how and where these conditions can occur is important to development team
What develops is known as a race condition, or a vulnerable time of check/ time of use attack
`A time of check/ time of use attack is one that takes advantage of a seperation between the the time a program checks a value and when it uses the value, allowing an unathorized manipulation that can affect the outcome of a process`
###### Improper Error Handling
Forcing errors to move an application from normal operation to exception handling
During an exception, it is common to report the condition in a log file and the error condition
This information can be valuable to an attacker
The best method is to capture it in a log file and secured by an access control list (ACL)
Echoing error condition details to users can provide information to attackers when they cause errors on purpose
*Improper error handling* disclose data structures and date elements with SQL
Remote procedure call (RPC) errors can give filenames, paths, and server names
Programmatic errors can disclose line numbers
Attackers can use the information they gather to further their attack
###### Improper Input Handling
*Improper input handling* is the true number-one cause of software vulnerabilities
This is the root cause behind most overflows, injection attacks, and structure errors
Newer input handling attacks include canonicalization attacks and arithmetic attacks

`Input validation is suited for the vulnerabilities: buffer overflow, XSS, cross-site request forgery (XSRF), path traversal, and incorrect calculation buffer size`

What can work is a whitelisting approach, here the input is validated, and then parsed into a standard structure that is then executed
##### Replay Attacks
Attempting to re-create the conditions that existed the first time the sequence of events occur
If an attacker can record a series of packets and then replay them, what was valid before may be valid again
There is a wide range of defenses against these attacks, this shouldn't be issue
###### Session Replay
When a user connects to a system via the web, the connection forms a "session" that transmits back and forth between client and server
*Session Replay* is the re-creation of this interaction after it has occurred
For replay to work, there needs to be instrumentation because most of the content and transactions are stateless by themselves, in that they don't have the information of where the user came from or where they went
Replay can be managed from either the client side or server side, each having advantage and disadvantage
The server side can be captured based on history of requests, but wont show the mouse movements and such as client-only activity
On client side, tags allow you to capture details of pages. Any data coming in from a client is subject to blocking and manipulation
##### Integer Overflow
Programming error when a program attempts to store a numeric value, in a value that is too small to hold it
It can also roll over to a negative value because the most significant bit is usually reserved for the sign of a number
Integer overflows are easily tested for and static code analyzers can point out where they are likely to occur
##### Request Forgery
A class of attack where a user performs a state-changing action on behalf of another user, typically without knowledge
These attack utilize the behavioral characteristics of web-based protocols and browsers, and they occur because of client-side issues but they can be seen on both server-side and client side
###### Server-Side Request Forgery
When an attacker sends requests to the server-side application to make HTTP requests to an arbitrary domain of the attacker's choosing
These attacks exploit the trust relationship between server and the target, forcing the vulnerable application to perform unauthorized action.
Common attacks include having the server attack itself or attack another server in the organization.
###### Cross-Site Request Forgery (XSRF)
Utilize unintended behaviors that are proper in defined use but are performed under circumstances outside the authorized use.
A class of problems where one entity performs an action on behalf of another.

It is performed against sites that have an authenticated user and exploits the site's trust in a previous authentication event.
Then by tricking a user's browser into sending an HTTP request to the target site, the trust is exploited.
If a user is logged in and has not closed their browser, then an action in another browser tab could send a hidden request resulting in an event that appears to be authorized but in fact was not done by the user.

Mitigation methods can be employed, from limiting authentication times, to cookie expiration, to managing elements of a web page. The strongest method is the use of a random XSRF token in form submissions.
##### Application Programming Interface (API) Attacks
An app typically interfaces with the service via an application programming interface (API)
API's are subject to attack and abuse
An application programming interface attack is one where an attacker specifically attacks the API and the service behind it by manipulating inputs.
APIs are used to feed data to an application, so some of the processing is done in the application
This means that the interface is more of a raw feed data with less work and checking sone on the server.
API interfaces that are not monitored can result in data breaches and data disclosures
##### Resource Exhaustion
Where the attack's aim is to deplete resources
Failure to complete handshakes, program running out of memory, having the necessary amount of bandwidth, processing.
Ten to result in a system crash
##### Memory Leak
Memory management encompasses the actions used to control and coordinate computer memory, assigning memory, and reclaiming when no longer used.
Errors in management can result in a memory leak, which can grow over time, consuming more and more resources.
New programming languages provide automatic memory management with garbage collection
##### Secure Sockets Layer (SSL) Stripping
Man in the middle attack against all SSL and early versions of TLS connections
Wireless hotspots are a prime location
Attack works by intercepting the initial request for HTTPS, redirecting it to an HTTP site, and then mediating in the middle

The reason this works is because the beginning of an SSL and TLS handshake is vulnerable to attack.
Main defense is only use TLS 1.2 or 1.3
##### Driver Manipulation
Attack on a system by changing drivers, thus changing behavior of the system
Driers may not be as protected as other parts of the core system
###### Shimming
Process of putting a layer of code between the driver and the OS
Shimming allows flexibility and portability by enabling changes between different versions of an OS without modifying the original driver code
Shimming also represents a mean by which malicious code can change a driver's behavior without changing the driver itself
###### Refactoring
Process of restucturing existing computer code without changing its external behavior
Refactoring is done to improve nonfunctional attributes of the software such as improving code readability and/or reducing complexity
Refactoring can incover design flaws that lead to vulnerabilities
Refactoring is a means by which an attacker can add functionality to a driver yet maintain its desired functionality

`Shimming is the process of putting a layer of code between the driver and the OS and Refactoring is the process of restructuring existing code without changing its external behavior`
##### Pass the Hash
Hacking technique where the attacker captures the hash used to authenticate a process
This is a highly technical attack that targets the Windows authentication process by injecting a copy of the password hash directly into the system

The attacker does not need to know the password, but instead use a captured hash and inject it directly
	This is very technical hack, tools have been developed to facilitate its operation

