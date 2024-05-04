[Objective 3.4] Given a scenario, install and configure wireless security settings
##### Cryptographic Protocols
Standards used to describe cryptographic methods and implementations to ensure interoperability between different vendors equipment
##### WPA2
Uses 802.1X to provide authentication and uses advanced encryption standard (AES) as the encryption protocol
WPA2 uses the AES block cipher
WPA2 specifies the use of the Counter Mode with CBC-MAC Protocol
WPA2-Personal passphrase can be cracked using brute force attacks
WPA2 comes in Personal and Enterprise
Personal is also called PSK
Enterprise uses 8021.X
##### WPA3
WPA3 uses Simultaneous Authentication of Equals (SAE)
This allows WPA3-Personal networks to employ simple passphrases that are more harder to break than WPA/WPA2
WPA3 integrates with enterprise authentication such as RADIUS 
QR codes can be used to connect
`WPA2 uses PSK, WPA3 does not. If SAE is used it is for WPA3 level authentication.Forward secrecy is only provided by WPA3`
##### Counter Mode/CBC-MAC Protocol (CCMP)
Is a data encapsulation encryption designed for wireless use
CCMP is the mode which the AES cipher is used to provide message integrity
##### Simultaneous Authentication of Equals (SAE)
Is a password based key exchange method developed for mesh networks
It is resistant to active, passive, and dictionary attacks
##### Authentication Protocols
###### EAP
EAP can support multiple authentication mechanisms, including tokens, smart cards, certificates, one time passwords and public key encryption authentication
###### PEAP
Protected EAP, provides protection via a TLS tunnel
###### EAP-FAST
Offers a lightweight tunneling protocol to enable authentication
Client credentials verified through TLS tunnel
###### EAP-TLS
Considered one of the most secure implementations
EAP-TLS relies on TLS using SSL structure to pass credentials
`EAP-TLS for mutual authentication requires client and server certificates. PEAP and EAS-TTLS eliminate the requirment to deploy or use client certificates. EAP-FAST does not require certificates`
###### EAP-TTLS
Same as EAP-TLS with server authenticatin to the client with a certificate, but the protocol tunnels the client side of the authentication, allowing the use of legacy authentication protocols
EAP-TTLS the authentication process is protected by the tunnel from man in the middle attacks, and although client side certificates can  be used they are not required
`WPA3 is designed to work together with a cariety of EAP methods in an enterprise.`
##### Site Surveys
Involves several steps: mapping the floor plan, testing for RF interferences, RF coverage.
Watching signal strength and signal to noise ratio.
##### Heat Maps
A map of wireless signal coverage and strength
Shows a layout of a room, floor, with a graphical representation of a wireless signal
##### Wi-Fi Analyzers
Determine signal strength and interference
RF device that measures signal strength and quality
