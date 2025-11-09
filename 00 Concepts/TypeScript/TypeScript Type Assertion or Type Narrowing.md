### Type Assertion (`as` or `<type>`)

Tells TypeScript to treat a value as a specific type. It doesn't change the actual value, only how TypeScript understands it.

Syntax:
```typescript
value as Type
// or
<Type>value
````

Example:

```typescript
let someValue: any = "Hello World";
let strLength: number = (someValue as string).length;
console.log(strLength); // 11
```

> Use assertions when you know more about the type than TypeScript does.

Note: Avoid overusing type assertions — they can hide real type mistakes!

---

### Type Narrowing

Refines the type of a variable based on checks like `typeof`, `instanceof`, `in`, or custom type guards.

Example using `typeof`:

```typescript
function printId(id: number | string) {
  if (typeof id === "string") {
    console.log(id.toUpperCase()); // id is treated as string here
  } else {
    console.log(id); // id is number here
  }
}
```

Example using `in`:

```typescript
type Admin = { role: string };
type User = { username: string };

function isAdmin(account: Admin | User) {
  if ("role" in account) {
    console.log("Admin:", account.role);
  } else {
    console.log("User:", account.username);
  }
}
```

Example using `instanceof`:

```typescript
class Car {
  drive() { console.log("Driving"); }
}

class Bike {
  ride() { console.log("Riding"); }
}

function move(vehicle: Car | Bike) {
  if (vehicle instanceof Car) {
    vehicle.drive();
  } else {
    vehicle.ride();
  }
}
```

> Type narrowing helps TypeScript understand exactly which type you're working with at different points in the code.

---

### Summary

| Concept        | Purpose                                             | Syntax Example                      |
| -------------- | --------------------------------------------------- | ----------------------------------- |
| Type Assertion | Tell TypeScript to treat a value as a specific type | `value as Type`                     |
| Type Narrowing | Refine the type based on conditions                 | `typeof`, `in`, `instanceof` checks |
