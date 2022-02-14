# Variables

## Note From &nbsp; [hhu-wtag](https://github.com/hhu-wtag)

### **JS VARIABLES**

We can declare variables in JavaScript in 3 ways. `var`, `let` and `const`.
When `var` is used to declare a variable,
It has the scope of its current execution context and closures. Let’s study this code block.

```js
function foo() {
  var a = 10;
  
  console.log(a); //a is in the scope of foo

  function bar() {
    console.log(a); //bar encloses variable a.
  }
    
  bar()
}

foo()
```

`var a` has the scope of the function `foo` and the functions that encloses it. 


### **Something called Hoisting:**

First let’s check out this block of code.

```js
console.log(foo);
var foo = 10
console.log(foo);
```
The expected behavior of the execution of the above code is that it’s gonna throw a ReferenceError because we are trying to print a value of a variable that doesn’t exist.
But the execution of the above code block will result in: `undefined 10`.

This happens because of something called **HOISTING**. What hoisting is that JavaScript moves all the variable declarations to the top of function scope or global scope. Any variable declared with var is by default undefined. So when we write code like the above code block what it is actually is, 

```js
var foo; //undefined by default
console.log(foo); //spits out undefined
foo = 10
console.log(foo); //spits out 10
```

But when we use `let`/`const` instead of `var`, we get `ReferenceError`. Because for `let` which is lexically scoped which when declared without any values stays uninitialized. 
