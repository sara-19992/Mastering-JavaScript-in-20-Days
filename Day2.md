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
 null is assigned value to variable means empty (non-exist).
 
 undefined used when variable has not been assigned to value.

 
 ### String
 string is sequence of characters can write in :
 - double quotation 
 - single quotation 
 - back ticks (`)


 ### Coding Examples

```javascript
 //indexOf return the index of the first char or substring given it and f does not find return -1

 "hey JS".indexOf("J")
 //return a 4

 "hey JS".indexOf("H")
 //return a -1

 //includes return a boolean data if the string contains a given string
 "hey JS".includes("ey")
 //return true

 //startsWith return a boolean data if the string start with a given string
 "hey JS".startsWith("hel")
 //return false

 //operator + use to concatenate a strings
 "hey " + "JS"
 //return "hey JS"
```


  ## Operators
  1. Arithmetic operators (+,-, *, /)
  2. Comparison operator (>,<,==,!=,===,!==)

     
 ### Strict equal vs Loosey goosey equal 
 strict equal (triple equal) === compare a same valuse and same type 
 loosey goosey equal (double equal) == convert to same type and just compare a same value 

 
  ### Coding Examples

```javascript
1 == "1"
//return a true

3 === "3"
//return a false
```

## Declaring & Assigning Variables
when declaration a variable and assign it to value, JS create this variable and pointed the variable to these value.

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

### 10.[Use Bracket Notation to Find the Nth Character in a String](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/use-bracket-notation-to-find-the-nth-character-in-a-string)

#### My Solution
```javascript
// Setup
const lastName = "Lovelace";

// Only change code below this line
const thirdLetterOfLastName = lastName[2]; // Change this line
```

### 11.[Store Multiple Values in one Variable using JavaScript Arrays](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/store-multiple-values-in-one-variable-using-javascript-arrays)

#### My Solution
```javascript
// Only change code below this line
const myArray = ["peanut butter", 25, "bread"];
```

### 12.[Nest one Array within Another Array](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/nest-one-array-within-another-array)

#### My Solution
```javascript
// Only change code below this line
const myArray = [["Sarah",25], ["Maram",20], ["Nour",21]];
```

## QUESTIONS
### 1. QUESTION #1

#### My Solution
```javascript
let a = 0;
let b = "0";
let c = false;
let d = "false";

console.log(a == b);
// log true to the console double equal compare the values (0 equal 0) and ignore the type 

console.log(b === c);
// log false to the console triple equal compare the values and type, 0 is equal false as a value but the type string does not equal a type boolean 

console.log(!!d);
// log true to the console variable d is a not empty string consider as true then !(!true) is true 
```

### 2. QUESTION #2

#### My Solution
```javascript
console.log(4 + 5 * "7");

// in arthmatic operator e.g. *,/,- JS convert string to number
// 5 * 7 = 35  mul has the highest priority over add
// 4 + 35 = 39 add operator
// log 39 on the console
```

### 3. QUESTION #3

#### My Solution
```javascript
let result = 5 + 2 * 3 - 1;

// 1. 2 * 3 = 6  mult has the highest priority over add/sub
// 2. 6 + 5 = 11 add and sub has same priority but the add operator come first in expression 
// 3. 11 - 1 = 10 sub operator
// the result equal 10 
```

### 4. QUESTION #4

#### My Solution
```javascript
let x = 10;
let y = '10';

console.log(x == y);
// log true to the console double equal compare the values (10 equal '10') and ignore the type (convert to the same type)

console.log(x === y);
// log false to the console triple equal compare the values and type, 10 is equal '10' as a value but the type string does not equal a type number 
```
### 5. QUESTION #5

#### My Solution
```javascript
let num = "15";
let isPositive = true;
let result = (num > 10 && isPositive) || num < 0;
console.log(result);

// 15 > 10 evaluate to true
// (true && true) is true
// 15 < 0 evaluate to false
// (true || false) is true
// result assign to true
// log true to the console 
```
