Set of rules that computers adhere to in order transmit data over the internet

#### Internet Protocol (IP)
- Every device needs to have a unique address according to IP
- Each IP address contains 4 [[Data Representation#^b773f4 | decimal]] values, each represented by 1 [[Data Representation#^ff39e6 | byte]] (0 to 255), written in format (#. #. #. #)

#### Transmission Control Protocol (TCP)
- Breaks down large amounts of data into segments ([[Data Transmission#^206809 | packets]]) and then re-assembles them
- Identifies unique services (ports)
```
21 FTP    File Transfer)
25 SMTP   (e-mail)
80 HTTP   (Web-Browsing)
443 HTTPS (Secure Web Browsing)
```

#### Domain Name System (DNS)
- A decentralized naming system used to translate human-readable domain names into web browser readable [[#Internet Protocol (IP) | IP]] addresses and vice versa
- It plays a crucial role in making the internet more user-friendly by allowing us to use easily memorable domain names instead of numeric [[#Internet Protocol (IP) | IP]]  addresses

#### Hyper Text Transfer Protocol / Secure (HTTP / HTTPS)
- A set of protocols used to communicate between web servers and web browsers (clients)
- HTTPS is the secure version of HTTP, where the communication is [[Data Security#Ciphers | encrypted]] using protocols like TLS (Transport Layer Security) or its predecessor SSL (Secure Sockets Layer).

![[HTTP.excalidraw | 450]]


