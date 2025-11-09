## 1. Primitives (Immutable)

These are the basic data types in TypeScript (same as JavaScript but with **type annotations**).

- **Number**: Represents all numbers (integers, floats).

```typescript   
let age: number = 8;
```   

- **String**: Represents sequences of characters.

```typescript
let name: string = "Afra";
```
  
- **Boolean**: Represents `true` or `false`.
  
```typescript   
let isStudent: boolean = true;
```
  
- **Undefined**: A variable that has been declared but not assigned.

```typescript 
let x: undefined = undefined;
```
  
- **Null**: Explicitly represents "no value".
   
```typescript
let user: null = null;
```
  
- **Symbol**: Unique and immutable identifier.
   
```typescript
let sym: symbol = Symbol('unique');
```
  
- **BigInt**: Very large integers.

```typescript
let big: bigint = 1234567890123456789012345678901234567890n;
```

  ---
## 2. Non-primitives (Mutable)

These types are more complex and can hold collections or structures.

- **Object**: Collection of key-value pairs.

```typescript
let person: { name: string; age: number } = { name: "Afra", age: 30 };
```
  
- **Array**: Ordered list of elements.
  
```typescript
let fruits: string[] = ["apple", "banana", "cherry"];
// OR
let numbers: Array<number> = [1, 2, 3];
```
  
- **Tuple**: Fixed-length array with known types at each position.
  
```typescript
let userInfo: [string, number] = ["Afra", 30];
```
  
- **Enum**: Named constants for better readability.
  
```typescript
enum Color { Red, Green, Blue }
let c: Color = Color.Green;
```
  
- **Function**: Function types can be explicitly typed.
 
```typescript
function greet(name: string): void {
	console.log(`Hello, ${name}!`);
}
```

- **Any**: Can be **any** type (use carefully!).
  
```typescript
let randomValue: any = 10;
randomValue = "Now a string";
```
  
- **Unknown**: Similar to `any`, but safer (forces type-checking before use).
  
    ```typescript
    let value: unknown = "Hello";
    ```
   

#### 3. Special Types

- **Void**: For functions that **do not return** anything.

```typescript
function logMessage(): void {
	console.log("Logging...");
	}
```

- **Never**: For functions that **never return** (e.g., error functions).
  
```typescript
function throwError(message: string): never {
    throw new Error(message);
}
```
  

#### **Summary**:

- **Primitives**: Same basic types as JavaScript but with strict typing.  
- **Non-primitives**: Arrays, Objects, Tuples, Enums, Functions.
- **Special Types**: `any`, `unknown`, `void`, `never`.