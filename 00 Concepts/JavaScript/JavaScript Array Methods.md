### Common Array Methods

1. **`push()`**: Adds one or more elements to the end of an array.
   ```javascript
   fruits.push('date'); // ['apple', 'blueberry', 'cherry', 'date']
   ```

2. **`pop()`**: Removes the last element from an arr///ay and returns it.
   ```javascript
   let lastFruit = fruits.pop(); // 'date'
   ```

3. **`shift()`**: Removes the first element from an array and returns it.
   ```javascript
   let firstFruit = fruits.shift(); // 'apple'
   ```

4. **`unshift()`**: Adds one or more elements to the beginning of an array.
   ```javascript
   fruits.unshift('apricot'); // ['apricot', 'blueberry', 'cherry']
   ```

5. **`splice()`**: Adds or removes elements from a specific position.
   ```javascript
   fruits.splice(1, 1, 'blackberry', 'coconut'); 
   // Removes 1 element at index 1, then adds 'blackberry' and 'coconut'
   // ['apricot', 'blackberry', 'coconut', 'cherry']
   ```

6. **`slice()`**: Returns a shallow copy of a portion of an array into a new array.
   ```javascript
   let citrus = fruits.slice(1, 3); // ['blackberry', 'coconut']
   ```

7. **`concat()`**: Merges two or more arrays.
   ```javascript
   let moreFruits = fruits.concat(['fig', 'grape']); 
   // ['apricot', 'blackberry', 'coconut', 'cherry', 'fig', 'grape']
   ```

8. **`join()`**: Joins all elements of an array into a string.
   ```javascript
   let fruitString = fruits.join(', '); // 'apricot, blackberry, coconut, cherry'
   ```

9. **`forEach()`**: Executes a function for each element of the array.
   ```javascript
   fruits.forEach(fruit => console.log(fruit));
   ```

10. **`map()`**: Creates a new array with the results of calling a function on every element.
    ```javascript
    let upperFruits = fruits.map(fruit => fruit.toUpperCase());
    // ['APRICOT', 'BLACKBERRY', 'COCONUT', 'CHERRY']
    ```

11. **`filter()`**: Creates a new array with all elements that pass a test.
    ```javascript
    let shortFruits = fruits.filter(fruit => fruit.length <= 6);
    // ['apple', 'banana']
    ```

12. **`find()`**: Returns the first element that satisfies a condition.
    ```javascript
    let foundFruit = fruits.find(fruit => fruit.startsWith('b'));
    // 'banana'
    ```

13. **`reduce()`**: Applies a function against an accumulator and each element to reduce it to a single value.
    ```javascript
    let totalLength = fruits.reduce((total, fruit) => total + fruit.length, 0);
    // Total length of all fruit names
    ```

14. **`sort()`**: Sorts the elements of an array in place.
    ```javascript
    fruits.sort(); // Alphabetical order
    ```

15. **`reverse()`**: Reverses the order of elements in an array.
    ```javascript
    fruits.reverse(); // Reverses the array order
    ```
### Array Properties

- **`length`**: Returns the number of elements in an array.
  ```javascript
  let length = fruits.length; // Number of elements
  ```