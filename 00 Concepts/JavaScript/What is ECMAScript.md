---
tags:
  - ecmascript
  - javascript
---

**ECMAScript (ES)** is the **standard** that defines how JavaScript works. It is **not** a separate language but a **set of rules and features** that JavaScript follows.

Think of **ECMAScript** as the blueprint, and **JavaScript** as the real-world implementation used in web browsers and servers.

---

## **1️⃣ History of ECMAScript**

- **JavaScript** was created by **Brendan Eich** in 1995.
    
- To avoid conflicts with other languages, JavaScript was standardized by **ECMA International** under the name **ECMAScript** in 1997.
    
- New ECMAScript versions (ES6, ES7, ES8, etc.) introduce **modern features**.
    

---

## **2️⃣ Key ECMAScript Versions**

Here are some major ECMAScript updates and their important features:

|**Version**|**Year**|**Major Features**|
|---|---|---|
|**ES1**|1997|First official version|
|**ES3**|1999|Introduced `try-catch` for error handling|
|**ES5**|2009|`JSON.parse()`, `strict mode` (`"use strict"`)|
|**ES6 (ES2015)**|2015|`let`, `const`, arrow functions, classes, template literals, promises|
|**ES7 (ES2016)**|2016|`Array.prototype.includes()`, `**` (exponentiation operator)|
|**ES8 (ES2017)**|2017|`async/await`, Object.entries(), Object.values()|
|**ES9 (ES2018)**|2018|`Rest/Spread` for objects, `Promise.finally()`|
|**ES10 (ES2019)**|2019|`flat()`, `flatMap()`, optional catch binding|
|**ES11 (ES2020)**|2020|`BigInt`, `nullish coalescing (??)`, optional chaining (`?.`)|
|**ES12 (ES2021)**|2021|`replaceAll()`, logical assignment operators (`&&=,|

---

## **3️⃣ Examples of ECMAScript Features**

### **🔹 ES5 Example (`var`, JSON, strict mode)**

```javascript
"use strict";
var name = "Afra";
console.log(name); // Afra
console.log(JSON.stringify({ key: "value" })); // '{"key":"value"}'
```

---

### **🔹 ES6 Example (`let`, `const`, arrow functions, template literals)**

```javascript
const name = "Afra";
const greet = () => `Hello, ${name}!`;

console.log(greet()); // Output: Hello, Afra!
```

---

### **🔹 ES7 Example (`Array.includes()`)**

```javascript
let numbers = [1, 2, 3, 4];
console.log(numbers.includes(3)); // true
```

---

### **🔹 ES8 Example (`async/await`)**

```javascript
async function fetchData() {
  let response = await fetch("https://jsonplaceholder.typicode.com/todos/1");
  let data = await response.json();
  console.log(data);
}

fetchData();
```

---

### **🔹 ES11 Example (Optional Chaining `?.`)**

```javascript
let user = { name: "Afra", details: null };
console.log(user.details?.age); // undefined (no error)
```

---

## **4️⃣ Why is ECMAScript Important?**

✅ **Standardizes JavaScript**, ensuring consistency across browsers.  
✅ **Introduces new features**, making JavaScript more powerful and efficient.  
✅ **Helps developers write modern and cleaner code**.

Would you like more details on any specific ES version? 🚀