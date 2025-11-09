### **What is `async/await`?**

`async/await` is a modern way to handle asynchronous operations in JavaScript, making code easier to read and maintain compared to using `.then()` with promises.

### **How it Works:**

1. **`async` keyword**: Declares a function as asynchronous, meaning it always returns a promise.
    
2. **`await` keyword**: Pauses the function execution until the promise resolves, then returns the result.
    

### **Example: Fetching Data from an API**

```javascript
async function fetchData() {
  try {
    const response = await fetch("https://api.example.com/data"); // Waits for response
    const data = await response.json(); // Waits for JSON conversion
    console.log(data);
  } catch (error) {
    console.error("Error:", error); // Catches any errors
  }
}

fetchData();
```

### **Why Use `async/await`?**

✅ **Cleaner syntax** than `.then()` chains  
✅ **Easier error handling** using `try...catch`  
✅ **Looks synchronous**, making it more readable