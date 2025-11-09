---
tags:
  - javascript
  - interview_question
---

An **IIFE (Immediately Invoked Function Expression)** is a function that **executes immediately after being defined**. It is mainly used to create a **private scope** and avoid polluting the global namespace.

---

## **1️⃣ Syntax of an IIFE**

```javascript
(function() {
  console.log("I am an IIFE and I run immediately!");
})();
```

### **How It Works:**

- The function is **wrapped in parentheses** to make it an **expression**.
    
- The `()` at the end **executes** the function **immediately**.
    

---

## **2️⃣ Why Use IIFE?**

✅ **Avoid Global Variable Pollution** → Keeps variables inside a local scope.  
✅ **Execute Code Immediately** → Useful for initialization tasks.  
✅ **[[Encapsulation]]** → Protects variables from being accessed or modified.

---

## **3️⃣ Types of IIFE with Examples**

### **🔹 1. Anonymous IIFE**

```javascript
(function() {
  console.log("Anonymous IIFE runs!");
})();
```

- A function **without a name** that executes immediately.
    

---

### **🔹 2. Named IIFE**

```javascript
(function myFunction() {
  console.log("Named IIFE runs!");
})();
```

- Even though it has a name (`myFunction`), it **cannot be called again**.
    

---

### **🔹 3. IIFE with Parameters**

```javascript
(function(name) {
  console.log(`Hello, ${name}`);
})("Afra");
```

- The function **accepts arguments** and executes immediately.
    

---

### **🔹 4. Arrow Function IIFE (ES6)**

```javascript
(() => {
  console.log("Arrow function IIFE runs!");
})();
```

- A **shorter** way to write an IIFE using **arrow functions**.
    

---

### **🔹 5. IIFE That Returns a Value**

```javascript
const result = (function() {
  return "Returned from IIFE!";
})();
console.log(result);  // Output: Returned from IIFE!
```

- The IIFE **returns a value**, which can be stored in a variable.
    

---

## **4️⃣ Use Cases of IIFE**

### **🔸 1. Avoid Global Variable Conflicts**

```javascript
let message = "Global";

(function() {
  let message = "Inside IIFE";
  console.log(message); // Output: Inside IIFE
})();

console.log(message); // Output: Global
```

- The variable `message` inside the IIFE **does not affect** the global `message`.
    

---

### **🔸 2. Module Pattern (Simulating Private Variables)**

```javascript
const counter = (function() {
  let count = 0;  // Private variable

  return {
    increment: function() {
      count++;
      console.log(`Count: ${count}`);
    },
    getCount: function() {
      return count;
    }
  };
})();

counter.increment();  // Output: Count: 1
counter.increment();  // Output: Count: 2
console.log(counter.getCount());  // Output: 2
```

- **Encapsulates `count`**, making it private.
    

---

### **🔸 3. Using IIFE in Asynchronous Code**

```javascript
(async function() {
  let data = await fetch("https://jsonplaceholder.typicode.com/todos/1")
                .then(response => response.json());

  console.log(data);
})();
```

- The **IIFE is `async`**, allowing it to execute immediately with `await`.
    

---

## **5️⃣ Summary**
- IIFE **runs immediately** after being defined.
- It helps **avoid global scope pollution**.
- It can be used for **modular patterns, async code, and encapsulation**.