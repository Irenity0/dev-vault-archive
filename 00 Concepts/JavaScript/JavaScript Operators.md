---
tags:
  - javascript
---
### **JavaScript Operators**

Operators are used to perform operations on values or variables.

#### **1. Arithmetic Operators**

Used for mathematical operations.

- **`+`**: Addition
    
    ```javascript
    let sum = 10 + 5; // 15
    ```
    
- **`-`**: Subtraction
    
    ```javascript
    let difference = 10 - 5; // 5
    ```
    
- **`*`**: Multiplication
    
    ```javascript
    let product = 10 * 5; // 50
    ```
    
- **`/`**: Division
    
    ```javascript
    let quotient = 10 / 5; // 2
    ```
    
- **`%`**: Modulus (remainder of division)
    
    ```javascript
    let remainder = 10 % 3; // 1
    ```
    
- **`++`**: Increment (increase by 1)
    
    ```javascript
    let count = 5;
    count++; // 6
    ```
    
- **`--`**: Decrement (decrease by 1)
    
    ```javascript
    let count = 5;
    count--; // 4
    ```
    

#### **2. Comparison Operators**

Used to compare values.

- **`\==`**: Equal to
    
    ```javascript
    10 == 10; // true
    ```
    
- **`\===`**: Strictly equal (checks value and type)
    
    ```javascript
    10 \=== '10'; // false
    ```
    
- **`!=`**: Not equal to
    
    ```javascript
    10 != 5; // true
    ```
    
- **`!==`**: Strictly not equal (checks value and type)
    
    ```javascript
    10 !== '10'; // true
    ```
    
- **`>`**: Greater than
    
    ```javascript
    10 > 5; // true
    ```
    
- **`<`**: Less than
    
    ```javascript
    5 < 10; // true
    ```
    
- **`>=`**: Greater than or equal to
    
    ```javascript
    10 >= 10; // true
    ```
    
- **`<=`**: Less than or equal to
    
    ```javascript
    5 <= 10; // true
    ```
    

#### **3. Logical Operators**

Used to perform logical operations.

- **`&&`**: Logical AND (both must be true)
    
    ```javascript
    true && false; // false
    ```
    
- **`||`**: Logical OR (one must be true)
    
    ```javascript
    true || false; // true
    ```
    
- **`!`**: Logical NOT (negates the value)
    
    ```javascript
    !true; // false
    ```
    

#### **4. Assignment Operators**

Used to assign values to variables.

- **`\=`**: Assign
    
    ```javascript
    let x = 10;
    ```
    
- **`+=`**: Add and assign
    
    ```javascript
    x += 5; // x = x + 5
    ```
    
- **`-=`**: Subtract and assign
    
    ```javascript
    x -= 5; // x = x - 5
    ```
    
- **`*=`**: Multiply and assign
    
    ```javascript
    x *= 5; // x = x * 5
    ```
    
- **`/=`**: Divide and assign
    
    ```javascript
    x /= 5; // x = x / 5
    ```
    
- **`%=`**: Modulus and assign
    
    ```javascript
    x %= 5; // x = x % 5
    ```
    

#### **5. Ternary (Conditional) Operator**

A shorthand for `if-else` conditions.

```javascript
let result = (10 > 5) ? "Yes" : "No"; // "Yes"
```

#### **6. Type Operators**

- **`typeof`**: Returns the type of a variable.
    
    ```javascript
    typeof "Hello"; // "string"
    ```
    
- **`instanceof`**: Checks if an object is an instance of a class.
    
    ```javascript
    let arr = [];
    arr instanceof Array; // true
    ```
    

#### **7. Bitwise Operators**

Perform bit-level operations on binary numbers.

- **`&`**: AND
- **`|`**: OR
- **`^`**: XOR
- **`~`**: NOT
- **`<<`**: Left shift
- **`>>`**: Right shift

### **Summary**:

- **Arithmetic**: Perform basic math operations.
- **Comparison**: Compare values.
- **Logical**: Combine boolean expressions.
- **Assignment**: Assign and modify values.
- **Ternary**: Simplified `if-else`.
- **Type**: Determine types and instances.