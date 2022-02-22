# Functions

### JS Functions

- A function in JavaScript is similar to a procedure—a set of statements that performs a task or calculates a value, but for a procedure to qualify as a function, it should take some input and return an output where there is some obvious relationship between the input and the output. To use a function, you must define it somewhere in the scope from which you wish to call it.

- A function definition (also called a function declaration, or function statement) consists of the function keyword, followed by:
 - The name of the function.
 - A list of parameters to the function, enclosed in parentheses and separated by commas.
 - The JavaScript statements that define the function, enclosed in curly brackets, {...}.
 - The `return` statement can be used to return the value to a function call.

- functions can also be created by a function expression. Such a function can be anonymous; it does not have to have a name (similar to lambda functions in Python).
`var anon = function (a, b) { return a + b };`

```
// we could write the above example as:
var anon = (a, b) => a + b;
// or
var anon = (a, b) => { return a + b };
// if we only have one parameter we can loose the parentheses
var anon = a => a;
// and without parameters
var () => {} // noop

// this looks pretty nice when you change something like:
[1,2,3,4].filter(function (value) {return value % 2 === 0});
// to:
[1,2,3,4].filter(value => value % 2 === 0);
```

- Function expressions are convenient when passing a function as an argument to another function. The following example shows a map function that should receive a function as first argument and an array as second argument:
```
function map(f, a) {
  let result = []; // Create a new Array
  let i; // Declare variable
  for (i = 0; i != a.length; i++)
    result[i] = f(a[i]);
  return result;
}
const f = function(x) {
   return x * x * x;
}
let numbers = [0, 1, 2, 5, 10];
let cube = map(f,numbers);
console.log(cube);
```

- Functions must be in scope when they are called, but the function declaration can be hoisted (appear below the call in the code). The scope of a function is the function in which it is declared (or the entire program, if it is declared at the top level).