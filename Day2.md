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

 ### Null vs Undefined
 
 ### String
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


  ## Operators
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

## Declaring & Assigning Variables
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

## Coding Exercises

### 4.[Word Blanks](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/word-blanks)

#### My Solution
```javascript
const myNoun = "dog";
const myAdjective = "big";
const myVerb = "ran";
const myAdverb = "quickly";

// Only change code below this line
const wordBlanks = myAdjective + " " + myNoun + " " + myVerb + " " + myAdverb ; // Change this line
// Only change code above this line
```

### 5.[Constructing Strings with Variables](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/constructing-strings-with-variables)

#### My Solution
```javascript
// Only change code below this line
const myName = "Sarah";
const myStr = "My name is " + myName + "and I am well!";
```

### 6.[Appending Variables to Strings](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/appending-variables-to-strings)

#### My Solution
```javascript
// Change code below this line
const someAdjective = "good";
let myStr = "Learning to code is ";
myStr += someAdjective;
```

### 7.[Find the Length of a String](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/find-the-length-of-a-string)

#### My Solution
```javascript
// Setup
let lastNameLength = 0;
const lastName = "Lovelace";

// Only change code below this line
lastNameLength = lastName.length;
```

### 8.[Use Bracket Notation to Find the First Character in a String](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/use-bracket-notation-to-find-the-first-character-in-a-string)

#### My Solution
```javascript
// Setup
let firstLetterOfLastName = "";
const lastName = "Lovelace";

// Only change code below this line
firstLetterOfLastName = lastName[0]; // Change this line
```

### 9.[Understand String Immutability](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/understand-string-immutability)

#### My Solution
```javascript
// Setup
let myStr = "Jello World";

// Only change code below this line
myStr = "Hello World"; // Change this line
// Only change code above this line
```

### 10.[]()

#### My Solution
```javascript

```

### 11.[]()

#### My Solution
```javascript

```

### 12.[]()

#### My Solution
```javascript

```

