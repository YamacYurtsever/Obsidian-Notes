- Javascript object notation is a lightweight data interchange format that is easy for humans to read and write, and easy for machines to parse and generate
- JSON is widely used in **[[APIs]]** for data exchange between a server and a client
- It's also used for **configuration files** and data storage formats

### Implementation
```javascript
let person = {
  "name": "John Doe",
  "age": 30,
  "isStudent": false,
  "grades": [90, 85, 92],
  "address": {
    "street": "123 Main St",
    "city": "Anytown",
    "zip": "12345"
  }
}
```

### Encoding and Decoding JSON
- Encoding JSON objects is a necessary step to represent structured data in a text-based format that can be easily transmitted, stored, and understood by other systems
```javascript
const jsonString = JSON.stringify(data); # Encoding
const receivedData = JSON.parse(jsonString); # Decoding
```