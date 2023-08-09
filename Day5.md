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
//5 grater than 3

compare(2,3);
//2 less than 3
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
  
backticks allow to add variable in string by us ${}
  
### Coding Examples
```javascript
function between(x){
  if(x > 5 && x < 10){
    console.log(`${x} between 5 & 10`);
  }else{
    console.log(`${x} not between 5 & 10`);
  }
}
between(12);
//12 not between 5 & 10

between(8);
//8 between 5 & 10

const s = 6 > 2 ? "number 1 grater" : "number 2 grater";
console.log(s);
//number 1 grater
```
### Loops
execute same code of multiple times 
1. for loop
2. for of loop (loop in each item in collection)
3. while loop until condition is trueloop until condition is true
   
array and string are iteratbles (can iterat over them)

## Map & Filter
methods use to process items in the array
- map create new array with do something on each item in array
- filter create new array with items which return true (filter out the item)

### Coding Examples
```javascript
const num = [1, 2, 4, 5, 7, 8];

const numMulti = num.map(n => n *= 4);
console.log(numMulti);
//[4, 8, 16, 20, 28, 32]

const numFilter = num.filter(n => n >= 5 );
console.log(numFilter);
//[5, 7, 8]
``` 
### Spread (...) 
spread the items around can use to
1. concatenate arrays
2. pass array items as arguments
### Coding Examples
```javascript
const a1 = ["nour", "ola", "ahmade"];
const a2 = ["zein", ...a1, "weal"];

console.log(a2);
//["zein", "nour", "ola", "ahmade", "weal"]
```   
### Random
use to return a random number between. the random function return a number between 0 and 1 to convert returned value to integer multiply the returned value by the range of number we need then use floor() function to return a close integer number equal or less than number.
### Coding Examples
```javascript
function getRandom(range){
  return Math.floor((Math.random() * range))
}

const x = getRandom(20);
const y = getRandom(20);
const z = getRandom(20);

//log number in range 0 - 19
console.log(x, y, z);
```

## Asynchronous vs Synchronous

synchronous meanning execute the code one by one,each line of code waits for previous line to get executed then it gets executed.
asynchronous JS can't do multiple tasks at the same time and when give JS a task that take time JS not stop and wait this task add this task to list and keep runing other tasks and run this task some time later.

setTimeout execute code after a certain milliseconds

### Coding Examples
```javascript

console.log("nour");

setTimeout(() => console.log("sarah"),1000)

console.log("alaa");

//nour
//alaa
//sarah
```
