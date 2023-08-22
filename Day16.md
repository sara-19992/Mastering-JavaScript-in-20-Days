## Scope
JS organizes scopes with functions and blocks

### Dynamic global variables & Strict mdoe
**Dynamic global variables**<br/>
if assign variable that never declared in functional scope, in executing ask the global scope about this variable and doesn't find it, then the global scope create a dynamic variable.
#### Coding Examples
```javascript
function names(){
  n = 'non';
  console.log(n);
}

names(); //log 'non'
```
**Strict mode**<br/>
in strict mode can't create dynamic global variable , should declare variable before use it.
#### Coding Examples
```javascript
"use strict";
 X(); //error x is not defined

function X(){
  x = 20;
}
```

### Function Expression
**Function type hierarchy (on more benefits):**<br/>
1. Named function declaration.
2. Named function expression.
3. Anonymous function expression.
   
**Named function expression benefits:**<br/>
1. recurison.
2. more debuggable.
3. more self-documanting code.


## Question Exercises
### 1.[Question 1](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week3%20-%20deep-javascript-foundations-v3/day%203/tasks.md)
#### My Solution
```javascript
const exampleNormalFunc1 = (a, b, c) => {
  return a * (b + c);
};

const exampleNormalFunc2 = (x, y) => {
  return x * y;
};

const exampleNormalFunc3 = (string) => {
  return string + " " + string + " " + string + "!";
};

const arrowHOF = (normalFunc) => {
  // write your code here;

  return (...args) => {
    return (x) => {
      let results = "";
      const result = normalFunc(...args) + " ";
      for (let i = 0; i < x; i++) {
        results += result;
      }
      return results || result;
    };
  };
};

const hofNormalFunc1 = arrowHOF(exampleNormalFunc1);
const hofNormalFunc2 = arrowHOF(exampleNormalFunc2);
const hofNormalFunc3 = arrowHOF(exampleNormalFunc3);

console.log(hofNormalFunc1(3, 4, 5)(2)); // logs 27 twice
console.log(hofNormalFunc2(20, 35)(4)); // logs 700 four times
console.log(hofNormalFunc3("Meow")()); // logs "Meow Meow Meow!" once
```
### 2.[Question 2](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week3%20-%20deep-javascript-foundations-v3/day%203/tasks.md)
#### My Solution
```javascript
// Example object
const obj = {
  name: "John",
  greet: (greeting) => {
    console.log(`${greeting}, ${this.name}!`);
  },
};

const preserveThis = (func) => {
  return (...args) => {
    return func.apply(this, args);
  };
};

// Wrap the greet function using preserveThis
const preservedGreet = preserveThis(obj.greet);

// Call the wrapped function as a method of the object
preservedGreet("Hello"); // Output: "Hello, John!"

```
### 3.[Question 3](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week3%20-%20deep-javascript-foundations-v3/day%203/tasks.md)
#### My Solution
**Example 1**
```javascript
function outer1() {
  var x = 10;

  var inner1 = function() {
    console.log(x);
  };

  inner1();
}

outer1(); // Output: 10

//first search on variable x at the current scope, can't found it so search in the outer scope of the current scope and can find it
//inner scope can access variable in outer scope

```
**Example 2**
```javascript
function outer2() {
  var x = 10;

  var inner2 = function() {
    var x = 20;
    console.log(x);
  };

  inner2();
}

outer2(); // Output: 20

//var keyword has different scoping role 
//declare variable use var with same name variable in outer scope reassign the variable in outer scope and not create new variable
//the new value for x variable is 20
```


   
