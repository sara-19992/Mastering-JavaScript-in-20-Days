## Functions
- values are things
- variables pointed to things 
- functions doing things 
 ### Coding Examples
```javascript
//declare function
function logHi(){
  console.log("hey JS");
}
```
### Parameters & Arguments 
arguments is values that  passed to the function but parameters is a variable in a function  definition
some function don't need any value to work (no parameters).

JS don't mind called function with missing or extra arguments (set to undefined).
 ### Coding Examples
```javascript
//add function
function add(num1 ,num2){
  return num1 + num2 ;
}

const sum = add(3,5);
console.log(sum);
//log 8


console.log(add(3));
//log NaN (number + undefined)

console.log(add(3,5,6));
//log undefined

```
### Functions return 
- output of function that getting back by using a return keyword
- some function don't use return keyword
- each functions return implicit value undefined expects function use a return keyword
- unreachable code is code after return statement
 ### Coding Examples
```javascript

function multi(num1 ,num2){
  const num = num1 * num2;
  return num;
  //unreachable code below this line
  console.log(num);
}

function sub(num1 ,num2){
  console.log(num1 - num2);
}

const num = sub(3,5);
console.log(num );
//log undefined)

```
### Declare functions 
1. normal named function (function keyword) 
2. unnamed function (assign function to variable )
3. arrow function => unnamed function is quick way to write small code function just returned a value without any complicated
```javascript
//named function
function sum(num1 ,num2){
  const num = num1 + num2;
  return num;
}

//assign function to variable
const sub = function (num1 ,num2){
  console.log(num1 - num2);
}

//arrow function
const multi = (num1 ,num2) => num1 * num2;
```
arrow function if take one parameter parentheses are optional for multiple parameters the parentheses required.if need to complete code and doing something use { } curly braces.

## Scope
JS care where and when declare variable
 1. Global scope widest scope
 2. Function scope each function has new own scope
 3. Block scope using our curly braces

the outside scope can't see the inner scops, but the inner scope can see the outside scope
global scope can't see variables in function scope. 

### let vs var
let and var variable in inner scope can assign outer scope variable but var has different scoping role than let,
if let keyword create a variable in inner scope with same named a global scope variable,let create a new variable different from variable in global scope. but var not create a new variable it change the value in the global scope variable (reassign it).

const like let but can't reaasign it. 

### Coding Examples
```javascript
declare functions 
- normal named function (function keyword) 
- unnamed function (assign function to variable )
- arrow function => unnamed function is quick way to write small code function just returned a value without any complicated.if take one parameter parentheses are optional for multiple parameters the parentheses required.if need to complete code and doing something use { } curly braces
```javascript
//a global scope variable
let str1 = "hey JS";
var str2 = "ahmade";

{
//a block scope variable
  let str1 = "text";
  var str2 = "nour";
}

console.log(str1);
//log hey JS

console.log(str2);
//log nour
```

## Events 
make page interactive,there a different kind of events (click,dbClick,mouseout)
event Object has some detailed about event handled

addEventListener function listen for events take two parameters :
 1. name of event to listen to it
 2. handler function calls when event happened
  
## Coding Exercises
### 19.[Global Scope and Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/global-scope-and-functions)
#### My Solution
```javascript
// Declare the myGlobal variable below this line
const myGlobal = 10;

function fun1() {
  // Assign 5 to oopsGlobal here
  oopsGlobal = 5;
}

// Only change code above this line

function fun2() {
  let output = "";
  if (typeof myGlobal != "undefined") {
    output += "myGlobal: " + myGlobal;
  }
  if (typeof oopsGlobal != "undefined") {
    output += " oopsGlobal: " + oopsGlobal;
  }
  console.log(output);
}
```
### 20.[Local Scope and Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/local-scope-and-functions)
#### My Solution
```javascript
function myLocalScope() {
  // Only change code below this line
  const myVar = "50";
  console.log('inside myLocalScope', myVar);
}
myLocalScope();

// Run and check the console
// myVar is not defined outside of myLocalScope
console.log('outside myLocalScope', myVar);
```
### 21.[Global vs. Local Scope in Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/global-vs--local-scope-in-functions)
#### My Solution
```javascript
// Setup
const outerWear = "T-Shirt";

function myOutfit() {
  // Only change code below this line
  const outerWear = "sweater";
  // Only change code above this line
  return outerWear;
}

myOutfit();
```
### 22.[Stand in Line](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/stand-in-line)
#### My Solution
```javascript
function nextInLine(arr, item) {
  // Only change code below this line
  arr.push(item);
  item = arr.shift();

  return item;
  // Only change code above this line
}

// Setup
let testArr = [1, 2, 3, 4, 5];

// Display code
console.log("Before: " + JSON.stringify(testArr));
console.log(nextInLine(testArr, 6));
console.log("After: " + JSON.stringify(testArr));
```
### 23.[Access Array Data with Indexes](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/access-array-data-with-indexes)
#### My Solution
```javascript
const myArray = [50, 60, 70];
console.log(myArray[0]);
const myData  = myArray[0];
```
### 24.[Modify Array Data With Indexes](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/modify-array-data-with-indexes)
#### My Solution
```javascript
// Setup
const myArray = [18, 64, 99];

// Only change code below this line
myArray[0] = 45;
```
### 25.[Access Multi-Dimensional Arrays With Indexes](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/access-multi-dimensional-arrays-with-indexes)
#### My Solution
```javascript
const myArray = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
  [[10, 11, 12], 13, 14],
];

const myData = myArray[2][1];
```
### 26.[Manipulate Arrays With push Method](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/manipulate-arrays-with-push)
#### My Solution
```javascript
// Setup
const myArray = [["John", 23], ["cat", 2]];

// Only change code below this line
myArray.push(["dog",3]);
```
### 27.[Manipulate Arrays With pop Method](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/manipulate-arrays-with-pop)
#### My Solution
```javascript
// Setup
const myArray = [["John", 23], ["cat", 2]];

// Only change code below this line
const removedFromMyArray = myArray.pop();
```
### 28.[Manipulate Arrays With shift Method](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/manipulate-arrays-with-shift)
#### My Solution
```javascript
// Setup
const myArray = [["John", 23], ["dog", 3]];

// Only change code below this line
const removedFromMyArray = myArray.shift();
```
### 29.[Manipulate Arrays With unshift Method](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/manipulate-arrays-with-unshift)
#### My Solution
```javascript
// Setup
const myArray = [["John", 23], ["dog", 3]];
myArray.shift();

// Only change code below this line
myArray.unshift(["Paul", 35]);
```
### 30.[Shopping List](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/shopping-list)
#### My Solution
```javascript
const myList = [["chips",5],["milk",10],["pasta",1],["ice cream",4],["chocolate",2]];
```
### 31.[Write Reusable JavaScript with Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/write-reusable-javascript-with-functions)
#### My Solution
```javascript
//create a function
function reusableFunction (){
  console.log("Hi World");
}

//call the function
reusableFunction();
```
### 32.[Passing Values to Functions with Arguments](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/passing-values-to-functions-with-arguments)
#### My Solution
```javascript
function functionWithArgs(num1,num2){
 console.log(num1 + num2);
}

functionWithArgs(7,5);
```
### 33.[Return a Value from a Function with Return](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/return-a-value-from-a-function-with-return)
#### My Solution
```javascript
//create function
function timesFive(num){
  return num *= 5;
}

console.log(timesFive(4));
//log 20
```
### 34.[Understanding Undefined Value returned from a Function](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/understanding-undefined-value-returned-from-a-function)
#### My Solution
```javascript
// Setup
let sum = 0;

function addThree() {
  sum = sum + 3;
}

// Only change code below this line
function addFive(){
  sum += 5;
}

// Only change code above this line

addThree();
addFive();
```
### 35.[Assignment with a Returned Value](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/assignment-with-a-returned-value)
#### My Solution
```javascript
// Setup
let processed = 0;

function processArg(num) {
  return (num + 3) / 5;
}

// Only change code below this line
processed = processArg(7);
```

### 36.[Understanding Boolean Values](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/understanding-boolean-values)
#### My Solution
```javascript
function welcomeToBooleans() {
  // Only change code below this line

  return true; // Change this line

  // Only change code above this line
}
```
### 37.[Use Conditional Logic with If Statements](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/use-conditional-logic-with-if-statements)
#### My Solution
```javascript
function trueOrFalse(wasThatTrue) {
  // Only change code below this line
  if(wasThatTrue) {
    return "Yes, that was true";
  }
  return "No, that was false";
  

  // Only change code above this line

}
```
### 38.[Comparison with the Equality Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/comparison-with-the-equality-operator)
#### My Solution
```javascript
// Setup
function testEqual(val) {
  if (val == 12) { // Change this line
    return "Equal";
  }
  return "Not Equal";
}

testEqual(10);
```
### 39.[Comparison with the Strict Equality Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/comparison-with-the-strict-equality-operator)
#### My Solution
```javascript
// Setup
function testStrict(val) {
  if (val === 7) { // Change this line
    return "Equal";
  }
  return "Not Equal";
}

testStrict(10);
```
### 40.[Practice comparing different values](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/practice-comparing-different-values)
#### My Solution
```javascript
// Setup
function compareEquality(a, b) {
  if (a === b) { // Change this line
    return "Equal";
  }
  return "Not Equal";
}

compareEquality(10, "10");
```
### 41.[Comparison with the Inequality Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/comparison-with-the-inequality-operator)
#### My Solution
```javascript
// Setup
function testNotEqual(val) {
  if (val != 99) { // Change this line
    return "Not Equal";
  }
  return "Equal";
}

testNotEqual(10);
```
### 42.[Comparison with the Strict Inequality Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/comparison-with-the-strict-inequality-operator)
#### My Solution
```javascript
// Setup
function testStrictNotEqual(val) {
  if (val !== 17) { // Change this line
    return "Not Equal";
  }
  return "Equal";
}

testStrictNotEqual(10);
```
### 43.[Comparison with the Greater Than Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/comparison-with-the-greater-than-operator)
#### My Solution
```javascript
function testGreaterThan(val) {
  if (val > 100) {  // Change this line
    return "Over 100";
  }

  if (val > 10) {  // Change this line
    return "Over 10";
  }

  return "10 or Under";
}

testGreaterThan(10);
```
### 44.[Comparison with the Greater Than Or Equal To Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/comparison-with-the-greater-than-or-equal-to-operator)
#### My Solution
```javascript
function testGreaterOrEqual(val) {
  if (val >= 20) {  // Change this line
    return "20 or Over";
  }

  if (val >= 10) {  // Change this line
    return "10 or Over";
  }

  return "Less than 10";
}

testGreaterOrEqual(10);
```
### 45.[Comparison with the Less Than Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/comparison-with-the-less-than-operator)
#### My Solution
```javascript
function testLessThan(val) {
  if (val < 25) {  // Change this line
    return "Under 25";
  }

  if (val < 55) {  // Change this line
    return "Under 55";
  }

  return "55 or Over";
}

testLessThan(10);
```
### 46.[Comparison with the Less Than Or Equal To Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/comparison-with-the-less-than-or-equal-to-operator)
#### My Solution
```javascript
function testLessOrEqual(val) {
  if (val <= 12) {  // Change this line
    return "Smaller Than or Equal to 12";
  }

  if (val <= 24) {  // Change this line
    return "Smaller Than or Equal to 24";
  }

  return "More Than 24";
}

testLessOrEqual(10);
```
### 47.[Comparisons with the Logical And Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/comparisons-with-the-logical-and-operator)
#### My Solution
```javascript
function testLogicalAnd(val) {
  // Only change code below this line

  if (val <= 50 && val >= 25) {
   return "Yes";
  }

  // Only change code above this line
  return "No";
}

testLogicalAnd(10);
```
### 48.[Comparisons with the Logical Or Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/comparisons-with-the-logical-or-operator)
#### My Solution
```javascript
function testLogicalOr(val) {
  // Only change code below this line

  if (val > 20  || val < 10) {
    return "Outside";
  }

  // Only change code above this line
  return "Inside";
}

testLogicalOr(15);
```
### 49.[Introducing Else Statements](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/introducing-else-statements)
#### My Solution
```javascript
function testElse(val) {
  let result = "";
  // Only change code below this line

  if (val > 5) {
    result = "Bigger than 5";
  }

  else {
    result = "5 or Smaller";
  }

  // Only change code above this line
  return result;
}

testElse(4);
```
### 50.[Introducing Else If Statements](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/introducing-else-if-statements)
#### My Solution
```javascript
function testElseIf(val) {
  if (val > 10) {
    return "Greater than 10";
  }else if (val < 5) {
    return "Smaller than 5";
  }else{
     return "Between 5 and 10";
  } 
}

testElseIf(7);
```
