**Scope** is just the "area" in your code where a variable or function can be used or accessed.

### Types of Scope:

1. **Global Scope**:
    - Variables declared outside any function are in the **global scope**. They can be accessed anywhere in your code.
    
    Example:
    ```javascript
    let x = 10; // global variable
    
    function showX() {
      console.log(x); // can access x because it's global
    }
    
    showX(); // prints 10
    ```

2. **Function Scope**:
    - Variables declared inside a function can only be used **inside that function**.
    
    Example:
    ```javascript
    function myFunc() {
      let y = 20; // function variable
      console.log(y); // works here
    }
    
    myFunc(); // prints 20
    console.log(y); // Error! y is not defined outside the function
    ```

3. **Block Scope** (using `let`/`const`):
    - Variables declared inside a block (like loops or conditionals) are only available **inside that block**.
    
    Example:
    ```javascript
    if (true) {
      let z = 30; // block-scoped variable
      console.log(z); // works here
    }
    
    console.log(z); // Error! z is not defined outside the block
    ```

### In short:

- **Global scope**: Accessible everywhere.
- **Function scope**: Accessible only inside the function.
- **Block scope**: Accessible only inside the block (like inside loops or if statements).
