- Events are incidents that happen as a result of user actions or or other activities in the browser
- Event handling involves defining functions (event handlers) that are executed in response to these events
- When an event occurs, an event object is created which contains information about the event such as: the type of event, target element, and other properties

#### Types of Events
- **User Events** 
	- `click`, `keydown`, `keyup`, `mouseover`, `mouseout`, `change`
- **Browser Events** 
	- `load`, `resize`
- **Network Events**
	- `fetch`, `catch`
- **Form Events** 
	- `submit`

#### Types of Event Handling
- **Inline Event Handling**
```html
<button onclick="myFunction()">Click me</button>
```
- **addEventListener**
```js
var element = document.getElementById('myButton');
element.addEventListener('click', event => {
	console.log('Event type:', event.type);
	console.log('Target element:', event.target);
});
```
