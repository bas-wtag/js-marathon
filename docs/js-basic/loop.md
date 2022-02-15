# Loop

**JS Loop (for, while, do-while, break, continue)**

- In programming, loops are used to repeat a block of code.

- The syntax of the `for` loop is:
```
for (initialExpression; condition; updateExpression) {
    // for loop body
}
```
Here,
1) The *initialExpression* initializes and/or declares variables and executes only once.
2) The *condition* is evaluated.
    -- If the condition is false, the for loop is terminated.
    -- If the condition is true, the block of code inside of the for loop is executed.
3) The *updateExpression* updates the value of initialExpression when the condition is true.
4) The condition is evaluated again. This process continues until the condition is false.

- The JavaScript `for in` statement loops through the properties of an Object:
```
for (key in object) {
  // code block to be executed
}
```
```
for (variable in array) {
  code
}
```

- The JavaScript `for of` statement loops through the values of an iterable object. It lets you loop over iterable data structures such as Arrays, Strings, Maps, NodeLists, and more:
```
for (variable of iterable) {
  // code block to be executed
}
```
Here,
1) variable - For every iteration the value of the next property is assigned to the variable. Variable can be declared with `const`, `let`, or `var`.
2) iterable - An object that has iterable properties.

- The syntax of the `while` loop is:
```
while (condition) {
    // body of loop
}
```
Here,
1) A while loop evaluates the *condition* inside the parenthesis ().
2) If the condition evaluates to true, the *code inside the while loop* is executed.
3) The condition is evaluated again.
4) This process continues until the condition is false.
5) When the condition evaluates to false, the loop stops.

- The syntax of the `do-while` loop is:
```
do {
    // body of loop
} while(condition)
```
Here,
1) The *body of the loop* is executed at first. Then the *condition* is evaluated.
2) If the condition evaluates to true, the body of the loop inside the do statement is executed again.
3) The condition is evaluated once again.
4) If the condition evaluates to true, the body of the loop inside the do statement is executed again.
5) This process continues until the condition evaluates to false. Then the loop stops.

- Infinite loop: If the test condition in a for loop is always true, it runs forever (until memory is full).

- A `for` loop is usually used when the number of iterations is known. Whereas, `while` and `do-while` loops are usually used when the number of iterations are unknown.

- When a loop is used inside another loop block, the result is a nested loop.

- The `break` statement is used to terminate the loop immediately when it is encountered.

- When `break` is used inside of two nested loops, break terminates the inner loop.

- The `continue` statement is used to skip the current iteration of the loop and the control flow of the program goes to the next iteration.

- When `continue` is used inside of two nested loops, continue skips the current iteration of the inner loop.
