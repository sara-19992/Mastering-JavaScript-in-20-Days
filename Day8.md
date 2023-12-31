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
      print('hello '+i);
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
// CHALLENGE 4
function once(func) {
  
 let output;
  
   function onceReturn(arg){

     output = output ? output : func(arg) 
     return output;
   } 

  
 return onceReturn;

}

const addByTwo = (x) => x + 2;


// /*** Uncomment these to check your work! ***/
const onceFunc = once(addByTwo);
console.log(onceFunc(4));  // => should log 6
console.log(onceFunc(10));  // => should log 6
console.log(onceFunc(9001));  // => should log 6
```
### 138.[Challenge 5](http://csbin.io/closures)
#### My Solution
```javascript
// CHALLENGE 5
function after(count, func) {
  let times = count; 
  
  function afterTimes(){
    times--;
    if(times === 0)console.log('hello');
  }
return afterTimes; 
}

// /*** Uncomment these to check your work! ***/
const called = function() { console.log('hello') };
const afterCalled = after(3, called);
afterCalled(); // => nothing is printed
afterCalled(); // => nothing is printed
afterCalled(); // => 'hello' is printed
```
### 139.[Challenge 6](http://csbin.io/closures)
#### My Solution
```javascript
// CHALLENGE 6
function delay(func, wait) {
  
  return setTimeout(func,wait);

}

const delay5 = delay(() => console.log('hello'), 2000);
```
### 140.[Challenge 7](http://csbin.io/closures)
#### My Solution
```javascript
// CHALLENGE 7
function rollCall(names) {
  
  let index = 0;
  
  return function (){
    index < names.length ? console.log(names[index++]) : console.log('Everyone accounted for');
  }

}

// /*** Uncomment these to check your work! ***/
const rollCaller = rollCall(['Victoria', 'Juan', 'Ruth'])
rollCaller() // => should log 'Victoria'
rollCaller() // => should log 'Juan'
rollCaller() // => should log 'Ruth'
rollCaller() // => should log 'Everyone accounted for'
```
### 141.[Challenge 8](http://csbin.io/closures)
#### My Solution
```javascript
// CHALLENGE 8
function saveOutput(func, magicWord) {
  const magic = magicWord;
  const saveObject = {};
  
  return function (arg){   
     return arg === magic ? saveObject : saveObject[arg] = func(arg);
  }

}

// /*** Uncomment these to check your work! ***/
const multiplyBy2 = function(num) { return num * 2; };
const multBy2AndLog = saveOutput(multiplyBy2, 'boo');
console.log(multBy2AndLog(2)); // => should log 4
console.log(multBy2AndLog(9)); // => should log 18
console.log(multBy2AndLog('boo')); // => should log { 2: 4, 9: 18 }
```
### 142.[Challenge 9](http://csbin.io/closures)
#### My Solution
```javascript
// CHALLENGE 9
function cycleIterator(array) {
  let index = 0;
  
  return function(){
    if(index === array.length)index = 0;
    return array[index++];
  }

}

// /*** Uncomment these to check your work! ***/
const threeDayWeekend = ['Fri', 'Sat', 'Sun'];
const getDay = cycleIterator(threeDayWeekend);
console.log(getDay()); // => should log 'Fri'
console.log(getDay()); // => should log 'Sat'
console.log(getDay()); // => should log 'Sun'
console.log(getDay()); // => should log 'Fri'
```
### 143.[Challenge 10](http://csbin.io/closures)
#### My Solution
```javascript
// CHALLENGE 10
function defineFirstArg(func, arg) {

  return function(...inputs){
    let sum = 0; 
    for(let input of inputs){
      sum += input;
    }
   return func(arg, sum);
  }
}  



// /*** Uncomment these to check your work! ***/
const subtract = function(big, small) { return big - small; };
const subFrom20 = defineFirstArg(subtract, 20);
console.log(subFrom20(5)); // => should log 15
console.log(subFrom20(5,2,3)) // => should log 10
```
### 144.[Challenge 11](http://csbin.io/closures)
#### My Solution
```javascript
// CHALLENGE 11
function dateStamp(func) {
  
  return function (...args){
    const obj = [];
    obj['date'] = new Date().toLocaleDateString();
    for(let arg of args){
      obj.push({'date': new Date().toLocaleDateString(), 'output': func(arg)})
    }
    return obj;
  }

}

// /*** Uncomment these to check your work! ***/
const stampedMultBy2 = dateStamp(n => n * 2);
console.log(stampedMultBy2(4)); // => should log { date: (today's date), output: 8 }
console.log(stampedMultBy2(6,5)); // => should log [{ date: (today's date), output: 12 },{ date: (today's date), output: 10 }]
```
