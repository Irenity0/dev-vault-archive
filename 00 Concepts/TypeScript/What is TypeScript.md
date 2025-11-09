**TypeScript** is a **superset of JavaScript** that adds **static typing** to the language. It's designed to help developers catch errors early in the development process and improve code quality.

### Key Features:

- **Static Typing**: Unlike JavaScript, where types are checked at runtime, TypeScript allows you to specify types for variables, function parameters, and return values. This helps prevent type-related errors.
- Example: 
    ```typescript
    let name: string = "Afra";
    let age: number = 25;
    ```

- **Type Inference**: TypeScript can often infer the type of a variable based on its value, so you don't always have to declare types manually.    
- Example:
```typescript
	let message = "Hello";  // TypeScript infers that message is a string
```

- **Compatibility with JavaScript**: TypeScript code is essentially JavaScript, so any valid JavaScript code is also valid TypeScript code. TypeScript just adds optional types and other features.  
- **Compilation to JavaScript**: TypeScript is not understood by browsers directly. It needs to be **compiled** (or transpiled) into regular JavaScript that browsers can execute.
- **Better Tooling**: TypeScript provides enhanced code editor support, such as autocompletion, type-checking, and easier refactoring, which can improve productivity.

### Example of TypeScript code:

```typescript
function greet(name: string): string {
  return `Hello, ${name}`;
}

console.log(greet("Afra"));
```

### Why Use TypeScript?
- **Catching Errors Early**: TypeScript helps catch errors during development instead of runtime, making the debugging process easier.
- **Improved Readability and Maintainability**: With static types, code is easier to understand and maintain, especially in large codebases.
- **Tooling**: IDEs and editors provide better auto-completion, error detection, and refactoring tools for TypeScript.

### Example of Benefits:

In JavaScript, if you accidentally pass the wrong type, you wouldn't catch the error until the code runs:
```javascript
function greet(name) {
  return "Hello " + name;
}

greet(5);  // This will work, but it's not what we intended
```

But in TypeScript, you get an error right away:
```typescript
function greet(name: string): string {
  return "Hello " + name;
}

greet(5);  // TypeScript will show an error: Argument of type 'number' is not assignable to parameter of type 'string'.
```

related links"
- [[Statically Typed Languages]]