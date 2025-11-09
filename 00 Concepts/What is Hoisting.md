**Hoisting** is JavaScript's behavior of **moving variable and function declarations to the top of their scope before execution**.

In simple words:  
📌 **You can use a function or variable before declaring it in your code.**

---

## **1️⃣ Hoisting with Variables**

#### 🔹 Example: Hoisting with `var`

```javascript
console.log(name); // Output: undefined
var name = "Afra";
console.log(name); // Output: Afra
```

✅ **Why?**

- JavaScript **hoists** the `var name;` declaration to the top.
- But **only the declaration** is hoisted, not the value.
- The variable **exists**, but it has **undefined** until it is assigned a value.
    

#### **Behind the Scenes (How JS sees it)**:

```javascript
var name; // Declaration is hoisted
console.log(name); // undefined
name = "Afra"; // Assignment stays in place
console.log(name); // Afra
```

---

### **🔹 Hoisting with `let` and `const`**

```javascript
console.log(age); // ❌ ReferenceError: Cannot access 'age' before initialization
let age = 25;
```

✅ **Why?**

- **`let` and `const` are hoisted**, but they are in a **"[[Temporal Dead Zone]]" (TDZ)** until they are assigned a value.    
- They **cannot** be accessed before the declaration.
    

#### **Example with `const`**

```javascript
console.log(city); // ❌ ReferenceError
const city = "New York";
```

---

## **2️⃣ Hoisting with Functions**

### **🔹 Function Declarations (✅ Hoisted)**

```javascript
greet(); // Output: Hello!

function greet() {
  console.log("Hello!");
}
```

✅ **Why?**
- Function **declarations** are **fully hoisted**, so you can call them before defining.
    

---

### **🔹 Function Expressions (`var`)**

```javascript
sayHi(); // ❌ TypeError: sayHi is not a function

var sayHi = function () {
  console.log("Hi!");
};
```

✅ **Why?**
- `var sayHi;` is hoisted, but **the function is not assigned yet**.    
- At the time of calling `sayHi()`, it is still `undefined`.
    

#### **Behind the Scenes:**

```javascript
var sayHi; // Declaration is hoisted
sayHi(); // ❌ TypeError
sayHi = function () { console.log("Hi!"); }; // Assignment happens later
```

---

### **🔹 Function Expressions (`let` or `const`)**

```javascript
greet(); // ❌ ReferenceError

const greet = function () {
  console.log("Hello!");
};
```

✅ **Why?**

- **`const` and `let` are in the [[Temporal Dead Zone]] (TDZ)**, so they **cannot** be accessed before declaration.
    

---

## **3️⃣ Summary of Hoisting Behavior**

|**Type**|**Hoisted?**|**Can Access Before Declaration?**|
|---|---|---|
|`var`|✅ Yes|⚠️ Yes, but `undefined`|
|`let`|✅ Yes|❌ No (TDZ)|
|`const`|✅ Yes|❌ No (TDZ)|
|Function Declaration|✅ Yes|✅ Yes|
|Function Expression (`var`)|✅ Yes (Only the variable)|❌ No (Undefined)|
|Function Expression (`let/const`)|✅ Yes|❌ No (TDZ)|

---

## **4️⃣ Key Takeaways**

✅ **Variable declarations are hoisted, but `let` and `const` are in the [[Temporal Dead Zone]] (TDZ).**  
✅ **Function declarations are fully hoisted, but function expressions are not.**  
✅ **Avoid confusion by declaring variables at the top and using `let`/`const` instead of `var`.**