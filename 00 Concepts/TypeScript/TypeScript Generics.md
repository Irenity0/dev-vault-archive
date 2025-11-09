### Generics

Generics allow you to create reusable components (functions, classes, types) that can work with **any data type**.

Syntax:
```typescript
function identity<Type>(value: Type): Type {
  return value;
}
````

Example:

```typescript
let output1 = identity<string>("Afra"); // Type is string
let output2 = identity<number>(42);     // Type is number
```

> Generics make your code more flexible and type-safe.

---

### Generic Function (Simpler Syntax)

You can shorten `<Type>` to `<T>` (common practice):

```typescript
function identity<T>(value: T): T {
  return value;
}
```

---

### Generic with Arrays

Example:

```typescript
function getFirstElement<T>(arr: T[]): T {
  return arr[0];
}

const first = getFirstElement<number>([10, 20, 30]);
console.log(first); // 10
```

---

### Generic Interfaces

You can also create generic interfaces:

```typescript
interface Box<T> {
  content: T;
}

const box: Box<string> = { content: "Hello" };
```

---

### Generic Constraints (`extends`)

You can **limit** what types are allowed using `extends`.

Example:

```typescript
function getLength<T extends { length: number }>(item: T): number {
  return item.length;
}

console.log(getLength("Afra"));   // OK
console.log(getLength([1, 2, 3])); // OK
```

> Here, `T` must have a `length` property.

---

### Summary

| Concept            | Purpose                              | Syntax Example                   |
| ------------------ | ------------------------------------ | -------------------------------- |
| Generics           | Work with any type in a reusable way | `function<T>(value: T)`          |
| Generic Constraint | Limit which types can be used        | `<T extends { length: number }>` |
