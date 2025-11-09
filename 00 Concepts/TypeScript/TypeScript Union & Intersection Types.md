### Union Types (`|`)

Union types allow a variable to hold more than one possible type.
Syntax: `type1 | type2`

Example:
```typescript
let value: string | number;
value = "Afra"; // valid
value = 42;     // also valid
````

You can also use unions in function parameters:

```typescript
function printId(id: string | number) {
  console.log(id);
}
```

> Think of unions like "either this OR that."

---

### Intersection Types (`&`)

Intersection types combine multiple types into one, meaning the value must satisfy all types.
Syntax: `type1 & type2`
Example:

```typescript
type Person = { name: string };
type Employee = { employeeId: number };

let worker: Person & Employee = {
  name: "Afra",
  employeeId: 1234
};
```

You can also use intersections in function parameters:

```typescript
function display(worker: Person & Employee) {
  console.log(worker.name, worker.employeeId);
}
```

> Think of intersections like "this AND that together."

---

### Summary

|Concept|Meaning|Syntax Example|
|---|---|---|
|Union|One type OR another|`string|
|Intersection|Must have properties from both types|`Person & Employee`|
