## Data Fetching & Promises
  - APIs provide URL that point to certain resource (data).
  - fetch() use to load data from APIs.

### Promises  
promises represent the value that don't have yet promises take time so its asynchronous ,JS add this task to list and keep running code but if we need data from promise, can stop JS execute and wait to for promise to resolve.

- fetch() take time to get data because its return a promise.
- await keyword stop JS and wait to finish asynchronous operation. 

promises states
  1. pending: still waiting, I promise to get value.
  2. fulfilled: get the value.
  3. reject: can't get the value.
     

step fetch data:
  1. use fetch(URL) with await.
  2. the browser send a request.
  3. receive a response object.
  4. use json() to parse body of response object.
  5.  use await with json (return another promise).
     
## Destructuring Objects & Arrays
   to break down an object and extract values from object and assign it to multiple variables.

   object
   - use { }.
   - use property name.
   - omit property name that don't need.
   - order not matter.
     
   array
   - use [ ].
   - use comma to skip value.
   - order is matter.
     
split() split string on delimiting char
trim() remove spaces from start and end of str 
### Coding Examples
```javascript
const names = ["nour", "alaa", "duaa"];
const [,name1, name2] = names;
console.log(name1, name2);
//alaa duaa

const player = {
name: "ahmade",
age: 45,
tall: 180
}
const {age, name} = player;
console.log(age, name);
//45 'ahmade'
```
## Async   
in async functons can use await 

render mean display it on the page
Document.createElement() create element
appendChile append child to element

## Modules 
  - modules mean split a big code to multiple files to make it easier to work with these files.
  - modules create own scope.
  - import to import variable from another module and use it.
  - export to export variable from modules scope to outside. 

can't use await outside function in a script
### Debugging 
find bugs and fix it
  1. console.log (warn(), error()).
  2. use a browser debugger tool (create a breakpoint by a debugger keyword).
      
### Error handling
use try catch to handle error and what want we do (add default thing, do something else) 
  - try something might get error
  - catch that error object which happened
    
## Coding Task 
### [Rick & Morty Character List](https://drive.google.com/drive/folders/1h5EJKbDkaIZzxFVEJBMlu5UczkE3g5gz?usp=sharing) 
#### My Solution
```javascript
display();

//get list of data
async function fetchList() {
  const response = await fetch("https://rickandmortyapi.com/api/character");
  const body = await response.json();
  const { results } = body;
  return results;
}

async function getCharList() {
  const characterList = await fetchList();
  return characterList;
}

//filter the list with 'Alive' status
//cut the list to 50 elements
function editList(list) {
  console.log(list);
  const filterList = list.filter((c) => c.status == "Alive");
  const cutList = filterList.slice(0, 50);
  return cutList;
}

//create a Image element
const createImage = (src) => {
  const img = document.createElement("img");
  img.setAttribute("src", src);
  return img;
};

//create a heading element
const createHeading = (text) => {
  const par = document.createElement("h2");
  par.textContent = text;
  return par;
};

//create a p element
const createPar = (text) => {
  const par = document.createElement("p");
  par.textContent = text;
  return par;
};

//create a li element
const createLi = (img, head, p1, p2, p3) => {
  const li = document.createElement("li");
  li.appendChild(head);
  li.appendChild(img);
  li.appendChild(p1);
  li.appendChild(p2);
  li.appendChild(p3);
  return li;
};

async function display() {
  try {
    const list = await getCharList();
    const edit = editList(list);
    displayCharList(edit);
  } catch (er) {
    displayNotFound();
    console.log(er);
  }
}

//display the character as list
function displayCharList(characterList) {
  const list = document.querySelector("#characterList");

  for (let char of characterList) {
    const img = createImage(char.image);
    const head = createHeading(char.name);
    const p1 = createPar(`Locatian: ${char.location.name}`);
    const p2 = createPar(`Species: ${char.species}`);
    const p3 = createPar(`Gener: ${char.gender}`);
    const li = createLi(img, head, p1, p2, p3);

    list.appendChild(li);
  }
}

function displayNotFound() {
  document
    .querySelector("#characterList")
    .appendChild(createHeading("404 Not Found"));
}
```
## Coding Exercises
### 101.[Use Destructuring Assignment to Extract Values from Objects](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/es6/use-destructuring-assignment-to-extract-values-from-objects)
#### My Solution
```javascript
const HIGH_TEMPERATURES = {
  yesterday: 75,
  today: 77,
  tomorrow: 80
};

// Only change code below this line

const {today, tomorrow} = HIGH_TEMPERATURES;

// Only change code above this line
```
### 102.[Use Destructuring Assignment to Assign Variables from Objects](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/es6/use-destructuring-assignment-to-assign-variables-from-objects)
#### My Solution
```javascript
const HIGH_TEMPERATURES = {
  yesterday: 75,
  today: 77,
  tomorrow: 80
};

// Only change code below this line
  
const {today: highToday,tomorrow:highTomorrow} = HIGH_TEMPERATURES; 

// Only change code above this line
```
### 103.[Use Destructuring Assignment to Assign Variables from Nested Objects](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/es6/use-destructuring-assignment-to-assign-variables-from-nested-objects)
#### My Solution
```javascript
const LOCAL_FORECAST = {
  yesterday: { low: 61, high: 75 },
  today: { low: 64, high: 77 },
  tomorrow: { low: 68, high: 80 }
};

// Only change code below this line
  
const {today:{low: lowToday,high: highToday}} = LOCAL_FORECAST;

// Only change code above this line
```
### 104.[Use Destructuring Assignment to Assign Variables from Arrays](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/es6/use-destructuring-assignment-to-assign-variables-from-arrays)
#### My Solution
```javascript
let a = 8, b = 6;
// Only change code below this line
[a,b] = [b,a];
```
### 105.[Destructuring via rest elements](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/es6/use-destructuring-assignment-with-the-rest-parameter-to-reassign-array-elements)
#### My Solution
```javascript
function removeFirstTwo(list) {
  // Only change code below this line
  const [, , ...shorterList] = list; // Change this line
  // Only change code above this line
  console.log(shorterList);
  return shorterList;
}

const source = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
const sourceWithoutFirstTwo = removeFirstTwo(source);
```
### 106.[Use Destructuring Assignment to Assign Variables from Objects](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/es6/use-destructuring-assignment-to-assign-variables-from-objects)
#### My Solution
```javascript
const stats = {
  max: 56.78,
  standard_deviation: 4.34,
  median: 34.54,
  mode: 23.87,
  min: -0.75,
  average: 35.85
};

// Only change code below this line
const half = ({max, min}) => (max + min) / 2.0; 
// Only change code above this line
```
### 107.[Create Strings using Template Literals](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/es6/create-strings-using-template-literals)
#### My Solution
```javascript
const result = {
  success: ["max-length", "no-amd", "prefer-arrow-functions"],
  failure: ["no-var", "var-on-top", "linebreak"],
  skipped: ["no-extra-semi", "no-dup-keys"]
};
function makeList(arr) {
  // Only change code below this line
  const failureItems = [];
  for(let item of arr){
    const str = `<li class="text-warning">${item}</li>`
    failureItems.push(str);
  }
  // Only change code above this line
  return failureItems;
}

const failuresList = makeList(result.failure);
```
### 108.[Write Concise Object Literal Declarations Using Object Property Shorthand](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/es6/write-concise-object-literal-declarations-using-object-property-shorthand)
#### My Solution
```javascript
const createPerson = (name, age, gender) => {
  // Only change code below this line
  return {name,age,gender};
  // Only change code above this line
};
```
### 109.[Write Concise Declarative Functions with ES6](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/es6/write-concise-declarative-functions-with-es6)
#### My Solution
```javascript
// Only change code below this line
const bicycle = {
  gear: 2,
  setGear(newGear) {
    this.gear = newGear;
  }
};
// Only change code above this line
bicycle.setGear(3);
console.log(bicycle.gear);
```
### 110.[Use class Syntax to Define a Constructor Function](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/es6/use-class-syntax-to-define-a-constructor-function)
#### My Solution
```javascript
// Only change code below this line
class Vegetable {
  constructor(vegetable){
   this.name = vegetable;
  }

}
// Only change code above this line

const carrot = new Vegetable('carrot');
console.log(carrot.name); // Should display 'carrot'
```
### 111.[Use getters and setters to Control Access to an Object](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/es6/use-getters-and-setters-to-control-access-to-an-object)
#### My Solution
```javascript
// Only change code below this line
class Thermostat{
  constructor(temp){
    this.temp = 5/9 * (temp - 32);
  }
  //getter 
  get temperature(){
    return this.temp;
  } 
  //setter
  set temperature(temp){
    this.temp = temp;
  } 
}
// Only change code above this line

const thermos = new Thermostat(76); // Setting in Fahrenheit scale
let temp = thermos.temperature; // 24.44 in Celsius
thermos.temperature = 26;
console.log(thermos.temp);
temp = thermos.temperature; // 26 in Celsius
```
### 112.[Create a Module Script](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/es6/create-a-module-script)
#### My Solution
```javascript
<html>
  <body>
    <!-- Only change code below this line -->
<script type="module" src="index.js"></script>
    <!-- Only change code above this line -->
  </body>
</html>
```
### 113.[Use export to Share a Code Block](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/es6/use-export-to-share-a-code-block)
#### My Solution
```javascript
const uppercaseString = (string) => {
  return string.toUpperCase();
}

const lowercaseString = (string) => {
  return string.toLowerCase()
}

export {uppercaseString, lowercaseString};
```
### 114.[Reuse JavaScript Code Using import](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/es6/reuse-javascript-code-using-import)
#### My Solution
```javascript
import {uppercaseString, lowercaseString} from './string_functions.js'; 
// Only change code above this line

uppercaseString("hello");
lowercaseString("WORLD!");
```
### 115.[Use * to Import Everything from a File](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/es6/use--to-import-everything-from-a-file)
#### My Solution
```javascript
import * as stringFunctions from './string_functions.js';
// Only change code above this line

stringFunctions.uppercaseString("hello");
stringFunctions.lowercaseString("WORLD!");
```
### 116.[Create an Export Fallback with export default](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/es6/create-an-export-fallback-with-export-default)
#### My Solution
```javascript
export default function subtract(x, y) {
  return x - y;
}
```
### 117.[Import a Default Export](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/es6/import-a-default-export)
#### My Solution
```javascript
import subtract from './math_functions.js';  
// Only change code above this line

subtract(7,4);
```

    
    
    
