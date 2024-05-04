##### Environment
Designed to provide isolation between the functions of development, test, staging, and production.
Primary purpose if separate environments is to prevent security incidents arising from untested code ending up in the production environment
Moving code between environments requires a special account that can access both, minimizing issues of cross-contamination.
###### Development
Development environment is sized, configured, and set up for developing applications and systems.
The development hardware does not have to be scalable and it probably does not have to be as responsive for given transactions.
After code is successfully developed, it is moved to test system.
###### Test
Closely mimics production environment
Purpose of test is to test a system fully prior to deploying it into production to esnsure it is bug free
###### Staging
The staging environment is an optional environment, but is commonly used when an organization has multiple production environments.
Primary purpose is to serve as a sandbox after testing, so the test system can test the next set while the current set is deployed across the enterprise.
###### Production
Where the system works with real data, doing what its intended to perform
Very few changes occur, those that do must first be approved and tested via the management process.
###### Quality Assurance
Focus in quality and security issues in maintaining the bug register and helping the correct people on the team get the correct information to building secure software.
##### Provisioning and Deprovisioning
*Provisioning* is the process of assigning permissions or authorities to objects.
Users can be provisioned into groups and computer processes or threads can be provisioned to higher levels of authority when executing.
*Deprovisioning* is the removal of permissions or authorities. 
In secure coding provisioning a thread to elevated permissions when needed and deprovisioned once done.
##### Integrity Measurement
Integrity in the security field is data that ho no unauthorized changes.
Important because little changes can cause huge issues and difficult to detect.
A hash algorithm creates a unique hash value for each unique item it operates on.
Hash values ensure code has not been changed.
##### Secure Coding Techniques
Secure Development Lifecycle (SDL) can assist in developing secure code.
###### Normalization
Normalization is an initial step in the input validation process.
It is the process of creating the simplest form of a string before processing.
Strings can be decoded using Unicode and other encoding methods
Process of normalization converts "a rose is a rose is a r%6fse" all of these to "rose"
###### Stored Procedures
Stored procedures are methods of interfacing with database engines
Stored procedures are precompiled scripted methods of data access that offer advantages
Such as speed, this can run efficiently in production environment but offer less flexibility
`A stored procedure is a group of one or more statements stored within a database`
###### Obfuscation/Camouflage
Making a system harder to understand is a good thing. Removing or hiding hints makes the work harder and offer another layer of protection.
Works well for data names and other exposed names on the outside, not within code
###### Code Reuse and Dead Code
During the design phase, decisions should be made as to the appropriate level of reuse.
Inclusion of previous code can reduce development efforts and risk. Dead code elimination are compiler options that can remove dead code.
###### Server-Side  vs. Client-Side Execution and Validation
Data can be checked for compliance with input/output requirements either on the server or on the client.
Advantages of verifying data elements on the client before sending to the server - efficiency.
Doing checks on the client saves a round trip and delays before the user is alerted to a problem.

The client is not a suitable place to perform any critical value checks or security checks.
	The client can change anything after the first check. The data can be altered while in transit or at an intermediary proxy.
	<mark style="background: #FF5582A6;">The verification checks should be performed on the server side</mark>, where the data is free from unauthorized alterations.
###### Memory Management
Memory management is the actions used to control and coordinate computer memory.
Errors in memory can result in a program that has a memory leak, and it can grow over time consuming more resources.
The routine to clean up memory that has been allocated and no longer needed is called garbage collection.
Newer programming languages provide automatic memory management.
###### Use of Third-Party Libraries and Software Development Kits (SDKs)
Software developers user packages sets of software programs and tools called SDKs to create apps
###### Data Exposure
*Data exposure* is the loss of control over data from a system during operations
Data must be protected during storage, communications, even during use.
Failure of confidentiality and integrity
###### Open Web Application Security Project (OWASP)
Foundation to improving web-based application software security
Best known for top 10 web app vulnerabilities.
###### Software Diversity
Having different components with different software elements.
Having many common elements exists possibilities for common vulnerabilities
###### Compilers
Takes computer programs written in one language and convert them to a set of codes that can run on a specific set of hardware.
Compilers can manage aspects, such as memory, code efficiency, and more
###### Binaries
Binary diversity is the creation of identically functioning binary images, but with different instructions.
	Different memory location, different pointer offsets, and different layouts in memory and still preserve functionality.
This type of defense makes it difficult for attacker to bypass controls and inject something.
###### Automation/Scripting
The use of these technology-backend methods has led to a development known as DevOps
DevOps is a combination of development and operations
Leads to many small incremental changes but less time between updates and less time to fix
##### Automates Courses of Action
DevOps relies on automation for much of its efficiencies
Security automation can do the same for security that automation has in DevOps
Automating routines and extensive processes allow fewer resources to cover more of the environment in a more efficient and effective manner.
###### Continuous Monitoring
Term used to describe the technologies and processes employed to enable rapid detection of compliance and security risks.
Can provide full time monitoring of processes and conditions, feeding alerts for review
###### Continuous Validation
Continuous validation is the testing to support the process of development that occurs in DevOps.
A code is changed the new code must be tested with the existing codebase to ensure functionality and stability.
###### Continuous Integration
Is the manner of continually updating and improving the production codebase.
Allows for testing and updating without a lot of overhead
Instead of large updates, a series of small integrations are run.
This reduces interaction errors
###### Continuous Delivery
Is the extension of integration where you can quickly release new changes to production in a sustainable way.
Relies on automated testing and automated release process that delivers updates when complete at any time
Automation but under operator control
###### Continuous Deployment
Is continuous delivery on autopilot
One step further in that release is <mark style="background: #FFB86CA6;">automatic</mark>
No human intervention and deployment send the code to production
##### Elasticity
How changes in its environment while remaining secure. Add or subtract resources without issue.
Legacy is not elastic
##### Scalability
Characteristic to process higher workloads on its current resources or on additional resources without interruption
Current is scale up
Additional resources is scale out
Scaling out to multiple machines brings issues of synchronization and coordination
##### Version Control
Tracking which version of a program is is being worked on, whether in dev, test, or production
Multiple versions brings focus into change management
You need a change management process that ensures all changes in production are authorized , tested, and rolled back if failed, and have proper documentation.

caab