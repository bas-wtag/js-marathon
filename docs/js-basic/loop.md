# Loop

## Note From &nbsp; [hhu-wtag](https://github.com/hhu-wtag)

### **JS LOOPS**

To do stuff repeatedly we use loops in programming languages. JS offers different sorts of looping mechanisms.

Basic for loop:

```js
for(let i=0; i<10; i++){
  console.log(‘Walking’)
}
```
This loop is similar to C and Javas For loop.


While Loop:

```js
let i=0
while(i < 10){
  console.log(i)
  i += 1
}
```

The key difference between while and loop is that while only takes the condition. The initialization and increment expressions are done separately.

Do while Loop:

```js
let n = 0

do{
  console.log(n);
  n += 1
}while(n < 10)
```

One main difference between do while and for/while is that, do while runs at least one time no matter what the value of condition turns out to be.

Break statement


When used a break statement will terminate the innermost enclosing while, do-while for or switch statement.

```js
for(let i =0 ; i<10; i++){
  if( i === 5 ){
    console.log("Broke out of the loop half way");
    break;
  }

  console.log(i);
}
```

Continue Statement

If we want to skip some iteration step we can continue to do so. When continue is encountered inside a loop, the loop will go to the next iteration without finishing the last iteration.

```js
for(let i = 0 ; i<10; i++){
  if( i%2 === 0 ) {
    continue; //if the value of i is even, skip this iteration
  }

  console.log(i);
}
```

The above code will only print the odd values of i.
