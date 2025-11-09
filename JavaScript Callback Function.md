A **callback function** is a function **passed as an argument** to another function, which is then **executed** after a certain event or task is completed.

📌 **It allows functions to be executed asynchronously or in response to an event.**

---

## **1️⃣ Simple Example of a Callback Function**

### **Example: Using a Callback Function**

```javascript
function greet(name, callback) {
    console.log("Hello " + name);
    callback();
}

function sayGoodbye() {
    console.log("Goodbye!");
}

greet("Afra", sayGoodbye);
```

### **🔹 Output:**

```
Hello Afra
Goodbye!
```

✅ **Why?**

- The `greet` function receives `sayGoodbye` as a callback.
    
- After logging "Hello Afra", it calls `sayGoodbye`, which logs "Goodbye!".
    

---

## **2️⃣ Callback Functions with Asynchronous Code**

Callbacks are commonly used in **asynchronous operations** like reading files, fetching data from an API, or setTimeout.

### **Example: Using a Callback with `setTimeout`**

```javascript
console.log("Start");

setTimeout(function () {
    console.log("This runs after 2 seconds");
}, 2000);

console.log("End");
```

### **🔹 Output:**

```
Start
End
This runs after 2 seconds
```

✅ **Why?**

- The `setTimeout` function takes a callback function that is executed after the specified delay (2000ms).
    
- **"End"** gets logged before the callback, even though `setTimeout` is called first, because it is asynchronous.
    

---

## **3️⃣ Callback Function with Array Methods**

Array methods like `map()`, `filter()`, and `forEach()` also use callbacks.

### **Example: Using `forEach` with a Callback**

```javascript
const numbers = [1, 2, 3, 4, 5];

numbers.forEach(function (num) {
    console.log(num * 2);
});
```

### **🔹 Output:**

```
2
4
6
8
10
```

✅ **Why?**

- The `forEach` method takes a callback function that runs on each item in the `numbers` array, doubling each value.
    

---

## **4️⃣ Key Takeaways**

✅ **A callback function** is passed as an argument to another function and is executed at a later time.  
✅ **Callbacks are used** for both synchronous and asynchronous operations.  
✅ They're **common in handling events**, **working with arrays**, and **dealing with asynchronous behavior** (like API calls or timers).

Would you like a more complex example involving **nested callbacks**?