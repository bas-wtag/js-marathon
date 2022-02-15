# Loop

Loops can execute a block of code a number of times. It is handy if we want to do the same thing again and again. Say for example, if we want to print "Hello World" for 10 times then what would be the solution ? If we think about this solution without loop then we need to write "Hello World" 10 times. But with the help of loop we can write "Hello World" once and execute 10 times.

**for loop**

for is one of the loop. for loop has the following syntax:

```javascript
for (initialization; condition; increment/decrement) {
// code block to be executed
}
```
initialization part is executed once before the execution of the code block. Its initialize the loop variable.
condition part defines the condition for executing the code block and when to stop.
increment/decrement part is executed every time after the code block has been executed.
For example if we want to print "Hello World" 10 times then the code will be:

```javascript
for(let i=0; i<10; i++) {
console.log("Hello World");
}
```

**for-in loop**

for-in statement loops through the properties of an object. Syntax-
```javascript
for (key in object) {
// code block to be executed
}
```

**for of loop**

for-of statement loops through the values of an iterable object. We can use for-of loop in array, object, map and more. Syntax of for-of loop -
```javascript
for (variable of iterable) {
// code block to be executed
}
```
where, in variable, the next property is assigned and iterable is an object that has iterable properties.

Example:
```javascript
const str = ["Hello", "Welldev"];

for (let x of str) {
console.log(x);
}
```

**while loop**

The while statement loops through a block of code as long as a specified condition is true. Syntax-
```javascript
while(condition) {
// code block to be executed
}
```
So every time it will first check the condition and if it is true then execute the block of code.

**do while loop**

The do while loop also works like while loop. But there are some difference between while and do while. Syntax-
```javascript
do {
// code block to be executed
}
while (condition);
```

so in this loop, for the very first time it will execute the block of code without checking any condition. But from the next time it will check the condition and decide whether to execute the block of code or not.

**Break Statement**

break statement is used to stop any loop. That means it "jumps out" of a loop.

For Example-
```javascript
for( let i=1; i<=10; i++) {
    if(i == 5) break;
    console.log(i);
}
```

In the previous example, it will print 1, 2, 3 and 4. But when i will be equal 5, the if statement will be true and break statement will work. So it will jumps out from the loop and wont print anything else.

**Continue Statement**

The continue statement is used to skip or jumps over one iteration in loop. For example-
```javascript
for( let i=1; i<=10; i++) {
    if(i == 5) continue;

    console.log(i);
}
```
In this example, it will first print 1 to 4. When 'i' will become 5 it will skip console.log(i) statement and wont print 5. But after that it will again print 6-10.