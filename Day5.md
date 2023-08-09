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
### Coding Examples
```javascript
for(let char of "hey JS"){
  console.log(char);
}
//h
//e
//y
//
//J
//S
```
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
## Coding Exercises
### 51.[Use Multiple Conditional (Ternary) Operators](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/use-multiple-conditional-ternary-operators)
#### My Solution
```javascript
function checkSign(num) {
return num === 0 ? "zero" : num > 0 ? "positive" : "negative";
}

checkSign(10);
```
### 52.[Use the map Method to Extract Data from an Array](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-the-map-method-to-extract-data-from-an-array)
#### My Solution
```javascript
// The global variable
const watchList = [
  {
    "Title": "Inception",
    "Year": "2010",
    "Rated": "PG-13",
    "Released": "16 Jul 2010",
    "Runtime": "148 min",
    "Genre": "Action, Adventure, Crime",
    "Director": "Christopher Nolan",
    "Writer": "Christopher Nolan",
    "Actors": "Leonardo DiCaprio, Joseph Gordon-Levitt, Elliot Page, Tom Hardy",
    "Plot": "A thief, who steals corporate secrets through use of dream-sharing technology, is given the inverse task of planting an idea into the mind of a CEO.",
    "Language": "English, Japanese, French",
    "Country": "USA, UK",
    "Awards": "Won 4 Oscars. Another 143 wins & 198 nominations.",
    "Poster": "http://ia.media-imdb.com/images/M/MV5BMjAxMzY3NjcxNF5BMl5BanBnXkFtZTcwNTI5OTM0Mw@@._V1_SX300.jpg",
    "Metascore": "74",
    "imdbRating": "8.8",
    "imdbVotes": "1,446,708",
    "imdbID": "tt1375666",
    "Type": "movie",
    "Response": "True"
  },
  {
    "Title": "Interstellar",
    "Year": "2014",
    "Rated": "PG-13",
    "Released": "07 Nov 2014",
    "Runtime": "169 min",
    "Genre": "Adventure, Drama, Sci-Fi",
    "Director": "Christopher Nolan",
    "Writer": "Jonathan Nolan, Christopher Nolan",
    "Actors": "Ellen Burstyn, Matthew McConaughey, Mackenzie Foy, John Lithgow",
    "Plot": "A team of explorers travel through a wormhole in space in an attempt to ensure humanity's survival.",
    "Language": "English",
    "Country": "USA, UK",
    "Awards": "Won 1 Oscar. Another 39 wins & 132 nominations.",
    "Poster": "http://ia.media-imdb.com/images/M/MV5BMjIxNTU4MzY4MF5BMl5BanBnXkFtZTgwMzM4ODI3MjE@._V1_SX300.jpg",
    "Metascore": "74",
    "imdbRating": "8.6",
    "imdbVotes": "910,366",
    "imdbID": "tt0816692",
    "Type": "movie",
    "Response": "True"
  },
  {
    "Title": "The Dark Knight",
    "Year": "2008",
    "Rated": "PG-13",
    "Released": "18 Jul 2008",
    "Runtime": "152 min",
    "Genre": "Action, Adventure, Crime",
    "Director": "Christopher Nolan",
    "Writer": "Jonathan Nolan (screenplay), Christopher Nolan (screenplay), Christopher Nolan (story), David S. Goyer (story), Bob Kane (characters)",
    "Actors": "Christian Bale, Heath Ledger, Aaron Eckhart, Michael Caine",
    "Plot": "When the menace known as the Joker wreaks havoc and chaos on the people of Gotham, the caped crusader must come to terms with one of the greatest psychological tests of his ability to fight injustice.",
    "Language": "English, Mandarin",
    "Country": "USA, UK",
    "Awards": "Won 2 Oscars. Another 146 wins & 142 nominations.",
    "Poster": "http://ia.media-imdb.com/images/M/MV5BMTMxNTMwODM0NF5BMl5BanBnXkFtZTcwODAyMTk2Mw@@._V1_SX300.jpg",
    "Metascore": "82",
    "imdbRating": "9.0",
    "imdbVotes": "1,652,832",
    "imdbID": "tt0468569",
    "Type": "movie",
    "Response": "True"
  },
  {
    "Title": "Batman Begins",
    "Year": "2005",
    "Rated": "PG-13",
    "Released": "15 Jun 2005",
    "Runtime": "140 min",
    "Genre": "Action, Adventure",
    "Director": "Christopher Nolan",
    "Writer": "Bob Kane (characters), David S. Goyer (story), Christopher Nolan (screenplay), David S. Goyer (screenplay)",
    "Actors": "Christian Bale, Michael Caine, Liam Neeson, Katie Holmes",
    "Plot": "After training with his mentor, Batman begins his fight to free crime-ridden Gotham City from the corruption that Scarecrow and the League of Shadows have cast upon it.",
    "Language": "English, Urdu, Mandarin",
    "Country": "USA, UK",
    "Awards": "Nominated for 1 Oscar. Another 15 wins & 66 nominations.",
    "Poster": "http://ia.media-imdb.com/images/M/MV5BNTM3OTc0MzM2OV5BMl5BanBnXkFtZTYwNzUwMTI3._V1_SX300.jpg",
    "Metascore": "70",
    "imdbRating": "8.3",
    "imdbVotes": "972,584",
    "imdbID": "tt0372784",
    "Type": "movie",
    "Response": "True"
  },
  {
    "Title": "Avatar",
    "Year": "2009",
    "Rated": "PG-13",
    "Released": "18 Dec 2009",
    "Runtime": "162 min",
    "Genre": "Action, Adventure, Fantasy",
    "Director": "James Cameron",
    "Writer": "James Cameron",
    "Actors": "Sam Worthington, Zoe Saldana, Sigourney Weaver, Stephen Lang",
    "Plot": "A paraplegic marine dispatched to the moon Pandora on a unique mission becomes torn between following his orders and protecting the world he feels is his home.",
    "Language": "English, Spanish",
    "Country": "USA, UK",
    "Awards": "Won 3 Oscars. Another 80 wins & 121 nominations.",
    "Poster": "http://ia.media-imdb.com/images/M/MV5BMTYwOTEwNjAzMl5BMl5BanBnXkFtZTcwODc5MTUwMw@@._V1_SX300.jpg",
    "Metascore": "83",
    "imdbRating": "7.9",
    "imdbVotes": "876,575",
    "imdbID": "tt0499549",
    "Type": "movie",
    "Response": "True"
  }
];

// Only change code below this line

const ratings = watchList.map(film => {
   return {title: film.Title,rating: film.imdbRating}
});


// Only change code above this line

console.log(JSON.stringify(ratings));
```
### 53.[Use the filter Method to Extract Data from an Array](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-the-filter-method-to-extract-data-from-an-array)
#### My Solution
```javascript
// The global variable
const watchList = [
  {
    "Title": "Inception",
    "Year": "2010",
    "Rated": "PG-13",
    "Released": "16 Jul 2010",
    "Runtime": "148 min",
    "Genre": "Action, Adventure, Crime",
    "Director": "Christopher Nolan",
    "Writer": "Christopher Nolan",
    "Actors": "Leonardo DiCaprio, Joseph Gordon-Levitt, Elliot Page, Tom Hardy",
    "Plot": "A thief, who steals corporate secrets through use of dream-sharing technology, is given the inverse task of planting an idea into the mind of a CEO.",
    "Language": "English, Japanese, French",
    "Country": "USA, UK",
    "Awards": "Won 4 Oscars. Another 143 wins & 198 nominations.",
    "Poster": "http://ia.media-imdb.com/images/M/MV5BMjAxMzY3NjcxNF5BMl5BanBnXkFtZTcwNTI5OTM0Mw@@._V1_SX300.jpg",
    "Metascore": "74",
    "imdbRating": "8.8",
    "imdbVotes": "1,446,708",
    "imdbID": "tt1375666",
    "Type": "movie",
    "Response": "True"
  },
  {
    "Title": "Interstellar",
    "Year": "2014",
    "Rated": "PG-13",
    "Released": "07 Nov 2014",
    "Runtime": "169 min",
    "Genre": "Adventure, Drama, Sci-Fi",
    "Director": "Christopher Nolan",
    "Writer": "Jonathan Nolan, Christopher Nolan",
    "Actors": "Ellen Burstyn, Matthew McConaughey, Mackenzie Foy, John Lithgow",
    "Plot": "A team of explorers travel through a wormhole in space in an attempt to ensure humanity's survival.",
    "Language": "English",
    "Country": "USA, UK",
    "Awards": "Won 1 Oscar. Another 39 wins & 132 nominations.",
    "Poster": "http://ia.media-imdb.com/images/M/MV5BMjIxNTU4MzY4MF5BMl5BanBnXkFtZTgwMzM4ODI3MjE@._V1_SX300.jpg",
    "Metascore": "74",
    "imdbRating": "8.6",
    "imdbVotes": "910,366",
    "imdbID": "tt0816692",
    "Type": "movie",
    "Response": "True"
  },
  {
    "Title": "The Dark Knight",
    "Year": "2008",
    "Rated": "PG-13",
    "Released": "18 Jul 2008",
    "Runtime": "152 min",
    "Genre": "Action, Adventure, Crime",
    "Director": "Christopher Nolan",
    "Writer": "Jonathan Nolan (screenplay), Christopher Nolan (screenplay), Christopher Nolan (story), David S. Goyer (story), Bob Kane (characters)",
    "Actors": "Christian Bale, Heath Ledger, Aaron Eckhart, Michael Caine",
    "Plot": "When the menace known as the Joker wreaks havoc and chaos on the people of Gotham, the caped crusader must come to terms with one of the greatest psychological tests of his ability to fight injustice.",
    "Language": "English, Mandarin",
    "Country": "USA, UK",
    "Awards": "Won 2 Oscars. Another 146 wins & 142 nominations.",
    "Poster": "http://ia.media-imdb.com/images/M/MV5BMTMxNTMwODM0NF5BMl5BanBnXkFtZTcwODAyMTk2Mw@@._V1_SX300.jpg",
    "Metascore": "82",
    "imdbRating": "9.0",
    "imdbVotes": "1,652,832",
    "imdbID": "tt0468569",
    "Type": "movie",
    "Response": "True"
  },
  {
    "Title": "Batman Begins",
    "Year": "2005",
    "Rated": "PG-13",
    "Released": "15 Jun 2005",
    "Runtime": "140 min",
    "Genre": "Action, Adventure",
    "Director": "Christopher Nolan",
    "Writer": "Bob Kane (characters), David S. Goyer (story), Christopher Nolan (screenplay), David S. Goyer (screenplay)",
    "Actors": "Christian Bale, Michael Caine, Liam Neeson, Katie Holmes",
    "Plot": "After training with his mentor, Batman begins his fight to free crime-ridden Gotham City from the corruption that Scarecrow and the League of Shadows have cast upon it.",
    "Language": "English, Urdu, Mandarin",
    "Country": "USA, UK",
    "Awards": "Nominated for 1 Oscar. Another 15 wins & 66 nominations.",
    "Poster": "http://ia.media-imdb.com/images/M/MV5BNTM3OTc0MzM2OV5BMl5BanBnXkFtZTYwNzUwMTI3._V1_SX300.jpg",
    "Metascore": "70",
    "imdbRating": "8.3",
    "imdbVotes": "972,584",
    "imdbID": "tt0372784",
    "Type": "movie",
    "Response": "True"
  },
  {
    "Title": "Avatar",
    "Year": "2009",
    "Rated": "PG-13",
    "Released": "18 Dec 2009",
    "Runtime": "162 min",
    "Genre": "Action, Adventure, Fantasy",
    "Director": "James Cameron",
    "Writer": "James Cameron",
    "Actors": "Sam Worthington, Zoe Saldana, Sigourney Weaver, Stephen Lang",
    "Plot": "A paraplegic marine dispatched to the moon Pandora on a unique mission becomes torn between following his orders and protecting the world he feels is his home.",
    "Language": "English, Spanish",
    "Country": "USA, UK",
    "Awards": "Won 3 Oscars. Another 80 wins & 121 nominations.",
    "Poster": "http://ia.media-imdb.com/images/M/MV5BMTYwOTEwNjAzMl5BMl5BanBnXkFtZTcwODc5MTUwMw@@._V1_SX300.jpg",
    "Metascore": "83",
    "imdbRating": "7.9",
    "imdbVotes": "876,575",
    "imdbID": "tt0499549",
    "Type": "movie",
    "Response": "True"
  }
];

// Only change code below this line
const mapList = watchList.map(film => {
  return {title: film.Title, rating: film.imdbRating}
});
const filteredList = mapList.filter(film => Number(film.rating) >= 8)

// Only change code above this line

console.log(filteredList);
```
### 54.[Golf Code](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/golf-code)
#### My Solution
```javascript
const names = ["Hole-in-one!", "Eagle", "Birdie", "Par", "Bogey", "Double Bogey", "Go Home!"];

function golfScore(par, strokes) {
  // Only change code below this line
  let str = "";
  if(strokes === 1)str = "Hole-in-one!";
  else if (strokes <= par - 2)str = "Eagle";
  else if (strokes === par - 1)str = "Birdie";
  else if (strokes === par)str = "Par";
  else if (strokes === par + 1)str = "Bogey";
  else if (strokes === par + 2)str = "Double Bogey";
  else if (strokes >= par + 3)str = "Go Home!";
  
  return str;
  // Only change code above this line
}

golfScore(5, 4);
```
### 55.[Logical Order in If Else Statements](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/logical-order-in-if-else-statements)
#### My Solution
```javascript
function orderMyLogic(val) {
  if (val < 5) {
    return "Less than 5";
  } else if (val < 10) {
    return "Less than 10";
  } else {
    return "Greater than or equal to 10";
  }
}

orderMyLogic(4);
```
### 56.[Chaining If Else Statements](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/chaining-if-else-statements)
#### My Solution
```javascript
function testSize(num) {
  // Only change code below this line
  let str = ""; 
  if(num < 5)str = "Tiny";
  else if(num < 10)str = "Small";
  else if(num < 15)str = "Medium";
  else if(num < 20)str = "Large";
  else if(num >= 20)str = "Huge";      
  return str;
  // Only change code above this line
}

testSize(7);
```
### 57.[Selecting from Many Options with Switch Statements](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/selecting-from-many-options-with-switch-statements)
#### My Solution
```javascript
function caseInSwitch(val) {
  let answer = "";
  // Only change code below this line
   switch(val){
     case 1: 
       answer = "alpha";
       break;
     case 2: 
       answer = "beta";
       break;
     case 3:
       answer = "gamma";
       break;
     case 4: 
       answer = "delta";
       break;
   }
  // Only change code above this line
  return answer;
}

caseInSwitch(1);
```
### 58.[Adding a Default Option in Switch Statements](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/adding-a-default-option-in-switch-statements)
#### My Solution
```javascript
function switchOfStuff(val) {
  let answer = "";
  // Only change code below this line
  switch(val){
    case 'a':
      answer = "apple"
      break;
    case 'b':
      answer = "brid"
      break; 
    case 'c':
      answer = "cat"
      break;  
    default : 
      answer = "stuff" 
      break;
  } 
  // Only change code above this line
  return answer;
}

switchOfStuff(1);
```
### 59.[Multiple Identical Options in Switch Statements](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/multiple-identical-options-in-switch-statements)
#### My Solution
```javascript
function sequentialSizes(val) {
  let answer = "";
  // Only change code below this line
  switch(val){
    case 1:
    case 2:
    case 3:
      answer = "Low";
      break;
    case 4:
    case 5:
    case 6:
      answer = "Mid";
      break; 
    case 7:
    case 8:
    case 9:
      answer = "High";
      break;  
  }
  // Only change code above this line
  return answer;
}

sequentialSizes(1);
```
### 60.[Replacing If Else Chains with Switch](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/replacing-if-else-chains-with-switch)
#### My Solution
```javascript
function chainToSwitch(val) {
  let answer = "";
  // Only change code below this line
   switch(val){
     case "bob":
      answer = "Marley";
      break;
     case 42:
      answer = "The Answer";
      break;
     case 1:
      answer = "There is no #1";
      break;
     case 99:
      answer = "Missed me by this much!";
      break; 
    case 7:
      answer = "Ate Nine";
      break; 
   }
  // Only change code above this line
  return answer;
}

chainToSwitch(7);
```
### 61.[Returning Boolean Values from Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/returning-boolean-values-from-functions)
#### My Solution
```javascript
function isLess(a, b) {
  // Only change code below this line
  return a < b;
  // Only change code above this line
}

isLess(10, 15);
```
### 62.[Return Early Pattern for Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/return-early-pattern-for-functions)
#### My Solution
```javascript
// Setup
function abTest(a, b) {
  // Only change code below this line
 if(a < 0 ||  b < 0)return; 
  

  // Only change code above this line

  return Math.round(Math.pow(Math.sqrt(a) + Math.sqrt(b), 2));
}

abTest(2,2);
```
### 63.[Counting Cards](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/counting-cards)
#### My Solution
```javascript
let count = 0;

function cc(card) {
  // Only change code below this line
  const a1 = [2, 3, 4, 5, 6];
  const a2 = [7, 8, 9];
  const a3 = [10, 'J', 'Q', 'K', 'A'];

  if(a1.includes(card))count += 1;
  else if (a2.includes(card))count += 0;
  else if (a3.includes(card))count += -1;

  return count > 0 ?`${count} Bet`:`${count} Hold`;
  // Only change code above this line
}

cc(2); cc(3); cc(7); cc('K'); cc('A');
```
### 64.[Build JavaScript Objects](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/build-javascript-objects)
#### My Solution
```javascript
const myDog = {
  // Only change code below this line
  name: 'df',
  legs: 4,
  tails: 20,
  friends: ['d','a','b'] 
  // Only change code above this line
};
```
### 65.[Accessing Object Properties with Dot Notation](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/accessing-object-properties-with-dot-notation)
#### My Solution
```javascript
// Setup
const testObj = {
  "hat": "ballcap",
  "shirt": "jersey",
  "shoes": "cleats"
};

// Only change code below this line
const hatValue = testObj.hat;      // Change this line
const shirtValue = testObj.shirt;    // Change this line
```
### 66.[Accessing Object Properties with Bracket Notation](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/accessing-object-properties-with-bracket-notation)
#### My Solution
```javascript
// Setup
const testObj = {
  "an entree": "hamburger",
  "my side": "veggies",
  "the drink": "water"
};

// Only change code below this line
const entreeValue = testObj["an entree"];   // Change this line
const drinkValue = testObj["the drink"];    // Change this line
```
### 67.[Accessing Object Properties with Variables](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/accessing-object-properties-with-variables)
#### My Solution
```javascript
// Setup
const testObj = {
  12: "Namath",
  16: "Montana",
  19: "Unitas"
};

// Only change code below this line
const playerNumber = 42;  // Change this line
const player = testObj[playerNumber];   // Change this line
```
### 68.[Updating Object Properties](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/updating-object-properties)
#### My Solution
```javascript
// Setup
const myDog = {
  "name": "Coder",
  "legs": 4,
  "tails": 1,
  "friends": ["freeCodeCamp Campers"]
};

// Only change code below this line
myDog.name = "Happy Coder";
```
### 69.[Add New Properties to a JavaScript Object](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/add-new-properties-to-a-javascript-object)
#### My Solution
```javascript
const myDog = {
  "name": "Happy Coder",
  "legs": 4,
  "tails": 1,
  "friends": ["freeCodeCamp Campers"]
};

myDog.bark = "woof";
```
### 70.[Delete Properties from a JavaScript Object](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/delete-properties-from-a-javascript-object)
#### My Solution
```javascript
// Setup
const myDog = {
  "name": "Happy Coder",
  "legs": 4,
  "tails": 1,
  "friends": ["freeCodeCamp Campers"],
  "bark": "woof"
};

delete myDog.tails;
// Only change code below this line

```
### 71.[Using Objects for Lookups](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/using-objects-for-lookups)
#### My Solution
```javascript
// Setup
function phoneticLookup(val) {
  let result = "";

  // Only change code below this line
  let lookup = {
    "alpha": "Adams",
    "bravo": "Boston",
    "charlie": "Chicago",
    "delta": "Denver",
    "echo": "Easy",
    "foxtrot": "Frank"
  }
  
  result = lookup[val];
  // Only change code above this line
  return result;
}

phoneticLookup("charlie");
```
### 72.[Testing Objects for Properties](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/testing-objects-for-properties)
#### My Solution
```javascript
function checkObj(obj, checkProp) {
  // Only change code below this line

  return obj[checkProp] ? obj[checkProp] : "Not Found";
  // Only change code above this line
}
```
### 73.[Manipulating Complex Objects](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/manipulating-complex-objects)
#### My Solution
```javascript
const myMusic = [
  {
    "artist": "Billy Joel",
    "title": "Piano Man",
    "release_year": 1973,
    "formats": [
      "CD",
      "8T",
      "LP"
    ],
    "gold": true
  }
];

const album = {
   "artist": "nour",
    "title": "flower",
    "release_year": 1999,
    "formats": [
      "CD",
      "8T",
      "LP"
    ],
  };

myMusic.push(album);

```
### 74.[Accessing Nested Objects](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/accessing-nested-objects)
#### My Solution
```javascript
const myStorage = {
  "car": {
    "inside": {
      "glove box": "maps",
      "passenger seat": "crumbs"
     },
    "outside": {
      "trunk": "jack"
    }
  }
};

const gloveBoxContents = myStorage.car.inside["glove box"];
```
### 75.[Accessing Nested Arrays](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/accessing-nested-arrays)
#### My Solution
```javascript
const myPlants = [
  {
    type: "flowers",
    list: [
      "rose",
      "tulip",
      "dandelion"
    ]
  },
  {
    type: "trees",
    list: [
      "fir",
      "pine",
      "birch"
    ]
  }
];

const secondTree = myPlants[1].list[1];
```
### 76.[Record Collection](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/record-collection)
#### My Solution
```javascript
// Setup
const recordCollection = {
  2548: {
    albumTitle: 'Slippery When Wet',
    artist: 'Bon Jovi',
    tracks: ['Let It Rock', 'You Give Love a Bad Name']
  },
  2468: {
    albumTitle: '1999',
    artist: 'Prince',
    tracks: ['1999', 'Little Red Corvette']
  },
  1245: {
    artist: 'Robert Palmer',
    tracks: []
  },
  5439: {
    albumTitle: 'ABBA Gold'
  }
};

// Only change code below this line
function updateRecords(records, id, prop, value) {
  if(!value){
    delete records[id][prop];
  }else {
    if(prop !== 'tracks')records[id][prop] = value;
    else {
        if(records[id][prop])records[id][prop].push(value);
        else{
         records[id][prop] = [value];
        }
      }
      
    }
  return records;
}

updateRecords(recordCollection, 2548, "artist", "")
```
### 77.[Iterate with JavaScript While Loops](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/iterate-with-javascript-while-loops)
#### My Solution
```javascript
// Setup
const myArray = [];

// Only change code below this line
while(myArray.length <= 5){
  myArray.push(5 - myArray.length);  
}

```
### 78.[Iterate with JavaScript For Loops](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/iterate-with-javascript-for-loops)
#### My Solution
```javascript
// Setup
const myArray = [];

// Only change code below this line
for(let i = 0; i < 5; i++){
  myArray.push(i+1);
}
```
### 79.[Iterate Odd Numbers With a For Loop](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/iterate-odd-numbers-with-a-for-loop)
#### My Solution
```javascript
// Setup
const myArray = [];

// Only change code below this line
for(let i = 1; i < 10 ; i += 2){
  myArray.push(i);
}
```
### 80.[Count Backwards With a For Loop](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/count-backwards-with-a-for-loop)
#### My Solution
```javascript
// Setup
const myArray = [];

// Only change code below this line
for(let i = 9; i > 0; i -= 2){
  myArray.push(i);
}
```
### 81.[Iterate Through an Array with a For Loop](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/iterate-through-an-array-with-a-for-loop)
#### My Solution
```javascript
// Setup
const myArr = [2, 3, 4, 5, 6];

// Only change code below this line
let total = 0;

for(let i = 0; i < myArr.length; i++){
  total += myArr[i];
}
```
### 82.[Nesting For Loops](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/nesting-for-loops)
#### My Solution
```javascript
function multiplyAll(arr) {
  let product = 1;
  // Only change code below this line
  for(let i = 0;i < arr.length; i++){
    for(let j = 0;j < arr[i].length; j++){
      product *= arr[i][j];
    }

  }
  // Only change code above this line
  return product;
}

multiplyAll([[1, 2], [3, 4], [5, 6, 7]]);
```
### 83.[Iterate with JavaScript Do...While Loops](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/iterate-with-javascript-do---while-loops)
#### My Solution
```javascript
// Setup
const myArray = [];
let i = 10;

// Only change code below this line
do{
  myArray.push(i);
  i++;
}while (i < 5)
```
### 84.[Replace Loops using Recursion](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/replace-loops-using-recursion)
#### My Solution
```javascript
function sum(arr, n) {
  // Only change code below this line
  if(n === 0){
    return 0;
  }
  else {
    return sum(arr, n - 1) + arr[n - 1];
  }
  // Only change code above this line
}
```
### 85.[Generate Random Fractions with JavaScript](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/generate-random-fractions-with-javascript)
#### My Solution
```javascript
function randomFraction() {

  // Only change code below this line

  return Math.random();

  // Only change code above this line
}
```
### 86.[Generate Random Whole Numbers with JavaScript](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/generate-random-whole-numbers-with-javascript)
#### My Solution
```javascript
function randomWholeNum() {
  return Math.floor(Math.random() * 10);
}
```
### 87.[Generate Random Whole Numbers within a Range](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/generate-random-whole-numbers-within-a-range)
#### My Solution
```javascript
function randomRange(myMin, myMax) {
  return Math.floor(Math.random()*(myMax - myMin + 1) + myMin);
}
```
### 88.[Use the parseInt Function](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/use-the-parseint-function)
#### My Solution
```javascript
function convertToInteger(str) {
 return parseInt(str);
}

convertToInteger("56");
```
### 89.[Use the parseInt Function with a Radix](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/use-the-parseint-function-with-a-radix)
#### My Solution
```javascript
function convertToInteger(str) {
  return parseInt(str,2);
}

convertToInteger("10011");
```
### 90.[Use the Conditional (Ternary) Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/use-the-conditional-ternary-operator)
#### My Solution
```javascript
function checkEqual(a, b) {
 return a === b ? 'Equal' : 'Not Equal';
}

checkEqual(1, 2);
```
### 91.[]()
#### My Solution
```javascript

```
### 92.[]()
#### My Solution
```javascript

```
