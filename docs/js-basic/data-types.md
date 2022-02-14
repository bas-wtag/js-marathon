# Data Types

**JS Data types (Call by value, call by reference)**

- primitive data types: `Number`, `String`, `Boolean`, `Undefined` (a data type whose variable is not initialized), `Null`, `Symbol` (data type whose instances are immutable, unique).
- non-primitive data types: `Arrays`, `Objects`
- Call by value: When a variable is passed into a function if the variable is of primitive data type, a copy of it is created inside the function. Since the variable is a copy if it is changed within the function, the original variable that is passed remains unaffected.
- Call by reference: In the case of a variable of a non-primitive data type, the variable is passed to the function as its reference (address to the memory location). Since both the variable in and out of the function points to the same address, any changes in the value of the parameter in the function would also change the original variable's value.
- In order to make the non-primitive values to behave like being called by value in a function, a copy of that non-primitive type can be created explicitly and the copy can be updated keeping the original variable unchanged, as the copy now points to a different memory location.
- For arrays, we can use the higher order function map, as it returns a new array (object reference).
 