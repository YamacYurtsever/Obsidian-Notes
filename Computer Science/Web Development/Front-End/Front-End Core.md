### HTML (Hypertext Markup Language)
- Structure of a website

![[Front-End Technologies 2023-12-24 22.09.51.excalidraw | 300]]

### CSS (Cascading Style Sheets)
 - Aesthetics of a website

##### CSS Selectors
- Type Selector
	- `tag {}`
	- Universal Selector: `* {}`
- Class Selector
	- `.class {}`
- ID Selector
	- `#id {}`
- Attribute Selector
	- `selector[attribute = "value"] {}`
- Pseudo Classes
	- `selector::pseudo-class {}`

##### CSS Specificity
Inline CSS > External CSS

1. ID Selectors
2. Class Selectors & Attribute Selectors & Pseudo-Classes
3. Type Selectors 

If the specificities are the same, the one that appears later in the stylesheet takes precedence due to the "cascade"

##### CSS Combinators
- Descendant Selector: `(space)`
- Child Selector: `>`
- Adjacent Sibling Selector: `+`
- General Sibling Selector: `~`

##### Box Model
![[Pasted image 20231225134340.png | 300]]
- `box-sizing: border-box` includes the padding and border in an element's total width and height

##### Responsive Design
- Viewport
	- `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
- Media Queries
	- `@media only screen and (max-width: 600px)`
- Layout
	- Floats
	- Flexbox
	- CSS Grid
- CSS Units
	- px
	- em
	- rem
	- vh, vw

##### Animations
```css
@keyframes animation-name {
	from {}
	to {}
	/* OR */
	0% {}
	50% {}
	100% {}
}

element {
	animation-name: xxx;
	animation-duration: xxx;
	...
}
```

### Javascript
- Interactivity of a website
- It is used for [[DOM]] manipulation