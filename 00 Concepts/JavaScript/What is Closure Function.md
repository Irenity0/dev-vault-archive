A **closure** is a function that **remembers the variables** from its **outer scope**, even after the outer function has finished executing.

In simple terms:  
📌 **A function inside another function that can still access the outer function’s variables, even after the outer function is gone.**

---

## **1️⃣ Basic Example of Closure**

```javascript
function outerFunction() {
  let outerVar = "I'm from outer function"; // Outer variable

  function innerFunction() { // Inner function (Closure)
    console.log(outerVar); // Accessing outer variable
  }

  return innerFunction; // Returning inner function
}

const myClosure = outerFunction(); // Outer function executes
myClosure(); // Output: "I'm from outer function"
```

✅ Even though `outerFunction()` has finished executing, `innerFunction()` still remembers `outerVar`. This is **closure**.

---

## **2️⃣ Why Use Closures?**

Closures are useful for:

1. **Data Privacy** (like private variables).
    
2. **Function Factories** (creating multiple similar functions).
    
3. **Maintaining State** in event handlers or callbacks.
    

---

## **3️⃣ Real-World Examples**

### **🔹 Example 1: Data Privacy (Encapsulation)**

Closures help **protect variables** from being modified directly.

```javascript
function counter() {
  let count = 0; // Private variable

  return function () {
    count++;
    console.log(count);
  };
}

const increment = counter(); 
increment(); // 1
increment(); // 2
increment(); // 3
```

✅ The `count` variable is **hidden** inside `counter()` and can only be accessed via the returned function.

---

### **🔹 Example 2: Function Factory**

Closures allow us to **create multiple customized functions**.

```javascript
function makeMultiplier(multiplier) {
  return function (num) {
    return num * multiplier;
  };
}

const double = makeMultiplier(2);
const triple = makeMultiplier(3);

console.log(double(5)); // 10
console.log(triple(5)); // 15
```

✅ `double` and `triple` are different functions that **remember** their `multiplier` values.

---

### **🔹 Example 3: Maintaining State in Event Listeners**

```javascript
function clickCounter() {
  let count = 0;
  return function () {
    count++;
    console.log(`Button clicked ${count} times`);
  };
}

const buttonClick = clickCounter();

document.getElementById("myButton").addEventListener("click", buttonClick);
```

✅ The `count` variable keeps increasing **inside the closure**, even when the event fires multiple times.

---

## **4️⃣ Key Points About Closures**

✅ **Closures "remember" variables** even after the outer function has finished.  
✅ **Used for private variables, function factories, and event handling.**  
✅ **Avoid memory leaks** by not overusing closures in long-running applications.