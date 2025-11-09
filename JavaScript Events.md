A JavaScript event is a specific action that occurs within a web page or application, such as clicking on an element, moving the mouse, pressing a key, or loading a page.

---

### **1️⃣ Adding Event Listeners**

#### **Method 1: Inline Event (Not Recommended)**

```html
<button onclick="alert('Button Clicked!')">Click Me</button>
```

#### **Method 2: Using `addEventListener` (Recommended)**

```javascript
document.getElementById("btn").addEventListener("click", function() {
    alert("Button Clicked!");
});
```

```html
<button id="btn">Click Me</button>
```

---

### **2️⃣ Common Events**

|Event|Description|
|---|---|
|`click`|Fires when an element is clicked|
|`mouseover`|Fires when mouse is over an element|
|`keydown`|Fires when a key is pressed|
|`submit`|Fires when a form is submitted|
|`load`|Fires when the page loads|

---

### **3️⃣ Removing Event Listeners**

```javascript
function sayHello() {
    console.log("Hello!");
}
document.getElementById("btn").addEventListener("click", sayHello);
document.getElementById("btn").removeEventListener("click", sayHello);
```

---

### **4️⃣ Event Object (`event`)**

Every event handler gets an `event` object with details:

```javascript
document.addEventListener("click", function(event) {
    console.log("Clicked on:", event.target);
});
```

---

### **5️⃣ Event Propagation**

- **[[JavaScript Event Bubbling]]:** Event triggers from the **innermost** to the **outermost** element.
  [[JavaScript Event Delegation]]
    
- **[[JavaScript Event Capturing]]:** Event triggers from the **outermost** to the **innermost** element.
    

```javascript
document.getElementById("parent").addEventListener("click", function() {
    console.log("Parent Clicked!");
}, true); // Capturing phase (true)
```

---

### **6️⃣ Prevent Default Behavior**

Some events have default actions (e.g., form submission). Use `preventDefault()` to stop them.

```javascript
document.getElementById("myLink").addEventListener("click", function(event) {
    event.preventDefault(); // Prevents page navigation
});
```

```html
<a href="https://example.com" id="myLink">Click Me</a>
```

---

### **🔹 Key Takeaways**

✅ **Events allow interaction with users**  
✅ Use `addEventListener` for better flexibility  
✅ **Event propagation** affects how events bubble up  
✅ Use `preventDefault()` to stop default behaviors

