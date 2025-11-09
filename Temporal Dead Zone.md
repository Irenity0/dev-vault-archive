The **Temporal Dead Zone (TDZ)** is the period **between** when a variable is **hoisted** and when it is **initialized**. ([[What is Hoisting]])

📌 **In this period, accessing the variable will cause a `ReferenceError`.**

---

## **1️⃣ Example of Temporal Dead Zone**

```javascript
console.log(name); // ❌ ReferenceError: Cannot access 'name' before initialization
let name = "Afra";
console.log(name); // ✅ Afra
```

✅ **Why?**

- The **`let name;` declaration is hoisted** to the top.
- But JavaScript **does not assign it `undefined`** like `var`.
- Instead, it remains **in the TDZ until it is assigned a value** (`name = "Afra"`).

---

## **2️⃣ TDZ with `const` and `let`**

```javascript
console.log(age); // ❌ ReferenceError
const age = 20;
console.log(age); // ✅ 20
```

✅ **`const` behaves the same way as `let` in the TDZ**.

---

## **3️⃣ No TDZ with `var`**

```javascript
console.log(city); // ✅ undefined
var city = "New York";
console.log(city); // ✅ New York
```

✅ **`var` is hoisted and initialized as `undefined`, so no TDZ.**

---

## **4️⃣ TDZ in a Block Scope (`let` and `const` inside `{}`)**

```javascript
{
  console.log(value); // ❌ ReferenceError
  let value = 100;
  console.log(value); // ✅ 100
}
```

✅ The TDZ **exists inside the block `{}`** from the start until `value = 100;` is executed.

---

## **5️⃣ TDZ in Function Parameters**

```javascript
function example(x = y, y = 2) {
  console.log(x, y);
}

example(); // ❌ ReferenceError: y is not defined
```

✅ Here, `y` is **not yet initialized** when `x = y` runs, causing a **TDZ error**.

---

## **6️⃣ Summary**

|**Variable Type**|**Hoisted?**|**In TDZ?**|**Can Access Before Declaration?**|
|---|---|---|---|
|`var`|✅ Yes|❌ No|⚠️ Yes, but `undefined`|
|`let`|✅ Yes|✅ Yes|❌ No (`ReferenceError`)|
|`const`|✅ Yes|✅ Yes|❌ No (`ReferenceError`)|

---

## **7️⃣ Key Takeaways**

✅ **`let` and `const` are hoisted but stay in the TDZ until initialized.**  
✅ **Trying to access a variable in the TDZ causes a `ReferenceError`.**  
✅ **Avoid TDZ issues by always declaring variables before using them.**