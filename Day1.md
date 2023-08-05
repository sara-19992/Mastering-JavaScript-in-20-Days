## What is JS
JavaScript is a web programming language that can be used to modify and interact with web pages.JS run on the server and browser side.

## Where to write JS
we can write JS on the browsers JS console.to open a browsers console open a developer browsers tool by right click > inspect then open console tab. 

after entering some code on console and press on the enter button the JS will run the code and try to evaluate it. 
### Coding Examples

```javascript
//print on console "hey JS" 
console.log("hey JS")

//JS evaluate this expression and return 2 on console 
1 + 1 
```
## What is DOM
Document Object Model is an object contains the structural of web page (HTML elements). 
### Coding Examples

```javascript
//return the title of the current page
document.title

//return the body element
document.body

//return the collection of elements in the body  
document.body.children

```
## Finding Elements in a Web Page
 type of selectors to finding elements
  1. Name
  2. Tag Name
  3. ID (use # symbol)
  4. Class Name (use . symbol) 

 ### Coding Examples

  ```javascript
  //return the first element with id = backgroundImage
  document.getElementById("backgroundImage")
  
  //return the element with id = sidebar
  document.querySelector("#sidebar")

  //return the node list of div elements
  document.querySelectorAll("div")

  // return the length of node list (number of elements)
  document.querySelectorAll("div").length
  ```

## Changing a Web Page
modify the HTML elements (add,update,remove)
 ### Coding Examples

  ```javascript
  //change the Page title
  document.title="new title"
  
  //return the inner text in element
  document.querySelector("p").textContent

  //change the text in p element to "sun"
  document.querySelector("p").textContent="sun"
  //append to the end of text in p element "sun & moon"
  document.querySelector("p").append=" & moon"

  //return the node list of div elements
  document.querySelectorAll("div")
  ```
  Every time refresh the page after making changes, the page returns as it was, in every reload of page, the browser creates a new DOM that is    
  generated from the source code of page. 
  
  
## Coding Exercises

### 1.[Compound Assignment With Augmented Multiplication](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/compound-assignment-with-augmented-multiplication)

#### My Solution
```javascript
//Example 1 :  use the *= operator
let a = 5;
let b = 12;
let c = 4.6;

// Only change code below this line
a *= 5;
b *= 3;
c *= 10;
```

### 2.[Concatenating Strings with the Plus Equals Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/concatenating-strings-with-the-plus-equals-operator)

#### My Solution
```javascript
//Example 2 :  use the += operator
let myStr = "This is the first sentence. ";
myStr += "This is the second sentence.";

//Print on console
console.log(myStr);
```
### 3.[Use Bracket Notation to Find the Nth-to-Last Character in a String](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-javascript/use-bracket-notation-to-find-the-nth-to-last-character-in-a-string)


#### My Solution
```javascript
//Example 3 :  find the second-to-last character
// Setup
const lastName = "Lovelace";

// Only change code below this line
const secondToLastLetterOfLastName = lastName[lastName.length - 2]; // Change this line

console.log(secondToLastLetterOfLastName);
```
