#### What is JavaScript?
JavaScript is a high-end interpreted language that is used to add interactivity to static web pages.

#### Where is JavaScript used?
It is added in frontend for interactivity and dynamic features, backend for server-side development. Also in mobile apps, game development, and desktop apps.

#### What are variables?
Variables are used to store data that can be referenced or manipulated later. We can declare a variable using 3 ways:
- **Var** is the oldest way to declare a variable, it is globally scoped, so it can be accessed from anywhere. The declaration is hoisted (moved to the top of the scope), but the initialization remains in place.
- **Let** is block-scoped, meaning it is limited to the block where it is defined. It can be updated but can't be redeclared within the same scope. It is also technically hoisted but stays in the [[Temporal Dead Zone]] until the line where it's declared. It was introduced in ES6.
- **Const** is the same as Let except Const cannot be redeclared or updated. It's suitable for constant values and must be declared while being initialized.

#### What are Data Types?
There are
- **Primitive** data types that hold a single value and are immutable: `number`, `string`, `boolean`, `undefined`, `null`, `symbol`, and `bigInt`.
- **Non-primitive** data types, which are more complex and mutable, like **objects**, **arrays**, and **functions**.
 
#### What is an Array?
In JavaScript, arrays are used to store multiple values in a single variable. They are collections of elements, which can be of any data type.

#### How do you create an array?
An array can be created using: 
- Array literals
- The Array constructor

#### How can you access/modify array elements?
Array elements can be accessed and modified using bracket notation with the index of the element inside the notation.

#### What are some common array methods?
Some common array methods are:
1. `push()`: Adds one or more elements to the end of an array.
2. `pop()`: Removes the last element from an array and returns it.
3. `shift()`: Removes the first element from the array and returns it.
4. **`unshift()`**: Adds one or more elements to the beginning of an array.
5. **`splice()`**: Adds or removes elements from a specific position.
6. **`slice()`**: Returns a shallow copy of a portion of an array into a new array.
7. **`concat()`**: Merges two or more arrays.
8. **`join()`**: Joins all elements of an array into a string.
9. **`forEach()`**: Executes a function for each element of the array.
10. **`map()`**: Creates a new array with the results of calling a function on every element.
11. **`filter()`**: Creates a new array with all elements that pass a test.
12. **`find()`**: Returns the first element that satisfies a condition.
13. **`reduce()`**: Applies a function against an accumulator and each element to reduce it to a single value.
14. **`sort()`**: Sorts the elements of an array in place.
15. **`reverse()`**: Reverses the order of elements in an array.
16. **`length`**: Returns the number of elements in an array.

#### What is an object?
An object is a collection of key-value pairs, where each key (property) is a string, and the value can be of any data type. Objects are a fundamental part of JavaScript and are used to store and organize data.

#### How can you declare an object?
An object can be created using:
- Object literals
- The `new` keyword: creates a new object using a class (?)
- Object constructors
- `Object.create()`: Creates an object from an existing object
- `Object.fromEntries()`: Creates an object from a list of key/value pairs

#### What are some common object methods?
- **`Object.keys()`**: Returns an array of the object’s property names.
- **`Object.values()`**: Returns an array of the object’s property values.
- **`Object.entries()`**: Returns an array of the object’s `[key, value]` pairs.
- **`Object.assign()`**: Copies properties from one or more source objects to a target object.

#### What is a JavaScript function?
JavaScript functions are reusable blocks of code that perform a specific task. They allow you to group multiple statements together, name them, and execute them whenever you want (this is called "calling" the function).

#### Why use functions?
- To avoid repeating code (DRY principle: _Don’t Repeat Yourself_).
- To break your code into smaller, manageable chunks.
- To make your code reusable and easier to debug.

#### How do you define a function?
We can define a function using the `function` keyword/expression, followed by the function name, parentheses for parameters, and curly brackets for the function body.

#### What is an arrow function?
An arrow function is a shorter syntax for writing functions in JavaScript. It uses the `/=>` symbol instead of the `function` keyword. It is often used for shorter functions, especially when working with callbacks or functions passed as arguments.

#### What do you mean by Anonymous Function?
Functions without a name are called anonymous functions. They are often used in places like event handlers or immediately executed code.

#### What are parameters & arguments? What is the difference between them?
- **Parameters** are placeholders for input when defining a function, while
- **Arguments** are the actual values you pass when calling the function.

#### What are default parameters?
You can assign default values to parameters in case the caller doesn’t provide any value. If no value is passed for that parameter, the default value will be used.

#### What are REST parameters?
The **rest parameter** allows a function to accept an indefinite number of arguments as an array. It’s denoted by `...` (spread operator) before the parameter name. It’s useful when you don’t know how many arguments will be passed to the function.

#### What is Spread Operator?
The spread operator (`...`) spreads elements from an array or object. It helps in copying, merging, and passing values without modifying the original data.

#### What are template literals?
Template literals are strings enclosed in backticks (`` ` ``) that allow embedded expressions using `${}`. They support multi-line strings and dynamic content.

#### What is destructuring?
Destructuring is a way to extract values from arrays or properties from objects into separate variables in a concise manner.

#### What is scope?
Scope is the "area" in your code where a variable or function can be accessed. Types of scope include:
- **Global scope**: The variable can be accessed anywhere in your code.
- **Function scope**: Variables declared inside the function can only be used inside that function.
- **Block scope**: Variables declared inside a block are only accessible within that block.

#### What is Hoisting?
Hoisting is JavaScript's default behavior of moving variable and function declarations to the top of their scope before execution. Only declarations are hoisted, not initializations.

#### What is ECMAScript?
ECMAScript (ES) is a standardized scripting language specification that JavaScript is based on. It defines the core features and syntax of JavaScript to ensure consistency across different implementations.

#### Name some ES6 features
- `Let` and `Const` variables
- Arrow functions
- Template literals
- Default parameters
- Destructuring assignment
- Spread & Rest operators
- Promises
- Modules

#### What are JavaScript Events?
A JavaScript event is a specific action that occurs within a web page or application, such as clicking on an element, moving the mouse, pressing a key, or loading a page.

#### What is Event Loop?
The event loop in javascript manages asynchronous tasks despite being single-threaded. Whn a function is call, it runs on the call stack. Time-consuming tasks are handed to web apis, and thier callbacks wait in a callback queue. The event loop keeps checking if the stack is empty, and if is empty, it moves callbacks from the queue to the stack for execution. This process ensures tast run smoothing without blocking the main thread.

#### What is EventListener?
Event listeners allow you to listen for user interactions and execute a function when an event occurs.

#### What is event bubbling?
Event bubbling refers to the way events propagate from the target element up to its parent elements.

#### What is event delegation?
Event delegation is to add a single event listener to a parent element to manage events for children elements, taking advantage of event bubbling

#### What is Event Queue?
The **event queue** is a data structure in JavaScript that holds events or messages waiting to be processed. When asynchronous operations like user interactions, timers, or API responses are triggered, their corresponding event handlers are placed in the event queue. The event loop checks the queue and processes these events when the call stack is empty.


#### What is call stack?
The call stack is a data structure in JavaScript that keeps track of function execution. When a function is called, it’s added to the stack, and when it returns, it’s removed. It operates on a **LIFO (Last In, First Out)** basis.

#### What are JavaScript Higher Order Functions?
When a function takes a function as an argument or returns a new function, it is then called a Higher Order Function.

#### What is Callback function?
A callback is a function that is passed as an argument to another function and is executed after the completion of that function. Callbacks are primarily used to handle asynchronous operations like API requests, file reading, or timers.

#### What is Callback Hell?
Callback Hell refers to a situation in JavaScript where multiple nested callbacks are used for asynchronous tasks, making the code difficult to read, debug, and maintain. It looks like a "pyramid of doom" or deeply nested code.

#### How to prevent Callback Hell?
use promises and the async/await syntax to structure asychronous operations

#### What are microtasks/macrotasks? 
Mircotasks are high-priority asynchronous tasks, that run right after the current execution. And Microtasks are secondary to them, executing after macrotasks. 

#### What is closure function?
A closure is a function that retains access to variables from its lexical scope (the scope in which it was created) even after that scope has finished executing. In simpler terms, closures allow a function to "remember" the environment in which it was created, including variables and parameters from the outer scope. 

#### Why are Closures useful? 
Data Encapsulation: You can create private variables that are inaccessible from outside the closure but can be manipulated by the inner function. .
Maintaining State: Closures allow you to maintain state across multiple function calls without using global variables.

#### What is Data Encapsulation?
Data encapsulation, also known as data hiding, is the mechanism whereby the implementation details of a class are kept hidden from the user.

#### What is control structure? 
Control structures are used to control the flow of execution in a program. They can decide which block of code should be executed based on conditions or loops. 
- *Conditional statements :*  Used to make decisions based on conditions. like if, else, elseif, switch 
- *Looping Statements :* Used to repeatedly execute a block of code. like for, while, do...while 
- *Break & Continue :* Used to alter loops, break exits the loop completely while continue skips the current iteration then continues the loop

#### What is jwt? 
JWT (JSON Web Token) is a compact, URL-safe token used for securely transmitting information between parties. It consists of three parts: a header, payload (data), and signature, often used for authentication and authorization. 

#### What are Promises?
A promise is an object representing the eventual completion (or failure) of an asynchronous operation and its resulting value. Promises allow chaining of operations/methods, making the code more readable and avoiding callback hell.

#### What is `async/await`?
`async/await` provides a cleaner syntax for working with promises.
- `async` makes a function return a promise.
- `await` is used to wait for a promise to resolve or reject.

#### Arrow Functions and `this`
Arrow functions do not have their own `this` context. Instead, they inherit the value of `this` from the surrounding context. This makes them particularly useful in certain scenarios like event handling where you don’t want the value of `this` to change.

#### Prototype Chain
In JavaScript, objects can inherit properties and methods from other objects through the prototype chain. Every object has a prototype, and properties/methods are looked up through the prototype chain if not found directly on the object.

#### Event Capturing vs. Event Bubbling
- **Event capturing** starts from the root and goes down to the target element.
- **Event bubbling** starts from the target element and bubbles up to the root element.

#### Deep Copy vs Shallow Copy
- **Shallow copy** copies the object’s references but not the actual objects, meaning changes in nested objects will affect both the original and copied objects.
- **Deep copy** creates a completely independent copy of an object and its nested objects, meaning the original and copied objects are fully isolated
#### When should we not use arrow function? \*
- **When you need a dynamic `this` context** (e.g., object methods or event handlers).
- **When you need to use the `arguments` object** (arrow functions don’t have their own `arguments`).
- **As constructor functions** (arrow functions cannot be used with `new`).
- **In class methods** that need to use `super` or dynamically bind `this`.
- **For event handlers** if you need `this` to refer to the element that triggered the event.

#### What is type coercion? \*
Type coercion refers to **the automatic conversion of values from one data type to another, typically performed during operations or comparisons involving different data types**. By using Type Coercion, JavaScript attempts to make the data types compatible to complete the operation or comparison