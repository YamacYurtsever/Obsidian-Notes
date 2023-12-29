- A Virtual Private Network is a technology that provides a secure and encrypted connection over the internet, allowing users to access resources and share data as if they were directly connected to a private [[Network | network]]
- VPNs are commonly used for enhancing privacy, security, and anonymity when accessing the internet

### Types of VPNs (According to Users):
- **Site-to-Site VPN:** 
Connects entire [[Network | network]] in different locations, enabling secure communication over the internet. This is commonly used for linking branch offices in a corporate network.
- **Remote Access VPN:** 
Allows individual users to connect securely to a company's [[Network | network]] over the internet. This is often used for remote employees or workers on the go.

### Types of VPNs (According to the Provider):
- **Secure VPN:** 
All traffic on the VPN is encrypted, authenticated and is sent along virtual tunnel
- **Trusted VPN:** 
All traffic on the VPN relies on the security of the providers [[Network | network]] to protect the traffic
- **Hybrid VPN:** 
Combines elements of both secure and trusted VPNs

### What makes VPNs secure?
- **Authentication**: 
	- Authentication is the process of verifying the identity of users or devices attempting to connect to the VPN
	- It ensures that only authorized individuals or systems can access the [[Network | network]]
	- Knowing the identity of all clients helps maintain the security and integrity of the VPN
- **Encryption**: 
	- Encryption is the process of encrypting data to make it unreadable to unauthorized users.
	- In the context of VPNs, all data transmitted over the [[Network | network]] is typically encrypted, ensuring that even if it is intercepted, it remains unreadable without the appropriate decryption key.
	- This is a crucial aspect of VPN security to protect sensitive information
- **Tunneling**: 
	- Tunneling involves encapsulating data in a secure "tunnel" for transmission over an untrusted network, such as the internet
	- VPNs use tunneling protocols to create a secure path between the client and the server. The security properties of these tunnels are determined by the administrators configuring the VPN endpoints
	- Common tunneling protocols include PPTP, L2TP/IPsec, and OpenVPN
- **Multiple Exit Nodes**: 
	- Multiple exit nodes refer to having different points of exit from the VPN network
	- This can enhance privacy and make it more challenging for external entities to determine the origin of the data
	- It helps in hiding the source of the data and adds an additional layer of anonymity