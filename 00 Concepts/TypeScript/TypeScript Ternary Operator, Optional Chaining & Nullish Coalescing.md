### Ternary Operator (`? :`)
A shorthand way to write `if-else` statements.
Syntax:

```typescript
condition ? valueIfTrue : valueIfFalse
````

Example:

```typescript
let age = 18;
let message = age >= 18 ? "Adult" : "Minor";
console.log(message); // "Adult"
```

> Think of it as a quick "if-else" in one line.

---

### Optional Chaining (`?.`)
Safely access deeply nested properties without causing an error if an intermediate property is `null` or `undefined`.
Syntax:

```typescript
object?.property
object?.method?.()
```

Example:

```typescript
let user = { name: "Afra", address: { city: "Paris" } };

console.log(user.address?.city);    // "Paris"
console.log(user.contact?.phone);   // undefined (no error)
```

> Stops checking if the part before `?.` is `null` or `undefined`.

---

### Nullish Coalescing Operator (`??`)
Provides a default value **only if** the left-hand side is `null` or `undefined` (not for `0`, `false`, or `''`).
Syntax:

```typescript
value ?? defaultValue
```

Example:

```typescript
let userInput = null;
let name = userInput ?? "Guest";
console.log(name); // "Guest"
```

Another example:

```typescript
let count = 0;
let result = count ?? 10;
console.log(result); // 0 (because 0 is not null or undefined)
```

> Only replaces `null` or `undefined`, not falsy values like `0` or `false`.