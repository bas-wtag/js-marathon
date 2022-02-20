# Objects

## Note From &nbsp; [hhu-wtag](https://github.com/hhu-wtag)

### Ways to create objects

We can create an instance of the Object prototype to create an empty object.

```js
let obj = new Object()

console.log(obj) // {}
```

We can also use more simpler form of object creation.

```js
let obj = {}

console.log(obj) // {}
```

An object is made up of multiple members. Each member is a **Key-Value** pair. Each **Key-Value** pair is Colon ( `:` ) separated and each member is comma( , ) separated.

```js
const person = {
  name: "Dwight Schrute",
  age: 35,
}
```

So what can we add to objects? LITERALLY everything. Strings, numbers, boolean, functions, arrays, OBJECTS? you name it. Let’s see a more complex object.

```js
const country = {
  name: "Bangladesh",
  currency: "Taka",

  capital: {
    name: "Dhaka",
    population: "21,741,090",
  },

  places_to_visit: ["Lalbagh Fort", "Ahsan Manzil Museum"],

  sayHello: function () {
    console.log("Hello from Bangladesh")
  },
}
```

So as we can see we can have normal key-value member like name and currency. Then we can have objects inside objects like the capital which can have the same variable name as its parents. Then we can have arrays and functions.

### Accessing JS Objects

We can access JS Objects using dot notation or **C-LIKE** array notation.

```js
//Dot Notation
console.log(person.name) // Dwight Schrute
console.log(person.age) // 35

//Array Notation
console.log(person["name"]) //Dwight Schrute
console.log(person["age"]) // 35
```

To access more nested object methods we can use a mixture of dot and array notation.

```js
console.log(country.capital.population) // 21,741,090
```

So what we are doing is tapping into our country object and accessing the capital object member. Then we can access the population member of capital object.

What if we want to access the first item of the array **_places_to_visit_**?

```js
console.log(country.capital.places_to_visit[0]) // Lalbagh Fort
```

We are first accessing the array using dot notation. Then we are accessing the first index by using array notation.

### Mutating JS Objects

We can mutate JS objects on the fly.

```js
person.name = "Micheal Scott"

console.log(person) // { name: "Micheal Scott", age: 35 }
```

We can also add new members on the fly.

```js
person.bye = function () {
  console.log("Bye Bye!")
}

person.bye() // Bye Bye!
```

### Accessing members inside functions in JS Objects

When accessing members of the object itself we have to harness the power of **_this_**. So what is **_this?_** Inside an object, **_this_** refers to the object itself. We can see it in action here.

```js
/*
	let's change the sayHello method of the country
	object.
*/

const country = {
  sayHello: function () {
    console.log("Hello " + this.name)
  },
}

country.sayHello() // Hello Bangladesh
```

Let’s printout the **_this_** itself and see what it’s actually.

```js
const country = {
  sayHello: function () {
    console.log(this)
  },
}

country.sayHello()
/*
{
  name: 'Bangladesh',
  currency: 'Taka',
  capital: {
    name: 'Dhaka',
    population: '21,741,090',
    places_to_visit: [ 'Lalbagh Fort', 'Ahsan Manzil Museum' ],
    printThis: [Function: printThis]
  },
  sayHello: [Function: sayHello]
}
*/
```

```js
const country = {
  sayHello: function () {
    console.log(this)
  },
}

country.sayHello()
/*
{
  name: 'Bangladesh',
  currency: 'Taka',
  capital: {
    name: 'Dhaka',
    population: '21,741,090',
    places_to_visit: [ 'Lalbagh Fort', 'Ahsan Manzil Museum' ],
    printThis: [Function: printThis]
  },
  sayHello: [Function: sayHello]
}
*/
```

So as we can see **_this_** is not a magic item but simply the object itself.

### Shallow Copy vs Deep Copy of Objects in JS

When we copy one object to another using Object.assign() we make a **shallow copy** of the object. Let’s see what that means.

```js
const person = {
  name: "John Doe",
  info: {
    address: "Dhaka",
  },
}

const copiedPerson = Object.assign({}, person)

copiedPerson.name = "Jane Doe"
copiedPerson.info.address = "Cox's Bazar"

console.log(person)
// { name: 'John Doe', info: { address: "Cox's Bazar" } }

console.log(copiedPerson)
// { name: 'Jane Doe', info: { address: "Cox's Bazar" } }
```

We can see that the name member is unaffected in person object because it’s a primitive value. But the address member of the info object is changed. This is because the address object is a reference to an object in heap memory. This is an example of **shallow copy** where some properties are connected with the original variable and some of them are disconnected. A **deep copy** is where every property is disconnected from the original object. An example of **deep copy** is given below.

```js
const person = {
  name: "John Doe",
  info: {
    address: "Dhaka",
  },
}

let jsonPerson = JSON.stringify(person)
const copiedPerson = JSON.parse(jsonPerson)

copiedPerson.name = "Jane Doe"
copiedPerson.info.address = "Cox's Bazar"

console.log(person)
// { name: 'John Doe', info: { address: 'Dhaka' } }

console.log(copiedPerson)
// { name: 'Jane Doe', info: { address: "Cox's Bazar" } }
```
