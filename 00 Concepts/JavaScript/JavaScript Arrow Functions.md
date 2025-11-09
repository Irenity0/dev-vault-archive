### **Arrow Function**

An **arrow function** is a shorter syntax for writing functions in JavaScript. It uses the `\=>` symbol instead of the `function` keyword. It is often used for shorter functions, especially when working with callbacks or functions passed as arguments.

#### **Syntax:**

```javascript
const greet = (name) => {
  return "Hello, " + name;
};
```

For a single line function, you can omit the `return` and curly braces `{}`:

```javascript
const greet = (name) => "Hello, " + name;
```

#### **Example**:

```javascript
const greet = (name) => "Hello, " + name;
console.log(greet("John")); // "Hello, John"
```

---

### **Summary**:

- **Arrow Function**: A shorter and more concise way to write functions using `\=>`.