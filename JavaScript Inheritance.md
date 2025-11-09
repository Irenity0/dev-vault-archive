Inheritance in JavaScript allows one class or object to inherit properties and methods from another. This helps in code reuse and organization.

### Example (Class-based Inheritance):

```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }

  speak() {
    console.log(`${this.name} makes a sound.`);
  }
}

class Dog extends Animal {
  speak() {
    console.log(`${this.name} barks.`);
  }
}

const dog = new Dog("Buddy");
dog.speak(); // Buddy barks.
```

Here, `Dog` inherits from `Animal`, but overrides the `speak` method.