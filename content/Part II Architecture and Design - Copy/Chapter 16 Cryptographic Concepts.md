##### General Cryptographic Concepts
When plaintext needs to be protected it is encrypted into ciphertext
##### Fundamental Methods
Encryption operations are characterized by the quantity and type of protection sought
Integrity is characterized by the level of assurance desired
Data is characterized By its usage: data in transit, data at rest, or data in use
##### Digital Signatures
Designed to demonstrate authenticity
Using public key cryptography, a digital signature allows traceability to the person signing through the use of their private key
Upon receipt the recipient can decrypt the hash using the senders public key
`Digital signature guarantees the contents have not been altered while in transit`
##### Key Length
A longer length key is more secure, but will take longer to compute
###### Key Stretching
Takes what would be weak keys and stretches them to make the system more secure against brute force attacks
To make matching the hash more difficult, one must increase the key space or slow down the computation.
Key stretching involves increasing the computation complexity by adding iterative rounds of computation.
###### Salting
Entropy is a term in cryptography; it refers to the level of randomness
To provide sufficient entropy for low-entropy inputs to hash functions, a high-entropy piece of data can be concatenated with the material being hashed.
##### Hashing
Commonly used encryption methods.
Hashing function is a special mathematical function that performs one-way encryption
Also there is no way to generate two different plaintexts that compute the same hash value
You could hash a message to get a *message authentication code (MAC)* and then computation number would of the message would show that no intermediary modified the message.
HMAC *Hash-based Message Authentication Code*, is a special subset of hashing technology . It is a hashing algorithm applied to a message to make a MAC, but it is done with a previously shared secret.
##### Key Exchange
Foundational element of secure symmetric encryption system
Maintaining the secrecy of the symmetric key is the basis of secret communication
##### Elliptic Curve Cryptography
ECC requires less computing power for a given bit strength. This makes ECC ideal for use in low-power mobile devices.
`There is ECDHE and ECDSA that can be found in the books glossary`
##### Perfect Forward Secrecy (PFS)
PFS is a property of a public key system in which a key derived from another key is not compromised, even if the originating key is compromised in the future
If perfect forward secrecy was not in place, then past messages that been been recorded could be decrypted.
##### Quantum Cryptography
Is the use of quantum computing hardware to perform encryption and decryption processes.
Quantum key distribution (QKD) does not encrypt communication but rather provides a mean for users to securely distribute keys that are used for encrypting the communication channel.
Quantum computing is still in early stages but will revolutionize cryptography
Quantum uses qubits
##### Ephemeral Keys
Cryptographic keys that are used only once after generation
##### Modes of Operation
The basic premise is to use some source of entropy before encrypting subsequent blocks so that identical blocks of plaintext produce different blocks of ciphertext
Can be broken into three groups: authenticated, unauthenticated, and counter
###### Authenticated
Authenticated encryption with associated data (AEAD) is a form of encryption designed to provide both confidentiality and authenticity services.
Authenticated modes available including GCM, OCB, and EAX
	OCM is *Offset Codebook Mode*, a patented implementation that offers the highest performance but not included in international standards
	EAX solves the patent problem, but likewise has not been adopted by international standards
###### Counter
Counter mode (CTM) uses a "counter" function to generate a nonce that is used for each block encryption
GCM adds an authentication function to the cipher mode and that Galois field used in the process can be parallelized providing efficient operations.
GCM is employed in international standards
###### Unauthenticated
Unauthenticated modes use a non-identity based source for the entropy element for subsequent blocks
CBC is one of the most common modes used, but has two major weaknesses. First there is dependence on previous blocks, the algorithm cannot be parallelized for speed and efficiency. Second, because of the nature of the chaining, a plaintext can be recovered from two adjacent blocks of ciphertext.
##### Blockchain
Blockchains are a list of records where each addition in the list is done by a cryptographic algorithm
Records in a blockchain are resistant to modification
This has both verification and integrity
While it can be altered it would require all records after it to be also be altered
Blockchain was invented to create a public transaction ledger of cryptocurrencies
##### Cipher Suites
Cipher suite refers to a set of algorithms used together in cryptography with the most famous being the TLS cipher suite
The cipher suite will lost the key exchange mechanism, the authentication protocol, the block/stream cipher, and message authentication.
###### Block
Block ciphers operate on input data in a series of blocks
In the TLS cipher suite several block ciphers are available
With TLS 1.3 this list is trimmed to only ciphers that can support AEAD operations
This removes CBC versions of AES
###### Stream
Stream ciphers operate on streams of data instead of blocks
Stream operations typically take place on a single byte at a time. The challenge is to produce a long pseudorandom string of bytes that can be used to both encrypt and decrypt the stream.
`A block cipher encrypts plaintext one block at a time`
`A stream encrypts one byte at a time`
##### Symmetric vs. Asymmetric
Symmetric encryption tends to be faster, is less computationally involved and is better for bulk transfers. But suffers from a key management problem in that keys must be protected from unauthorized parties.
Asymmetric methods resolve the key secrecy issue with public keys, but they add significant computation complexity which makes them less suited for bulk encryption.

Bulk encryption can be done using both systems, using asymmetric encryption to pass a symmetric key.
##### Lightweight Cryptography
Lightweight cryptography is a specialized suite of cryptographic algorithm designed to operate in this resource-constrained environment.
These devices are small, cheap, and are hundreds or millions
##### Steganography
Hidden data inside data.
Example includes hiding data in an image.
The data is also encrypted so if found it is secured
Least significant bit , LIB, encoding is a method of encoding into an image while altering the actual visual image as little as possible.
##### Homomorphic Encryption
Data that is encrypted while stored or being moved is protected from observation or alteration by unauthorized parties.
This also forces authorized parties to perform decryption steps before performing computations, which represents a significant penalty use.
*Homomorphic encryption* is a set of algorithms that allow operations to be conducted on encrypted data, without decrypting and encrypting.
Most operations associated with homomorphic encrypted data involve work on numbers
<mark style="background: #FFF3A3A6;">Makes homomorphic methods valuable for many transactional based systems.</mark>
##### Common Use Cases
###### Low-Power Devices
Such as mobile phones or portable electronics are commonplace and these devices have needs for cryptographic purposes.
<mark style="background: #BBFABBA6;">Elliptical  curve cryptography  are well suited for low power applications</mark>
###### Low-Latency Operations
Specialized cryptographic functions needed to support operations that have extreme time constraints
<mark style="background: #BBFABBA6;">Stream ciphers are example of low-latency applications</mark>
###### High-Resiliency Systems
Characterized by functions that have the ability to resume normal operational conditions after an extreme disruption
Cryptographic modules can support resiliency through a standardized implementation of cryptographic flexibility
###### Support for Confidentiality
Primary means for protecting data confidentiality at rest and in transit
###### Support for Obfuscation
Protected from causal observation
Obfuscation can protect the code from observation by unauthorized parties
###### Supporting Authentication
Cryptographic functions can be employed to demonstrate authentication such as the validation that an entity has a specific private key associated with a presented public key, this proving identity.
###### Support for Nonrepudiation
Nonrepudiation is a property that deals with the ability to verify that a message has been sent and received so that the sender (or receiver) cannot refute sending (or receiving) the information.
`Nonrepudiation is the ability to verify that a message has been sent or received so that the sender (or receiver) cannot refute sending (or receiving) the information.`
##### Limitations
###### Speed
More complex the algorithm, the more rounds that are performed and the stronger the encryption, but the slower the throughput.
Computational efficiency is an important benchmark in modern cryptography and has led to algorithms such as ChaCha20 as it has advantage over AES
###### Size
Bigger the key the more data, that can be throughput and the stronger encryption
Size comes with a trade-off: speed.
###### Weak Keys
Strength is a function of the algorithm strength and the strength of the key
A perfect algorithm would have no weak key values, but not all algorithms share this trait.
Currently DES,RC4, IDEA, Blowfish, and GMAC algorithms can suffer from weak keys
###### Time
Given enough time, encryption can be broken
This is referred to as brute force attack
The objective is to protect data for a long enough period that brute force in not a factor
###### Predictability
Remove the element of predictability
Use of cryptographic random numbers
###### Reuse
Reusing keys is a sure way to result in failure
In block encryption, introducing a variable element of data between identical blocks prevents simple cryptanalysis.
The use of ephemeral keys is another example of preventing reuse of a cryptographic element as ephemeral keys are used only once.
###### Entropy
Level or amount of randomness is referred to as entropy
Entropy is the measure of uncertainty associated with a series of values.
A measure of entropy is in bits, where the bits are the power of 3, which represents the number of choices.
###### Computational Overhead
Limitation is the level of computational overhead needed to generate the system
One of many factors that must be considered when developing a soltuion
###### Weak/Deprecated Algorithms
New forms of functions are available, such as AES and ChaCha20
Sha-1 and Sha-256 have issues because they are suspect to forced collisions.
Data Encryption Standard (DES) and 3DES have fallen from favor.
##### PGP
Pretty Good Privacy is an encryption program that provides cryptographic privacy and authentication for data communication.
Relies on asymmetric algorithm