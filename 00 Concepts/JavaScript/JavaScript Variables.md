---
tags:
  - javascript
---
Variables are used to store data that can be referenced and manipulated later.

#### **Types of Variables**

1. **`var`**:
    
    - **Oldest way** to declare variables.
    - **Function-scoped**: Variables are limited to the function in which they are defined.
    - Can be **redeclared** and **updated**.
    - **Hoisted**: The declaration is moved to the top of its scope, but the initialization/assignment remains in place.
    
    ```javascript
    var name = "John";
    var name = "Doe"; // Redeclaring is allowed
    ```

2. **`let`:**
    
    - **Block-scoped**: The variable is limited to the block (e.g., within a loop, function, or condition) where it is defined.
    - Can be **updated** but **not redeclared** in the same scope.
    - **Hoisted**, but stays in the **[[Temporal Dead Zone]] (TDZ)** until the line where it's declared. This means you **cannot access it before its declaration.**
    - Introduced in ES6 (ES2015).
    
    ```javascript
    console.log(age); // ReferenceError: Cannot access 'age' before initialization
    let age = 30; 
    age = 31; // Allowed
    ```
    
3. **`const`:**
    
    - **Block-scoped**: Like `let`, but the value **cannot be reassigned** once it’s set.
    - Ideal for **constant values** or variables that should remain unchanged.
    - **Hoisted**, but also stays in the **[[Temporal Dead Zone]] (TDZ)** until the line where it's declared. Additionally, it **must be initialized** at the time of declaration.
    - Introduced in ES6 (ES2015).
    
    ```javascript
    console.log(age); // ReferenceError: Cannot access 'age' before initialization
    const age = 30;
    age = 31; // TypeError: Assignment to constant variable
    ```
  
  ```javascript
    const pi = 3.14;
    pi = 3.1415; // Error: Assignment to constant variable.
    ```

---

### Key Point on Hoisting:

- **`var`:** Hoisted and initialized with `undefined`. You can access it before declaration.
- **`let` & `const`:** Hoisted, but stay in the **[[Temporal Dead Zone]] (TDZ)** until the code execution reaches their declaration line. Accessing them before declaration will throw a **ReferenceError.**

---

### **Key Differences**:

- **Scope**:
    - `var`: Function-scoped.
    - `let`, `const`: Block-scoped.
- **Reassignment**:
    - `var` and `let`: Can be reassigned.
    - `const`: Cannot be reassigned.
- **Redeclaration**:
    - `var`: Can be redeclared.
    - `let` and `const`: Cannot be redeclared in the same scope.

### **Best Practice**:

- Use `let` for variables that might change.
- Use `const` for values that shouldn’t change.