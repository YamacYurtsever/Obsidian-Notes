#### Timeout
- A way to execute a [[Functions | function]] or code snippet once after a specified amount of time has passed

```js
var timeoutId = setTimeout(myFunction, 3000);

clearTimeout(timeoutId); 
// Executes the function inside the timeout before it finishes
```

```c#
IEnumerator timeoutCoroutine() {
	yield return new WaitForSeconds(2);
	// Do Things
}
```

#### Intervals
- A way to repeatedly execute a [[Functions | function]] or code snippet continuously at specified time intervals until stopped

```js
var intervalId = setInterval(myFunction, 1000); // Start

clearInterval(intervalId); // Stop
```

```c#
IEnumerator intervalCoroutine() {
	yield return new WaitForSeconds(2);
	// Do Things
	StartCoroutine(intervalCoroutine());
}
```