- Messages that servers send back to clients as a result of receiving [[HTTP Requests]]
- The [[Network Protocols#Hyper Text Transfer Protocol / Secure (HTTP / HTTPS) | HTTP]] response typically contains information about the status of the request and the requested data

### Status Codes
- A three-digit numeric code that indicates the outcome of the server's attempt to process the request
	- **1xx (Informational)**: The request was received, continuing process
	- **2xx (Successful)**: The request was successfully received, understood, and accepted
	- **3xx (Redirection)**: Further action needs to be taken in order to complete the request
	- **4xx (Client Error)**: The request contains bad syntax or cannot be fulfilled
	- **5xx (Server Error)**: The server failed to fulfill a valid request
- E.g.: 404 Not Found Error

