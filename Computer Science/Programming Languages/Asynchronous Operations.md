### Callbacks
- A function that is passed as an argument to another function and is intended to be executed after the completion of some asynchronous operation or at a specified time

### Promises
- A programming pattern that represent the eventual completion or failure of an asynchronous operation and its resulting value
- **States of a Promise**:
	- **Pending**: 
		The initial state, the promise is neither fulfilled nor rejected
	- **Fulfilled**: 
		The asynchronous operation completed successfully, the promise has a resulting value
	- **Rejected**: 
		The asynchronous operation encountered an error, the promise has a reason for the failure
- E.g.: [[HTTP Requests#FetchAPIs | Fetch APIs]]

### Timeouts
- A way to execute a [[Functions | function]] or code snippet once after a specified amount of time has passed

javascript
```js
var timeoutId = setTimeout(myFunction, 3000);

clearTimeout(timeoutId); 
// Executes the function inside the timeout before it finishes
```

python
```python
import time  

time.sleep(3)
```

C# (Unity Coroutines)
```csharp
IEnumerator timeoutCoroutine() {
	yield return new WaitForSeconds(2);
	// Do Things
}
```

### Intervals
- A way to repeatedly execute a [[Functions | function]] or code snippet continuously at specified time intervals until stopped

javascript
```js
var intervalId = setInterval(myFunction, 1000); // Start

clearInterval(intervalId); // Stop
```

C# (Unity Coroutines)
```csharp
IEnumerator intervalCoroutine() {
	yield return new WaitForSeconds(2);
	// Do Things
	StartCoroutine(intervalCoroutine());
}
```