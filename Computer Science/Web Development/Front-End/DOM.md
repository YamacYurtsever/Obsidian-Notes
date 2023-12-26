- Document Object Model is a model that treats a [[HTML, CSS & JavaScript#HTML (Hypertext Markup Language)| HTML]] document like a tree structure

![[DOM.png | 500]]

### DOM Manipulation
- The process of interacting with the DOM of a web page using programming languages like JavaScript

##### Accessing Elements
```js
parentElement.getElementsByTagName('tag');
parentElement.getElementsByClassName('class');
parentElement.getElementById('id');
parentElement.querySelector('CSS Selector');
parentElement.querySelectorAll('CSS Selector');
```

##### Modifying Elements
```js
element.textContent = 'New text';
element.innerHTML = '<p>New HTML content</p>';
element.setAttribute('attributeName', 'newValue');
element.style.property = 'value';
```

##### Creating, Removing, Copying Elements
```js
newElement = document.createElement('tag');
parentElement.appendChild(newElement);

clonedElement = originalElement.cloneNode(true);
parentElement.appendChild(clonedElement);

elementToRemove.parentElement.removeChild(elementToRemove);
```

##### Datasets
```html
<div id="user" data-user-id="123"></div>
```

```javascript
var userElement = document.getElementById('user'); 

var userId = userElement.dataset.userId;
var username = userElement.dataset.username;
var age = userElement.dataset.age;

userElement.dataset.age = '26';
userElement.dataset.email = 'john@example.com';
delete userElement.dataset.age;
```


