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
    
## Coding Exercises
## [Rick & Morty Character List](https://drive.google.com/drive/folders/1h5EJKbDkaIZzxFVEJBMlu5UczkE3g5gz?usp=sharing)    
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
    
