### Abstract Operations (ToPremitive)

### Coercion
converts of values from one data type to another
#### Coding Examples
```javascript
var x = 10 + '30';
console.log(x);
//log 1030

console.log("ahmade" + 25)
//log ahmade25

console.log("ahmade" + true)
//log ahmadetrue
```

#### ToString
```javascript

null      //"null"
undefined //"undifined"
true      //"true"
false     //"false"
0         //"0"
-0        //"0"
30        //"30"
[]        //""
[1,3]     //"1,3"
{}        //[object Object] 
```
#### ToNumber
```javascript
null      //0
undefined //NaN
true      //1
false     //0
"0"       //0
"-0"      //-0
"0."      //0
"003"     //3
"30.12"   //30.12
[]        //0
[1,3]     //NaN
```
#### ToBoolean
```javascript
null      //false
undefined //false
true      //true
false     //false
0         //false
-0        //false
20        //true 
"30.12"   //true
[1,3]     //true
```
## Coding Exercises
### 211.[Use an Array to Store a Collection of Data](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/use-an-array-to-store-a-collection-of-data)
#### My Solution
```javascript
let yourArray = [10, "add", true, 20, 12]; // Change this line
```
### 212.[Access an Array's Contents Using Bracket Notation](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/access-an-arrays-contents-using-bracket-notation)
#### My Solution
```javascript
let myArray = ["a", "b", "c", "d"];
// Only change code below this line
myArray[1] = 'q';
// Only change code above this line
console.log(myArray);
```
### 213.[Add Items to an Array with push() and unshift()](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/add-items-to-an-array-with-push-and-unshift)
#### My Solution
```javascript
function mixedNumbers(arr) {
  // Only change code below this line
  arr.unshift('I', 2, 'three'); 
  arr.push(7, 'VIII', 9);
  // Only change code above this line
  return arr;
}

console.log(mixedNumbers(['IV', 5, 'six']));
```
### 214.[Remove Items from an Array with pop() and shift()](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/remove-items-from-an-array-with-pop-and-shift)
#### My Solution
```javascript
function popShift(arr) {
  let popped = arr.pop(); // Change this line
  let shifted = arr.shift(); // Change this line
  return [shifted, popped];
}

console.log(popShift(['challenge', 'is', 'not', 'complete']));
```
### 215.[Remove Items Using splice()](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/remove-items-using-splice)
#### My Solution
```javascript
const arr = [2, 4, 5, 1, 7, 5, 2, 1];
// Only change code below this line
let a  = arr.splice(1,4);
// Only change code above this line
console.log(arr);
```
### 216.[Add Items Using splice()](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/add-items-using-splice)
#### My Solution
```javascript
function htmlColorNames(arr) {
  // Only change code below this line
  arr.splice(0,2,'DarkSalmon','BlanchedAlmond');
  // Only change code above this line
  return arr;
}

console.log(htmlColorNames(['DarkGoldenRod', 'WhiteSmoke', 'LavenderBlush', 'PaleTurquoise', 'FireBrick']));
```
### 217.[Copy an Array with the Spread Operator](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/copy-an-array-with-the-spread-operator)
#### My Solution
```javascript
function copyMachine(arr, num) {
  let newArr = [];
  while (num >= 1) {
    // Only change code below this line
    newArr.push([...arr]);
    // Only change code above this line
    num--;
  }
  return newArr;
}

console.log(copyMachine([true, false, true], 2));
```
### 218.[Check For The Presence of an Element With indexOf()](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/check-for-the-presence-of-an-element-with-indexof)
#### My Solution
```javascript
function quickCheck(arr, elem) {
  // Only change code below this line
   return arr.indexOf(elem) !== -1 ? true : false;
  // Only change code above this line
}

console.log(quickCheck(['squash', 'onions', 'shallots'], 'mushrooms'));
```
### 219.[Iterate Through All an Array's Items Using For Loops](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/iterate-through-all-an-arrays-items-using-for-loops)
#### My Solution
```javascript
function filteredArray(arr, elem) {
  let newArr = [];
  // Only change code below this line
   for(let a of arr){
     if(a.indexOf(elem) === -1){
        newArr.push(a);
     }
   }
  // Only change code above this line
  return newArr;
}

console.log(filteredArray([[3, 2, 3], [1, 6, 3], [3, 13, 26], [19, 3, 9]], 3));
```
### 220.[Create complex multi-dimensional arrays](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/create-complex-multi-dimensional-arrays)
#### My Solution
```javascript
let myNestedArray = [
  // Only change code below this line
  ['unshift', false, 1, 2, 3, 'complex', 'nested',
  ['deep'],
  [
    ['deeper']
  ],
  [
    [
      ['deepest']
    ]
  ]
  
  ],
  ['loop', 'shift', 6, 7, 1000, 'method'],
  ['concat', false, true, 'spread', 'array'],
  ['mutate', 1327.98, 'splice', 'slice', 'push'],
  ['iterate', 1.3849, 7, '8.4876', 'arbitrary', 'depth']
  // Only change code above this line
];
```
### 221.[Add Key-Value Pairs to JavaScript Objects](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/add-key-value-pairs-to-javascript-objects)
#### My Solution
```javascript
let foods = {
  apples: 25,
  oranges: 32,
  plums: 28
};

// Only change code below this line
foods.bananas = 13;
foods.grapes = 35;
foods.strawberries = 27;

// Only change code above this line

console.log(foods);
```
### 222.[Modify an Object Nested Within an Object](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/modify-an-object-nested-within-an-object)
#### My Solution
```javascript
let userActivity = {
  id: 23894201352,
  date: 'January 1, 2017',
  data: {
    totalUsers: 51,
    online: 42
  }
};

// Only change code below this line
userActivity.data.online = 45;
// Only change code above this line

console.log(userActivity);
```
### 223.[Access Property Names with Bracket Notation](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/access-property-names-with-bracket-notation)
#### My Solution
```javascript
let foods = {
  apples: 25,
  oranges: 32,
  plums: 28,
  bananas: 13,
  grapes: 35,
  strawberries: 27
};

function checkInventory(scannedItem) {
  // Only change code below this line
  return foods[scannedItem]; 
  // Only change code above this line
}

console.log(checkInventory("apples"));
```
### 224.[Use the delete Keyword to Remove Object Properties](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/use-the-delete-keyword-to-remove-object-properties)
#### My Solution
```javascript
let foods = {
  apples: 25,
  oranges: 32,
  plums: 28,
  bananas: 13,
  grapes: 35,
  strawberries: 27
};

// Only change code below this line
delete foods.oranges;
delete foods.plums;
delete foods.strawberries;
// Only change code above this line

console.log(foods);
```
### 225.[Check if an Object has a Property](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/check-if-an-object-has-a-property)
#### My Solution
```javascript
let users = {
  Alan: {
    age: 27,
    online: true
  },
  Jeff: {
    age: 32,
    online: true
  },
  Sarah: {
    age: 48,
    online: true
  },
  Ryan: {
    age: 19,
    online: true
  }
};

function isEveryoneHere(userObj) {
  // Only change code below this line
  return userObj.hasOwnProperty('Alan') && 
         userObj.hasOwnProperty('Jeff') &&
         userObj.hasOwnProperty('Sarah') &&
         userObj.hasOwnProperty('Ryan');
  // Only change code above this line
}

console.log(isEveryoneHere(users));
```
### 226.[Iterate Through the Keys of an Object with a for...in Statement](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/iterate-through-the-keys-of-an-object-with-a-for---in-statement)
#### My Solution
```javascript
const users = {
  Alan: {
    online: false
  },
  Jeff: {
    online: true
  },
  Sarah: {
    online: false
  }
}

function countOnline(allUsers) {
  // Only change code below this line
  let count = 0;
  for(let user in allUsers){
    if(allUsers[user].online === true)count++;
  }
  return count;
  // Only change code above this line
}

console.log(countOnline(users));
```
### 227.[Generate an Array of All Object Keys with Object.keys()](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/generate-an-array-of-all-object-keys-with-object-keys)
#### My Solution
```javascript
let users = {
  Alan: {
    age: 27,
    online: false
  },
  Jeff: {
    age: 32,
    online: true
  },
  Sarah: {
    age: 48,
    online: false
  },
  Ryan: {
    age: 19,
    online: true
  }
};

function getArrayOfUsers(obj) {
  // Only change code below this line
  return Object.keys(obj);
 
  // Only change code above this line
}

console.log(getArrayOfUsers(users));
```
### 228.[Modify an Array Stored in an Object](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-data-structures/modify-an-array-stored-in-an-object)
#### My Solution
```javascript
let user = {
  name: 'Kenneth',
  age: 28,
  data: {
    username: 'kennethCodesAllDay',
    joinDate: 'March 26, 2016',
    organization: 'freeCodeCamp',
    friends: [
      'Sam',
      'Kira',
      'Tomo'
    ],
    location: {
      city: 'San Francisco',
      state: 'CA',
      country: 'USA'
    }
  }
};

function addFriend(userObj, friend) {
  // Only change code below this line
   userObj.data.friends.push(friend); 
   return userObj.data.friends;
  // Only change code above this line
}

console.log(addFriend(user, 'Pete'));
```
