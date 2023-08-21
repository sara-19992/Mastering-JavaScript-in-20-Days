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
### 233.[]()
#### My Solution
```javascript

```
### 234.[]()
#### My Solution
```javascript

```
### 235.[]()
#### My Solution
```javascript

```
### 236.[]()
#### My Solution
```javascript

```
### 237.[]()
#### My Solution
```javascript

```
### 238.[]()
#### My Solution
```javascript

```
### 239.[]()
#### My Solution
```javascript

```
### 240.[]()
#### My Solution
```javascript

```
