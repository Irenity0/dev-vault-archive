JavaScript classes are templates for creating objects. They allow you to define object properties and methods in a structured way using the `class` keyword.

Example:

```javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log(`Hello, my name is ${this.name}.`);
  }
}

const person1 = new Person("Alice", 25);
person1.greet(); // Hello, my name is Alice.
```

They are essentially syntactic sugar over JavaScript’s prototype-based inheritance.