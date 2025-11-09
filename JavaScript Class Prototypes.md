Prototypes in JavaScript are the mechanism by which objects inherit properties and methods from other objects. Every JavaScript object has an internal link to another object called its **prototype**.

Example:

```javascript
function Person(name) {
  this.name = name;
}

Person.prototype.greet = function () {
  console.log(`Hello, my name is ${this.name}.`);
};

const person1 = new Person("Alice");
person1.greet(); // Hello, my name is Alice.
```

Here, `greet` is added to `Person.prototype`, so all instances of `Person` can use it without duplicating the function in memory.