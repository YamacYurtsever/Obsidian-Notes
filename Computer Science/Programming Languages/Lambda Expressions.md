- Lambda expressions are a concise way to represent anonymous [[Functions | functions]]
- Anonymous [[Functions | functions]] are small, unnamed functions which are usually short-lived and are often passed as [[Parameters | arguments]] to higher-order [[Functions | functions]]
- Lambda expressions can also be used for [[Function Mapping]]

```javascript
document.querySelectorAll('button').forEach(button => {

});

// SAME AS

document.querySelectorAll('button').forEach(function(button) {

});
```