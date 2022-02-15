# Scoping

**JS Scoping**

- Scope refers to the availability of variables and functions in certain parts of the code.

- In JavaScript, a variable has three types of scope: Global Scope, Local Scope, Block Scope.

- A variable declared at the top of a program or outside of a function is considered a global scope variable. It means the variable can be used anywhere in the program.

- The value of a global variable can be changed inside a function.

- In JavaScript, a variable can also be used without declaring it. If a variable is used without declaring it, that variable automatically becomes a global variable (unless "strict mode" is enabled).

- A variable can also have a local scope, i.e it can only be accessed within a function.

- For block scope, variables declared inside a { } block cannot be accessed from outside the block. `const` and `let` have block scopes.

-  Variables declared with the `var` keyword can NOT have block scope and can be accessed from outside the block. They have function scope/ local scope. 
