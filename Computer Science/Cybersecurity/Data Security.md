#### Hashing
- Inputting a given series of characters into a [[Hash Tables#Hash Function | hash function]] which transforms it into a fixed-size string of characters called the hash value

![[Data Security 2023-12-29 01.52.22.excalidraw | 500]]

#### Salting
- Adding a unique and random value to each input before hashing them 
- This ensures that even if two users have the same password, their hashed passwords will be different due to the unique salt
- The salt is stored with the hash value
- When a user attempts to log in, the system retrieves the stored salt for that user, combines it with the entered password, hashes the result, and compares it to the stored hash to check if the password is correct

