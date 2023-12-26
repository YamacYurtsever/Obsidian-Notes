- A JavaScript library for building user interfaces, particularly for single-page applications where user interactions are dynamic and frequent
- React allows developers to create reusable UI components and manage the state of an application efficiently
- It follows a declarative and component-based paradigm, making it easier to understand, maintain, and scale complex applications

#### Virtual DOM
- React uses a virtual [[DOM]] to improve performance by minimizing the number of direct manipulations to the actual DOM
- The virtual DOM is a lightweight copy of the actual DOM, and React calculates the most efficient way to update the actual DOM based on changes to the virtual DOM

#### JSX (Javascript XML)
- A syntax extension for JavaScript that allows you to write HTML-like code in your JavaScript files, making it more readable and expressive

#### Components
- Components are the building blocks of a React application
- They represent different parts of the user interface and can be composed to create complex UIs
- 
##### Class Components:
```js
class MyClassComponent extends React.Component { 
	// Class component code goes here 
}
```

##### Functional Components:  
```js
function MyFunctionalComponent(props) { 
	// Functional component code goes here 
}
```

#### State
- Represents the local data that a React component can hold and manage
- It is mutable and can be modified using the `setState` method
- It is used when a component needs to keep track of data that may change over time
	  
```js
class Counter extends Component {
  constructor(props) {
    super(props);
    this.state = {
      count: 0,
    };
  }

  increment = () => {
    this.setState({ count: this.state.count + 1 });
  };

  render() {
    return (
      <div>
        <p>Count: {this.state.count}</p>
        <button onClick={this.increment}>Increment</button>
      </div>
    );
  }
}
```

#### Props
- Used to pass data from a parent component to a child component
- They are immutable and are passed down as attributes in the JSX
- They are used when you want to provide data or behavior from a parent component to a child component

```js
function Hello(props) {
  return (
	  <h1>Hello {props.name}!</h1>
  );
}

function App() {
	return (
		<div>
			<Hello name="Harry"/>
			<Hello name="Ron"/>
			<Hello name="Hermione"/>
		</div>
	);
}
```

#### Hooks
- Functions that allow functional components to use state and lifecycle features
- `useState` for managing state, `useEffect` for handling side effects

```js
function Counter() {
  const [count, setCount] = useState(0); // Initialized to 0

  const increment = () => {
    setCount(count + 1);
  };

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={increment}>Increment</button>
    </div>
  );
}
```

#### Re-Rendering
- Every time the state or props of a React component get changed, the component is re-rendered automatically
- Also the the re-render can be forced through `this.forceUpdate();`
