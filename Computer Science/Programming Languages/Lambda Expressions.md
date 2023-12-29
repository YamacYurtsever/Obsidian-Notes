- A concise way to define small, unnamed functions in programming languages that support [[Functional Programming]] paradigms
- Lambda expressions are commonly used in anonymous functions and functional mapping

### Anonymous Functions
- Small, unnamed [[Functions | functions]] which are usually short-lived and are often passed as [[Parameters | arguments]] to higher-order [[Functions | functions]]

```javascript
document.querySelectorAll('button').forEach(button => {

});

// SAME AS

document.querySelectorAll('button').forEach(function(button) {

});
```

### Functional Mapping

- The process of applying a [[Functions | function]] to each element of a collection, producing a new collection of results

Python:
```python
numbers = [1, 2, 3, 4, 5]
squared = map(lambda x: x**2, numbers)
# squared will be [1, 4, 9, 16, 25]
```

JavaScript
```javascript
let numbers = [1, 2, 3, 4, 5];
let squared = numbers.map(x => x**2);
// squared will be [1, 4, 9, 16, 25]
```