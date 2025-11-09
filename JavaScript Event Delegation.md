**Event Delegation** is a technique where you **attach a single event listener** to a **parent element**, instead of adding individual listeners to each child element.

📌 **This takes advantage of event bubbling to handle events for dynamically added or multiple child elements.**

---

## **1️⃣ Basic Example of Event Delegation**

### **Scenario: Click Event for Multiple Buttons**

Imagine you have several buttons in a list and want to handle their clicks without attaching individual event listeners to each one.

### **HTML:**

```html
<ul id="buttonList">
    <li><button>Button 1</button></li>
    <li><button>Button 2</button></li>
    <li><button>Button 3</button></li>
</ul>
```

### **JavaScript with Event Delegation:**

```javascript
document.getElementById("buttonList").addEventListener("click", function(event) {
    if (event.target.tagName === "BUTTON") {
        console.log("Button clicked: " + event.target.textContent);
    }
});
```

### **🔹 Expected Output when Clicking a Button:**

```
Button clicked: Button 1
Button clicked: Button 2
Button clicked: Button 3
```

✅ **Why?**
- We attached **one event listener** to the parent element (`#buttonList`).    
- The **event bubbles up** to the parent, and we check if the target is a `<button>` element before logging the message.

---

## **2️⃣ Benefits of Event Delegation**

1. **Efficient Memory Usage**
    - Instead of attaching listeners to each button, we attach **one listener to the parent**.    
    - This **reduces memory usage** when you have many elements.

2. **Handles Dynamically Added Elements**    
    - Event delegation works even if buttons are **added dynamically** to the list after the page loads. Without delegation, new buttons wouldn't have listeners attached.
        

### **Example: Dynamically Added Buttons**

```javascript
let buttonList = document.getElementById("buttonList");

// Add a new button dynamically
let newButton = document.createElement("li");
newButton.innerHTML = "<button>Button 4</button>";
buttonList.appendChild(newButton);
```

- Even **Button 4** will work with the event listener we added to the parent, thanks to **event delegation**.
    

---

## **3️⃣ Real-World Example: Form Validation**

If you have a form with multiple input fields and want to handle validation when the user interacts with any field, event delegation helps reduce repetitive code.

```html
<form id="myForm">
    <input type="text" name="username" placeholder="Username">
    <input type="email" name="email" placeholder="Email">
    <button type="submit">Submit</button>
</form>
```

### **JavaScript with Event Delegation:**

```javascript
document.getElementById("myForm").addEventListener("input", function(event) {
    if (event.target.tagName === "INPUT") {
        console.log(event.target.name + " input changed");
    }
});
```

- Now, each **input field** will be handled by the same event listener on the form.
    

---

## **4️⃣ Key Takeaways**

✅ **Event delegation** lets you handle events on many elements with a single event listener.  
✅ It makes your code more **efficient**, especially with **dynamic elements**.  
✅ **Event bubbling** makes delegation possible, as the event propagates from the child to the parent.