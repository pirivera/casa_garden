[Objective 2.4] Summarize authentication and authorization design concepts
##### Authentication Methods
Process of verifying and identity established in a computer system
###### Directory Services
*Lightweight Directory Access Protocol (LDAP)* is commonly used to handle user authentication and authorization and to control access to Active Directory objects
AD can be integrated with cloud based systems
###### Federation
Federation or identity federation defines policies protocols and practices to manage identities across system and organizations.
Federation is enabled through the use of SAML
`Federated identity access management systems allow users to authenticate and access resources across multiple enterprises using a single credential. Not to be confused with SSO`
###### Attestation
Attestation is supplying proof or evidence of some fact
In authentication, this can be done by a service that checks the credentials supplied
##### Technologies
There ae multiple ways to perform authentication and multiple technologies can be employed to assist in the effort
###### Time-based One-Time Password (TOTP)
Implementation of an HOTP that uses a secret key with a current timestamp to generate a OTP
Considered more secure because they are valid a short time and change often
###### HMAC-based One-Time Password (HOTP)
Is an algorithm that can be used to authenticate a user in a system by using an authentication server
###### Short Message Service (SMS)
Message is sent provides a code that the user enters into the system
Typically has expiration time
###### Token Key
Physical devices that carry a digital token used to identify the user
Proximity cards used in physical access systems are token-carrying devices
The keys can be dynamic, changing over time or static.
If they are lost they are backstopped with a PIN code
###### Static Codes
Codes do not change
Has a weakness that if compromised the keys are no longer valid
Standard is to use cryptographic protection of all static codes, even if communication is copied
###### Authentication Applications
Exists on many platforms, common method user by user input being correct
###### Push Notifications
Receives an alert an attempt is taking place, and they can choose to approve or dent
Out of band communication and demonstrates a second comm channel thus making account hacking more challenging
###### Phone Call
Call made to a specific number where user can verify
###### Smart Card Authentication
They can carry large cryptographic tokens
Can be integrated into Windows user access system
##### Biometrics
Biometric factors are measurements of certain biological factors to identify one person from others. Based on body parts that are unique.
When these are used for authentication there is a two part process: enrollment and then authentication.
During enrollment a computer takes the image and translated the biometric feature into a numeric value called a template.
When user tries to authenticate the computer compares the numeric value to the one stored on the database. If they match access is allowed.
This is considered analog. The problem with analog is it might not encode the same way twice.
###### Fingerprint
A fingerprint scanner takes the unique pattern and translate into a numeric value, a template.
Readers can be enhances to ensure the pattern is a live pattern to prevent spoofing with a mold.
###### Retina
Examines the blood vessel patterns in the back of the eye. Retinal scanning is not accepted by users which raises issues morally of the use of lasers.
###### Iris
Scans the pigmentation associated with the iris of the eye
Possible to mimic
###### Facial
Sensor that recognizes the facial pattern and used for logging into phone and even payments
###### Voice
Hardest to develop , due to false acceptance and rejection rates
###### Vein
Palms, fingers, veins in the retina
Noninvasive but require close proximity
###### Gait Analysis
Measurement of the pattern express when they talk
###### Efficacy Rates
Biometric measurements have a level of uncertainty, thus solutions has been an issue since they were first developed.
As each generation of sensor improves the accuracy of the measurements, the errors have been reduced to a manageable level.
The terms False Acceptance and False Rejection Rate describe the chance that an incorrect user will be falsely accepted or a correct user falsely rejected.
FRR should be below 3% and FAR should be below 0.1%
###### False Acceptance
(FAR) determines what level of false positives is allowed in the system.
The more curves overlap the larger the problem because that number defines the FAR
###### False Rejection
(FRR) determines what level of false negatives, or rejections, are going to be allowed in the system.
###### Crossover Error Rate
(CER) is where both accept and reject error rates are equal.
This is the desired state for the most efficient operation, and it can be managed by manipulating the threshold value used for matching.
`CER is the perventage at which the FAR and FARR are equal`
##### Multifactor Authentication (MFA) Factors and Attributes
Is the combination of two or more types of authentication
Five categories: something you know, something you have, somewhere you are, who you are, and something you do
Makes it difficult for attackers to obtain all correct materials for authentication.
##### Factors
Specific elements that compromise an item of proof. Three classes: something you know (passwords), something you have (token), and something you are (biometrics)
###### Something You Know
Common example is a password. Challenge of something you know is that it can be shared without knowing.
Another form of authentication using something you know is identity driven authentication
Calling in and having to answer questions based on previously given answers
###### Something You Have
Refers to security tokens and other items that a user can have physically.
Challenge is you need to have it on you whenever you wish to be authenticated.
You can also have something lost and now you don't have access
###### Something You Are
Refers to biometrics
Challenge is that its hard to change, once assigned they become immutable
Some biometrics are not usable in certain environments
##### Attributes
Collection of artifacts associated with a user such as location, ability, or something about the user.
###### Somewhere You Are
Geofencing to access resources, device can identify what location you are in
###### Something You Can Do
Refers to a physical action that you perform uniquely
Harder artifacts to capture without specialized hardware making it less as a method of authentication
###### Something You Exhibit
Is a special case of biometric.
An example is a brainwave response to seeing a picture, results of a lie detector test.
Concept is to present a trigger and measure results
###### Someone You Know
Specific memory, in this case an individual. Electronically this can be done via a chain of trust model
##### Authentication, Authorization, and Accounting (AAA)
*Authentication* is the process of verifying an identity. Each with advantage and disadvantages.
*Authorization* is the process of permitting or denying access to a specific resource. Many types but reason is the same: determine whether a user has permissions for a particular object or resource being requested.
*Accounting* is the process of ascribing resource usage by account for the purpose of tracking resource utilization.
##### Cloud vs. On-premises Requirements
Proper determination of authentication process should rest on data critically and who needs access
When establishing on cloud or on premise you use identity and authentication as the foundation of security.
