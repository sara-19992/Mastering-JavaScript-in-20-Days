## JavaScript Principles

### Thread of execution
- line by line execution the code
- JS single execution one line executed at once time

### Memory
- save the data to use it.
- save function code in memory to use it by call the function name with ().

### Execution Context
to run code of a function when call it by name & ().

### Call Stack
JS tracking a function running by call stack (global stack), push the run function to stack and when finish execute this function pop it from stack (delete it), the top of stack represent the function running now.

### Function
- when function execute create a new local memory (variable environment/state).
- when finish execute delete the local memory.
- make function reusable generalization (don't repeat yourself).
- function in JS is object (what do in object doing with function, assign it to variable, return it from function).
- arrow function is shorthand way to save function added in ES6 (make code pretty, legibility).
  
### Heigher Order Function
- higher order function means function take in a function.
- callback function means the function we insert it.

### Nested function scope
if can't find variable in function local memory go to outer function and search on it.

### CLousre
closure (backpack) pring the data with the function goes, pull the data around the function and push it
where my function saved.  

  
