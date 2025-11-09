#### What is ReactJS?
ReactJS is a popular JavaScript library for building user interfaces, especially for single-page applications. It allows developers to create reusable UI components, which makes the code more modular and easier to maintain. React uses a virtual DOM to improve performance, ensuring that only parts of the UI that have changed are re-rendered. It's widely used for creating dynamic, interactive web applications and is maintained by Facebook.

#### Key Features of React
Here are some key features of React:
1. *Component-Based Architecture*
2. *Virtual DOM*
3. *Unidirectional Data Flow*
4. *JSX (JavaScript XML*
5. *React Hooks*
6. *Declarative UI*
7. *Performance Optimization*
8. *Ecosystem and Libraries*

#### What is Unidirectional Data Flow?
*Unidirectional Data Flow* in React refers to the concept that data flows in one direction, from parent components to child components. This means that:
1. *Parent to Child*: Data is passed down from a parent component to its child components through **props**.
2. *State Management*: The component owning the state can modify it, but the state is not directly changed by its children. Any update to the state will trigger a re-render of the component, which updates the UI.
3. *Flow of Data*: Since data can only flow from parent to child, if a child component needs to communicate back to the parent, it uses *callback functions* passed as props. This keeps the data flow predictable and makes it easier to understand how the application behaves.

#### What is React's Virtual DOM and how does it work?
The Virtual DOM is a lightweight copy of the real DOM. When the state of a component changes, React updates the Virtual DOM first. It then compares the updated Virtual DOM with the previous version (a process called "reconciliation") and calculates the minimal number of changes required to update the real DOM. This makes React apps more efficient by minimizing costly DOM manipulations.

#### What is JSX?
JSX (JavaScript XML) is a syntax extension for JavaScript that allows you to write HTML-like code within JavaScript. It makes it easier to define the structure of the UI in a React component.

#### Can JSX use JavaScript Logic?
Yes, by using curly brackets `{}` to embed expressions like `{2 + 2}` or `{props.name}`.

#### How is JSX different from HTML?  
JSX uses `className` instead of `class`, `camelCase` for attributes, and requires a single parent element. And we can embed js inside it so.

#### What are components?
Components are the building blocks of a React application. They are JS functions/classes that accept inputs (called "props") and return UI elements (JSX). Components allow you to break down complex UIs into smaller, reusable pieces, making the code more manageable and maintainable.

#### How does React render components?
React renders components based on their state and props, updating only changed parts of the DOM.

#### What is the difference between class components and function components
- Function components are simple JS functions, that takes props as input and return JSX elements
- Class components are made using Js class, they extent from React.Component or React.PureComponent method and have a render method.

#### What is controlled component?
A controlled component is a form element (input, textarea, select) whose value is controlled by React state using `useState`. The component re-renders whenever the value changes, ensuring React has full control over the input.

#### What is uncontrolled component?
An uncontrolled component is a form element whose value is managed by the *DOM*, not React state. Instead of `useState`, you use **refs (`useRef`)** to access the value when needed

#### What is HOC
A **Higher-Order Component (HOC)** is a pattern in React that allows you to **reuse component logic**. It is a function that takes a component as an argument and returns a new component with additional functionality or props.

#### What are props?
props (short for "properties") are a mechanism for passing data and event handlers from one component to another, typically from a parent component to a child component.

#### How do you pass props?
suppose we want to pass a prop from parentComponent to childComponent, I'd write the prop name inside the childComponent tag that is inside the parentComponent then pass the prop as the value, just like attributes and value. `<ChildComponent name="React" />`, then use `props.name` in `ChildComponent`.

#### Why are props immutable?  
Props ensure one-way data flow, preventing unintended modifications.

#### What is prop-drilling?
The practice of passing data through props from a parent component down through multiple layers of child components, even though some of those intermediary components don't actually need the data, is called prop drilling. It is a bad practice and makes the code difficult to read and maintain.

#### How do you prevent prop-drilling?
We can prevent prop-drilling but using React Context API to share data across components without passing it through every level of the component tree.

#### What is key prop?
The key prop is a unique identifier that React uses to efficiently manage and update elements within a list
#### what is state?
State in React is an *object* that stores data that can change over time. It helps make components *dynamic and interactive*. Unlike *props* (which are read-only), *state is mutable* and can be updated using functions like `setState` (class components) or `useState` (functional components).

#### What is State Management in React?
State management in React refers to *the process of managing and updating the state of a React application

#### What is the difference between state and prop?
State is a component’s internal, mutable data, managed within the component using `useState`. Changing state triggers a re-render. Props are read-only, external data passed from a parent to a child component. They cannot be modified by the child.

#### What is Event Handling in React?
In React, events **handle user interactions within components**. They are similar to DOM events but offer a consistent interface across browsers. They are attached directly to JSX elements. React's synthetic event system simplifies handling interactions.

#### What are synthetic events in React?
Synthetic events are React's wrapper around native browser events. They provide a **consistent API across all browsers** and improve performance by using event delegation.

#### How do you prevent default behavior in React?
To prevent an event's default action (e.g., stopping form submission or link navigation), use `event.preventDefault()` inside the event handler.

#### What are Hooks?
Hooks are special functions in React that let you *use state and lifecycle features in functional components* without writing class components. Hooks must be used inside functional components and follow the **Rules of Hooks** (e.g., can't be used inside loops or conditionals).

#### Common Hooks
- `useState` – Manages **state** in a component.
- `useEffect` – Handles **side effects** like API calls.
- `useContext` – Accesses **context** without prop drilling.

#### What is useState?
`useState` is a React hook that allows functional components to manage state. It returns an array with two values: the current state and a function to update it.

#### What is useEffect?
`useEffect` is a hook for handling side effects (API calls, event listeners) in functional components. It runs after render and can have dependencies to control when it runs.

#### What is useContext hook?
`useContext` allows *direct access to context values* without prop drilling. It’s used with `createContext` to share data globally across components.

#### What is useMemo?
`useMemo` is a React hook that **memoizes** the result of a function to optimize performance. It only recalculates the value when its **dependencies** change, preventing unnecessary re-calculations on every render.

#### What is useReducer?
`useReducer` is a React hook used for managing more complex state logic in functional components. It works similarly to `useState`, but allows for more control over how state is updated, especially when the state depends on the previous state.
It takes two arguments:
1. A **reducer function** that specifies how the state should change based on the action.
2. The **initial state**.

#### What is useRef?
`useRef` is a React hook used to persist values across renders without causing re-renders. It is often used to access DOM elements directly or store mutable values that don't trigger re-renders when changed.

#### What is useCallback?
`useCallback` is a React Hook that memoizes functions, preventing them from being re-created on every render. It helps *optimize performance*, especially when passing functions as props to child components.

#### What is a custom Hook? How can you make one?
A custom hook in React is a reusable function that uses built-in hooks like `useState` or `useEffect` to encapsulate logic and share it across multiple components.
It follows the naming convention of starting with "use" and helps keep components cleaner by separating logic.

#### What is React Context API?
The **React Context API** is a built-in feature in React that allows data to be shared across multiple components without prop drilling (passing props through multiple layers manually). It helps manage global state efficiently.
#### What is createContext?
`createContext` is a function that creates a new context object. It provides a *global-like store* where data can be stored and accessed by components.

#### What is React Memoization?
React memoization refers to optimizing performance by **caching** the result of a component or function to avoid unnecessary re-rendering or recalculation. React provides tools like `React.memo` and `useMemo` to implement memoization.

#### What is the life cycle of a component?
In a function component, the life cycle is maintained by hooks like useEffect. When a component first renders, the mounting phase occurs, this is where we can run side effects using useEffect hook with an empty dependency array. When the state or props change/updates, the updating phase occurs, we can respond to this changes by adding dependencies to the useEffect. And finally then the component unmounts, we can run cleanup logic inside the return function of useEffect.

#### What is routing?
Routing in React refers to the process of handling navigation between different views or pages in a single-page application (SPA). It allows you to render different components or pages based on the URL, without reloading the page.

#### What is the difference between Route, Link & BrowserRouter in React?
BrowserRouter wraps the entire application and enables routing by keeping the UI in sync with the URL. It must be used at the top level of the app. Router defines a mapping between a URL path and a component to render. When the URL matches the path prop, the component inside it gets rendered. And Link is used for navigating between routes without refreshing the page. It prevents full-page reloads and updates the URL & content dynamically.

#### What is Suspense in React?
`Suspense` is a built-in React component used for *handling asynchronous operations*, such as lazy-loaded components or data fetching. It allows React to pause rendering until the required data or component is available, improving performance and user experience.

#### How Suspense works?
It displays a fallback UI (like a loading screen) until the component/data is loaded to be rendered. It is used with the React.lazy() method for code splitting. Like it'll load the component only when it's going to be needed.

#### How do you avoid re-renders in React?
- useMemo for expensive calculations and memoizes the value
- useCallBack for stable functions, it prevents unnecessary function re-creations in child components.
- avoid unnecessary updates when using the useContext hook
- Avoid inline functions and objects in JSX
- use key property in Lists
- and use React DevTools Profiler to identify unnecessary re-renders.

#### What is React Fragment?
A React Fragment (`<></>` or `<React.Fragment>`) is a wrapper that allows you to *return multiple elements* in a component without adding extra DOM nodes.

#### What is React Portal?
React Portal is a feature that allows rendering a child component outside its parent’s DOM hierarchy, typically used for modals, tooltips, or dropdowns.