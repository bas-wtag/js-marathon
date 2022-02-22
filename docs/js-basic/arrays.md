## Note from [aaf-wtag](https://github.com/aaf-wtag)

### JS Arrays

### JS Arrays

- An array is an object that can store multiple values at once. The JavaScript Array class is a global object that is used in the construction of arrays.

- Arrays are list-like objects whose prototype has methods to perform traversal and mutation operations. Neither the length of a JavaScript array nor the types of its elements are fixed. Since an array's length can change at any time, and data can be stored at non-contiguous locations in the array, JavaScript arrays are not guaranteed to be dense; this depends on how the programmer chooses to use them.

- Arrays can be created using:
 - `Array literal` [ ] : `const array1 = ["eat", "sleep"];`
 - 'new` keyword :  `const array2 = new Array("eat", "sleep");`

- You can access elements of an array using indices (0, 1, 2 …). JS arrays are zero-indexed.

- The `push()` method adds an element at the end of the array.

- The `unshift()` method adds an element at the beginning of the array.

- You can also add elements or change the elements by accessing the index value. Suppose, an array has two elements. If you try to add an element at index 3 (fourth element), the third element will be undefined.

- You can use the `pop()` method to remove the last element from an array. The pop() method also returns the returned value.

- If you need to remove the first element, you can use the `shift()` method. The shift() method removes the first element and also returns the removed element.

- You can find the length of an element (the number of elements in an array) using the `length` property.

- In JavaScript, an array is an object. And, the indices of arrays are objects keys. Since arrays are objects, the array elements are stored by reference. Hence, when an array value is copied, any change in the copied array will also reflect in the original array.

- *Shallow copy* of an array: top-level elements containing primitive values are copied, but if the array contains nested objects or arrays, those will reference elements in the original array. It can be done:
 - using `spead sequence` : `let shallowCopySpread = [...arrayName];`
 - using `Array.slice()` :  `let shallowCopySlice = arrayName.slice();`
 - using `Array.from()` : `let shallowCopyFrom = Array.from(name);`

- *Deep copy* of an array: Here even nested arrays don’t just reference elements in the original array but instead are also copied. One way to do it is using `JSON.stringify` to convert the array to a JSON string, and then `JSON.parse()` to convert the string back into an array: `let deepCopy = JSON.parse(JSON.stringify(arrayName));`

- Loop over an Array:
```
fruits.forEach(function(item, index, array) {
  console.log(item, index)
})
// Apple 0
// Banana 1
```

- To find the index of an item in the array use the `indexOf()` method: `arrayName.indexOf(value)`

- To remove item(s) from a specific index position: `arrayName.spliced(pos, numberOfItemsToBeRemoved)`