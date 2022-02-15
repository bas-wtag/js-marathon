# Variables
**JS Variable**

There are 3 kinds of variable:

i. var
ii. let
iii. const

**Var**:
1. When need to store aa variable use var
2. Unassigned variable can be set with var.
3. Result can be store using var.
4. Var can not be binded in block scope.
5. Variable defined with var are hoisted to the top, it set value = undefined, so var can be initialized at any where.
    
 Example:
        "name = "abcd";
        var name;
        console.log(name); //output : abcd
"
**Let**:

1. Variables defined with let can not be redeclared.
2. let must bee declared before use.
3. let works in block scope.
4. Redeclaring a variable with var impose problems, to avoid this problems let is introduced.
5. Redeclaring a variable using let inside a block scope will not redeclare the variable outside the block.
6. let hoisted at top of the block but do not initialize anything, because it doe not set any value to the memory.

**Const**:

1. const can re assigned

 Example:
        "const a=5;
         a=7; // This will give error."
2. Const need to use when declare a new array, object, function or RegEx
3. const defines a constant reference to a value.
4. Elements of array, object can be changed or add new element.
 Example:
"const a=[1,2,3,4];
a[0]=0; // array a will be [0,2,3,4]
"
5.Block scope works with const as same as let.
