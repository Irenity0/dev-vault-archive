---
tags:
  - javascript
---

In JavaScript, an **object method** is simply a function that is a property of an object. Here’s how you can define and use object methods in different ways:

---

### **1. Using a Function as a Method**

```javascript
const person = {
  name: "Afra",
  greet: function() {
    return `Hello, my name is ${this.name}`;
  }
};

console.log(person.greet());  // Output: Hello, my name is Afra
```

- Here, `greet` is a method of the `person` object.
    
- The `this` keyword refers to the object itself (`person`), allowing access to its properties.
    

---

### **2. Using ES6 Method Shorthand**

This is a cleaner way to define methods inside an object.

```javascript
const person = {
  name: "Afra",
  greet() {
    return `Hello, my name is ${this.name}`;
  }
};

console.log(person.greet());  // Output: Hello, my name is Afra
```

- Works the same way as the previous example but is shorter and more readable.
    

---

### **3. Using an Arrow Function (⚠️ Avoid Inside Objects)**

Arrow functions **don’t bind `this` to the object**, so they usually don’t work as expected in methods.

```javascript
const person = {
  name: "Afra",
  greet: () => {
    return `Hello, my name is ${this.name}`;
  }
};

console.log(person.greet());  // Output: Hello, my name is undefined
```

- Here, `this` refers to the **global scope**, not the `person` object, so `this.name` is `undefined`.
    

---

### **4. Adding Methods After Object Creation**

You can also define methods outside the object.

```javascript
const person = {
  name: "Afra"
};

person.greet = function() {
  return `Hello, my name is ${this.name}`;
};

console.log(person.greet());  // Output: Hello, my name is Afra
```

- Useful when you need to extend objects dynamically.
    

---

### **5. Using `Object.defineProperty()`**

This allows defining a method with specific properties (e.g., making it read-only).

```javascript
const person = { name: "Afra" };

Object.defineProperty(person, "greet", {
  value: function() {
    return `Hello, my name is ${this.name}`;
  },
  writable: false // The method cannot be changed
});

console.log(person.greet());  // Output: Hello, my name is Afra
```

---

### **Which Method Should You Use?**

✅ **Use ES6 shorthand** for cleaner code.  
✅ **Use function expressions** if you need more flexibility.  
❌ **Avoid arrow functions inside objects** unless you’re sure you don’t need `this`.