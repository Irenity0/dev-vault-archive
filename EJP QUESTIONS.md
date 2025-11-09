## HTML
#### What is HTML?
HTML (Hyper Text Markup Language) is a markup language as the name suggests. It is used for structuring a web page 

#### What is the difference between html & html5?
HTML is the standard markup language for structuring web pages, while HTML5 is its latest version with enhanced features. HTML5 introduced semantic elements like `<header>`, `<section>`, and `<article>` for better readability and SEO, native support for audio and video without plugins, and improved form controls like `<input type='email'>` and `<input type='date'>`. It also supports modern web APIs and better performance, making it more suitable for responsive and interactive web applications.

#### What are Tags? Do all Tags have an ending tag?
Tags are primary components of HTML that defines how the content would be structured. And not all HTML tags have an end tag. For example the `<br>` & `<img>` tags

#### What is semantic HTML?
Semantic HTML, also known as semantic markup, refers to the use of HTML tags that convey the meaning or semantics of the content contained within them. By adding semantic HTML tags to your pages, you provide additional information that helps define the roles and relative importance of the different parts of your page.

#### What are Attributes?
HTML Attributes are special words used within the opening tag of an HTML element. They provide additional information about HTML elements. HTML attributes are used to configure and adjust the element’s behavior, appearance, or functionality in a variety of ways.
#### How many types of headings does HTML contain
There are 6 types of headings in HTML from h1 (heading1) to h6 (heading 6). The size of the font gets progressively smaller.

#### What is the difference between HTML tags and elements
HTML Tags are building blocks of HTML Page. HTML Elements are components that are used in HTML Page

#### Is a hyperlink only applicable to text
No, Hyperlinks can be made for both images and texts.

---------------
## CSS

#### **What is CSS?**

CSS (Cascading Style Sheets) is a stylesheet language used to style HTML elements, controlling layout, colors, fonts, and responsiveness.

#### **What is the difference between `relative` and `absolute` units in CSS?**

- **Relative units** (e.g., `%`, `em`, `rem`, `vh`, `vw`) scale based on another element.
- **Absolute units** (e.g., `px`, `cm`, `mm`) have fixed values and don’t scale.

#### **What is the difference between `inline`, `block`, and `inline-block`?**

- **Inline**: Does not start a new line, width/height can’t be set (`<span>`).
- **Block**: Starts on a new line, takes full width (`<div>`).
- **Inline-block**: Like inline but allows width/height changes.

#### **What are CSS variables, and how do you use them?**

CSS variables (`--var-name`) store reusable values. They are defined in `:root` and used with `var()`.

`:root { --primary-color: #3498db; } h1 { color: var(--primary-color); }`

#### **What is the difference between relative, absolute, fixed, and sticky positioning in CSS?**

- **Relative**: Positioned relative to its normal position.
- **Absolute**: Positioned relative to the nearest positioned ancestor.
- **Fixed**: Stays in place relative to the viewport.
- **Sticky**: Behaves like relative until scrolled past a threshold, then acts like fixed.

#### **What are pseudo-classes and pseudo-elements in CSS?**

- **Pseudo-classes** (`:hover`, `:nth-child()`) apply styles based on state.
- **Pseudo-elements** (`::before`, `::after`) style specific parts of elements.

#### **What do you understand by the universal selector?**

The universal selector (`*`) applies styles to all elements.

`* { margin: 0; padding: 0; }`

#### **What is Box Model?**

The Box Model consists of **content, padding, border, and margin**, which define an element's total space.

#### **Define `z-index`.**

`z-index` controls the stacking order of elements. A higher value places an element above lower values.

#### **How can you target `h3` and `h2` with the same styling?**

Use a comma-separated selector:

`h2, h3 { color: blue; font-size: 20px; }`

-------
## JavaScript
#### **What is JavaScript?**

JavaScript is a lightweight, interpreted programming language used for building interactive web pages. It runs in the browser and can also be used on the server with Node.js.

#### **Explain the different data types available in JavaScript.**

JavaScript has primitive types: **String, Number, Boolean, Null, Undefined, Symbol, and BigInt**, and one non-primitive type: **Object**, which includes Arrays, Functions, and more.

#### **What are the differences between `var`, `let`, and `const`?**

- `var`: Function-scoped, allows redeclaration, hoisted but undefined.
- `let`: Block-scoped, no redeclaration, hoisted but uninitialized.
- `const`: Block-scoped, cannot be reassigned, must be initialized.

#### **Can you explain hoisting in JavaScript?**

Hoisting moves function and variable declarations to the top of their scope. Variables declared with `var` are hoisted as `undefined`, while `let` and `const` are hoisted but not initialized.

#### **What is a closure, and how is it used?**

A closure is a function that remembers variables from its outer scope even after the outer function has finished execution.  
Example:

```js
function outer() {
  let count = 0;
  return function inner() {
    count++;
    console.log(count);
  };
}
const counter = outer();
counter(); // 1
counter(); // 2
```

#### **Describe the concept of prototypal inheritance.**

In JavaScript, objects can inherit properties and methods from other objects using prototypes instead of classes. This allows for shared functionality.

#### **What are the different ways to create objects in JavaScript?**

- Object literals: `{ key: value }`
- Constructor functions: `new FunctionName()`
- `Object.create(prototype)`
- ES6 Classes

#### **Explain the event loop and how it works in JavaScript.**

The event loop allows JavaScript to handle asynchronous operations. It processes tasks from the **call stack** and **task queue** so that JavaScript remains non-blocking.

#### **What is the difference between synchronous and asynchronous code?**

- **Synchronous:** Code executes line by line, blocking execution.
- **Asynchronous:** Code runs in the background (via callbacks, promises, or async/await) without blocking.

#### **How do promises work, and what are their states?**

A promise represents a future value and has three states:

- **Pending:** Initial state
- **Resolved (Fulfilled):** Successful completion
- **Rejected:** Failed execution

#### **What are `async/await`, and how do they relate to promises?**

`async/await` makes working with promises easier. It allows writing asynchronous code in a synchronous style.  
Example:

```js
async function fetchData() {
  let data = await fetch("url");
  return data.json();
}
```

#### **Can you explain the concept of a callback function?**

A callback is a function passed as an argument to another function and executed later.  
Example:

```js
function greet(name, callback) {
  console.log("Hello, " + name);
  callback();
}
greet("John", () => console.log("Welcome!"));
```

#### **What is the purpose of the `this` keyword, and how is its context determined?**

`this` refers to the object calling the function. Its value depends on **where and how** a function is called.

#### **How do the `bind()`, `call()`, and `apply()` methods work?**

- `bind()`: Returns a new function with `this` set to a specific object.
- `call()`: Calls a function immediately with `this` and arguments.
- `apply()`: Same as `call()`, but takes an array of arguments.

#### **What is event delegation, and why is it useful?**

Event delegation allows a parent element to handle events for its children using event bubbling. This improves performance for dynamic elements.

#### **Explain the difference between `==` and `===`.**

- `==`: Loose equality, converts types before comparing.
- `===`: Strict equality, compares both value and type.

#### **What are Immediately Invoked Function Expressions (IIFE)?**

An IIFE is a function that runs immediately after being defined.  
Example:

```js
(function() {
  console.log("Runs immediately!");
})();
```

#### **How does JavaScript handle scope, and what is the difference between global and local scope?**

Scope determines variable accessibility.

- **Global scope:** Variables accessible everywhere.
- **Local scope:** Variables accessible only within a function or block.

#### **What is the module pattern, and how is it implemented?**

The module pattern creates private and public variables using closures.  
Example:

```js
const module = (function () {
  let privateVar = "secret";
  return {
    getVar: () => privateVar,
  };
})();
console.log(module.getVar()); // "secret"
```

#### **Can you explain the concept of garbage collection in JavaScript?**

Garbage collection automatically removes unused variables and objects to free memory. The most common method is **mark-and-sweep**.

#### **What are higher-order functions, and can you provide an example?**

A higher-order function takes another function as an argument or returns one.  
Example:

```js
function operate(fn, a, b) {
  return fn(a, b);
}
console.log(operate((x, y) => x + y, 3, 5)); // 8
```

#### **How do you handle errors in JavaScript?**

Use `try...catch` blocks or `Promise.catch()` for handling errors.  
Example:

```js
try {
  throw new Error("Something went wrong!");
} catch (error) {
  console.log(error.message);
}
```

#### **What is the difference between `null` and `undefined`?**

- `null`: Explicitly set as empty.
- `undefined`: A variable declared but not assigned a value.

#### **Explain the concept of debouncing and throttling in JavaScript.**

- **Debouncing:** Delays execution until after a certain time has passed since the last function call.
- **Throttling:** Ensures a function runs at most once in a given period.

#### **What are template literals, and how do they differ from regular strings?**

Template literals use backticks (`` ` ``) and allow embedding variables using `${}`.  
Example:

```js
let name = "Alice";
console.log(`Hello, ${name}!`); // "Hello, Alice!"
```

#### **How can you manipulate the DOM using JavaScript?**

Use `document.querySelector()`, `document.getElementById()`, or `innerHTML`.  
Example:

```js
document.getElementById("demo").textContent = "Hello!";
```

#### **What is the difference between `map()`, `filter()`, and `reduce()` methods in arrays?**

- `map()`: Transforms each element and returns a new array.
- `filter()`: Returns a new array with elements that pass a condition.
- `reduce()`: Accumulates values into a single result.

#### **Can you explain the concept of immutability in JavaScript?**

Immutability means not modifying existing data but creating a new copy instead. Example:

```js
const arr = [1, 2, 3];
const newArr = [...arr, 4]; // Instead of modifying arr
```

#### **What are generators, and how do they differ from regular functions?**

Generators (`function*`) allow pausing and resuming execution using `yield`.  
Example:

```js
function* generator() {
  yield 1;
  yield 2;
}
const gen = generator();
console.log(gen.next().value); // 1
```

#### **How does JavaScript handle asynchronous operations, and what are the common patterns for managing them?**

JavaScript handles async tasks using **callbacks, promises, and async/await** to prevent blocking the main thread.

------------
## Reactjs

1. **What is React?**
    
    - React is a JavaScript library for building user interfaces with a component-based structure and Virtual DOM for optimized rendering.
2. **What are the major features of React?**
    
    - Features include the Virtual DOM, JSX, component-based structure, one-way data binding, and unidirectional data flow.
3. **What is JSX?**
    
    - JSX is a syntax extension that allows you to write HTML-like code in JavaScript, which React then transforms into JavaScript objects.
4. **What is the Virtual DOM?**
    
    - The Virtual DOM is a lightweight copy of the real DOM, used by React to improve rendering performance by updating only necessary parts.
5. **What are props in React?**
    
    - Props are read-only attributes passed from parent to child components, enabling data flow and customization.
6. **What is state in React?**
    
    - State is a mutable object inside a component that holds data affecting its rendering and behavior.
7. **What is the difference between state and props?**
    
    - Props are immutable and passed from parent to child, while state is mutable and managed within the component.
8. **What are controlled components?**
    
    - Controlled components are form elements whose values are controlled by React's state.
9. **What are uncontrolled components?**
    
    - Uncontrolled components manage their own internal state, with React accessing their values via refs.
10. **What is the purpose of the render() method in React?**
    

- The render() method returns JSX to be rendered in the DOM and is called in the component’s lifecycle.

1. **What are React Hooks?**

- React Hooks are functions that allow functional components to manage state and side effects, making code more concise.

2. **What is the useState hook?**

- `useState` is a hook that lets functional components have state, returning the state value and a function to update it.

3. **What is the useEffect hook?**

- `useEffect` performs side effects in functional components, like data fetching or manual DOM manipulation.

4. **What is the Context API in React?**

- The Context API allows components to share values (like themes) across the component tree without prop drilling.

5. **What is prop drilling?**

- Prop drilling is passing data through multiple layers of components, which can become cumbersome in deeply nested trees.

6. **What are error boundaries in React?**

- Error boundaries catch JavaScript errors in their child components, log the errors, and display a fallback UI.

7. **What is the purpose of keys in React lists?**

- Keys uniquely identify list elements to help React efficiently update and render items when changes occur.

8. **What is the difference between class components and functional components?**

- Class components manage state and have lifecycle methods, while functional components are simpler and use Hooks.

9. **What is the useRef hook?**

- `useRef` is a hook that allows direct access to DOM elements or persists values across renders without re-rendering.

10. **What is the purpose of the componentDidMount lifecycle method?**

- `componentDidMount` is called after the component is rendered and added to the DOM, typically used for data fetching.

11. **What is the purpose of the shouldComponentUpdate lifecycle method?**

- `shouldComponentUpdate` determines if a component should re-render, optimizing performance.

12. **What is the purpose of the componentWillUnmount lifecycle method?**

- `componentWillUnmount` is called before a component is removed from the DOM, useful for cleanup tasks.

13. **What is the purpose of the getDerivedStateFromProps lifecycle method?**

- `getDerivedStateFromProps` updates state before every render based on changes in props.

14. **What is the purpose of the getSnapshotBeforeUpdate lifecycle method?**

- `getSnapshotBeforeUpdate` captures information from the DOM before React applies changes from the virtual DOM.

15. **What is the purpose of the componentDidUpdate lifecycle method?**

- `componentDidUpdate` is called after a component updates, often used for post-update operations.

16. **What is the purpose of the componentDidCatch lifecycle method?**

- `componentDidCatch` catches errors thrown by child components and logs them, helping handle errors gracefully.

17. **What is the purpose of the static getDerivedStateFromError lifecycle method?**

- `getDerivedStateFromError` updates the state when an error is thrown, allowing a fallback UI to be displayed.

18. **What is the purpose of the static getSnapshotBeforeUpdate lifecycle method?**

- `getSnapshotBeforeUpdate` captures data from the DOM before the update, providing insight into the pre-update state.

20. **What is the purpose of the componentWillReceiveProps lifecycle method?**

- `componentWillReceiveProps` is called before receiving new props, useful for updating state based on prop changes. (This method is deprecated in newer React versions).

--------
## ExpressJS

#### **What is Express.js, and how does it relate to Node.js?**

Express.js is a lightweight web framework for Node.js that simplifies building APIs and web applications.

#### **What are the key features of Express.js?**

- Fast and minimalist framework
- Middleware support
- Routing system
- Template engine support
- Error handling

#### **How do you handle routing in Express.js?**

Use `app.get()`, `app.post()`, etc., to define routes.

```js
app.get('/home', (req, res) => res.send('Welcome!'));
```

#### **Explain the role of middleware in Express.js.**

Middleware functions process requests before sending a response. They handle authentication, logging, and error handling.

#### **How can you serve static files in Express.js?**

Use `express.static()` to serve files like images, CSS, and JavaScript.

```js
app.use(express.static('public'));
```

#### **What is the purpose of the `next()` function in Express.js middleware?**

`next()` passes control to the next middleware function in the stack.

#### **How do you handle errors in Express.js applications?**

Use an error-handling middleware with four parameters.

```js
app.use((err, req, res, next) => res.status(500).send(err.message));
```

#### **What is the difference between `app.use()` and `app.get()` in Express.js?**

- `app.use()`: Applies middleware to all requests.
- `app.get()`: Handles only GET requests for a specific route.

#### **How can you set up a basic server using Express.js?**

```js
const express = require('express');
const app = express();
app.get('/', (req, res) => res.send('Hello World!'));
app.listen(3000, () => console.log('Server running on port 3000'));
```

#### **How do you manage sessions in Express.js?**

Use `express-session` middleware.

```js
const session = require('express-session');
app.use(session({ secret: 'secret', resave: false, saveUninitialized: true }));
```

----
## MongoDB

#### **What is MongoDB, and why is it classified as a NoSQL database?**

MongoDB is a document-based NoSQL database that stores data in JSON-like format. It's classified as NoSQL because it doesn’t use tables or structured schemas like relational databases.

#### **What are the key features of MongoDB?**

MongoDB is schema-less, highly scalable, supports high-performance queries, automatic sharding, replication, and has a powerful aggregation framework.

#### **Explain the structure of a MongoDB document.**

A MongoDB document is a JSON-like object with key-value pairs. For example:

```json
{ "name": "John", "age": 30, "skills": ["JavaScript", "MongoDB"] }
```

#### **What is a collection in MongoDB?**

A collection is a group of MongoDB documents, similar to a table in relational databases but without a fixed schema.

#### **How does MongoDB handle indexing, and what types of indexes are available?**

MongoDB uses indexes to speed up queries. It supports single-field, compound, text, geospatial, hashed, and TTL indexes.

#### **What is sharding in MongoDB, and how does it work?**

Sharding is MongoDB's way of distributing large datasets across multiple servers. Data is split into chunks and stored in different shards for better scalability and performance.

#### **Define replication in MongoDB and explain its importance.**

Replication is the process of copying data across multiple servers. It improves availability, prevents data loss, and ensures automatic failover in case of server failure.

#### **What is the aggregation framework in MongoDB?**

The aggregation framework processes large amounts of data using a pipeline of operations like filtering, grouping, and sorting, similar to SQL’s `GROUP BY` and `JOIN` functions.

#### **Explain the concept of a replica set in MongoDB.**

A replica set is a group of MongoDB servers with one primary and multiple secondary nodes. The primary handles writes, while secondaries replicate data for backup and failover.

#### **What are the advantages of using MongoDB over traditional relational databases?**

MongoDB is schema-flexible, scales horizontally, handles unstructured data well, supports fast reads/writes, and has built-in replication and sharding for better performance.

-------

