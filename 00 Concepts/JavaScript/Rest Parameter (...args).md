The **rest parameter** allows a function to accept an indefinite number of arguments as an array. It’s denoted by `...` before the parameter name.

#### **Syntax**:

```javascript
function myFunction(...args) {
  console.log(args);
}
```

- `args` is an array that holds all the arguments passed to the function.

#### **Example**:

```javascript
function sum(...numbers) {
  return numbers.reduce((total, num) => total + num, 0);
}

console.log(sum(1, 2, 3, 4)); // 10
console.log(sum(5, 10)); // 15
```

- `numbers` is an array that holds all the values passed to the function.

#### **Important Notes**:

- The rest parameter must be the last parameter in the function.
- It allows you to handle any number of arguments in a flexible way.

---

### **Summary**:

- **Rest Parameter (`...args`)**: Captures multiple arguments as an array.
- It’s useful when you don’t know how many arguments will be passed to the function.