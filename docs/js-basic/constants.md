# Constants

## Note From &nbsp; [hhu-wtag](https://github.com/hhu-wtag)

JavaScript constants are block scoped.
The value of a constants can’t be changed through reassignment.

```js
const number = 42

number = 99 // This would result in a TypeError
```

However arrays and object created using const can be updated and removed.

```js
const obj = {
  name: "Hasib",
}

obj.name = "Adib"

console.log(obj) //{ name: ‘Adib’ }
```

However reassignments of object aren’t allowed like other const variables.

```js
const obj = {
  name: "Hasib",
}
obj = {
  age: 25,
}

console.log(obj) // TypeError
```

> A good coding convention is to write constant variables in all uppercase letters.

> Variables created using const in global context don't become properties of the window object unlike var variable.

> The const declaration creates a read only reference to a value.

### Block Scoping

```js
const PI = 3.1415

console.log(PI)

if (PI === 3.1415) {
  let PI = 100 // This is okay because of block scopping nature of both let and const

  console.log(PI) // PI is now 100

  var PI = 200
  /*
    this will throw an error. because,
    var PI is hoisted to the global context.
    But a const variable with the name PI is
    already there. So it will throw a SyntaxError
  */
}

console.log(PI) // const PI is printed
```
