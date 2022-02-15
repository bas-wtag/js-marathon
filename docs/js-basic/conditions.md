# Conditions
Conditional Statements control behavior and determine whether or not pieces of code can run.

There are multiple different types of conditionals -
* if statements
* else statements
* else statements
* switch case statements

**if statements**

It is used where if a condition is true it is used to specify execution for a block of code. Example :
```javascript
if(age >= 18) {
    console.log("Adult");
}
```
in this example, Adult will be printed if the age is greater than or equal to 18.

**else statements**

else statements work with a previous if. If a 'if' statement fails then else will work. Otherwise the else block will never be executed. For example:
```javascript
if(age>=18) {
    console.log("Adult");
}
else {
    console.log("Minor");
}
```
In this example, Minor will be printed when the age is less than 18. That mean else will work when the previous 'if' of 'else if' is false.

**else if statements**

This statement specifies a new test if the first condition is false. We cannot write this statement without a previous 'if' statement. For example -
```javascript
if(number > 0) {
    console.log("Positive");
}
else if(number < 0) {
    console.log("Negative");
}
```
In this example, first it will check whether the if statement is true or not. If the 'if' statement is false then it will check for 'else if' statement whether it is true or not. If it is true then Negative will be printed.

**switch case statement**

switch statement evaluates an expression and try to match the expression's value with a case clause and executes statement associated with that case. switch case syntax-
```javascript
switch (expression) {
    case x:
    // code here
    break;
    case y:
    // code here
    break;
    default:
    // code here
}

switch is evaluated once. That means after matching with any case if we don't use break statement then it will print the other staffs associated with other cases before getting a break statement.
For example -

switch (number) {
    case 0: console.log("Zero")
        break;
    case 1: console.log("One");
        break;
    case 2: console.log("Two");
        break;
    case 3: console.log("Three");
    case 4: console.log("Four");
        break;
    default: console.log("Invalid");
}
```
In the previous example if the number is 0, 1 or 2 then it will print Zero, One or Two respectively. But if the number is 3 then it will print Three and Four.