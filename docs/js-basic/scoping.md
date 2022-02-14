# Scoping

- Scopes can either be global or local.
- Variables declared on the top of the file or not within a pair of braces or functions are considered global. They can be accessed from anywhere.
- Variables declared inside a function can be accessed only from that function. The keyword `var` generally declares a variable that is function scoped.
- Variables declared using the `let` keyword is bracket scoped. The variable is accessible only from that bracket. However, declaring a variable using `let` outside of any function/braces can be considered as a global variable.
- Variables that are redeclared within a different scope can take precedence over the global one if accessed from the same environment.
- Assigning values to a non declared variable automatically moves it to the top of their scope. For instance, if this occurs in a function scope, then the scoping will be moved to global.
- Items from a child scope can access elements of its parent scope.
