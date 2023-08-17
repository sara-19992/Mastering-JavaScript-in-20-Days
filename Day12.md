

## Coding Exercises
### 191.[Learn About Functional Programming](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/learn-about-functional-programming)
#### My Solution
```javascript
// Function that returns a string representing a cup of green tea
const prepareTea = () => 'greenTea';

/*
Given a function (representing the tea type) and number of cups needed, the
following function returns an array of strings (each representing a cup of
a specific type of tea).
*/
const getTea = (numOfCups) => {
  const teaCups = [];

  for(let cups = 1; cups <= numOfCups; cups += 1) {
    const teaCup = prepareTea();
    teaCups.push(teaCup);
  }
  return teaCups;
};

// Only change code below this line
const tea4TeamFCC = getTea(40);
// Only change code above this line
```
### 192.[Understand Functional Programming Terminology](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/understand-functional-programming-terminology)
#### My Solution
```javascript
// Function that returns a string representing a cup of green tea
const prepareGreenTea = () => 'greenTea';

// Function that returns a string representing a cup of black tea
const prepareBlackTea = () => 'blackTea';

/*
Given a function (representing the tea type) and number of cups needed, the
following function returns an array of strings (each representing a cup of
a specific type of tea).
*/
const getTea = (prepareTea, numOfCups) => {
  const teaCups = [];

  for(let cups = 1; cups <= numOfCups; cups += 1) {
    const teaCup = prepareTea();
    teaCups.push(teaCup);
  }
  return teaCups;
};

// Only change code below this line
const tea4GreenTeamFCC = getTea(prepareGreenTea, 27);
const tea4BlackTeamFCC = getTea(prepareBlackTea, 13);
// Only change code above this line

console.log(
  tea4GreenTeamFCC,
  tea4BlackTeamFCC
);
```
### 193.[Understand the Hazards of Using Imperative Code](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/understand-the-hazards-of-using-imperative-code)
#### My Solution
```javascript
// tabs is an array of titles of each site open within the window
const Window = function(tabs) {
  this.tabs = tabs; // We keep a record of the array inside the object
};

// When you join two windows into one window
Window.prototype.join = function(otherWindow) {
  this.tabs = this.tabs.concat(otherWindow.tabs);
  return this;
};

// When you open a new tab at the end
Window.prototype.tabOpen = function(tab) {
  this.tabs.push('new tab'); // Let's open a new tab for now
  return this;
};

// When you close a tab
Window.prototype.tabClose = function(index) {

  // Only change code below this line
  const tabsBeforeIndex = this.tabs.slice(0, index); // Get the tabs before the tab
  const tabsAfterIndex = this.tabs.slice(index + 1); // Get the tabs after the tab
console.log(tabsBeforeIndex);
console.log(tabsAfterIndex);
  this.tabs = tabsBeforeIndex.concat(tabsAfterIndex); // Join them together

  // Only change code above this line

  return this;
 };

// Let's create three browser windows
const workWindow = new Window(['GMail', 'Inbox', 'Work mail', 'Docs', 'freeCodeCamp']); // Your mailbox, drive, and other work sites
const socialWindow = new Window(['FB', 'Gitter', 'Reddit', 'Twitter', 'Medium']); // Social sites
const videoWindow = new Window(['Netflix', 'YouTube', 'Vimeo', 'Vine']); // Entertainment sites

// Now perform the tab opening, closing, and other operations
const finalTabs = socialWindow
  .tabOpen() // Open a new tab for cat memes
  .join(videoWindow.tabClose(2)) // Close third tab in video window, and join
  .join(workWindow.tabClose(1).tabOpen());
console.log(finalTabs.tabs);
```
### 194.[Avoid Mutations and Side Effects Using Functional Programming](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/avoid-mutations-and-side-effects-using-functional-programming)
#### My Solution
```javascript
// The global variable
let fixedValue = 4;

function incrementer() {
  // Only change code below this line
  let v = fixedValue;
  return ++v;

  // Only change code above this line
}
```
### 195.[Pass Arguments to Avoid External Dependence in a Function](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/pass-arguments-to-avoid-external-dependence-in-a-function)
#### My Solution
```javascript
// The global variable
let fixedValue = 4;

// Only change code below this line
function incrementer(value) {
  return ++value;
  // Only change code above this line
}
```
### 196.[Refactor Global Variables Out of Functions](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/refactor-global-variables-out-of-functions)
#### My Solution
```javascript
// The global variable
const bookList = ["The Hound of the Baskervilles", "On The Electrodynamics of Moving Bodies", "Philosophiæ Naturalis Principia Mathematica", "Disquisitiones Arithmeticae"];

// Change code below this line
function add(bookList, bookName) {
  const book = [...bookList];
  book.push(bookName);
  return book;
  
  // Change code above this line
}

// Change code below this line
function remove(bookList, bookName) {
  const book = [...bookList];
  const book_index = book.indexOf(bookName);
  if (book_index >= 0) {

    book.splice(book_index, 1);
    return book;

    // Change code above this line
    }
}
```
### 197.[Implement map on a Prototype](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/implement-map-on-a-prototype)
#### My Solution
```javascript
Array.prototype.myMap = function(callback) {
  const newArray = [];
  // Only change code below this line
  this.forEach((element, index, array) => newArray.push(callback(element, index, array)))
  // Only change code above this line
  return newArray;
};
```
### 198.[Implement the filter Method on a Prototype](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/implement-the-filter-method-on-a-prototype)
#### My Solution
```javascript
Array.prototype.myFilter = function(callback) {
  const newArray = [];
  // Only change code below this line
   this.forEach((element, index, array) => {
     if(callback(element, index, array)) newArray.push(element);
     }
     );
   console.log(newArray);  
  // Only change code above this line
  return newArray;
};
```
### 199.[Return Part of an Array Using the slice Method](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/return-part-of-an-array-using-the-slice-method)
#### My Solution
```javascript
function sliceArray(anim, beginSlice, endSlice) {
  // Only change code below this line
  return anim.slice(beginSlice, endSlice);

  // Only change code above this line
}

const inputAnim = ["Cat", "Dog", "Tiger", "Zebra", "Ant"];
sliceArray(inputAnim, 1, 3);
```
### 200.[Remove Elements from an Array Using slice Instead of splice](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/remove-elements-from-an-array-using-slice-instead-of-splice)
#### My Solution
```javascript
function nonMutatingSplice(cities) {
  return [...cities].slice(0, 3);
}
```
### 201.[Combine Two Arrays Using the concat Method](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/combine-two-arrays-using-the-concat-method)
#### My Solution
```javascript
function nonMutatingConcat(original, attach) {
  // Only change code below this line
   return [...original].concat(attach);

  // Only change code above this line
}

const first = [1, 2, 3];
const second = [4, 5];
nonMutatingConcat(first, second);
```
### 202.[Add Elements to the End of an Array Using concat Instead of push](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/add-elements-to-the-end-of-an-array-using-concat-instead-of-push)
#### My Solution
```javascript
function nonMutatingPush(original, newItem) {
  // Only change code below this line
  return [...original].concat(newItem);

  // Only change code above this line
}

const first = [1, 2, 3];
const second = [4, 5];
nonMutatingPush(first, second);
```
### 203.[Use the reduce Method to Analyze Data](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/use-the-reduce-method-to-analyze-data)
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

function getRating(watchList) {
  // Only change code below this line
  let christopher = watchList.filter((m) => m.Director === 'Christopher Nolan'); 

  let averageRating = christopher.reduce((sum, m) => {
   sum += parseFloat(m.imdbRating);
   return sum;
  }, 0);
   
   averageRating = averageRating / christopher.length;

  // Only change code above this line
  return averageRating;
}

console.log(getRating(watchList));
```
### 204.[]()
#### My Solution
```javascript

```
### 205.[]()
#### My Solution
```javascript

```
### 206.[]()
#### My Solution
```javascript

```
### 207.[]()
#### My Solution
```javascript

```
### 208.[]()
#### My Solution
```javascript

```
### 209.[]()
#### My Solution
```javascript

```
