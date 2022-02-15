# Conditions

**JS Conditions (if-else, switch-case)**

- In computer programming, there may arise situations where you have to run a block of code among more than one alternatives. For this purpose, conditionals can be used.

- In JavaScript we have the following conditional statements:
1) Use `if` to specify a block of code to be executed, if a specified condition is true
2) Use `else` to specify a block of code to be executed, if the same condition is false.
3) Use `else if` to specify a new condition to test, if the first condition is false
4) Use `switch` to specify many alternative blocks of code to be executed

- The difference between using a chain of if blocks and using a chain of if-else if blocks is that after one of the else if blocks is executed, the if-else if-else chain is broken (the conditions were mutually exclusive). Whereas in a chain of if blocks, each if condition is checked (and executed if the condition is true) even if the predecessors are true and the if blocks executed (the conditions are independent).

- If a conditional block is used inside another conditional block, they are called nested conditionals.

- Syntax of the switch block:
```
switch(expression) {
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block
}
```

- The switch expression is evaluated once.
The value of the expression is compared with the values of each case.
If there is a match, the associated block of code is executed.
If there is no match, the `default` code block is executed.

- The `break` statement is optional. If the break statement is encountered, the switch statement ends.
- If the break statement is not used, the cases after the matching case are also executed.
- The `default` clause is also optional.