# Data Types

## Note From &nbsp; [hhu-wtag](https://github.com/hhu-wtag)

In JS, primitives such as boolean, numbers, strings, BigInt are allocated memory during compilation and their size is fixed. They are allocated data in stack data structure.

For functions and objects JS stores these in the heap data structure. No fixed sizes are allocated for them. So their sizes can be changed during runtime.

During assignment operation,
JS Engine creates a copy of that value and assigns it to the new variable.

```js
let age = 24
let newAge = age

newAge = newAge + 1
console.log(age) // this would result in 24``
```

### Parameter Passing

This is similar to assignments. JS will create a copy of the variables and their state will be destroyed after the function scope ends.

```js
let age = 20
let e_name = "John Doe"

function changeStuff(ageParam, nameParam) {
  ageParam = ageParam + 10
  nameParam = "Edward Norton"
}

changeStuff(age, e_name)
console.log(age, e_name) // John Doe 20
```

We changed the values of `age` and `e_name` but their change didn’t affect the original variables.

But the most interesting thing happens when we do this.

```js
let e_name = "Micheal Scott"
let info = {
  age: 45,
  position: "Manager",
}

function changeStuff(e_name, info) {
  e_name = "Andy Bernard"

  info.age = 35
}

changeStuff(e_name, info)
console.log(e_name, info) // Micheal Scott {age: 35, position: ‘Manager’}
```

`e_name` didn’t change but the `age` property of the `info` object changed from 45 to 35. Hmm. Why?

This is because, although the parameters are passed by value, the properties of the objects are references. So when we tap into the object itself and mutate its properties the changes are persistent. To make sure this is the actual issue, what if we do this,

```js
let e_name = "Micheal Scott"
let info = {
  age: 45,
  position: "Manager",
}

function changeStuff(e_name, info) {
  e_name = "Andy Bernard"

  info = {
    age: 10,
    position: "None",
  }
}

changeStuff(e_name, info)
console.log(e_name, info) // Micheal Scott { age: 45, position: 'Manager' }
```

This time we are reassigning the info object into a new object but the original object is unchanged. **So what this implies is that, although all the parameters passed to a function are called by value, the properties of objects passed(if any object passing is involved) are actually references and mutating them inside the function scope would mutate the object that was passed from the caller scope.**
