- A JavaScript library for building user interfaces, particularly for single-page applications where user interactions are dynamic and frequent
- React allows developers to create reusable UI components and manage the state of an application efficiently
- It follows a declarative and component-based paradigm, making it easier to understand, maintain, and scale complex applications

#### Virtual DOM
- React uses a virtual [[DOM]] to improve performance by minimizing the number of direct manipulations to the actual DOM
- The virtual DOM is a lightweight copy of the actual DOM, and React calculates the most efficient way to update the actual DOM based on changes to the virtual DOM

#### Components
- Components are the building blocks of a React application
- They represent different parts of the user interface and can be composed to create complex UIs

#### State and Props
- **State:** Each component in React can have its own local state, allowing it to manage and respond to changes
- State is mutable and can be modified using the `setState` function.
- **Props (Properties):** Props are inputs to a React component, allowing data to be passed from parent components to child components

#### Hooks
- Functions that allow functional components to use state and lifecycle features that were previously available only in class components
Common Hooks: useState for managing state, useEffect for handling side effects, useContext for accessing context, and more

#### JSX (Javascript XML)
- A syntax extension for JavaScript that allows you to write HTML-like code in your JavaScript files, making it more readable and expressive
