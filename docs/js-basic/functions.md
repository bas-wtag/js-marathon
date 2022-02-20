# Functions

## Note From &nbsp; [hhu-wtag](https://github.com/hhu-wtag)

### Function Creation

We can create functions using the function keyword.

```js
function sayHello() {
  console.log("Hello") // Hello
}
```

We can pass parameters to function. They are normally **pass by value**. Meaning any change to those parameters will not affect the variables where they were called from.

```js
let a = 1
let b = 2 //Caller Scope

function changeNumbers(a, b) {
  a = 100
  b = b * 2 //Function Scope
}

changeNumbers(a, b)

console.log(a, b) // Caller Scope. log will be: 1 2
```

But when we pass an object into a function, a modification to that object inside the function scope will modify the object in the caller scope.

```js
const obj = {
  name: "Michael Scott",
}

function changeObj(obj) {
  obj.name = "Dwight Schrute"
}

changeObj(obj)

console.log(obj) // { name: 'Dwight Schrute'}
```

This happens because although the object is passed as a value but the properties of that object are references pointing to some values in heap memory.

### Function Expressions

We can create anonymous functions which doesn’t contain names.

```js
const sayBye = function () {
  console.log("Bye!")
}
sayBye() // Bye!
```

### Function Scope

Variables defined inside a function can’t be accessed from anywhere outside the function. This is because of the local scope of the function.

```js
function someFunction() {
  let a = 10 //Local Scope #1

  function someOtherFunction() {
    let b = 10 //Local Scope #2
  }

  console.log(b)
  //Outer function doesn't have access to inner function
  //Throws an ReferenceError
}

someFunction()
```

### Closures

We know that JS allows nesting functions. The inner function has access to all the members of outer function. But the outer function can’t access the inner functions properties. This sorts of creates an **encapsulation** for the inner function. When used this can be a powerful feature to leverage.

```js
function Employee(_name, age) {
  var _name
  var age

  return {
    setName: function (newName) {
      _name = newName
    },
    setAge: function (newAge) {
      age = newAge
    },
    getAge: function () {
      console.log(age)
    },
    getName: function () {
      console.log(_name)
    },
  }
}

let toby = Employee("Toby", 24)
toby.getAge() // 24
toby.getName() // Toby

toby.setName("Micheal")
toby.getName() // Micheal
```
