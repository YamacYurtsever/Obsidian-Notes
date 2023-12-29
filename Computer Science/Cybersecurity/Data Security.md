#### Hashing
- Inputting a given series of characters into a [[Hash Tables#Hash Function | hash function]] which transforms it into a fixed-size string of characters called the hash value

![[Data Security 2023-12-29 01.52.22.excalidraw | 500]]

#### Salting
- Adding a unique and random value to each input before hashing them 
- This ensures that even if two users have the same password, their hashed passwords will be different due to the unique salt
- This also protects agains [[Data Threats#Rainbow Tables | rainbow tables]] as the salt values are random
- The salt is stored with the hash value in the database
- When a user attempts to log in, the system retrieves the stored salt for that user, combines it with the entered password, hashes the result, and compares it to the stored hash value to check if the password is correct

#### Codes
- A system of symbols, letters, or numbers used to represent information
- Codes don't necessarily provide security
- **Encoding**:
	- Converting information from one form to another, often for the purpose of efficient transmission or storage
- **Decoding**:
	- Converting encoded information back into its original form
- E.g.: [[Data Representation#^06f8fb | ASCII]], [[Data Representation#^55e4eb | Unicode]], [[JSON#Encoding and Decoding JSON | JSON Encoding]]

#### Ciphers
- A set of rules (encryption/decryption algorithm) to transform plaintext into ciphertext or vice versa
- The purpose of ciphers is to secure information during transmission or storage
- **Keys**:
	- A piece of information used in conjunction with an algorithm to perform encryption, decryption, or authentication
	- Keys are essential for securing information and ensuring that only authorized individuals can access or manipulate the data
- **Encryption**:
	- Converting plaintext into ciphertext using a cipher and a secret key
	- The resulting ciphertext should be unintelligible to anyone who does not possess the key to decrypt it
- **Decryption**:
	- Converting ciphertext back into plaintext using the appropriate cipher and the secret key
	- Only individuals or systems with the correct decryption key should be able to decipher the message

![[Pasted image 20231229125151.png | 450]]

#### Secret (Symmetric) Key Cryptography
- The same key is used for both encryption and decryption
- This key must be kept secret between the communicating parties

#### Public (Asymmetric) Key Cryptography
- A pair of keys is used: a public key which is shared openly and a private key which is kept secret
- The public key is used for encryption, and the private key is used for decryption
- E.g.: RSA, Diffy-Hellman

#### Rotational (Caesar) Cipher
- Rotating each character (on the alphabet) as much as the key value
![[Data Security 2023-12-29 13.04.01.excalidraw]]
