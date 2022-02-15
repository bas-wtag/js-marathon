# Variables

**JS Variables**

- A variable is a container (storage area) to hold data in memory. 

- In JavaScript, we use either `var` or `let` keyword to declare variables. However, `var` is used in the older versions of JavaScript and `let` is used from ES6 (ES2015). 

- `var` is function scoped (the variable declared inside a function with var can be used anywhere within a function) and `let` is block scoped ( (variable can be accessed only in the immediate block). So `let` is recommended for usage.

- In JavaScript, it's possible to declare variables in a single statement.
``` let x = 5, y = 6, z = 7; ```

- If you use a variable without initializing it, it will have an undefined value.

- Variable names must start with either a letter, an underscore `_`, or the dollar sign `$`.

- Variable names cannot start with numbers.

- JS is case-sensitive.

- Keywords cannot be used as variable names.

- It's a good practice to give a descriptive variable name. Although, the name should not be too long. Using a camel-case for each new word in the variable starting from the second word makes it more readable.