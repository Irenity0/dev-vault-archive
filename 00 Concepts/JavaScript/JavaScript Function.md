---
tags:
  - javascript
---

JavaScript **functions** are reusable blocks of code that perform a specific task. They allow you to group multiple statements together, name them, and execute them whenever you want (this is called "calling" the function).

Think of a function as a **machine**:

1. You provide **input** (optional). [[JavaScript Array Methods]]
2. The machine processes the input.
3. It gives you **output** (optional).

---

### **Why Use Functions?**

- To avoid repeating code (DRY principle: _Don’t Repeat Yourself_).
- To break your code into smaller, manageable chunks.
- To make your code reusable and easier to debug.

---

### **Defining a Function**

There are several ways to create a function in JavaScript:

#### 1. **Function Declaration**

```javascript
function greet() {
  console.log("Hello, world!");
}
```

- **How to call it**:
    
    ```javascript
    greet(); // Output: Hello, world!
    ```
    

#### 2. **Function Expression**

- You can assign a function to a variable:
    
    ```javascript
    const greet = function() {
      console.log("Hello, world!");
    };
    
    greet(); // Output: Hello, world!
    ```
    

#### 3. **Arrow Functions (ES6)**

- A shorter way to write functions:
    
    ```javascript
    const greet = () => {
      console.log("Hello, world!");
    };
    
    greet(); // Output: Hello, world!
    ```
    

---

### **Parameters and Arguments**

- **Parameters**: Placeholders for input when defining a function.
- **Arguments**: Actual values you pass when calling the function.

#### Example:

```javascript
function greet(name) { // 'name' is the parameter
  console.log(`Hello, ${name}!`);
}

greet("Afra"); // Output: Hello, Afra! ('Afra' is the argument)
```

---

### **Returning a Value**

Functions can return a result using the `return` keyword.

#### Example:

```javascript
function add(a, b) {
  return a + b;
}

const sum = add(3, 5);
console.log(sum); // Output: 8
```

- `return` ends the function and gives back a value.

---

### **Anonymous Functions**

- Functions without a name are called **anonymous functions**.
- They're often used in places like event handlers or immediately executed code:
    
    ```javascript
    const sayHi = function() {
      console.log("Hi!");
    };
    
    sayHi(); // Output: Hi!
    ```
    

---

### **Key Takeaways**

4. Functions are reusable blocks of code.
5. They can take inputs (parameters) and return outputs (results).
6. Functions make your code cleaner, reusable, and modular.

In JavaScript, functions are everywhere—you'll use them in everything from handling user clicks to fetching API data.