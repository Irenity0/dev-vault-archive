**Event Bubbling** is when an event **starts from the innermost element** and **propagates (moves) up** to its parent elements.

📌 **Think of it like bubbles rising in water – the event starts at the target element and "bubbles up" to the ancestors.**

---

## **1️⃣ Example of Event Bubbling**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Event Bubbling Example</title>
</head>
<body>
    <div id="parent">
        <button id="child">Click Me</button>
    </div>

    <script>
        document.getElementById("parent").addEventListener("click", function () {
            console.log("Parent Clicked!");
        });

        document.getElementById("child").addEventListener("click", function () {
            console.log("Child Clicked!");
        });
    </script>
</body>
</html>
```

### **🔹 Expected Output when Clicking the Button:**

```
Child Clicked!
Parent Clicked!
```

✅ **Why?**

1. The button (`#child`) is clicked **first**.
    
2. The event **bubbles up** to the parent (`#parent`), triggering its event listener **after** the child.
    

---

## **2️⃣ Stopping Event Bubbling (Using `stopPropagation()`)**

If we **don't want** the event to bubble up, we can use `.stopPropagation()`.

### **🔹 Example: Prevent Bubbling**

```javascript
document.getElementById("child").addEventListener("click", function (event) {
    console.log("Child Clicked!");
    event.stopPropagation(); // Stops event from reaching parent
});
```

### **🔹 Now, clicking the button only logs:**

```
Child Clicked!
```

✅ **The parent’s event is NOT triggered!**

---

## **3️⃣ When is Event Bubbling Useful?**

🔹 **[[JavaScript Event Delegation]]** → Instead of adding event listeners to multiple child elements, attach **one listener** to the parent.  
🔹 **Handling Nested Elements** → It allows capturing events on both parent and child elements.

[[JavaScript Event Delegation]]
