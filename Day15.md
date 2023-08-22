## Equality 

### Loose Equality vs Strict Equality 

#### Loose Equality (==)
1. check value.
2. allows coercion (different types).
3. prefer to numeric comparison (ToNumber).
4. invoke coercion if type is different.
5. if non-primitive ToPrimitive.
6. algorithm repeat itself.
7. comparison with known types.
#### Coding Examples.
```javascript
console.log(null == undefined);
//log true

console.log(42 == [42]); 
//convert [42] ToPrimitive to "42"
//prefer numeric and convert string to 42
//log true

console.log([] == ![]); 
//[] == false 
//"" == false
//0 == false
//0 == 0 
//log true
```
#### Avoid loose equal 
1. with non-primitive.
2. with true and false.
3. with 0 or "".

#### Strict Equality 
triple equal (===):
1. check value and type
2. disallows coercion (same types)

#### The Case of Double equal
not knowing a types means not fully understand the code
  * if the same types prefer use == over === (== faster).
  * if types are different use === be broken, prefer use == or not compare.
  * if know the types whether it's match or not, == is more sensible choice.
  * if don't know the types, === is the reasonable choice (not knowing types should be obvious to reader).


### Static Typing
benefits:
1. catch types mistakes 
2. communicate type intent
3. provide IDE feedback
4. define custom types
5. validating operands types

#### TypeScript & Flow 
Pros
1. make types more obvious.
2. look like other language types (java, c++).
3. popular.
4. very sophisticated.
   
Cons
1. non JS standard.
2. require a build process.
3. their sophisticated can be intimidating without formal types experience.
4. focus on static types (variable, parameters, returns, properties) than value types.


## Question Exercises
### 1.[Question 1](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week3%20-%20deep-javascript-foundations-v3/day%201/tasks.md)
#### My Solution
```javascript
function convertStringToNumber(input) {
  //write your own code here
  if (typeof input != "string") {
    return { value: input, type: typeof input };
  } else {
    return +input;
  }
}
console.log(convertStringToNumber("1")); //log 1
console.log(convertStringToNumber("1dfd")); //log NaN
console.log(convertStringToNumber(true)); //log {value: true, type: 'boolean'}
```
### 2.[Question 2](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week3%20-%20deep-javascript-foundations-v3/day%201/tasks.md)
#### My Solution
```javascript
const checkNaN = (value) => {
  //write your own code here
  return value !== value;
};
```
### 3.[Question 3](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week3%20-%20deep-javascript-foundations-v3/day%201/tasks.md)
#### My Solution
```javascript
function isEmptyValue(value) {
  //write your own code here
  return !value;
}
```
### 4.[Question 4](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week3%20-%20deep-javascript-foundations-v3/day%201/tasks.md)
#### My Solution
```javascript
function compareObjects(input1, input2) {
  //write your own code here
  if (
    typeof input1 == "object" &&
    typeof input2 == "object" &&
    !!input1 &&
    !!input2
  ) {
    return JSON.stringify(input1) === JSON.stringify(input2);
  } else {
    return [input1, input2];
  }
}

console.log(compareObjects({ a: [1], b: 5 }, { a: [1] })); //log false
console.log(compareObjects(5, null)); //log [5, null]
```
### 5.[Question 5](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week3%20-%20deep-javascript-foundations-v3/day%201/tasks.md)
#### My Solution
```javascript
const complexCoercion = (input) => {
  //write your own code here
  if (typeof input == "object" && input != null) {
    return input;
  } else {
    if (typeof input == "number") return !!input.toString();
    else return !!input;
  }
};
```
## Question Exercises
### 1.[Question 1](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week3%20-%20deep-javascript-foundations-v3/day%202/tasks.md)
#### My Solution
```javascript

```
### 2.[Question 2](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week3%20-%20deep-javascript-foundations-v3/day%202/tasks.md)
#### My Solution
```javascript
function testScope1() {
  if (true) {
    var a = 1;
    let b = 2;
    const c = 3;
  }
  console.log(a);
  console.log(b);
  console.log(c);
}

testScope1();

//log 1, ReferenceError (choice D)
//var can't have a block scope, can accesses outside the block scope if
//let and const has a block scope, can't accesses outside block scope if (ReferenceError)
//first log 1 then reference error and stop executing
```
### 3.[Question 3](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week3%20-%20deep-javascript-foundations-v3/day%202/tasks.md)
#### My Solution
```javascript

```
### 4.[Question 4](https://github.com/orjwan-alrajaby/gsg-QA-Nablus-training-2023/blob/main/learning-sprint-1/week3%20-%20deep-javascript-foundations-v3/day%202/tasks.md)
#### My Solution
```javascript

```
## Coding Exercises
### 229.[Convert Celsius to Fahrenheit](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-algorithm-scripting/convert-celsius-to-fahrenheit)
#### My Solution
```javascript
function convertCtoF(celsius) {
  let fahrenheit = celsius * (9/5) + 32;
  return fahrenheit;
}

convertCtoF(30);
```
### 230.[Reverse a String](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-algorithm-scripting/reverse-a-string)
#### My Solution
```javascript
function reverseString(str) {
  str = [...str].reverse().join(""); 
  return str;
}

reverseString("hello");
```
### 231.[Factorialize a Number](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-algorithm-scripting/factorialize-a-number)
#### My Solution
```javascript
function factorialize(num) {
  if(num == 0)return 1;
  return num * factorialize(num - 1);
}

factorialize(5);
```
### 232.[Find the Longest Word in a String](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-algorithm-scripting/find-the-longest-word-in-a-string)
#### My Solution
```javascript
function findLongestWordLength(str) {
  let arr = str.split(' ');
  let leg = arr.map((s) => s.length);
  return Math.max(...leg);
}

findLongestWordLength("The quick brown fox jumped over the lazy dog");
```
### 233.[Return Largest Numbers in Arrays](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-algorithm-scripting/return-largest-numbers-in-arrays)
#### My Solution
```javascript
function largestOfFour(arr) {
  let a = arr.map((s) => Math.max(...s));
  return a;
}

largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);
```
### 234.[Confirm the Ending](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-algorithm-scripting/confirm-the-ending)
#### My Solution
```javascript
function confirmEnding(str, target) {
  let l = target.length;
  return str.slice(str.length - l, str.length) == target;
}

confirmEnding("Bastian", "n");
```
### 235.[Repeat a String Repeat a String](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-algorithm-scripting/repeat-a-string-repeat-a-string)
#### My Solution
```javascript
function repeatStringNumTimes(str, num) {
  let s = '';
  if(num > 0){
     for(let i = 0; i < num; i++){
       s += str;
     }
     return s;
  } else {
    return '';
  }
}

repeatStringNumTimes("abc", 3);
```
### 236.[Truncate a String](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-algorithm-scripting/truncate-a-string)
#### My Solution
```javascript
function truncateString(str, num) {
  if(str.length <= num){return str;}
  else { return str.slice(0, num) + '...';}
}

truncateString("A-tisket a-tasket A green and yellow basket", 8);
```
### 237.[Finders Keepers](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-algorithm-scripting/finders-keepers)
#### My Solution
```javascript
function findElement(arr, func) {
  let num = 0;
  console.log(arr.some(func));
  let a = arr.filter((x) => func(x) == true);
  return a ? a[0] : undefined;
}

findElement([1, 2, 3, 4], num => num % 2 === 0);
```
### 238.[Boo who](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-algorithm-scripting/boo-who)
#### My Solution
```javascript
function booWho(bool) {
  return bool === true || bool === false;
}

booWho(null);
```
### 239.[Title Case a Sentence](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-algorithm-scripting/title-case-a-sentence)
#### My Solution
```javascript
function titleCase(str) {
let arr = str.split(" ");
let a = arr.map((s) => s[0].toUpperCase() + s.slice(1, s.length).toLowerCase());
  console.log(a.join(' '));
  return a.join(' ');
}

titleCase("I'm a little tea pot");
```
### 240.[Slice and Splice](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-algorithm-scripting/slice-and-splice)
#### My Solution
```javascript
function frankenSplice(arr1, arr2, n) {
  // for(let i = 0; i < arr2.length; i++){
  //   arr2
  // }
  let a = [...arr2.slice(0,n),...arr1,...arr2.slice(n, arr2.length)];
  console.log(a);
  return a;
}

frankenSplice([1, 2, 3], [4, 5, 6], 1);
```
### 241.[Falsy Bouncer](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-algorithm-scripting/falsy-bouncer)
#### My Solution
```javascript
function bouncer(arr) {
  return arr.filter((x) => !!x);
}

bouncer([7, "ate", "", false, 9]);
```
### 242.[Where do I Belong](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-algorithm-scripting/where-do-i-belong)
#### My Solution
```javascript
function getIndexToIns(arr, num) {
  let a = arr.sort((a, b) => a - b);
  console.log(a);
  let i = 0;
  for( ; i < a.length; i++){
    if(num <= a[i]) break;
  }
  return i;
}

getIndexToIns([40, 60], 50);
```
### 243.[Mutations](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-algorithm-scripting/mutations)
#### My Solution
```javascript
function mutation(arr) {
  let bool = true;
  for(let c of arr[1].toLowerCase()){
    if(!arr[0].toLowerCase().includes(c))bool = false;
  } 
  return bool;
}

mutation(["hello", "hey"]);
```
### 244.[Chunky Monkey](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/basic-algorithm-scripting/chunky-monkey)
#### My Solution
```javascript
function chunkArrayInGroups(arr, size) {
  let newArr = [];
  for(let i = 0; i < arr.length; i += size){
    newArr.push(arr.slice(i, i + size));
  }
  console.log(newArr);
  return newArr;
}

chunkArrayInGroups(["a", "b", "c", "d"], 2);
```

