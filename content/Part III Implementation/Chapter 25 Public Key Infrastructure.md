[Objective 3.9] Given a scenario, implement public key infrastructure
##### Public Key Infrastructure (PKI)
Composed of several components, working together to handle the distribution and management of keys in a public key cryptosystem
Keys are carried via a certificate
Certificate authorities and registration authorities exist to manage certificates
`A registration authority (RA) verifies certificate requests and forwards them to a certificate authority (CA). The CA is a trusted organization that validates and issues digital certificates`
###### Key Management
Is the set of activities that an organization must undertake to ensure that keys enable proper cryptography and do not cause security issues
##### Certificate Authority (CA)
Digital certificate establishes an association between the subjects identity and a public key
The private key that is paired with the public key in the certificate is stored separately
###### Intermediate CA
Function to transfer trust between different CAs
##### Registration Authority (RA)
The PKI component that accepts a request for a digital certificate and performs the necessary steps of registering and authenticating the person requesting the certificate
The authentication requirements differ depending on the type of certificate being requested
Each higher class carry our more powerful and critical tasks than the one below
###### Certificate Revocation List (CRL)
The CA provides protection against bad certificates by maintaining a certificate revocation list, a list of serial numbers of certificates that have been revoked
Lists why and when certificates were revoked
Expired are not the same as those revoked
The CA is responsible for maintaining the CRL and posting it in a publicly available directory
<mark style="background: #FFB86CA6;">The mechanism used to protect integrity of a CRL is a digital signature</mark>
##### Certificate Signing Request (CSR)
Is the actual request to a CA containing a public key and the requisite information needed tp generate a certificate
CSR contains all identifying information that is to be bound to the key by the certificate generation process
###### CN
Common Name field is represented in the Subject field  of the certificate and is the fully qualified domain name (FQDN) for which the certificate is valid
###### Pinning
When a certificate is presented for a host this information can be saved in an act called pinning, which is the process of associating a host with a previously provided X.509 certificate or public key

`The X.509 standard is used to define the properties of digital certificated`