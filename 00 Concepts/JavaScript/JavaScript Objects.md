A **JavaScript object** is a collection of key-value pairs, where each key (also called a property) is a string, and the value can be any data type (e.g., string, number, array, function, or even other objects). Objects are a fundamental part of JavaScript and are used to store and organize data.

#### **Object Syntax**:

```javascript
let person = {
  name: "John",
  age: 30,
  greet: function() {
    console.log("Hello, " + this.name);
  }
};
```

- `name` and `age` are properties (keys) of the object.
- `"John"` and `30` are the values of those properties.
- `greet` is a method (a function inside the object).

#### **Accessing Object Properties**:

You can access object properties in two ways:

1. **Dot Notation**:
    
    ```javascript
    console.log(person.name); // "John"
    ```
    
2. **Bracket Notation** (useful when property names have spaces or special characters):
    
    ```javascript
    console.log(person["age"]); // 30
    ```
    

#### **Modifying Object Properties**:

You can change the values of an object's properties:

```javascript
person.name = "Alice"; // Change the name
person["age"] = 25; // Change the age
```

#### **Adding New Properties**:

You can add new properties to an object:

```javascript
person.city = "New York"; // Add a new property
console.log(person.city); // "New York"
```

#### **Example**:

```javascript
let car = {
  brand: "Toyota",
  model: "Corolla",
  year: 2020,
  getInfo: function() {
    return this.brand + " " + this.model + " " + this.year;
  }
};

console.log(car.getInfo()); // "Toyota Corolla 2020"
```

---
### **Deleting Properties**:

```javascript
  delete person.email; // Remove the email property
 ```

----

### **Summary**:

- **JavaScript Object**: A collection of key-value pairs, where the key is a string and the value can be any data type.
- **Methods**: Functions can also be stored as values in an object, making them part of the object.
- **Accessing & Modifying**: You can access properties using dot or bracket notation and modify them directly.