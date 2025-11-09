JavaScript **modules** allow you to split code into **separate files** and import/export them when needed. This improves **organization, reusability, and maintainability**.

---

### **1️⃣ ES6 Modules (Modern JavaScript)**

- **Exporting (module.js)**
    
    ```javascript
    export const greeting = "Hello";
    export function greet(name) {
        console.log(`${greeting}, ${name}!`);
    }
    ```
    
- **Importing (app.js)**
    
    ```javascript
    import { greeting, greet } from './module.js';
    console.log(greeting);  // "Hello"
    greet("Afra");  // "Hello, Afra!"
    ```
    

---

### **2️⃣ Default Export**

- **Exporting**
    
    ```javascript
    export default function() {
        console.log("Default function");
    }
    ```
    
- **Importing**
    
    ```javascript
    import myFunc from './module.js';
    myFunc();  // "Default function"
    ```
    

---

### **3️⃣ Dynamic Import**

Load modules **only when needed**:

```javascript
import('./module.js').then(module => module.greet('Afra'));
```

---

### **4️⃣ Key Points**

✅ **Prevents global scope pollution**  
✅ **Better code organization**  
✅ **Works in modern browsers & Node.js (with HTTP server)**

Need details on **CommonJS (Node.js) modules**?