# Arrays

## Note From &nbsp; [hhu-wtag](https://github.com/hhu-wtag)

### Create an Array

```js
let names = ["John Doe", "Jim Morrison"]

console.log(names) // ["John Doe", "Jim Morrison"]
```

Unlike C or Java we can have different kinds of items inside an array

```js
let info = [
  "John Doe",
  10,
  {
    type: "Object",
  },
]

console.log(info) // [ 'John Doe', 10, { type: 'Object' } ]
```

### Accessing Array elements

We can access array elements using array notation similar to C or Java

```js
console.log(info[0], info[1]) // John Doe 10
```

We can also use Array.prototype.at() function to access certain array element. It also accepts negative values meaning negative integers count back from the last item.

```js
console.log(info.at(-1)) // { type: 'Object' }
```

### Iteration in Array

We can use various ES6 methods to iterate over an array. Most popular one is Array.map()

```js
let countries = ["Bangladesh", "India", "Bhutan"]

countries.map((country) => {
  console.log(country)
})
/*
Bangladesh
India
Bhutan
*/
```

It iterates over each element in the Array and fires a **CallBack** **Function.**

We can also use forEach method to loop over an array.

```js
countries.forEach((country) => {
  console.log(country)
})
/*
Bangladesh
India
Bhutan
*/
```

Wait. They look exactly the same and works the same!

Actually not true. The main difference between Array.map() and Array.forEach() is that Array.map() creates a copy of the main array and return an array. Whereas forEach() works on the original array and doesn’t return anything.

```js
let result = countries.forEach((country) => {
  return country
})

console.log(result) // undefined
```

But if we try the same thing with map() we can see the difference.
