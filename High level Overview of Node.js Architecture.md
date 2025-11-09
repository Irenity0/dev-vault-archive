## 🧱 Core Components

### 1. **V8 Engine**

- Developed by Google for Chrome.
    
- Compiles JavaScript to **machine code** for fast execution.
    
- Node.js uses V8 to run JavaScript **outside the browser**.
    

### 2. **Libuv**

- A C library that handles:
    
    - **Asynchronous I/O** (file system, networking)
        
    - **Event loop**
        
    - **Thread pool**
        
- Acts as the backbone of Node.js’s **non-blocking** architecture.
    

### 3. **Event Loop**

- A loop that constantly checks for tasks, executes them, and waits for new ones.
    
- Key to **asynchronous behavior** in Node.js.
    
- Handles all callbacks and scheduled tasks using a **single thread**.
    

### 4. **Node.js Bindings**

- Connect JavaScript with C/C++ features under the hood.
    
- Allows Node.js to use native system capabilities (like file systems, sockets).
    

### 5. **Thread Pool**

- Managed by Libuv.
    
- Used for handling **blocking operations** (e.g., file reading, DNS lookup) without blocking the main event loop.
    
- Default size: 4 threads (can be changed).
    

---

## ⚙️ How It Works (Flow)

1. **Code Execution Starts**  
    JavaScript code is run by the **V8 engine**.
    
2. **Event Loop Begins**  
    Starts listening for events like HTTP requests, timers, or completed I/O.
    
3. **Async I/O Calls**  
    When an I/O operation is triggered (e.g., `fs.readFile()`):
    
    - It is sent to **Libuv**, which may delegate it to the **thread pool**.
        
    - The main thread **does not wait**—it continues executing.
        
4. **Callback Queuing**  
    Once the operation completes:
    
    - The callback is queued into the **event loop**.
        
    - The loop picks it up and executes it when idle.
        
5. **Handling Requests**  
    HTTP or WebSocket requests are handled through event-driven callbacks.
    

---

## 🔁 Event Loop Phases

Node.js breaks each cycle of the event loop into **phases**:

1. **Timers** – executes `setTimeout()` and `setInterval()` callbacks.
    
2. **Pending Callbacks** – for operations deferred to the next loop.
    
3. **Idle/Prepare** – internal use.
    
4. **Poll** – waits for new I/O events; executes I/O callbacks.
    
5. **Check** – executes `setImmediate()` callbacks.
    
6. **Close Callbacks** – e.g., `socket.on('close', ...)`.
    

---

## 📌 Summary Table

|Component|Responsibility|
|---|---|
|**V8**|Runs JavaScript quickly|
|**Libuv**|Manages async I/O, thread pool, and event loop|
|**Event Loop**|Central system that manages all async tasks|
|**Thread Pool**|Handles blocking operations in background|
|**Bindings**|Bridges JS and native system APIs|

---

## 📚 References

- Node.js Docs: [https://nodejs.org/en/docs](https://nodejs.org/en/docs)
- Libuv: [https://libuv.org](https://libuv.org/)
- Event Loop Explained (MDN): [https://developer.mozilla.org/en-US/docs/Web/JavaScript/EventLoop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/EventLoop)
- Node.js Event Loop Guide: [https://nodejs.dev/en/learn/the-nodejs-event-loop](https://nodejs.dev/en/learn/the-nodejs-event-loop)