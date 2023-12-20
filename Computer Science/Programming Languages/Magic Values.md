- A "magic value" is a string or number used in a program that is essential to its proper function but provides no context or explanation for why it is what it is

```javascript
function isWithinThreeDays(date1, date2) {
  const difference = Math.abs(date1 - date2)
  return difference <= 259200000
}
```
- In the code above 259200000 is a "magic value" which actually refers to three days in milliseconds, but it not labeled properly
```javascript
const DAY_IN_MS = 1000 * 60 * 60 * 24

function isWithinThreeDays(date1, date2) {
  const difference = Math.abs(date1 - date2)
  return difference <= DAY_IN_MS * 3
}
```
- In the code above there is no longer a "magic value"