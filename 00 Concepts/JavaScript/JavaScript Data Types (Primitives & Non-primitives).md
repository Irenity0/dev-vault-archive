#### **1. Primitives (Immutable)**

These are basic data types that hold a single value and are immutable (cannot be changed directly).

- **Number**: Represents numerical values. `let age = 30;`
- **String**: Represents a sequence of characters. `let name = "Afra";`
- **Boolean**: Represents either `true` or `false`. `let isStudent = true;`
- **Undefined**: Represents a variable that has been declared but not assigned a value. `let x; // x is undefined`
- **Null**: Represents the absence of any value or object. `let user = null;`
- **Symbol**: Represents a unique and immutable value used as an identifier for object properties. `let sym = Symbol('unique');`
- **BigInt**: Represents large integers beyond the `Number` type’s limit. `let big = 1234567890123456789012345678901234567890n;`

#### **2. Non-primitives (Mutable)** 
These are more complex data types and are mutable (can be modified).

**Object**: Represents a collection of key-value pairs.
```javascript
let person = { name: "Afra", age: 30 };
```
  
 **Array**: A special type of object used for storing ordered collections.
 Example: `let fruits = ["apple", "banana", "cherry"];`

- **Function**: Functions are also objects in JavaScript.

```javascript
function greet() { console.log("Hello!"); }
```

### **Summary**:

- **Primitives**: Immutable, hold a single value (e.g., `Number`, `String`).
- **Non-primitives**: Mutable, can hold collections of values (e.g., `Object`, `Array`).