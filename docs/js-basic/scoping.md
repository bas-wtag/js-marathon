# Scoping

## Note From &nbsp; [hhu-wtag](https://github.com/hhu-wtag)

### **JS Scope**

Scope is the accessibility of variables, functions and objects in some particular part of a code.

There are two types of scope in JS.
- Global Scope
- Local Scope

When we write code in a document we are in global scope.
There is only one global scope throughout a JS document. 

```js
var e_name = "Joey"

console.log(e_name) // logs Joey

function howYouDoin(){
  console.log(e_name) // e_name is accessible inside this function and everywhere else
}

howYouDoin()
```

When we declare variables using var they are added to the global object model hence they are always in global scope.

Variables declared inside functions have local scopes.
Variables declared inside a function cannot be accessed outside of its scope.

```js
function foo(){
  const PI = 3.1415
}

console.log(PI);
```



Variables having the same name can be used inside different functions.

```js
function foo(){
  let eName = "Micheal Scott" // local scope #1

  function bar(){
      // let eName = "Pam Beesely" // local scope #2
      console.log(eName); // this eName is different than the outer eName
  }

  console.log(eName);
  bar()
}

foo()
```



### **Scope in Block Statements**

If/switch or while/for, unlike functions don’t create a new scope. 

```js
if(true){	
  var name = “John Doe” // name is in the global context
}
```

From ES6, we now can replace var with let and const which work a tad bit differently.
Unlike var, let and const will create a local scope inside block statements and they won’t be accessible outside of the block statement.

```js
if(true){
  var _name = "Doe" // has global scope
  let age = 10 // has local scope
  const PI = 3.1415
}

console.log(_name) // spits "Doe"
console.log(age) // ReferenceError
console.log(PI) // ReferenceError
```
