## Values & Data Types
Value is units of information can be in different data type.

### JS has two type of data
1. Primitive data types
    - string
    - number
    - boolean
    - null
    - undefined
      
2. Objects

 ### Coding Examples

```javascript
//typeof return the type of data as a string

//return a string
typeof "hey JS"

//return a number 
typeof 54
```
 ### null vs undefined
 
 ### string
 string is sequence of characters can write in :
 - double quotation 
 - single quotation 
 - back ticks (`)

 ### Coding Examples

```javascript
//indexOf return the index of the first char or substring given it and f does not find return -1
//return a 4
"hey JS".indexOf("J")
//return a -1
"hey JS".indexOf("H")

//includes return a boolean data if the string contains a given string
//return true
"hey JS".includes("ey")

//startsWith return a boolean data if the string start with a given string
//return false
"hey JS".startsWith("hel")

//operator + use to concatenate a strings
//return "hey JS"
 "hey " + "JS"
```
  ### operators
  1. Arithmetic operators (+,-, *, /)
  2. Comparison operator (>,<,==,!=,===,!==)
     
 ### Strict equal vs Loosey goosey equal 
 strict equal (triple equal) === compare a same valuse and same type 
 loosey goosey equal (double equal) == convert to same type and just compare a same value 
 
  ### Coding Examples

```javascript
//return a true
1 == "1"

//return a false
3 === "3"
```
### Declaring & Assigning Variables
when declaration a variable and assign it to value, JS create this variable and pointed the variable to these value 
keywords to declare Variables:
 - var
 - let
 - const
   
let and const keywords added in ES6.

the const keyword can just assigned to initial value in declaration once time but the let and var can be reassigned.

 ### Coding Examples

```javascript
//declare a variable then assign it 
let firstName;
firstName="Sarah";

//declare a variable and assign it 
let lastName="Sarah";
```
### Statements vs Expressions
expression ask JS for a value but statement tells JS to do something 
### Coding Examples

```javascript
//expression 
10 + 7

//a statement to log on the console
console.log("hey JS");
```
