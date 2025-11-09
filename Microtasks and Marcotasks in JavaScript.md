JavaScript handles asynchronous operations using the **Event Loop**, where tasks are divided into **Microtasks** and **Macrotasks** (also called "Tasks").

---

## **1️⃣ Microtasks (Higher Priority)**

Microtasks **run immediately after the current script execution finishes** and **before any macrotasks**.

### **Examples of Microtasks:**

✅ **Promises (`.then`, `.catch`, `.finally`)**  
✅ **MutationObserver (Detects DOM changes)**  
✅ **QueueMicrotask() (Explicitly adding a microtask)**

### **Example:**

```javascript
console.log("Start");

Promise.resolve().then(() => console.log("Microtask 1"));
queueMicrotask(() => console.log("Microtask 2"));

console.log("End");
```

**Output:**

```
Start  
End  
Microtask 1  
Microtask 2  
```

🔹 **Microtasks run after synchronous code but before macrotasks.**

---

## **2️⃣ Macrotasks (Lower Priority)**

Macrotasks run **after microtasks are completed** and include:

✅ **setTimeout & setInterval**  
✅ **setImmediate (Node.js only)**  
✅ **I/O operations (like file reading)**  
✅ **Message Channels**

### **Example:**

```javascript
console.log("Start");

setTimeout(() => console.log("Macrotask 1"), 0);

Promise.resolve().then(() => console.log("Microtask"));

console.log("End");
```

**Output:**

```
Start  
End  
Microtask  
Macrotask 1  
```

🔹 **Even with `setTimeout(0)`, the promise runs first because microtasks have higher priority!**

---

## **3️⃣ Execution Order**

1️⃣ **Synchronous code** (Top priority)  
2️⃣ **Microtasks** (Promises, queueMicrotask, MutationObserver)  
3️⃣ **Macrotasks** (setTimeout, setInterval, I/O, setImmediate)

---

## **4️⃣ Key Takeaways**

✅ **Microtasks run first before any macrotask**  
✅ **Promises & queueMicrotask are microtasks**  
✅ **setTimeout & setInterval are macrotasks**  
✅ **Event loop ensures everything runs smoothly**