

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
### 196.[Implement map on a Prototype](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/functional-programming/implement-map-on-a-prototype)
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
### 197.[]()
#### My Solution
```javascript

```
### 198.[]()
#### My Solution
```javascript

```
### 199.[]()
#### My Solution
```javascript

```
### 200.[]()
#### My Solution
```javascript

```
