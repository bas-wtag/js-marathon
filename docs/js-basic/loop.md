# Loop

## For

- `For` loops have three statements. The first statement is the initial expression, which is the value/state based on which the loop performs. The second one is conditional expression which is checked before every iteration. And the final one denotes the changes to be performed on the initial expression after every iteration. However, the initial expression can also be stated before the loop begins.
- There is also an enhanced for loop (`for in` and `for of` in JS) which is a bit more efficient than the for loop but less flexible as `for` loop allows us to perform changes as we want which cannot be guaranteed in for-each/enhanced for loop

## While

- `while` loop checks a condition before entering the loop. It executes the instructions only when the condition is `true`. Changes to be performed on the initial condition can be placed anywhere inside the loop.

## Do-While

- `Do while` loops performs some specific action at least once unlike other loops as it does not perform any checks before the first iteration. After the first iteration it works like a traditional `while` loop. The syntax is quite similar to a `while` loop except a `do {}` block precedes the `while {}` block. This loop is useful when the instructions must be performed at least once.

## Break

- The `break` statement is used to stop a block from executing. It halts the execution of the nearest code block. To break outer loops labels can be used as `labels : <statements>` and break operation can be performed on any label by mentioning the label name after break as `break : <label>`. Furthermore, the break statement can also be used in switch statements to stop the execution.

## Continue

- `continue` statement stops the execution of the statements after it but only for one iteration. In a while/do while loop it goes back to the condition and in a for loop it jumps to the update statement.
- `continue` can be used with labels to enable the program to jump to the next iteration of the labeled loop
