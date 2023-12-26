## Synchronous Programming
- Tasks are executed one after the other in a sequential manner where each operation must complete before the program moves on to the next one
- This is the traditional and simpler way of handling tasks

## Asynchronous Programming
- Tasks can be executed concurrently, without waiting for each task to complete before moving on to the next one
- This is particularly useful when dealing with operations that may take some time to complete, such as reading data from a file, making [[HTTP Requests]], or handling user input

#### Callbacks
- Functions that are passed as arguments to other functions to be invoked after the completion of an asynchronous operation or at a specified time
```js
function performAsyncOperation(callback) {
  console.log('Start of the operation');
  
  // Simulating an asynchronous operation
  setTimeout(function() {
    const result = 'Operation completed successfully';
    callback(result);
  }, 2000);
}

function handleResult(result) {
  console.log('Handling the result:', result);
}

performAsyncOperation(handleResult);
```
- **Callback hell** refers to a situation where multiple nested callbacks make the code hard to read and maintain which often occurs when dealing with a series of asynchronous tasks
```js
getUser(function(user) {
  getProfile(user, function(profile) {
    getPosts(user, function(posts) {
      getComments(posts[0], function(comments) {
        displayUserDetails(user, profile, posts, comments);
      });
    });
  });
});
```

#### Promises
- Objects that represent the eventual completion or failure of an asynchronous operation and its resulting value
- **States of a Promise**:
	- **Pending**: 
		The initial state, the promise is neither fulfilled nor rejected
	- **Fulfilled**: 
		The asynchronous operation completed successfully, the promise has a resulting value
	- **Rejected**: 
		The asynchronous operation encountered an error, the promise has a reason for the failure
- E.g.: [[HTTP Requests#FetchAPIs | Fetch APIs]]

#### Timeouts
- A way to execute a [[Functions | function]] or code snippet once after a specified amount of time has passed

JavaScript
```js
var timeoutId = setTimeout(myFunction, 3000);

clearTimeout(timeoutId); 
// Executes the function inside the timeout before it finishes
```

C# (Unity Coroutines)
```csharp
IEnumerator timeoutCoroutine() {
	yield return new WaitForSeconds(2);
	// Do Things
}
```

#### Intervals
- A way to repeatedly execute a [[Functions | function]] or code snippet continuously at specified time intervals until stopped

JavaScript
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