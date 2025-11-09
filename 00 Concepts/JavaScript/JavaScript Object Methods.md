### Object Methods

- **`Object.keys()`**: Returns an array of the object’s property names.
  ```javascript
  let keys = Object.keys(person); // ['name', 'age', 'greet']
  ```

- **`Object.values()`**: Returns an array of the object’s property values.
  ```javascript
  let values = Object.values(person); // ['Alice', 30, function]
  ```

- **`Object.entries()`**: Returns an array of the object’s [key, value] pairs.
  ```javascript
  let entries = Object.entries(person); // [['name', 'Alice'], ['age', 30], ['greet', function]]
  ```

- **`Object.assign()`**: Copies properties from one or more source objects to a target object.
  ```javascript
  let person = { name: 'Alice' };
  let additionalInfo = { age: 30, job: 'Engineer' };
  Object.assign(person, additionalInfo);
  // person now has name, age, and job properties
  ```
