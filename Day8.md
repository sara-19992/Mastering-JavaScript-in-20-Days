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
  ### Coding Examples
```javascript
//higher order function is printInput
//callback function is print
function printInput(print){

 for(let i = 1; i <= 5 ; i++){
  print('hello '+i)
 }
}

function print(input){
    console.log(input);
}

printInput(print);

```

### Nested function scope
if can't find variable in function local memory go to outer function and search on it.

### CLousre
closure (backpack) pring the data with the function goes, pull the data around the function and push it
where my function saved (call function outside of the function call).  

## Closures, Scope, and Execution Context Exercises

### 134.[Challenge 1](http://csbin.io/closures)
#### My Solution
```javascript
// CHALLENGE 1
function createFunction() {
  
  const log = () => console.log('hello');
  
  return log;

}

// /*** Uncomment these to check your work! ***/
const function1 = createFunction();
function1(); // => should console.log('hello');
```
### 135.[Challenge 2](http://csbin.io/closures)
#### My Solution
```javascript
// CHALLENGE 2
function createFunctionPrinter(input) {
  
  function print(){
    console.log(input);
  }
  
  return print;

}

// /*** Uncomment these to check your work! ***/
const printSample = createFunctionPrinter('sample');
printSample(); // => should console.log('sample');
const printHello = createFunctionPrinter('hello');
printHello(); // => should console.log('hello');
```
### 136.[Challenge 3](http://csbin.io/closures)
#### My Solution
```javascript
// CHALLENGE 3
function addByX(X) {
  
  const addBy = X;
  
  function add (x){
    console.log(addBy + x);
    return addBy + x ;
  }
  
  return add;

}

/*** Uncomment these to check your work! ***/
const addByTwo = addByX(2);
addByTwo(1); // => should return 3
addByTwo(2); // => should return 4
addByTwo(3); // => should return 5

const addByThree = addByX(3);
addByThree(1); // => should return 4
addByThree(2); // => should return 5

const addByFour = addByX(4);
addByFour(4); // => should return 8
addByFour(5); // => should return 9
```
### 137.[Challenge 4](http://csbin.io/closures)
#### My Solution
```javascript
// CHALLENGE 3
function addByX(X) {
  
  const addBy = X;
  
  function add (x){
    console.log(addBy + x);
    return addBy + x ;
  }
  
  return add;

}

/*** Uncomment these to check your work! ***/
const addByTwo = addByX(2);
addByTwo(1); // => should return 3
addByTwo(2); // => should return 4
addByTwo(3); // => should return 5

const addByThree = addByX(3);
addByThree(1); // => should return 4
addByThree(2); // => should return 5

const addByFour = addByX(4);
addByFour(4); // => should return 8
addByFour(5); // => should return 9
```  
