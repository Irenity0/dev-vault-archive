Asynchronous JavaScript allows tasks to run **without blocking** the execution of other code. This is important for handling time-consuming operations like API requests, file reading, or timers without freezing the webpage.

---

### **How it Works**

JavaScript is **single-threaded**, meaning it executes one operation at a time. But with asynchronous programming, tasks like fetching data or waiting for user input can be handled in the background while the rest of the code runs.

---

## **Ways to Handle Asynchronous Code**

#### 1️⃣ **Callbacks** (Old method, can lead to "callback hell")

```javascript
setTimeout(() => {
  console.log("This runs after 2 seconds.");
}, 2000);
```

➡ Executes after 2 seconds while other code runs.

#### 2️⃣ **Promises** (Modern alternative to callbacks)

```javascript
fetch("https://api.example.com/data")
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error("Error:", error));
```

➡ Uses `.then()` to handle the result when ready.

#### 3️⃣ **async/await** (More readable approach)

```javascript
async function fetchData() {
  try {
    const response = await fetch("https://api.example.com/data");
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error("Error:", error);
  }
}

fetchData();
```

➡ Looks synchronous but runs asynchronously.

---

### **Why is Asynchronous JavaScript Important?**

✅ Prevents UI from freezing  
✅ Handles network requests smoothly  
✅ Improves performance