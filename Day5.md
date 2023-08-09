## Conditionals  
condition evaluate to boolean value
  1. if statement execute code under a condition
  2. else statement execute other code if condition not happened (if false)
  3. else if statement for multiple condition
     
### Coding Examples
```javascript
function compare(x ,y){
  if(x > y){
      console.log(x,"grater than",y);
   }else{
       console.log(x,"less than",y);
   }
}

//comma in console log add spaces (multiple things)

compare(5,3);
//log 5 grater than 3

compare(2,3);
//log 2 less than 3
```
JS determine if value of variables true or false
  - Non-empty string is true value & empty string false
  - Null array is true (object is the true value)
  - Number if zero is false
  - Null and undefined are false

### Logical & Ternary Operators
- ! opposite boolean value 
- && and true if both values true 
- || or only one value true to be true 
- ternary operator condition ? ifTrue : ifFalse
### Coding Examples
```javascript
function between(x){
  if(x > 5 &&  < 10
    console.log(x, "between 5 & 10");
  }else{
    console.log(x, "not between 5 & 10");
  }
}
between(12);
//log 12 not between 5 & 10

between(8);
//log 8 between 5 & 10

const s = 6 > 2 ? "number 1 grater" : "number 2 grater";
console.log(s);
//log number 1 grater

```
