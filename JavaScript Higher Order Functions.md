A ****higher-order function**** is a function that does one of the following:

- Takes another function as an argument.
- Returns another function as its result.

Higher-order functions help make your code more reusable and modular by allowing you to work with functions like any other value.

```javascript
function fun() {     
	console.log("Hello, World!"); 
	} 
function fun2(action) {     
	action();     
	action(); 
	}  
fun2(fun);
```

****In this example****

- fun2 is a higher-order function because it takes another function (action) as an argument.
- It calls the action function twice.