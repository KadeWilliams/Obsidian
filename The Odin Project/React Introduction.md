# Components
Applications made with React are made with (reusable) components. Components are your "building blocks". To gain confidence using React, you should learn to divide your application or project into these separate components. 
- `App` -> which represents the main application and will be the parent of all other components. 
- `Navbar` -> navigation bar
- `MainArticle`  -> the component that renders your main content
- `NewsletterForm`  -> simple form that lets a user input their email to receive the weekly newsletter

In React, each component is defined in an ES6 module. ES6 introduced the `import` statement which allows you to import code from one module into another module. This allows us to write each component in a separate file and import all components into the parent component:
`import ExampleComponent from "./components/ExampleComponent"`

In the beginning, it might be a little bit difficult to figure out the best component structure, especially when state and props come into play. React components, in general, usually have parent and/or child components. This system of structuring your applications helps you keep your code organizedand makes it easy to keep track of your components' relationships with eachother 

```JS
import React, { Component } from 'react'

class App extends Component {
	constructor() {
		super()
	}
	render() {
		return (
			<div className="App">
				Hello World!
			<div>
		)
	}
}

export default App

```

Default exports are imported without curly brackets; everything else must be wrapped in curly brackets. 

We are declaring the class component, `App`. We do this by extending the React class Component, which we imported at the top of the file. In doing this, we are essentially "Reactifiying" our App component by giving it all of the fun methods and properties every React component should have. One thing to notice is that React components, like all classes and factory functions, should always be declared with a capital letter at the beggining (PascalCase). This is a naming convention used by most developers and recommended by the React core team. 

Next is the constructor. A constructor is not obligatory in a class component, but you will most likely encounter one because it becomes important when concepts like inheritance and state are involved. You will usually see developers passing `props` as an argument to the constructor and also the `super()` call, which must be called in any React constructor. 

The most unfamiliar code is likely the `render()` function, which returns something that looks like HTML, but is actually **JSX**. JSX is an HTML-like syntax that is "transpiled" (converted) into JavaScript so a browser is able to process it. One of the primary characteristics and features of React is the ability to combine JavaScript and JSX. One thing you should know about JSX is that you can't use some JavaScript protected words as HTML attributes anymore, such as `class`, `onchange`, or `for`. Instead of `class` you will need to use `className`, instead of `onchange` you write `onChange`, instead of `for`, you must use `htmlFor`.

The `render()` function you see is the most used React "lifestyle" function. The only thing you should know for now is that every React class component needs a render function, which returns *one* top-level JSX element. When you want to return elements nested within one another, they need to be wrapped in a single parent element. 

```js
render() {
	return (
		<div>
			<h1>Hello World!</h1>
			<h2>Welcome to my React page!</h2>
		</div>
	)
}
```

Finally, to able to reuse this `App` component we have to export the component. 

```js
export { ComponentA, ComponentB, ComponentC }
```

When you want to import them, they will each need to be wrapped in curly braces. If you export a component as a default, you can import it without the curly braces. If you export multiple components, you have to import them inside of curly brackets. 

Using class components is one of two ways of defining components in React. The other, more modern, approach is to define the component as a function (like a factory function).

A basic functional component looks something like this:

```js
import React from 'react';

function App() {
	return <div className="App">Hello World!</div>
}

/* or */

const App = () => {
	return <div className="App">Hello World!</div>
}

/* or */

const App = () => <div className="App">Hello World!</div>

export default App;
```

As you can see, there are a few differences between functional and class components. With functional components:

1. We don't have to import and extend "Component" from React
2. We don't need a constructor
3. We don't need the render function, instead we put the return statement right at the end of the function body. 

A component is a reusable chunk of code. Components make it possible to dvide any UI into independent, reusable pieces and think about these pieces in isolation. Just like a pure function (?), a component should ideally do just one thing. 

In React, components conventionally start with a capital letter to differentiate them from normal HTML elements. 

`render()` is an important part of each component class. It should be present in every component class. It must also contain a return statement. Basically `render()` is a function that defines what should be returned in a component. This could be a react element, a string or number or even a component. 

The `render()` function should be pure. This means that it does not modify component state, it returns the same result each time it's invoked, and it does not directly interact with the browser. 

# Create-react-app
Developers at Facebook came up with a great tool called `create-react-app`, which sets up a complete React application for you. By running one command, it does all the necessary setup and configuration for you to immediately start working on your project.

