#### **1. Parameters**

Parameters are variables defined in a function declaration that specify what values the function expects when called.

Example:

```javascript
function greet(name) {
  return "Hello, " + name;
}
```

- `name` is the parameter in this function.

#### **2. Default Parameters**

You can assign default values to parameters in case the caller doesn’t provide any value. If no value is passed for that parameter, the default value will be used.

Example:

```javascript
function greet(name = "Guest") {
  return "Hello, " + name;
}

console.log(greet("John")); // "Hello, John"
console.log(greet()); // "Hello, Guest"
```

- If no `name` is provided, the default `"Guest"` is used.

---

### **Summary**:

- **Parameters**: Variables that specify what data the function needs.
- **Default Parameters**: Values assigned to parameters in case no argument is provided.