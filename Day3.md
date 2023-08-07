## Arrays
array is a object data type (js every thing else premitiv data is objects) ,contains items can be in different types.

each item in array pointed to index to accesses it 

 ### Coding Examples

```javascript
//declare empty array
const days = [];

//array of diffrent item type
const arr = ["Ahmade",45,true];

console.log(arr[0]);
//log "Ahmade" to the console
```

### Array methodes
 some of array methods:
  - push (append item to array and return the new length of array)
  - pop (remove the last item of array and return it)
  - sort (sort the array in alphabetical order)
  - join (join the item of array by a string)
  - concat (create a new array and concatenate the two array together)
  - includes (if array contains a given item)

 ### Coding Examples
```javascript
//declare array
const numbers = [1,2,3,7];

let num=numbers.pop()
console.log(num)
//log 7

console.log(numbers)
//log [1,2,3]

numbers.push(4);
console.log(numbers);
//log [1,2,3,4]

const arr=numbers.concat([5,6]);
console.log(arr);
//arr = [1,2,3,4,5,6]

const names = ["aseel","nour","alaa"];
console.log(names.join(" , "));
//log "aseel , nour , alaa"

```    

### immutable vs mutable
there are two type of data:
  1. immutable cant be change (always stay the same)
  2. mutable cne be change

  for variable
- let and var is a mutable can change it (reassign)
- const is immutable (declare and assign in the same time and can't change it)

  for data type  
- array is a mutable can change the items
- string is immutable can't change the items as array but can reassign the value of it

if declare a const array we can't reassign it but we can change the items in array because array is mutable  (const array itself can't be change but the item can be changed )
  
### Coding Examples
```javascript
const names = ["Ahmade","aseel","alaa"];
names[0] = "wael";
console.log(names[0]);
//log a new value "wael"

let str = "duaa fd";
str[0] = "a";
console.log(str[0]);
//log "d" because string is immutable  
```

## Objects
object indicate by curly brackets has a properties and values, can reassign the property to new value and can assign new property to the object.
property in object can be action (functions, methode)

object is mutable can change on it 

to accesses value and add new property use:
 - dot (.)
 - use square bracket of name property as string
   
in array JS naming items with index number but in object naming items by string (property name) so in object can't accesses value by number

### Coding Examples
```javascript
const person = {name:"alaa"};

console.log(person.name);
//log "alaa"

person["age"]=45;
console.log(person);
//log {name:"alaa" ,age:45}
```
this keyword use to refer back to the object

object can within object (nested object, array in object, object in array, ...)

### Coding Examples

```javascript
//objects in a array
const persons =[{name:"alaa" ,age:45},{name:"nour" ,age:20}]

console.log(persons[1]);
//log {name:"nour" ,age:20}
```

## Built-in Object
object that defined in JS language
 - DOM
 - Console
 - Math
 - String
   
JS can wrote in html file in script tag (script element)     


## Coding Exercises

### 13.[Copy Array Items Using slice()](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/copy-array-items-using-slice)

#### My Solution
```javascript
function forecast(arr) {
  // Only change code below this line

  return arr.slice(2,4);
}

// Only change code above this line
console.log(forecast(['cold', 'rainy', 'warm', 'sunny', 'cool', 'thunderstorms']));
```
### 14.[Combine Arrays with the Spread Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/combine-arrays-with-the-spread-operator)

#### My Solution
```javascript
function spreadOut() {
  let fragment = ['to', 'code'];
  let sentence = ['learning', ...fragment , 'is', 'fun']; // Change this line
  return sentence;
}

console.log(spreadOut());
```
### 15.[Profile Lookup](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/profile-lookup)

#### My Solution
```javascript
// Setup
const contacts = [
  {
    firstName: "Akira",
    lastName: "Laine",
    number: "0543236543",
    likes: ["Pizza", "Coding", "Brownie Points"],
  },
  {
    firstName: "Harry",
    lastName: "Potter",
    number: "0994372684",
    likes: ["Hogwarts", "Magic", "Hagrid"],
  },
  {
    firstName: "Sherlock",
    lastName: "Holmes",
    number: "0487345643",
    likes: ["Intriguing Cases", "Violin"],
  },
  {
    firstName: "Kristian",
    lastName: "Vos",
    number: "unknown",
    likes: ["JavaScript", "Gaming", "Foxes"],
  },
];

function lookUpProfile(name, prop) {
  // Only change code below this line 
  for(let i=0;i<contacts.length;i++){
    if(contacts[i].firstName === name){     
     if(contacts[i][prop] === undefined) return "No such property"
     else return contacts[i][prop];
    }
  }
  return "No such contact";
  
  // Only change code above this line
}
```

### 16.[Write Reusable JavaScript with Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/write-reusable-javascript-with-functions)

#### My Solution
```javascript
//create a function
function reusableFunction (){
  console.log("Hi World");
}

//call the function
reusableFunction();
```

### 17.[Understanding Undefined Value returned from a Function](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/understanding-undefined-value-returned-from-a-function)

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


### 18.[Return a Value from a Function with Return](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/return-a-value-from-a-function-with-return)

#### My Solution
```javascript
//create function
function timesFive(num){
  return num *= 5;
}

console.log(timesFive(4));
//log 20
```

