## Advanced Scope

### Lexical scope vs Dynamic scope
**Lexical scope** is scope of a variables or functions based on where it is defined in the code.
**Dynamic scope** is scope where functions is called. 

### Blcok scope
scope done with blocks by curly braces

### Hoisting
JS move variable and function declaration to the top of scope before executing.  
1. hoisting sometimes bad (variable declaration) / sometimes useful (function declaration).
2. function hoisting is useful to put the executable code at the top (call function before their declaration).
3. function expression not hoisted.
4. variable hoisting can use them before declare and assigned to undefined (var, const).
5. let is hoist, not initialize can't touch it like var and const.

