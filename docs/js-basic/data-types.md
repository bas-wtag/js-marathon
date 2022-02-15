# Data Types
* JavaScript types are dynamic
* There are mainly two types of JS Data, primitive values and objects.
* Primitive types are Boolean, Null, Undefined, Number, BigInt, String, Symbol etc.
* Boolean types can have two values, true and false.
* Null means empty or unknown values.
* The Undefined data type represents value that is not assigned. For example- if a variable is declared but not assigned then the value of that variable will be undefined.
* Number provides integer and floating numbers. A number type can be +Infinity, -Infinity, NaN (not a number). Number type can only represent number from (-2^53 to 2^53 - 1).
* BigInt number can contain large number. BigInt number is created by appending n to the end of an integer.
* JS String is used to store text. String value can be declared using single quotes, double quotes and backticks.
* Symbol is an immutable primitive value that is unique.
* Object is a complex type by how we can store collections of data within a single variable.

**Call by Value**

Let 'a' is variable and a = 5. If we copy the value of 'a' to another variable 'b' that is b = a then b will point to a new location in memory, containing the same data as 'a'.

This approach is called call by value where 'a' and 'b' become the same by copying the value but in different spots in the memory.

**Call by Reference**

Lets 'a' is variable and an object stored in 'a'. The variable 'a' stores the location or the address of the object. If we try to copy 'a' to another variable 'b' by assigning b = a then no new object will be created. Variables 'b' instead of pointing to a new location in the memory, points to the same location of 'a'.

This approach is called call by reference where 'a' and 'b' both refer to the same object.