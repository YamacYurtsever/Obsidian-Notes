- Document Object Model is a model that treats a [[HTML, CSS & JavaScript#HTML (Hypertext Markup Language)| HTML]] document like a tree structure

![[DOM.png | 500]]

### DOM Manipulation
- The process of interacting with the DOM of a web page using programming languages like JavaScript

#### Accessing Elements
```js
parentElement.getElementsByTagName('tag');

parentElement.getElementsByClassName('class');

parentElement.getElementById('id');

parentElement.querySelector('CSS Selector');

parentElement.querySelectorAll('CSS Selector');
```

#### Modifying Elements
```js
element.textContent = 'New text';

element.innerHTML = '<p>New HTML content</p>';

element.setAttribute('attributeName', 'newValue');

element.style.property = 'value';
```

#### Creating, Cloning, Removing Elements
```js
// Creating
newElement = document.createElement('tag');
parentElement.appendChild(newElement);

// Cloning
clonedElement = originalElement.cloneNode(true);
parentElement.appendChild(clonedElement);

// Removing
elementToRemove.parentElement.removeChild(elementToRemove);
```

#### Datasets
```html
<div id="user" data-user-id="123"></div>
```

```js
var userElement = document.getElementById('user'); 
var userId = userElement.dataset.userId;
```

#### Detecting Scroll
```js
// Current vertical scroll position
var currentScrollPosition = window.scrollY;

// Height of the visible portion of the window
var windowHeight = window.innerHeight;

// Total height of the page
var totalPageHeight = document.body.offsetHeight;

// Detecting when the user scrolls to the bottom of the page: 
var isAtBottom = currentScrollPosition + windowHeight >= totalPageHeight;
```

#### Controlling CSS Animations
```js
element.animationPlayState = "paused";

element.animationPlayState = "running";

element.addEventListener('animationend', () => {});
```

#### History API
- A way to manipulate the browser's history and navigate between different states of the web page without triggering a full page reload
```js
history.pushState({ page: 1 }, "Title", "/page-1");

window.onpopstate = () => {}; // Back or forward in browser event

window.location.href = "/new-url";
```



