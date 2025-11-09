Control structures are used to control the flow of execution in a program. They can decide which block of code should be executed based on conditions or loops.

#### **1. Conditional Statements**

Used to make decisions based on conditions.

- **`if`**: Executes a block of code if a condition is true.
    
    ```javascript
    if (x > 10) {
      console.log("x is greater than 10");
    }
    ```
    
- **`else`**: Executes a block of code if the `if` condition is false.
    
    ```javascript
    if (x > 10) {
      console.log("x is greater than 10");
    } else {
      console.log("x is 10 or less");
    }
    ```
    
- **`else if`**: Used to specify multiple conditions.
    
    ```javascript
    if (x > 10) {
      console.log("x is greater than 10");
    } else if (x == 10) {
      console.log("x is exactly 10");
    } else {
      console.log("x is less than 10");
    }
    ```
    
- **`switch`**: A more readable way to check multiple conditions based on a single expression.
    
    ```javascript
    switch (day) {
      case 1:
        console.log("Monday");
        break;
      case 2:
        console.log("Tuesday");
        break;
      default:
        console.log("Other day");
    }
    ```
    

#### **2. Looping Statements**

Used to repeatedly execute a block of code.

- **`for`**: Used when the number of iterations is known.
    
    ```javascript
    for (let i = 0; i < 10; i++) {
      console.log(i); // Outputs 0 to 4
    }
    ```
    
- **`while`**: Executes a block of code as long as a condition is true.
    
    ```javascript
    let i = 0;
    while (i < 5) {
      console.log(i); // Outputs 0 to 4
      i++;
    }
    ```
    
- **`do...while`**: Executes a block of code once, and then repeats as long as the condition is true.
    
    ```javascript
    let i = 0;
    do {
      console.log(i); // Outputs 0 to 4
      i++;
    } while (i < 5);
    ```
    

#### **3. Break & Continue**

Control the flow inside loops.

- **`break`**: Exits the loop completely.
    
    ```javascript
    for (let i = 0; i < 5; i++) {
      if (i === 3) {
        break; // Stops loop when i equals 3
      }
      console.log(i); // Outputs 0, 1, 2
    }
    ```
    
- **`continue`**: Skips the current iteration and moves to the next one.
    
    ```javascript
    for (let i = 0; i < 5; i++) {
      if (i === 3) {
        continue; // Skips when i equals 3
      }
      console.log(i); // Outputs 0, 1, 2, 4
    }
    ```
    

### **Summary**:

- **Conditionals**: Control flow based on conditions (`if`, `else`, `switch`).
- **Loops**: Repeat actions (`for`, `while`, `do...while`).
- **Control flow**: Alter loops with `break` and `continue`.