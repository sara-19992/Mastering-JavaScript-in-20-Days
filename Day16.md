## Scope
JS organizes scopes with functions and blocks

### Dynamic global variables & Strict mdoe
**Dynamic global variables**
if assign variable that never declared in functional scope, in executing ask the global scope about this variable and doesn't find it, then the global scope create a dynamic variable.
**Coding Examples**
```javascript
function names(){
  n = 'non';
  console.log(n);
}

names(); //log 'non'
```
**Strict mode**
in strict mode can't create dynamic global variable , should declare variable before use it.
**Coding Examples**
```javascript
"use strict";
 X(); //error x is not defined

function X(){
  x = 20;
}
```

### Function Expression
**Function type hierarchy (on more benefits):**
1. Named function declaration.
2. Named function expression.
3. Anonymous function expression.
**Named function expression benefits:**
1. recurison.
2. more debuggable.
3. more self-documanting code.


   
