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
### 217.[]()
#### My Solution
```javascript

```
### 218.[]()
#### My Solution
```javascript

```
### 219.[]()
#### My Solution
```javascript

```
### 220.[]()
#### My Solution
```javascript

```
