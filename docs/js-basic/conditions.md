# Conditions

## Note From &nbsp; [hhu-wtag](https://github.com/hhu-wtag)

### **JS CONDITIONS**

Like other popular languages JS has conditional statements like if else if else and switch statements.

```js
let age = 10

if(age < 10){
  console.log("Child");
}else{
  console.log("Young")
}
```

Conditions are expressions that evaluate to be either truthy or falsy. On the above code age will be evaluated to either truthy or falsy.

For more complex conditions where there is no binary choice, we can use else if.

```js
let age = 10

if(age < 10){
  console.log("Kid");
}else if(age >=10 && age < 30){
  console.log("Young");
}else{
  console.log("Adult");
}
```

If we have a lot of options to choose from, use of if elseif can be repetitive and hard to read. To increase the code readability we can use switch statements

```js
let country = "Bangladesh"

switch (country) {
  case "Bangladesh":
    console.log("Bangladeshi");
    break;
  case "India":
    console.log("Indian");
    break;

  case "USA":
    console.log("American");
    break;
      
  case "Australia":
    console.log("Australian");
    break;

  default:
    console.log("Can't recognize country");
    break;
}
```

We can also use ternary operators in JS to write if else statements.
Let’s checkout the below code block

```js
let country = "Bangladesh"

let money = (country === "Bangladesh") ? "Taka" : "Dollar"
```


The variable money is assigned a statement that has three parts. On the left side of the ? mark is the condition we want to evaluate. On the right side we have two statements separated by Colon(:). If the result of the condition is truthy then the left segment of the colon will be resolved. Else the right side will be resolved.  To understand better we can write the above code in a normal if else statement like this.

```js
let country = "Bangladesh"

if(country === "Bangladesh"){
    money = "Taka"
}else{
    money = "Dollar"
}

console.log(money);
```