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
### 1.[Question 1]()
#### My Solution
```javascript

```
### 2.[Question 2]()
#### My Solution
```javascript

```
### 3.[Question 3]()
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


   
