- Messages sent by a client to a server specifying an action to be performed, to which the server responds by [[HTTP Responses]]
- The most common ways of making [[Network Protocols#Hyper Text Transfer Protocol / Secure (HTTP / HTTPS) | HTTP]] Requests are **forms and fetch [[APIs]]**
- HTTP Methods indicate the desired action to be performed by the server
	- `GET`: Retrieves data from server to the client
	- `POST`: Sends data from the client to the server
	- `PUT`: Updates the data in the server
	- `DELETE`: Removes data from the server
	- ! GET method is typically visible in the browser's address bar, as it appends the data to the URL, while POST is not
- Example HTTP Request (Can be seen through browser > inspect > network):

![[HTTP Requests 2023-12-25 19.43.02.excalidraw | 400]]

### Forms
- HTML element that contains interactive elements, such as text fields, checkboxes, radio buttons, buttons, and more
- Users can input data into these elements, and when the form is submitted, the data is sent to a server for processing
```html
<form action="/submit" method="post">
    <label for="name">Name:</label>
    <input type="text" id="name" name="user_name" required>
    
    <input type="submit" value="Submit">
  </form>
```
- When the form is submitted, the data is sent to the server as key-value pairs, where the name attributes act as the keys
```python
user_name = request.form.get('user_name')
```


### FetchAPI
- JavaScript interface for making HTTP requests

1. Promise Based
```javascript
fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

2. Async/Await
```javascript
async function fetchData() {
  try {
    const response = await fetch('https://api.example.com/data');
    const data = await response.json(); // Decodes JSON
    console.log(data);
  } catch (error) {
    console.error('Error:', error);
  }
}
```

##### Promises
- A programming pattern that represent the eventual completion or failure of an asynchronous operation and its resulting value
- Fetch APIs use promises to wait for HTML responses
	- **`.then()`:** 
		Sets up a callback to be executed when the Promise is resolved
	- **`await`:** 
	Used inside an `async` function, it pauses the function's execution until the awaited Promise is resolved
- States of a Promise:
	- **Pending**: 
		The initial state, the promise is neither fulfilled nor rejected
	- **Fulfilled**: 
		The asynchronous operation completed successfully, the promise has a resulting value
	- **Rejected**: 
		The asynchronous operation encountered an error, the promise has a reason for the failure

##### AJAX (Asynchronous javascript and XML)
-  A set of web development techniques that allows web pages to be updated asynchronously by exchanging data with the server behind the scenes
- This means that instead of reloading the entire web page when a user performs an action, such as submitting a form, only the specific part of the page that needs to be updated is refreshed
- This can be achieved using Fetch APIs
- E.g.: Loading related items from the database when/after writing search queries