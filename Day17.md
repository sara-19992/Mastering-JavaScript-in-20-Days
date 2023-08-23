## Advanced Scope

### Lexical scope vs Dynamic scope
**Lexical scope** is scope of a variables or functions based on where it is defined in the code.
**Dynamic scope** is scope where functions is called. 

### Blcok scope
scope done with blocks by curly braces.

### Hoisting
JS move variable and function declaration to the top of scope before executing. and hoisting sometimes bad / sometimes useful. 

**function hoisting**
1. call function before their declaration.
2. function hoisting is useful to put the executable code at the top.
3. unction expression not hoisted.
   
**variable hoisting**   
1. variable hoisting can use them before declare
2. var are hoisted and assigned to undefined.
3. let is hoist and not initialize, can't touch it like var and const.
4. const is not hoisted.

## ADVANCED SCOPE Exercises
### 1.[Question 1](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week3%20-%20deep-javascript-foundations-v3/day%204/tasks.md)
#### My Solution
```javascript
for (var i = 0; i < 5; i++) {
    setTimeout(function() {
      console.log("value of [i] is: ", i);
    }, 100);
}
//log value of [i] is:  5 five times
//setTimeout function is async and take time to execute, JS put it into browser feather and continue execute loop and increment the variable i
//then variable i become 5 then execute setTimeout 5 times with value of i (5).

for (var i = 0; i < 5; i++) {
  (function (i) {
    setTimeout(function () {
      console.log("value of [i] is: ", i);
    }, 100);
  })(i);
}
//log value of [i] is:  0, value of [i] is:  1, value of [i] is:  2, value of [i] is:  3, value of [i] is:  4  
//solution using closure by create new function scope for each iteration in the loop and pass the variable i to the function
//use IFEE (Immediately Invoked Function Expression) or can create function then call it.

```
### 2.[Question 2](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week3%20-%20deep-javascript-foundations-v3/day%204/tasks.md)
#### My Solution
```javascript
for (let i = 0; i < 5; i++) {
   let array = [];
   array.push(i);
   console.log("Current array is: ", array)
}
//log Current array is: [ 0 ], Current array is: [ 1 ], Current array is: [ 2 ], Current array is: [ 3 ], Current array is: [ 4 ]
//in each iteration a new array is created in the loop and the iteration index is pushed and then move to the next iteration and create a new array //again and so on

let array = [];
for (let i = 0; i < 5; i++) {
   array.push(i);
}
console.log("Current array is: ", array);
//solution declare the array outside the block scope for 
```
### 3.[Question 3](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week3%20-%20deep-javascript-foundations-v3/day%204/tasks.md)
#### My Solution
```javascript

```




